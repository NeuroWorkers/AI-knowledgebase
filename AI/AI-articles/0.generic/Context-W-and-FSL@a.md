---
aliases:
  - "Context windows and few-shot learning (article)"
up:
  - [[AI-articles]]
---
URL: https://artificial-intuition.beehiiv.com/p/few-shot-learning-context-learning

up:  [[AI-articles]]
# Context windows and few-shot learning.
Niranjan Sridhar March 18, 2023
## What is few-shot learning?

N-shot learning is when an machine learning model can learn a new task by seeing N examples of that task. So 1-shot means the model only needs a 1 labeled example to learn a new task, few-shot model needs more, say 5-20.

![[c2a51833a5f6c9a0e8b5acb828a1b4db_MD5.opti.webp]]

Prior to 2016, the best machine learning models (like Inception and Resnet) were supervised models that could reach human level image recognition performance. However, these models were large enough that they needed large amounts of data to train. On any small dataset, (e.g. medical) they would quickly overfit and be unusable. However, it was found that the Inception/Resnet models trained on large datasets could then be finetuned on small new datasets. Surprisingly, this works incredibly well. Not only do the finetuned models learn a completely new skill with very small data, they are actually perform much better on this new skill than models that are trained exclusively on the new skill.

Since then an active pursuit of machine learning research has been to measure and try to decrease the amount of data required learn a new skill.

_**Ok… still tho. Why is this important?**_

It might seem like few-shot learning is just one of the many ML training techniques, but there is reason to believe that it might be the most important feature that we should care about.

## Intuition 1 - Humans are few-shot learners

A 2 year old sees a car once or twice and can somehow connect the intellectual dots required to recognize the other moving objects on the road as cars. They can even connect images in books to real life objects. Adults can watch an instructional video of changing a tire and can transfer the skill to a real life flat-tire situation with a different car and new tools.

It is widely believed today that such 'persistent few-shot learning capability' is a necessary condition for human-level general intelligence. There is no theoretical reason to believe this, humans are the only example of general intelligence we have so it is a best guess. But why did I sneak in the word 'persistent' here?

When people learn a new task, they don't get worse at every other task they know. In general, finetuning a pretrained ML model on a new task _does_ make it worse on other tasks. The research literature is a bit confusing on this issue, as the meaning of 'few-shot learning' has evolved over the years. Papers from over 5+ years ago sometimes use few-shot learning when what they are really doing is transfer learning, i.e. the model learns something new but forget the old tasks. However, today the field has converged on a rigorous definition where few-shot learning means 'persistent few shot learning' i.e. the model has the ability to learn new tasks and learning one task does not affect the model’s performance on other tasks.

With this definition, humans, and as far as we know _only humans_, are few-shot learners.

## Intuition 2 - LLMs can learn in-context

The fundamental problem with few-shot learning is "how do you add new information to an already trained model"? Fine-tuning, the process of incremental training a pretrained model with a new objective or new data or both, is known to destroy already learned information in the model, i.e. this is not a good way to do persistent few-shot learning. For image models, the best option we have today is to finetune just a little bit so that only a little bit of information is destroyed and model is still usable.

Language is a unique data format where the information about the task can be contained within the input. It might be useful to see an example. Released in 2018, BERT was a large language model trained to do question-answering. You could ask "What color is the sky?" and you might expect the answer "Blue". But let's say you ask a language model "Repeat each letter of the answer twice. What color is the sky?" and it replies "Bblluuee". Now you have added some instructions about the task, known as the **context** and then you have asked a question which the model will answer keeping the context in mind.

OpenAI took this to its logical conclusion with GPT-3 in their paper ["Large Language Models are few-shot learners"](https://arxiv.org/pdf/2005.14165.pdf?utm_source=artificial-intuition.beehiiv.com&utm_medium=referral&utm_campaign=context-windows-and-few-shot-learning). They found that as the models became larger and train on more data, there are no limits to what can be in the context. For example you could _teach_ the model how to do mathematics or play games by putting those instructions in the context and the model would reply to questions as if it has learnt the new context.

![[7483599830912b3858e2260309b4e86c_MD5.opti.webp]]

You can train an LLM to do sentiment analysis by just giving it a few examples as context.

Now it starts becoming a little clearer why this is a big deal. There is no fine-tuning, no training or destruction of information. Using the unique property of language that allows both the rules and the tools of the game in the same format, large language models can 'learn' arbitrary new tasks within context. This also clarifies why the biggest mind blowing feature of GPT-4 is a context window of 32768 tokens, compared to GPT-3s context window of 2048 tokens. Longer context window means you can add more complex instructions and consequently the model can do more complex actions.

Of course today’s LLM’s are not as good as humans are at few-shot learning. But if we build LLMs with context window a few years long, could it match human level intelligence? Increasing context window sizes is a difficult technical challenge that we will revisit in a future post.