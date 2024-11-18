---
aliases: 
  - "12 GPT-4 Open-Source Alternatives (articles)"
up: [[AI-articles]]
---
up: [[AI-articles]]
https://www.datacamp.com/blog/12-gpt4-open-source-alternatives
# 12 GPT-4 Open-Source Alternatives

GPT-4 open-source alternatives that can offer similar performance and require fewer computational resources to run. These projects come with instructions, code sources, model weights, datasets, and chatbot UI.

Apr 2023 · 9 min read

CONTENTS orig
	- [1. ColossalChat](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#1.-colossalchat-colos)
	- [2. Alpaca-LoRA](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#2.-alpaca-lora-alpac)
	- [3. Vicuna](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#3.-vicuna-thevi)
	- [4. GPT4ALL](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#4.-gpt4all-gpt4a)
	- [5. Raven RWKV](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#5.-raven-rwkv-raven)
	- [6. OpenChatKit](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#6.-openchatkit-%3Cahre)
	- [7. OPT](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#7.-opt-opt(o)
	- [8. Flan-T5-XXL](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#8.-flan-t5-xxl-flan-)
	- [9. Baize](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#9.-baize-%3Cahre)
	- [10. Koala](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#10.-koala-theko)
	- [11. Dolly](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#11.-dolly-dolly)
	- [12. Open Assistant](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#12.-open-assistant-opena)
	- [Conclusion](https://www.datacamp.com/blog/12-gpt4-open-source-alternatives#conclusion-these)



[An avian AI exits its cage](https://images.datacamp.com/image/upload/v1682076850/An_avian_AI_exits_its_cage_8d2b033144.png)
GPT-4 is the most advanced Generative AI developed by OpenAI. It is changing the landscape of how we do work. However, GPT-4 is not open-source, meaning we don’t have access to the code, model architecture, data, or model weights to reproduce the results. We cannot create our own GPT-4 like a chatbot. 

To balance the scale, open-source communities have started working on GPT-4 alternatives that offer almost similar performance and functionality and require fewer computational resources.

You can learn about GPT-1, GPT-2, GPT-3, and GPT-4 by reviewing: [What is GPT-4 and Why Does it Matter?](https://www.datacamp.com/blog/what-we-know-gpt4), or you can learn to use [ChatGPT For Data Science Projects](https://www.datacamp.com/tutorial/chatgpt-data-science-projects) and master [prompt engineering](https://www.datacamp.com/blog/what-is-prompt-engineering-the-future-of-ai-communication) to get better at building end to end data science projects. 

In the article, we will introduce 12 GPT-4 alternatives with a brief description and links to the relevant research paper, blog post, chatbot demo, code source, and model card. 

Note: Some of the models mentioned have a non-commercial license, which restricts their use to research and academic purposes only. You need to understand these limitations before using them.

## 1. ColossalChat

ColossalChat is an open-source project that allows you to clone AI models using a complete RLHF (Reinforcement Learning from Human Feedback) pipeline. 

It is a completely open-source project comprising the bilingual dataset, training code, demo, and 4-bit quantized inference. All the components will help you create a customized chatbot cheaper and faster.

[image10.png](https://images.datacamp.com/image/upload/v1681725738/image10_4519004cab.png)

Image from [ColossalChat](https://chat.colossalai.org/)

- Research paper: [Colossal-AI: A Unified Deep Learning System For Large-Scale Parallel Training](https://arxiv.org/abs/2110.14883)
- Blog post: [ColossalChat: An Open-Source Solution for Cloning ChatGPT With a Complete RLHF Pipeline](https://medium.com/@yangyou_berkeley/colossalchat-an-open-source-solution-for-cloning-chatgpt-with-a-complete-rlhf-pipeline-5edf08fb538b)
- GitHub: [hpcaitech/ColossalAI](https://github.com/hpcaitech/ColossalAI)
- Demo: [ColossalChat (colossalai.org)](https://chat.colossalai.org/)

## 2. Alpaca-LoRA

Alpaca-LoRA is a model that was created using the [Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca) and [low-rank adaptation (LoRA)](https://arxiv.org/pdf/2106.09685.pdf). The low-rank adoption allows us to run an Instruct model of similar quality to GPT-3.5 on 4GB RAM Raspberry Pi 4. 

The project provides source code, fine-tuning examples, inference code, model weights, dataset, and demo. The best part is that we can train our model within a few hours on a single RTX 4090.

[image2.png](https://images.datacamp.com/image/upload/v1681725783/image2_1184e03f6c.png)

Image from [Alpaca-LoRA](https://huggingface.co/spaces/tloen/alpaca-lora)

- GitHub: [tloen/alpaca-lora](https://github.com/tloen/alpaca-lora)
- Model Card: [tloen/alpaca-lora-7b](https://huggingface.co/tloen/alpaca-lora-7b)
- Demo: [Alpaca-LoRA](https://huggingface.co/spaces/tloen/alpaca-lora)

## 3. Vicuna

The Vicuna can generate coherent and creative text for chatbots. It is a transformer-based architecture that was fine-turned on a conversational dataset collected from ShareGPT.com.

Vicuna provides almost 90% of ChatGPT performance. It is a part of [FastChat](https://github.com/lm-sys/FastChat#fine-tuning), an open platform that allows users to train, serve, and evaluate their chatbots. FastChat provides all the necessary components and tools for building a custom chatbot model.

[image14.png](https://images.datacamp.com/image/upload/v1681725821/image14_e4055cc639.png)

Image from [FastChat (lmsys.org)](https://chat.lmsys.org/)

- Blog post: [Vicuna: An Open-Source Chatbot Impressing GPT-4 with 90%* ChatGPT Quality | by the Team with members from UC Berkeley, CMU, Stanford, and UC San Diego](https://vicuna.lmsys.org/)
- GitHub: [lm-sys/FastChat](https://github.com/lm-sys/FastChat#fine-tuning)
- Demo: [FastChat (lmsys.org)](https://chat.lmsys.org/)

## 4. GPT4ALL
see MLops / [[GPT4All]] , 

GPT4ALL is a chatbot developed by the Nomic AI Team on massive curated data of assisted interaction like word problems, code, stories, depictions, and multi-turn dialogue. The model architecture is based on LLaMa, and it uses low-latency machine-learning accelerators for faster inference on the CPU.

With GPT4ALL, you get a Python client, GPU and CPU interference, Typescript bindings, a chat interface, and a Langchain backend.

[image3.png](https://images.datacamp.com/image/upload/v1681725872/image3_cb83c1b235.png)

Image from [gpt4all-ui](https://github.com/nomic-ai/gpt4all-ui)

- Technical Report: [GPT4All](https://s3.amazonaws.com/static.nomic.ai/gpt4all/2023_GPT4All_Technical_Report.pdf)
- GitHub: [nomic-ai/gpt4al](https://github.com/nomic-ai/gpt4all)
- Chatbot UI: [nomic-ai/gpt4all-ui](https://github.com/nomic-ai/gpt4all-ui)
- Model card: [nomic-ai/gpt4all-lora](https://huggingface.co/nomic-ai/gpt4all-lora)

## 5. Raven RWKV

Raven RWKV is part of [ChatRWKV](https://github.com/BlinkDL/ChatRWKV), which is an open-source model like ChatGPT but powered by RWKV (100% RNN) language model, not transformer based.

By utilizing RNNs, the model achieves comparable levels of quality and scalability as transformers, with the added benefits of faster processing speed and VRAM conservation. Raven was fine-tuned to follow instructions, and it was fine-tuned on Stanford Alpaca, code-alpaca, and more datasets. 

[image6.png](https://images.datacamp.com/image/upload/v1681725969/image6_729581c54e.png)

Image from [Raven RWKV 7B](https://huggingface.co/spaces/BlinkDL/Raven-RWKV-7B)

- GitHub: [BlinkDL/ChatRWKV](https://github.com/BlinkDL/ChatRWKV)
- Demo: [Raven RWKV 7B](https://huggingface.co/spaces/BlinkDL/Raven-RWKV-7B)
- Model card: [BlinkDL/rwkv-4-raven](https://huggingface.co/BlinkDL/rwkv-4-raven)

## 6. OpenChatKit

[OpenChatKit](https://www.kdnuggets.com/2023/03/openchatkit-opensource-chatgpt-alternative.html) is a comprehensive toolkit that offers an open-source alternative to ChatGPT for developing the chatbot application. 

The toolkit includes step-by-step instructions for training your own instruction-tuned large language model, fine-tuning the model, and an extensible retrieval system for updating the bot's responses. Additionally, it includes both moderation features that can help filter out inappropriate questions.

[image11.png](https://images.datacamp.com/image/upload/v1681726011/image11_7c8ba08336.png)

Image from [OpenChatKit](https://huggingface.co/spaces/togethercomputer/OpenChatKit) 

- Blog Post: [Announcing OpenChatKit — TOGETHER](https://www.together.xyz/blog/openchatkit)
- GitHub: [togethercomputer/OpenChatKit](https://github.com/togethercomputer/OpenChatKit)
- Demo: [OpenChatKit](https://huggingface.co/spaces/togethercomputer/OpenChatKit) 
- Model card: [togethercomputer/GPT-NeoXT-Chat-Base-20B](https://huggingface.co/togethercomputer/GPT-NeoXT-Chat-Base-20B)

## 7. OPT

OPT (Open Pre-trained Transformer) Language Models have demonstrated remarkable abilities in zero-shot and few-shot learning, as well as Stereotypical Bias analysis, despite not matching the quality of ChatGPT. 

OPT is a family of large language models ranging from 125M to 175B parameters. The models are decoder-only transformers, which means they generate text autoregressive from left to right.

[image4.png](https://images.datacamp.com/image/upload/v1681726054/image4_55ef104c33.png)

Image from [A Watermark for LLMs](https://huggingface.co/spaces/tomg-group-umd/lm-watermarking)

- Research Paper: [OPT: Open Pre-trained Transformer Language Models](https://arxiv.org/abs/2205.01068)
- GitHub: [facebookresearch/metaseq](https://github.com/facebookresearch/metaseq)
- Demo: [A Watermark for LLMs](https://huggingface.co/spaces/tomg-group-umd/lm-watermarking)
- Model card: [facebook/opt-1.3b](https://huggingface.co/facebook/opt-1.3b)

## 8. Flan-T5-XXL

Flan-T5-XXL was fine-tuned T5 models that have been trained on a vast collection of datasets presented in the form of instructions. This type of fine-tuning has significantly improved performance on a variety of model classes, such as PaLM, T5, and U-PaLM. Moreover, the Flan-T5-XXL model was fine-tuned on more than 1000 additional tasks covering multiple languages. 

[image1.png](https://images.datacamp.com/image/upload/v1681726098/image1_50e681134f.png)

Image from [Chat Llm Streaming](https://huggingface.co/spaces/olivierdehaene/chat-llm-streaming)

- Research Paper: [Scaling Instruction-Fine Tuned Language Models](https://arxiv.org/pdf/2210.11416.pdf)
- GitHub: [google-research/t5x](https://github.com/google-research/t5x)
- Demo: [Chat Llm Streaming](https://huggingface.co/spaces/olivierdehaene/chat-llm-streaming)
- Model card: [google/flan-t5-xxl](https://huggingface.co/google/flan-t5-xxl?text=Q%3A+%28+False+or+not+False+or+False+%29+is%3F+A%3A+Let%27s+think+step+by+step)

## 9. Baize

[Baize](https://www.kdnuggets.com/2023/04/baize-opensource-chat-model-different.html) exhibits impressive performance in multi-turn dialogues thanks to its guardrails that help mitigate potential risks. It has achieved this through a high-quality multi-turn chat corpus, which was developed by leveraging ChatGPT to facilitate conversations with itself.

Baize code source, model, and dataset are released under a non-commercial (research purposes) license. 

[image7.png](https://images.datacamp.com/image/upload/v1681726140/image7_3ecbc43362.png)Image from [Baize 7B](https://huggingface.co/spaces/project-baize/Baize-7B)

- Research Paper: [Baize: An Open-Source Chat Model with Parameter-Efficient Tuning on Self-Chat Data](https://arxiv.org/abs/2304.01196)
- GitHub: [project-baize/baize-chatbot](https://github.com/project-baize/baize-chatbot)
- Demo: [Baize 7B](https://huggingface.co/spaces/project-baize/Baize-7B)
- Model card: [project-baize/baize-lora-7B](https://huggingface.co/project-baize/baize-lora-7B)

## 10. Koala

The Koala is a chatbot trained by fine-tuning LLaMa on a dialogue dataset scraped from the web. Koala has performed better than Alpaca and is similar to ChatGPT in many cases. 

Koala provides training code, public weights, and dialogue fine tuner, and it was evaluated by 100 humans.  

[image8.png](https://images.datacamp.com/image/upload/v1681726176/image8_2eec0dfa2f.png)

Image from [FastChat/Koala](https://chat.lmsys.org/?model=koala-13b)

- Blog Post: [Koala: A Dialogue Model for Academic Research](https://bair.berkeley.edu/blog/2023/04/03/koala/)
- GitHub: [young-geng/EasyLM](https://github.com/young-geng/EasyLM#koala)
- Demo: [FastChat/Koala](https://chat.lmsys.org/?model=koala-13b)

## 11. Dolly

Dolly is a large language model that was trained by Databricks machine to demonstrate that we can use old open-source language mode and give them ChatGPT magic instruction following ability. Model training requires 30 minutes on one machine, using high-quality training data. You don’t even require large models to achieve high quality. The team has used the 6 billion parameters model, compared to 175 billion for GPT-3.

Check out [Dolly 2.0](https://www.databricks.com/blog/2023/04/12/dolly-first-open-commercially-viable-instruction-tuned-llm?ref=emergentmind), an instruction-following language model that can be used commercially.

[image12.png](https://images.datacamp.com/image/upload/v1681726206/image12_bccb7d8935.png)

Image from [Hello Dolly](https://www.databricks.com/blog/2023/03/24/hello-dolly-democratizing-magic-chatgpt-open-models.html)

- Blog Post: [Hello Dolly: Democratizing the magic of ChatGPT with open models](https://www.databricks.com/blog/2023/03/24/hello-dolly-democratizing-magic-chatgpt-open-models.html)
- GitHub: [databrickslabs/dolly](https://github.com/databrickslabs/dolly)
- Model card: [databricks/dolly-v1-6b](https://huggingface.co/databricks/dolly-v1-6b)

## 12. Open Assistant

Open Assistant is a truly open-source project, which means giving everyone access to top chat-based large language models. It aims to create a revolution in innovation in language by enabling people to interact with third-party systems, retrieve information dynamically, and create new applications using language. 

You can run the large language chatbot on a single high-end consumer GPU, and its code, models, and data are licensed under open-source licenses.

[image5.png](https://images.datacamp.com/image/upload/v1681726240/image5_f1ce4279a5.png)

Image from [open-assistant.io](https://open-assistant.io/chat)

- Blog Post: [Open Assistant First Models are here!](https://projects.laion.ai/Open-Assistant/blog/2023/04/06/open-assistant-first-models-are-here)
- GitHub: [LAION-AI/Open-Assistant](https://github.com/LAION-AI/Open-Assistant)
- Demo: [open-assistant.io](https://open-assistant.io/chat)
- Model card: [OpenAssistant/oasst-sft-1-pythia-12b](https://huggingface.co/OpenAssistant/oasst-sft-1-pythia-12b)

## Conclusion

These GPT-4 alternatives can help researchers, developers, and small companies to create their language-based technology and compete with giants in the industry. The performance of the models is not above GPT-4, but with time and community contribution, some could have the potential to overtake GPT-4.

If you are new to ChatGPT, try taking our [Introduction to ChatGPT](https://www.datacamp.com/courses/introduction-to-chatgpt) course, and if you are aware of generative AI, you can get better at prompting by reviewing the comprehensive [ChatGPT Cheat Sheet for Data Science,](https://www.datacamp.com/cheat-sheet/chatgpt-cheat-sheet-data-science) or by checking out the resources below.

- [Webinar] [A beginner’s guide to prompt engineering with ChatGPT](https://www.datacamp.com/resources/webinars/ungated-a-beginners-guide-to-prompt-engineering-with-chatgpt)
- [Cheat Sheet] [ChatGPT Cheat Sheet for Data Scientists](https://www.datacamp.com/cheat-sheet/chatgpt-cheat-sheet-data-science)
- [Podcast] [ChatGPT and How Generative AI is Augmenting Workflows](https://www.datacamp.com/podcast/chat-gpt-and-how-generative-ai-is-augmenting-workflows)
- [Start learning AI with DataCamp](https://www.datacamp.com/learn/ai)