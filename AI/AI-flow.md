---
aliases:
  - AI-flow (MAIN)
---
# AI-flow

#### Convolutional neural network
###### сверточные нейросети
сверточные нейросети
https://en.wikipedia.org/wiki/Convolutional_neural_network
https://ru.wikipedia.org/wiki/Свёрточная_нейронная_сеть 

[[ABGuide-TU-Convolutional-NN|A Beginner's Guide To Understanding Convolutional Neural Networks (article)]]


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


#### Why fine tune a 65B LLM instead of using established task specific smaller models (~200 millions)?

![[reddit--header.webp]]
https://www.reddit.com/r/MachineLearning/comments/15xfesk/d_why_fine_tune_a_65b_llm_instead_of_using/    [u/EnthusiasmNew7222](https://www.reddit.com/user/EnthusiasmNew7222/)
... Everywhere I look today (medium, reddit, twitter) everyone is talking about fine-tuning LLMs. How the future is taking billion size models and fine-tuning/distilling them to specialised LLMs that perform specific tasks (i.e: sentiment analysis, Q&A, summarisation).

Why not just use “small” (millions vs billion size) models



### What infrastructure do you use to train big LLMs
 What infrastructure do you use to train big LLMs?  : 
	https://www.reddit.com/r/MachineLearning/comments/17iz8i1/r_what_infrastructure_do_you_use_to_train_big_llms/  
	What infrastructure do you use to train big LLMs? 



#### embeddings  или fine-tuning? (misleading)
embeddings  или fine-tuning?
вопрос неправильный, правильный: RAG или fine-tuning?

see: [[AI-concept#Fine-tuning]]

https://www.iguazio.com/questions/what-is-the-key-difference-between-fine-tuning-and-embedding-a-foundational-model/
Fine-tuning is the process of taking a pre-trained model and training it further on a smaller, domain-specific dataset. This additional training helps the model adapt to the nuances and requirements of the specific task or domain.
Fine-tuning helps transferring the general knowledge learned from the foundational training on to specific tasks or domains, to enhance the model's performance on those tasks.

Embedding a foundational model means integrating or incorporating the pre-trained model into another system or application, but without significantly altering its learned parameters. This means using the model's capabilities as they are. (ПОКА НЕПОНЯТНО)


------
#### how-to-train-a-custom-llm-embedding-model

https://dagshub.com/blog/how-to-train-a-custom-llm-embedding-model/

------
#### Text embeddings

https://modal.com/blog/embedding-wikipedia

Text embeddings are a key component of production-ready applications using large language models (LLMs). A text embedding model transforms chunks of text into vectors of floating-point numbers that represent their semantic meaning, allowing us to quantitatively compare strings for similarity. Creating embeddings on a large corpus of text enables us to build applications like search and recommendation engines, as well as give additional context to LLMs for Retrieval-Augmented Generation (RAG) on custom documents.

Embedding models behind APIs like OpenAI’s text-embedding-ada-002 are a great way to get started with building for these use cases. However, as you gather user data and tailor your applications using that data, you will likely get higher-quality results at lower cost if you used this data to fine-tune an open-source embedding model. This requires setting up large-scale embedding jobs, which can be a challenge due to rate limits, infrastructure complexity, and the infeasibility of getting a large number of GPUs for short bursts of time. So what can we do? Enter Modal.

------
#### efficient compute frontier

https://www.youtube.com/shorts/35IpOK-WaNA
 The efficient compute frontier


#### 2024-03-21 // Linguistic Fingerprinting with Python
linguistic-fingerprinting-with-python
https://medium.com/m/global-identity-2?redirectUrl=https%3A%2F%2Ftowardsdatascience.com%2Flinguistic-fingerprinting-with-python-5b128ae7a9fc
Linguistic Fingerprinting with Python
Attributing authorship with punctuation heatmaps
member-only


------
#### Prompt injection explained, with video, slides, and a transcript

simonwillison.net (https://simonwillison.net/2023/May/2/prompt-injection-explained/?utm_source=substack&utm_medium=email)
Prompt injection explained, with video, slides, and a transcript
I participated in a webinar this morning about prompt injection, organized by LangChain and hosted by Harrison Ch....

YouTube: https://www.youtube.com/watch?v=FgxwCaL6UTA
![[2023-05-31_20-46.webp]]


## /end