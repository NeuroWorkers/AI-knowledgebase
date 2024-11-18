---
aliases:
  - Mixtral (model)
  - Mixtral (Mixture of Experts model)
up:
  - [[AI#AI Models]]
---
up:  [[AI#AI Models]]
# Mixtral
Mixtral-8x7B.
https://huggingface.co/docs/transformers/en/model_doc/mixtral
#### MoE – Mixture of Experts
Ее важная особенность, технология MoE – Mixture of Experts 
https://huggingface.co/blog/moe

see [[#MoE – Mixture of Experts – это не просто «склеить восемь сеток»]]


https://mistral.ai/news/mixtral-of-experts/
Today, the team is proud to release Mixtral 8x7B, a high-quality sparse mixture of experts model (SMoE) with open weights. Licensed under Apache 2.0. Mixtral outperforms Llama 2 70B on most benchmarks with 6x faster inference.

https://www.promptingguide.ai/models/mixtral
In this guide, we provide an overview of the Mixtral 8x7B model, including prompts and usage examples. The guide also includes tips, applications, limitations, papers, and additional reading materials related to Mixtral 8x7B.


#### Orig 2023-12

новость на гитхабе
	https://github.com/huggingface/transformers/releases/tag/v4.36.0
	v4.36: Mixtral, Llava/BakLlava, SeamlessM4T v2, AMD ROCm, F.sdpa wide-spread support
	.
	Mixtral is the new open-source model from Mistral AI announced by the blogpost [Mixtral of Experts](https://mistral.ai/news/mixtral-of-experts/). The model has been proven to have comparable capabilities to Chat-GPT



>open source моделей много скачать можно на hugging face. обычно the bloke выкладывает. можно запустить на cpu с помощью llama.cpp в формате gguf. для это модели надо прилично памяти 32Г/40Г




https://www.linux.org.ru/news/opensource/17451901
Mistral, французский ИИ-стартап, который выложил свою последнюю крупную языковую модель в ссылке на торрент.
	В понедельник компания наконец дополнила свой первоначальный релиз блог-постом с подробностями о программе, которая просто называется Mixtral-8x7B. Согласно приведенным в посте бенчмаркам, алгоритм Mistral превосходит некоторых американских конкурентов, включая семейство Llama 2 от Meta и GPT-3.5 от OpenAI. Похоже, люди в интернете согласны с тем, что новый алгоритм Mistral довольно хорош.
	Бонус к этому — Mixtral-8x7B имеет открытый исходный код, в отличие от иронически названной OpenAI, которая держит свои последние LLM закрытыми, что вызвало определенное недовольство среди сообщества.


Основное достижение - придумали и показали, как склеить вместе восемь 7B сеток, натренированных на разных наборах данных. [Barracuda72](https://www.linux.org.ru/people/Barracuda72/profile)(15.12.23) [Ссылка](https://www.linux.org.ru/news/opensource/17451901?cid=17452875) (https://www.linux.org.ru/news/opensource/17451901)

-------------------

 [работа по архитектуре Mamba](https://arxiv.org/ftp/arxiv/papers/2312/2312.00752.pdf), которая позволяет добавлять структурированные пространства состояний (SSM). Это позволяет использовать множественный контекст с линейной сложностью, а не квадратичной. Там и сокращение использования ресурсов при том же качестве модели по сравнению с Chat GPT и уверенная работа с последовательностями на порядки большей длины токенов чем в обучающих примерах и много чего еще.

----------------------------------

#### MoE – Mixture of Experts – это не просто «склеить восемь сеток»

MoE – Mixture of Experts – это не просто «склеить восемь сеток», это модель с точностью и качеством как у полносвязной модели аналогичного веса (40 млрд весов), при вычислительных затратах в режиме генерации как у модели на 7 миллиардов весов.

Еще это и в процессе обучения работает, но несколько меньший прирост даёт.

Обучается сеть как одно целое, а не раздельные части, не надо путать с мультимодальными моделями где есть основная модель и куча адаптеров которые переводят разные типы данных в понятны основно модели формат.

[timdorohin](https://www.linux.org.ru/people/timdorohin/profile) ★★★★ (16.12.23 17:15:16 GST) - [Ссылка](https://www.linux.org.ru/news/opensource/17451901?cid=17454250)

---------------------------








