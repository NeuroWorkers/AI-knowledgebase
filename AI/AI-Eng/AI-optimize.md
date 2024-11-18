---
aliases:
  - template1
up:
  - [[AI-Eng]]
---
up:  [[AI-Eng]]
![[AI-optimize#^m]]
# AI optimization



#### Sparse Models (optimization)
[[Sparse|Sparse Models]]  
![[Sparse#^tldr]]

##### TPI-LLM: Serving 70B-scale LLMs Efficiently on Low-resource Edge Devices (article-l)
https://www.reddit.com/r/LocalLLaMA/comments/1fvc44x/tpillm_serving_70bscale_llms_efficiently_on/
https://arxiv.org/abs/2410.00531
Abstract: Large model inference is shifting from cloud to edge due to concerns about the privacy of user interaction data. However, edge devices often struggle with limited computing power, memory, and bandwidth, requiring collaboration across multiple devices to run and speed up LLM inference. Pipeline parallelism, the mainstream solution, is inefficient for single-user scenarios, while tensor parallelism struggles with frequent communications. In this paper, we argue that tensor parallelism can be more effective than pipeline on low-resource devices, and present a compute- and memory-efficient tensor parallel inference system, named TPI-LLM, to serve 70B-scale models. ....
TPI-LLM demonstrated over 80% less time-to-first-token and token latency compared to Accelerate, and over 90% compared to Transformers and Galaxy, while cutting the peak memory footprint of Llama 2-70B by 90%, requiring only 3.1 GB of memory for 70B-scale models.

Code: [https://github.com/Lizonghang/TPI-LLM](https://github.com/Lizonghang/TPI-LLM)

##### LLM inference optimization (article-l)
[ LLM inference optimization](https://huggingface.co/docs/transformers/main/en/llm_optims)  /  [Hugging Face](https://huggingface.co/)
This guide will show you how to use the optimization techniques available in Transformers to accelerate LLM inference.

##### Efficient LLM Training: Memory & Compute Optimization (article-l)
https://medium.com/@ak16425/efficient-llm-training-memory-compute-optimization-f1aae81c83f4
Efficient LLM Training: Memory & Compute Optimization
Cached: [[ELLMTrai-MCOptimization@a|Efficient LLM Training: Memory & Compute Optimization (article)]]


# Attic

[[AI-on-CPU]] | [[AI-optimize]]
^m