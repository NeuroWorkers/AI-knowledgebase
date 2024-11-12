---
aliases:
  - AI Model Size - RAM and Disk
  - Потребление памяти у ИИ моделей
up:
  - [[AI-concept]]
---
up:  [[AI-concept]]  up: [[AI-Model-Sizes]]
# AI Model Size - RAM and Disk

See below: [[#Model Memory Calculator (Hugging Face 🤗)]]

### Model Precision
float32  | float16/bfloat16  |  int8  |  int4
1bit | 

#### Mixed precision
Mixed precision is the use of both 16-bit and 32-bit FP types in a model during training

google:// mixed precision
##### Mixed precision | TensorFlow Core
TensorFlow https://www.tensorflow.org › guide › mixed_precision
[Mixed precision | TensorFlow Core](https://www.tensorflow.org/guide/mixed_precision)   Mar 23, 2024 — _Mixed precision_ is the use of both 16-bit and 32-bit floating-point types in a model during training to make it run faster and use less memory.

#### Model Precision // Info
##### (D) What do papers mean when they say they "trained using bfloat16"?
https://www.reddit.com/r/MachineLearning/comments/1ajkcwy/d_what_do_papers_mean_when_they_say_they_trained/
2024-02  [AromaticCantaloupe19](https://www.reddit.com/user/AromaticCantaloupe19/)
[AerysSk](https://www.reddit.com/user/AerysSk/)  •[2024-02](https://www.reddit.com/r/MachineLearning/comments/1ajkcwy/comment/kp1mfl5/)•
> The standard precision for training is float32, which means it uses 32 bit floats. Bfloat16 uses 16 bit, which reduces the memory storage by half and also speeds up computation, but with a tradeoff of lower accuracy (depending on a lot of factors).
> It is common if the model does not fit in a single GPU or multiple GPUs, and is more common with LLMs.

##### How can I reduce memory usage in LLM?
**Quantization, Flash Attention, and data parallelism** are effective methods for reducing memory usage and enabling training on a single GPU or scaling model training horizontally across multiple GPUs. By employing these techniques, it is possible to train large language models efficiently and effectively.Feb 11, 2024
--> [Efficient LLM Training: Memory & Compute Optimization - Medium](https://medium.com/@ak16425/efficient-llm-training-memory-compute-optimization-f1aae81c83f4#:~:text=Quantization%2C%20Flash%20Attention%2C%20and%20data,language%20models%20efficiently%20and%20effectively.)


#### Model Memory Calculator (Hugging Face 🤗)
alias: Калькулятор потребления памяти у модели
https://huggingface.co/spaces/hf-accelerate/model-memory-usage
This tool will help you calculate how much vRAM is needed to train and perform big model inference on a model hosted on the 🤗 Hugging Face Hub. The minimum recommended vRAM needed for a model is denoted as the size of the "largest layer", and training of a model is roughly 4x its size (for Adam)






