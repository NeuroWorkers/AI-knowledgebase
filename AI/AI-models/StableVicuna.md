---
aliases:
  - template1
up:
  -  [[Stability-AI]] 
---
up: [[Stability-AI]]
## StableVicuna
NOTE: Created by [[Stability-AI]]
NOTE: StableVicuna это <font color="#00b0f0">model</font> ( -->  [[AI-basics#Model]] )
NOTE: StableVicuna это <font color="#00b0f0">chat-bot</font>
NOTE: StableVicuna based on <font color="#00b0f0">LLaMA</font> ( --> [[LLaMA]]   ) (see --> [[StableVicuna#^08bf25]])
NOTE: "ПРЕДОК" --> Vicuna ;


------
## Papers / Articles
### Stability AI releases StableVicuna, the AI World’s First Open Source RLHF LLM Chatbot

![[2023-06-12_18-27.webp|400]]  28 Apr 2023

**....**

### Introducing the First Large-Scale Open Source RLHF LLM Chatbot

We are proud to present StableVicuna, the first large-scale open source chatbot trained via reinforced learning from human feedback (RLHF). StableVicuna is a further instruction fine tuned and RLHF trained version of Vicuna v0 13b, which is an instruction fine tuned LLaMA 13b model. For the interested reader, you can find more about Vicuna here. 

-----
### StableVicuna-13B 

![[2023-06-14_01-03.webp]]

https://huggingface.co/CarperAI/stable-vicuna-13b-delta
StableVicuna-13B is a Vicuna-13B v0 model fine-tuned using reinforcement learning from human feedback (RLHF) via Proximal Policy Optimization (PPO) on various conversational and instructional datasets.

**Apply Delta Weights**
StableVicuna-13B cannot be used from the CarperAI/stable-vicuna-13b-delta weights alone. To obtain the correct model, one <font color="#00b0f0">must add back the difference between LLaMA 13B</font> and CarperAI/stable-vicuna-13b-delta weights. 

## Model Details
- **Trained by**: [Duy Phung](https://github.com/PhungVanDuy) of [CarperAI](https://carper.ai/)
- **Model type:** **StableVicuna-13B** is an auto-regressive language model based on the LLaMA transformer architecture.   ^08bf25
- **Language(s)**: English
- **Library**: [trlX](https://github.com/CarperAI/trlx)
- **License for delta weights**: [CC-BY-NC-SA-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
    - _Note_: License for the base LLaMA model's weights is Meta's [non-commercial bespoke license](https://github.com/facebookresearch/llama/blob/main/MODEL_CARD.md).

------

