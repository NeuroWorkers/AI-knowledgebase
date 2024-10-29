


технология и модель

#### Guanaco (+)
<font color="#00b0f0">Guanaco</font> is model used in <font color="#00b0f0">QloRA</font>  ---> [[QLoRA#QloRA]]
<span style="background:#affad1">OPENSOURCE</span>
#### QloRA (tech) (+)
finetuning that reduces memory usage
--------------------

#### /end


# QloRA
QLorRA

---
https://github.com/artidoro/qlora
> QLoRA: Efficient Finetuning of Quantized LLMs - GitHub ; https://github.com › artidoro › qlora
> We present QLoRA, an efficient finetuning approach that reduces memory usage enough to finetune a 65B parameter model on a single 48GB GPU while preserving full .

# QLoRA: Efficient Finetuning of Quantized LLMs
| [Paper](https://arxiv.org/abs/2305.14314) | [Adapter Weights](https://huggingface.co/timdettmers) | [Demo](https://huggingface.co/spaces/uwnlp/guanaco-playground-tgi) |
This repo supports the paper "QLoRA: Efficient Finetuning of Quantized LLMs", an effort to democratize access to LLM research.

## Overview

We present QLoRA, an efficient finetuning approach that <font color="#ffff00">reduces memory usage </font>enough to <font color="#ffff00">finetune a 65B </font>parameter model <font color="#ffff00">on a single 48GB GPU</font> while preserving full 16-bit finetuning task performance. QLoRA backpropagates gradients through a frozen, 4-bit quantized pretrained language model into Low Rank Adapters (LoRA). Our best model family, which we name Guanaco, outperforms all previous openly released models on the Vicuna benchmark, reaching 99.3% of the performance level of ChatGPT while only requiring 24 hours of finetuning on a single GPU. QLoRA introduces a number of innovations to save memory without sacrificing performance: (a) 4-bit NormalFloat (NF4), a new data type that is information theoretically optimal for normally distributed weights (b) Double Quantization to reduce the average memory footprint by quantizing the quantization constants, and (c) Paged Optimizers to manage memory spikes. We use QLoRA to finetune more than 1,000 models, providing a detailed analysis of instruction following and chatbot performance across 8 instruction datasets, multiple model types (LLaMA, T5), and model scales that would be infeasible to run with regular finetuning (e.g. 33B and 65B parameter models). Our results show that QLoRA finetuning on a small high-quality dataset leads to state-of-the-art results, even when using smaller models than the previous SoTA. We provide a detailed analysis of chatbot performance based on both human and GPT-4 evaluations showing that GPT-4 evaluations are a cheap and reasonable alternative to human evaluation. Furthermore, we find that current chatbot benchmarks are not trustworthy to accurately evaluate the performance levels of chatbots. <font color="#00b0f0">We release all of our models and code, including CUDA kernels for 4-bit training.</font>


----


# Guanaco
NOTE: Guanaco это <font color="#00b0f0">model</font> ( -->  [[AI-basics#Model]] )
NOTE: Guanaco это <font color="#00b0f0">chat-bot</font> model
NOTE: Guanaco based on <font color="#00b0f0">LLaMA</font> ( --> [[LLaMA]]   ) (see -->  [[QLoRA#^d6ddbd]] )


Guanaco модель для QLoRA

https://github.com/artidoro/qlora
... Our best model family, which we name <font color="#00b0f0">Guanaco</font>, outperforms all previous openly released models on the Vicuna benchmark ... 

##### License and Intended Use
We release the resources associated with QLoRA finetuning in this repository under MIT license. In addition, we release the <font color="#00b0f0">Guanaco model family for base LLaMA</font> model sizes of 7B, 13B, 33B, and 65B. These models are intended for purposes in line with the LLaMA license and require access to the LLaMA models.  ^d6ddbd




