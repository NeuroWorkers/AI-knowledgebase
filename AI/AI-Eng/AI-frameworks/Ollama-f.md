
up: [[MLOps#Ollama]]


https://www.reddit.com/r/LocalLLaMA/comments/1dhyxq8/why_use_ollama/



[TheTerrasque](https://www.reddit.com/user/TheTerrasque/)  •[2024](https://www.reddit.com/r/LocalLLaMA/comments/1dhyxq8/comment/l952o01/)
In my client app I can **just do one rest api call to download model if it doesn't exist**, and one rest api call to run inference. Without having to think about things like for example the model's template. Or having to download the model first if it's not there. Or having llama.cpp already running with that model.
Wanna try a different model? Just change the model in the api calls, no stress.
Also it unloads the model when it's not needed any more. P40 uses a lot less power when a model isn't loaded.
And before you ask, yes I do have different scripts that use different models.



