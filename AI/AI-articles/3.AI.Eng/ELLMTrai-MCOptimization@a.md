---
aliases:
  - "Efficient LLM Training: Memory & Compute Optimization (article)"
up:
  - [[AI-articles]]
---
up:  [[AI-articles]]
URL: https://medium.com/@ak16425/efficient-llm-training-memory-compute-optimization-f1aae81c83f4
# Efficient LLM Training: Memory & Compute Optimization
Amit Khandelwal - Feb 12, 2024
Train large language models without CUDA out of memory error.
#### Introduction
Foundation models possess a vast number of parameters, leading to frequent encounters with memory and computational hurdles when undertaking pre-training from scratch or fine-tuning processes. In this blog, we will explore various techniques for optimizing memory and compute resources during LLM training. We will discuss the motivation behind these techniques, how they work, and their benefits.
#### Motivation
To train a 7-billion parameter LLM would require ~168 GB of GPU RAM. At the same time, NVIDIA’s A100 and H100 have a maximum of 80GB RAM. Therefore, it is essential to employ techniques that can reduce memory usage and enable training on a single GPU or scale model training horizontally across multiple GPUs.

#### Decomposing Memory Requirements in Model Training
When training or fine-tuning a foundation model, several components utilize GPU memory to execute effectively. These components include:

Model weights (parameters)
Optimizer states
Gradients
Forward activations saved for gradient computation
Temporary buffers
Functionality-specific memory
Kernels

Model weights are typically stored as floating-point numbers, meaning each parameter occupies 4 bytes (32-bit) of memory. While other component details are not extensively discussed here, estimating their memory requirement at around 20 bytes per parameter provides a reasonable approximation.
***To compute the total memory needed for training a model, we consider that 24 bytes of memory are required for one fp32 parameter.***
For instance, training a 7-billion-parameter model would necessitate:

*~7 * 10⁹ * 24 bytes = 168GB of GPU RAM*

Understanding these memory requirements is crucial for effectively managing resources during model training or fine-tuning processes.

#### Techniques for Memory Optimization
##### 1. Quantization
Quantization is a technique to reduce the computational and memory costs of running inference by representing the weights and activations with low-precision data types like an 8-bit integer (int8), float16, or bfloat16 instead of the usual 32-bit floating point (float32).

![[1_sa28NSE8b8Pf_dtqCbK6Wg.webp]]
Comparison of data types used for quantization [4]

Reducing the number of bits means the resulting model requires less memory storage, consumes less energy (in theory), and operations like matrix multiplication can be performed much faster with integer arithmetic. It also allows to run models on embedded devices, which sometimes only support integer data types.

Quantization using fp16 or bf16 reduces the memory requirement by 50%, while using fp8 or int8 reduces by 75%. bf16 is generally preferred over fp16 as it has the same dynamic range (exponent bits) as fp32 and hence reduces overflow while conversion.

#####  2. Flash Attention
The performance of the transformer is limited by the computational and memory complexities of its self-attention layers. Flash Attention, a variant of the attention algorithm, not only offers a more memory-efficient solution but also enhances efficiency through optimized GPU memory usage.

The computation and memory demands of the transformer’s attention layers increase quadratically with the number of input tokens (O(n²)). Flash Attention addresses this quadratic scaling issue by **reducing both computational and memory requirements from quadratic (O(n²))** to linear (O(n)), resulting in a reduction in memory requirements by 10–20 times and a performance improvement of 2–4 times.

#####  3. Data Parallelism

When training on a single GPU is too slow or the model weights do not fit in a single GPU’s memory even after quantization, it is good to move to a multi-GPU setup. There are different ways to distribute the workload across resources, called parallelization. We will specifically look into two **distributed computing patterns, distributed data parallel (DDP) and fully sharded data parallel (FSDP).**

DDP is used when the model parameters, data batches, and additional data needed to fulfill the training loop can fit in a single GPU. In the Distributed Data-Parallel (DDP) approach, the model is replicated across each GPU, the data is partitioned into batches, and these batches are concurrently dispatched to each GPU. Through DDP, each GPU processes its respective batch of data in parallel, culminating in a synchronization phase where the outputs from all GPUs are harmonized. **The main benefit of DDP is the reduction in training time.**

FSDP is a data-parallel method that shards a model’s parameters, gradients, and optimizer states across the number of available GPUs. **When training with FSDP, the GPU memory footprint is smaller than when training with DDP across all workers. This makes the training of some very large models feasible by allowing larger models or batch sizes to fit on the device.** This comes with the cost of increased communication volume.

In FSDP (Fully Sharded Data Parallelism), the data required for computations is sharded, meaning it’s divided into parts and distributed across the GPUs. During the forward pass, each GPU requests the necessary data from the other GPUs as needed to reconstruct a complete set of unsharded, local data. This unsharded data is then used for processing on each GPU for the duration of the operation.
Once the forward pass is complete, FSDP releases the unsharded local data back to the other GPUs. This effectively returns the data to its original sharded state, where each GPU holds only a portion of the complete dataset. This step is crucial for memory management, as it frees up GPU memory that was temporarily occupied by the unsharded data, allowing it to be used for subsequent operations such as the backward pass.

#####  Conclusion

In this blog, we discussed various techniques for optimizing memory and compute resources during LLM training. Quantization, Flash Attention, and data parallelism are effective methods for reducing memory usage and enabling training on a single GPU or scaling model training horizontally across multiple GPUs. By employing these techniques, it is possible to train large language models efficiently and effectively.

#####  References
https://pytorch.org/tutorials/intermediate/FSDP_tutorial.html#:~:text=In%20DDP%20each%20process%20holds,followed%20by%20FSDP%20and%20DDP.
https://huggingface.co/docs/transformers
https://huggingface.co/docs/optimum/concept_guides/quantization
Generative AI on AWS — By Chris Fregly, Antje Barth, Shelbee Eigenbrode