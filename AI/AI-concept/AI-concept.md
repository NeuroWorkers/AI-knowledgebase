---
aliases:
  - Terminology (AI:ML,LLM)
up: [[AI]]
---
up: [[AI]]
иерархия
ML -> Deep Lerning -> Neural Networks -> LLM, Text2Img  (AI) ; See: [[AI-basics]]

# AI-concept
## AI concepts - Fundamental

### NLP - natural language processing 
What is NLP (natural language processing)?
https://www.ibm.com/topics/natural-language-processing

### Model (AI)
[[AI-Model|Model (AI)]]
#### LLM
See [[LLM]] ; 
##### Multimodal LLM
multimodal LLM is an AI system trained with multiple modes of data. For instance, existing multimodal LLM are trained on image, text, and audio data. --> [[AI-Model#Multimodal LLMs]]

### Inference (Model Inference)
основное юзерское использование модели - запрашиваем ей запрос и получаем результат. --> [[Inference#Inference (Model Inference)|Inference (Model Inference)]]
See also: [[#Chaining, Inference chaining, LLM chaining]]

#### LLM Temperature
[[Inference#LLM Temperature]]

### Context window
Alias: Контекстное окно, 
See: [[Context-window]]
##### Context window size 
[[Context-window#Context window size]]

### In-context learning
See: [[In-context-learning|ICL (In-context learning)]]
![[In-context-learning#^in-context-learning]]
### FSL - Few-shot learning
N-shot learning is when an machine learning model can learn a new task by seeing N examples of that task.
See [[FSL]]

### Zero-shot learning
See: [[Zero-shot|Zero-shot learning]]

### RLHF - Reinforcement Learning from Human Feedback
Reinforcement Learning from Human Feedback, RLHF
[[howto-StackLLaMA---LLaMA-RLHF]]

«обучение с подкреплением на основе отзывов людей» (Reinforcement Learning from Human Feedback, RLHF)
### Structured Output
It is often crucial to have LLMs return structured output. 
How: Prompting ; Function calling ; Tool calling; JSON mode
[[Structured-output|Structured output]]

### Quantization
... weights and/or activations. Convert the high precision numbers, typically used in neural networks, to lower precision formats. For example, 32-bit floating point could be converted to 16-bit.

https://adaptalent.com/ai-deep-dive-into-quantization/
AI: Building a LLM but want to keep computational costs down? Deep Dive into Quantization

### Model output size
See: [[AI-flow#Model output size (flow)]]

### LLM Reasoning
[[LLM-Reasoning]]

### LLM agents
LLM Агенты ; статья: LLM field landscape  https://habr.com/ru/articles/814665/
[LLM Агенты](https://habr.com/ru/articles/814665/#:~:text=%D1%8F%20%D0%BF%D0%BE%D1%81%D1%82%D0%B0%D1%80%D0%B0%D1%8E%D1%81%D1%8C%20%D0%B7%D0%B0%D1%85%D0%B2%D0%B0%D1%82%D0%B8%D1%82%D1%8C.-,LLM%20%D0%90%D0%B3%D0%B5%D0%BD%D1%82%D1%8B,-%D0%9C%D0%BE%D1%91%20%D0%B2%D0%BE%D0%BB%D1%8C%D0%BD%D0%BE%D0%B5%20%D0%BE%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)

### Automatic Speech Recognition
See: [[ASR]]  ; See: [[Diarization]]

## Tokenizers
GPT tokenizers, GPT token decoder and encoder.
[[Tokenizers]]


## AI-methods

### Fine-tuning
Fine-tuning is where you take an already-pre-trained model and further train it on a more specific dataset...  See: [[Fine-tuning]]


### Embedding (AI)
LLM embedding models;  [[Embeddings]]

### RAG 
Retrieval Augmented Generation (RAG). Добавление собственных данных в LLM. See: [[RAG]]

### Transfer learning
see: [[AI-Model-Sizes#^transfer-learning]]
> именно с этой концепцией связан расцвет многих опенсорс моделей


### Chaining, Inference chaining, LLM chaining
[[Chaining#Chaining, Inference chaining, LLM chaining]]

### LLM with RL
[[#RL - Reinforcement Learning, LLM with RL]]
### RL - Reinforcement Learning, LLM with RL
LLM with RL refers to the combination of Large Language Models (LLMs) with Reinforcement Learning (RL). 
https://github.com/floodsung/LLM-with-RL-papers

## MLOps concepts
terminology
#### Model server (LLM Model server)
[[AI-MLOps-flow#Model server (LLM Model server)]]


## /end