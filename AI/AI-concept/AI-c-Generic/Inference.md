---
aliases:
  - Inference (Model Inference)
  - Temperature (Inference)
up:
  - [[AI-concept#Inference (Model Inference)]]
---
up:  [[AI-concept#Inference (Model Inference)]]

## Inference (Model Inference)
основное юзерское использование модели - запрашиваем ей запрос и получаем результат.
See also: [[Chaining#Chaining, Inference chaining, LLM chaining]]

> Model inference (or machine learning inference) is when a model makes predictions on new, unseen input data (inference data) and produces predictions as output that are consumed by a user or service.  https://www.hopsworks.ai/dictionary/model-inference


### Parameters
#### LLM Temperature
**Controls randomness:** Higher temperature leads to more creative and diverse outputs, while lower temperature yields more focused and deterministic results. (C) [[Gemini-Google|Gemini]]

**What is LLM Temperature?**
https://www.iguazio.com/glossary/llm-temperature/
LLM temperature is a parameter that influences the language model’s output, determining whether the output is more random and creative or more predictable. A higher temperature will result in lower probability, i.e more creative outputs. A lower temperature will result in higher probability, i.e more predictable outputs.
> [!cite]- More about LLM Temperature ...
> 
> - **Low Temperature (<1.0)** – ... **makes the model’s output more deterministic and repetitive**. Lower temperatures lead to the model picking the most likely next word more often, reducing the variability of the output. ...
> - **High Temperature (>1.0)** – ... increases randomness in the generated text. ... select less probable words .... this can also result in **more errors or nonsensical responses**....
> - **Temperature of 1.0** – This is often the default setting, aiming for a balance between randomness and determinism.

##### Top-p (Nucleus Sampling)
  **Selects tokens based on cumulative probability:** A higher top-p value allows for more diverse outputs, while a lower value restricts the model to a smaller set of options. (C) [[Gemini-Google|Gemini]]
##### Top-k
  **Limits the number of tokens considered:** A higher value allows for more diverse outputs, while a lower value restricts the model to a smaller set of options. (C) [[Gemini-Google|Gemini]]
##### Repetition Penalty
  **Discourages repetitive sequences:** A higher penalty reduces the likelihood of repeating the same phrases or words. (C) [[Gemini-Google|Gemini]]
##### Frequency Penalty
 **Penalizes frequently used words:** A higher penalty encourages the model to use a wider vocabulary. (C) [[Gemini-Google|Gemini]]
##### Presence Penalty
**Penalizes words that have already appeared in the text:** A higher penalty discourages the model from repeating the same concepts. (C) [[Gemini-Google|Gemini]]

By adjusting these parameters, you can fine-tune the behavior of an LLM to generate text that is more creative, informative, or focused on specific tasks.

### More articles/info

reddit [Are there frameworks/models that allow you to set temperature sentence by sentence for the output of a LLM?](https://old.reddit.com/r/LocalLLaMA/comments/1bvynmz/are_there_frameworksmodels_that_allow_you_to_set/)

  2024-04  
Isn’t Dynamic Temperature sampling (supported in Kobold and llama.cpp) that does exactly this, but in a more sophisticated way? It adjusts temperature per token based on defined heuristics in the algorithm.

Is Temperature the Creativity Parameter of Large Language Models?  See: https://arxiv.org/html/2405.00492v1

##### Top P, Temperature and Other Parameters (article)
Dixn Jakindah / May 17, 2023
https://medium.com/@dixnjakindah/top-p-temperature-and-other-parameters-1a53d2f8d7d7

#### Model i#nference (hopsworks.ai/dictionary)
https://www.hopsworks.ai/dictionary/model-inference
Model inference requires a: 
ML model || inference data || an inference pipeline || prediction consumer. 
‍Batch Model Inference -> ...
‍Online Model Inference -> request-response network services, exposed as a REST or gRPC endpoint (authentication & access control )

###### Типы инференса ML моделей (article)
https://ml-system-design.ru/blog/inference/типы-инференса-ml-моделей 

###### inference pipeline
https://www.hopsworks.ai/dictionary/inference-pipeline




