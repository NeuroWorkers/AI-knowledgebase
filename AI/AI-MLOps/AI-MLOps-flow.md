---
up:
  - [[Flows]]
  - [[AI-MLOps]] 
---

up: [[AI-MLOps]]

-------------------------------
#### Model server (LLM Model server)
LLM model server
(LLM server?)
model running ( model runner?)

#### Using cpu memory as additional memory for GPU
https://discuss.pytorch.org/t/using-cpu-memory-as-additional-memory-for-gpu/100862
Is there a way in pytorch to borrow memory from the CPU when training on GPU. I am training a model related to video processing and would like to increase the batch size

https://discuss.pytorch.org/t/using-cpu-memory-as-additional-memory-for-gpu/100862/3
I also tried searching again with different keywords and found this repository [https://github.com/IBM/pytorch-large-model-support 411](https://github.com/IBM/pytorch-large-model-support) It enables memory swapping between CPU memory and GPU (similar to memory swap between CPU RAM and storage memory). I will leave the link here maybe it can help someone later on.


#### Model RAM usage
from claude: 8b -> 16-32G RAM
For a model with 8 billion parameters: Approximate RAM required: 16-32 GB ; 
This estimate assumes: 2-4 bytes per parameter (depending on precision) ; Some overhead for model operation. Actual usage may vary based on specific model architecture, framework, and optimizations used.

from claude: 8B --> 4-8 GB RAM
With quantization and memory optimization techniques applied to an 8B parameter model: Approximate RAM required: 4-8 GB
This estimate assumes:
4-bit or 8-bit quantization (0.5-1 byte per parameter)
Efficient memory management techniques
Some overhead for operation


#### The easiest AI local installation...
from: https://askubuntu.com/questions/1461564/install-llama-cpp-locally

see [[AI-MLOps#Oogabooga (Text generation web UI)]]

more: 
OobaBooga -  failed for my laptop ....
Dalai lama  - ....

#### ChatGPT Prompt Assistant and Website Chatbot

https://github.com/muratali016/ChatGPT-Prompt-Assistant-and-Website-Chatbot



#### What software engine used to run StableDuffusion

Stable Diffusion is a generative model that can be run on a variety of software engines, including:

- **PyTorch:** PyTorch is an open-source machine learning framework that is used for deep learning. It is a popular choice for running Stable Diffusion because it is easy to use and has a large community of users and developers.
- **TensorFlow:** TensorFlow is another open-source machine learning framework that is used for deep learning. It is similar to PyTorch in terms of its capabilities, but it has a different programming style.
- **JAX:** JAX is a high-performance numerical computation library that is built on top of Python. It is a good choice for running Stable Diffusion if you need to generate images quickly or if you need to use a lot of data.
- **Chainer:** Chainer is a deep learning framework that is written in Python. It is similar to PyTorch in terms of its capabilities, but it has a different programming style.

The best software engine for running Stable Diffusion will depend on your specific needs and preferences. If you are new to deep learning, I recommend starting with PyTorch. It is easy to learn and has a large community of users and developers.

Here are some links to learn more about the software engines that can be used to run Stable Diffusion:

- **PyTorch:** https://pytorch.org/
- **TensorFlow:** https://www.tensorflow.org/
- **JAX:** https://jax.readthedocs.io/en/latest/
- **Chainer:** https://chainer.org/

-------------------------------

#### Does some software engine used to run AI(neural networks) have MPI support
(from bard/geminy)

Yes, there are a number of software engines used to run AI (neural networks) that have MPI support. Some of the most popular ones include:

- **TensorFlow:** TensorFlow has MPI support through the `tensorflow.distribute.experimental.collective_all_reduce` API. This API allows you to distribute your neural network training across multiple machines using MPI.


-------------------------------
#### (bad) install your own ChatGPT bot on hosting, FROM chatgpt

To install your own ChatGPT bot on hosting, you'll need to follow these general steps:
1. Set up a hosting environment: Choose a hosting provider that supports running applications or servers. Common options include AWS, Google Cloud, or a VPS provider like DigitalOcean.
2. Set up the server: Once you have the hosting environment, you'll need to set up a server. This can be a virtual machine (VM) or a container. Install the necessary dependencies, such as Python and any frameworks or libraries required by ChatGPT.
3. Clone the ChatGPT repository: Clone the ChatGPT repository from the OpenAI GitHub page (https://github.com/openai/chatgpt) to your server.
4. Set up the environment: Create a virtual environment for ChatGPT and install the required dependencies using the provided requirements.txt file.
5. Obtain API credentials: To access the ChatGPT API, you'll need to obtain API credentials from OpenAI. Follow the instructions provided by OpenAI to get your API key.
6. Configure the bot: Set up the necessary configuration files for your bot, including specifying the API credentials obtained in the previous step.
7. Run the bot: Launch the bot by running the appropriate command or script specified in the ChatGPT repository. This will start the bot and make it accessible via the specified host and port.
8. Test and deploy: Test your bot by interacting with it through a chat interface or API. Once you're satisfied with its functionality, you can deploy it to a production environment and make it accessible to users.
Please note that these are general steps, and the specific details may vary depending on your hosting provider, server setup, and the implementation of your bot. It's recommended to refer to the documentation provided by OpenAI and your hosting provider for detailed instructions and best practices. 