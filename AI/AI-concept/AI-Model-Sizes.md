

## Model sizes
Размер модели
Варианты понимания термина Model size - 13B, 7B итп - количество параметров(весов, отсчетов) модели.
Альтернативное понимание, особенно в русском языке.
Размер который модель занимает на диске.
Размер который модель занимает в  памяти.

Примеры
llama 7B  ; See  [[#Example model sizes]]

#### Model sizes RAM/disk

Большая часть моделей: FP16 or BF16

FP16 or BF16
Vanilla LLMs are in 16-bit floating values (i.e., FP16 or BF16), and the bulk of any LLMs is matrix multiplication. Therefore, the major computation cost comes from the floating-point addition and multiplication operations.


-----
fp16, bf16


https://en.wikipedia.org/wiki/Bfloat16_floating-point_format
The bfloat16 (brain floating point)[1][2] floating-point format is a computer number format occupying 16 bits in computer memory; .. using a floating radix point. This format is a shortened (16-bit) version of the 32-bit IEEE 754 single-precision floating-point format (binary32)




-----
## Example model sizes

13B (that's small enough for a laptop).

https://aibusiness.com/nlp/7-language-models-you-need-to-know

### GPT-3 size
Developers: OpenAI
Parameters: 175 billion ~  2024-01
i.e <font color="#00b0f0">175</font>B

### LaMDA size
Developer: Google   ;   Parameters: 137 billion ~  2024-01

Google’s LaMDA (Language Model for Dialogue Applications) model is so accurate that it purportedly convinced an AI engineer it was sentient.
When it is not scaring engineers, the model can generate conversational dialogue in a free-form way – compared to task-based responses traditional models often come up with.
....

And at its 2022 I/O event, the company announced expansions to the model’s capabilities via LaMDA 2. The latest version is reportedly more finely tuned than the original − and can now provide recommendations based on user queries. LaMDA2 was trained on Google’s Pathways Language Model (PaLM), which has 540 billion parameters.  ^9c6b47

------
https://arxiv.org/abs/2207.02852

[Submitted on 5 Jul 2022]
### Machine Learning Model Sizes and the Parameter Gap

Pablo Villalobos, Jaime Sevilla, Tamay Besiroglu, Lennart Heim, Anson Ho, Marius Hobbhahn
We study trends in model size of notable machine learning systems over time using a curated dataset. From 1950 to 2018, model size in language models increased steadily by seven orders of magnitude. The trend then accelerated, with model size increasing by another five orders of magnitude in just 4 years from 2018 to 2022. Vision models grew at a more constant pace, totaling 7 orders of magnitude of growth between 1950 and 2022.
We also identify that, since 2020, there have been many language models below 20B parameters, many models above 70B parameters, but a scarcity of models in the 20-70B parameter range. We refer to that scarcity as the parameter gap.
We provide some stylized facts about the parameter gap and propose a few hypotheses to explain it. The explanations we favor are: (a) increasing model size beyond 20B parameters requires adopting different parallelism techniques, which makes mid-sized models less cost-effective, (b) GPT-3 was one order of magnitude larger than previous language models, and researchers afterwards primarily experimented with bigger models to outperform it. While these dynamics likely exist, and we believe they play some role in generating the gap, we don't have high confidence that there are no other, more important dynamics at play.



------
https://www.tasq.ai/glossary/model-size/


The size of the model is determined by the product being utilized and the contents of the model. This varies depending on the kind of task – classification, regression, technique – SVM, neural net, and data type – image, text, feature size, and so on.

"model size"...

Transfer learning, pruning, and quantization are three explicit techniques that might help democratize machine learning for businesses that don’t have a lot of money to invest in getting models into production. This is especially important for “edge” use cases, where larger, more specialized AI hardware is irrational.

../

Finally, while [transfer learning](https://www.tasq.ai/glossary/transfer-learning/) isn’t a model-contracting approach, it might be useful in situations when there isn’t enough data to train another model. As a first step, transfer learning employs pre-trained models. The model’s information may be “moved” to another job using a small dataset without having to retrain the original model. This is an important way to reduce the amount of computing power, energy, and money needed to train new models. ^transfer-learning