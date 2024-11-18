---
aliases:
  - Introduction to LLMs (article)
up:
  - [[AI-articles]]
---
up:  [[AI-articles]]

https://roadmap.sh/guides/introduction-to-llms

Introduction to LLMs
[PATRTIALLY CACHED]

-----
## Training an LLM Model

On a high level, training an LLM model involves three steps i.e. data collection, training and evaluation.

- **Data Collection** The first step is to collect the data that will be used to train the model. The data can be collected from various sources such as Wikipedia, news articles, books, websites etc.
    
- **Training**: The data then goes through a training pipeline where it is cleaned and preprocessed before being fed into the model for training. The training process usually takes a long time and requires a lot of computational power.
    
- **Evaluation**: The final step is to evaluate the performance of the model to see how well it performs on various tasks such as question answering, summarization, translation etc.
    

The output from the training Pipeline is an LLM model which is simply the parameters or weights which capture the knowledge learned during the training process. These parameters or weights are typically serialized and stored in a file, which can then be loaded into any application that requires language processing capabilities e.g. text generation, question answering, language processing etc.

## Types of LLMs
On a high level, LLMs can be categorized into two types i.e. Base LLMs and Instruction tuned LLMs.
### Base LLMs
Base LLMs are the LLMs which are designed to predict the next word based on the training data. They are not designed to answer questions, carry out conversations or help solve problems. For example, if you give a base LLM the sentence “In this book about LLMs, we will discuss”, it might complete this sentence and give you “In this book about LLMs, we will discuss **what LLMs are, how they work, and how you can leverage them in your applications.**.” Or if you give it “What are some famous social networks?”, instead of answering it might give back “Why do people use social networks?” or “What are some of the benefits of social networks?”. As you can see, it is giving us relevant text but it is not answering the question. This is where the Instruction tuned LLMs come in to the picture.

### Instruction tuned LLMs
Instruction Tuned LLMs, instead of trying to autocomplete your text, try to follow the given instructions using the data that they have been trained on. For example, if you input the sentence “What are LLMs?” it will use the data that it is trained on and try to answer the question. Similarly, if you input “What are some famous social networks?” it will try to answer the question instead of giving you a random answer.

Instruction Tuned LLMs are built on top of Base LLMs:

```
Instruction Tuned LLMs = Base LLMs + Further Tuning + RLHF
```

To build an Instruction Tuned LLM, a Base LLM is taken and is further trained using a large dataset covering sample “Instructions” and how the model should perform as a result of those instructions. The model is then fine-tuned using a technique called “Reinforcement Learning with Human Feedback” (RLHF) which allows the model to learn from human feedback and improve its performance over time.