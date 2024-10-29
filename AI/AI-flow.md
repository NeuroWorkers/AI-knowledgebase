---
aliases:
  - AI-flow (MAIN)
---
# AI-flow

#### Convolutional neural network
###### сверточные нейросети
сверточные нейросети
https://en.wikipedia.org/wiki/Convolutional_neural_network


#### instruct (suffix for LLM file)

As you browse the ever growing global catalogue of generative AI models, you will see some of the Large Language Models (LLMs) being listed with the suffix 'instruct' or 'chat'. What does this mean?

TL:DR; The 'instruct' version of the model has been fine-tuned to be able to follow prompted instructions. These models 'expect' to be asked to do something. Models with the 'chat' suffix have been fine-tuned to work in chatbots. These models 'expect' to be involved in a conversation with different actors. In contrast non-instruct tuned models will simply generate an output that follows on from the prompt. If you are making a chatbot, implementing RAG or using agents, use instruct or chat models. If in doubt us an instruct model.


#### Model output size (flow)
google:// chat gpt output size
community.openai.com:  [What is the maximum response length (output tokens) for each GPT model?](https://community.openai.com/t/what-is-the-maximum-response-length-output-tokens-for-each-gpt-model/524066)     Nov 2023
On https://platform.openai.com/docs/models 1.8k the following maximum response lengths are provided:
gpt-4-1106-preview (GPT4-Turbo): 4096
gpt-4-vision-preview (GPT4-Turbo Vision): 4096
gpt-3.5-turbo-1106 (GPT3.5-Turbo): 4096


#### Video -- multimodal LLM
google://
multimodal LLM that can analize video


The BEST open source Multimodal LLM I've seen so far - InternVL-Chat-V1.5   https://www.reddit.com/r/LocalLLaMA/comments/1c966ce/the_best_open_source_multimodal_llm_ive_seen_so/
 
It came out 2 days ago and apparently, it's a 20B LLM base with a 6B vision model that can accept up to a 4k(!) image.  github.com/OpenGVLab/InternVL


#### Structured Output
It is often crucial to have LLMs return structured output. 
How: Prompting ; Function calling ; Tool calling; JSON mode

Prompting: This is when you ask the LLM (very nicely) to return output in the desired format (JSON, XML). This is nice because it works with all LLMs. It is not nice because there is no guarantee that the LLM returns the output in the right format.
Function calling: This is when the LLM is fine-tuned to be able to not just generate a completion, but also generate a function call. The functions the LLM can call are generally passed as extra parameters to the model API. The function names and descriptions should be treated as part of the prompt (they usually count against token counts, and are used by the LLM to decide what to do).
Tool calling: A technique similar to function calling, but it allows the LLM to call multiple functions at the same time.
JSON mode: This is when the LLM is guaranteed to return JSON.


#### LLM Reasoning
LLM Reasoning ability
> LLM Reasoning // Prompt Engineering Guide : https://www.promptingguide.ai › research › llm-reasoning // More recently, LLMs have shown the potential to exhibit reasoning abilities when scaled to a large enough size. https://www.promptingguide.ai/research/llm-reasoning


atfortes/Awesome-LLM-Reasoning
[atfortes/Awesome-LLM-Reasoning](https://github.com/atfortes/Awesome-LLM-Reasoning)
Curated collection of papers and resources on how to unlock the reasoning ability of LLMs and MLLMs

Curated collection of papers and resources on _how to unlock the reasoning ability of LLMs_ and MLLMs.
#### Independency temperature (prompts)
"required independency temperature", как в промпте 

#### Inference (Model Inference)
основное юзерское использование модели - запрашиваем ей запрос и получаем результат.

> Model inference (or machine learning inference) is when a model makes predictions on new, unseen input data (inference data) and produces predictions as output that are consumed by a user or service.  https://www.hopsworks.ai/dictionary/model-inference

https://www.hopsworks.ai/dictionary/model-inference
Model inference requires a: 
ML model || inference data || an inference pipeline || prediction consumer. 
‍Batch Model Inference -> ...
‍Online Model Inference -> request-response network services, exposed as a REST or gRPC endpoint (authentication & access control )


###### Типы инференса ML моделей (article)
https://ml-system-design.ru/blog/inference/типы-инференса-ml-моделей 


###### inference pipeline
https://www.hopsworks.ai/dictionary/inference-pipeline


#### Context window, Контекстное окно (flow)

##### \*  Оценка LLM с большим окном контекста
Sivchenko_translate 2 авг 2023 https://habr.com/ru/articles/752062/
MTS AI  .... свои фундаментальные языковые модели. ...  получилось достичь уровня gpt-4 на собственном ограниченном датасете большого контекста.



##### \*  Как сделать контекстное окно на 100K в большой языковой модели: обо всех фокусах в одном посте
Sivchenko_translate   2 авг 2023  https://habr.com/ru/articles/752062/

в статье рассмотрены приёмы, позволяющие ускорить обучение больших языковых моделей (LLM) и нарастить в них вывод (inference). Для этого нужно использовать большое контекстное окно, в котором умещается до 100K входных токенов. Вот эти приёмы: ALiBi с подмешиванием в вектор позиции слова в последовательности (positional embedding), разреженное внимание (Sparse Attention), мгновенное внимание (Flash Attention),



#### Context window size

2023 <font color="#ffff00">65K</font> , <font color="#ffff00">100K</font>   ,  GPT-4 <font color="#00b050">32K</font> токенов. опенсорс LLM <font color="#00b050">2K</font>

Недавно прошло несколько анонсов по поводу новых больших языковых моделей (LLM), настроенных на приём исключительно крупного контекстного окна, целых 65K токенов (MPT-7B-StoryWriter-65k+ от MosaicML) или даже 100K токенов (описано в статье Introducing 100K Context Windows от Antropic)
...
Для сравнения: современная модель GPT-4 может работать, получая контекст длиной 32K входных токенов. Большинство же опенсорсных моделей LLM работают с контекстным окном длиной 2K токенов.
see: [[#* Как сделать контекстное окно на 100K в большой языковой модели обо всех фокусах в одном посте]]


#### Fine-tuning (flow)
Fine-tuning in machine learning is the process of adapting a pre-trained model for specific tasks or use cases. https://www.ibm.com/topics/fine-tuning


>  Fine-tuning is where you take an already-pre-trained model and further train it on a more specific dataset. This dataset is typically smaller and focused on a particular domain or task. The purpose of fine-tuning is to adapt the model to perform better in specific scenarios or on tasks that were not well covered during pre-training. The new knowledge added during fine-tuning is more about enhancing the model's performance in specific contexts rather than broadly expanding its general knowledge.
[reddit>>](https://www.reddit.com/r/learnmachinelearning/comments/19f04y3/comment/kjgtuwu/)



#### embeddings  или fine-tuning? (misleading)
embeddings  или fine-tuning?
вопрос неправильный, правильный: RAG или fine-tuning?

see: [[AI-concept#Fine-tuning]]

https://www.iguazio.com/questions/what-is-the-key-difference-between-fine-tuning-and-embedding-a-foundational-model/
Fine-tuning is the process of taking a pre-trained model and training it further on a smaller, domain-specific dataset. This additional training helps the model adapt to the nuances and requirements of the specific task or domain.
Fine-tuning helps transferring the general knowledge learned from the foundational training on to specific tasks or domains, to enhance the model's performance on those tasks.

Embedding a foundational model means integrating or incorporating the pre-trained model into another system or application, but without significantly altering its learned parameters. This means using the model's capabilities as they are. (ПОКА НЕПОНЯТНО)


