---
aliases:
  - "How an LLM Understands Input: The Math Under the Hood (article)"
up:
  - [[AI-articles]]
---
up:  [[AI-articles]]
URL: https://medium.com/@amallya0523/how-an-llm-understands-input-the-math-under-the-hood-114ac69f96c6
# How an LLM Understands Input: The Math Under the Hood
Ajay Mallya  Mar 30, 2024
## A brief preface…
I started drafting technical blogs to develop my understanding of computer science and other topics (think Feynman technique), and I noticed that there isn’t an abundance of intuitive articles about the applied mathematics behind complex topics such as LLMs. Personally, I love reading about the inner workings of any technology that I regularly interact with. With respect to LLMs and AI, I hope to understand their internal structure at a significantly granular level so I can use them without feeling a creeping sense of complacency. Anyone interested in AI and LLMs (Large Language Models) knows of the ground-breaking paper, [“Attention is All You Need](https://arxiv.org/abs/1706.03762).” In case you are unfamiliar, the transformer model dictated in this white paper is what has propelled the LLM world forward (feed-forward? haha). Anyway, I have gone through “Attention is All You Need,” and I hope this blog offers an intuitive mathematical exploration and treatment of the transformer model for anyone new to the field. As for some of the linear algebra involved, it’s almost all just multiplication and addition in rows and columns; a quick web search will tell you how to do things like [matrix multiplication](https://www.mathsisfun.com/algebra/matrix-multiplying.html).

> Remark: Although this bugs me as a applied mathematics major, I’ve decided to sacrifice some accuracy here and there for the sake of making this more understandable for more people.

## Analogy
When a baby learns to speak, they absorb vocabulary, syntax, and how different words or concepts are related to one another from surrounding people. An LLM is a baby learning to speak. The more content this baby is exposed to, the more it learns and understands. However, if I ask this baby what my social security number is, fortunately it won’t know the answer. This LLM baby only understands basic syntax and whatever information it hears from its parents (whoever trains the LLM).

The transformer architecture allows LLMs to learn vocabulary, syntax, relationships between words, etc. to provide human-like responses to your questions. For example, and this is probably at the expense of some accuracy, if we trained an LLM on everything related to Game of Thrones, it would excel at answering questions about the show but not much else.

Thus, the transformer helps the LLM learn everything first (training), and it can subsequently deal with user input and generate the most probable outputs (inference). To make this more user-friendly, I’ll focus on inferencing, from user input to LLM output. I hope to write another article about training to explain a few ambiguities that come up here. I will also also add a section about the decoder but first publish this with just the encoder portion.

## Roadmap
Now that we have sufficient high level context regarding this blog’s intentions, here’s a succinct roadmap:

1. Transformer Model: Bird’s-Eye View
2. Encoder: Under the Hood
3. Feed Forward Neural Networks (FFNN), etc.
4. Concluding Thoughts

## Transformers Model: Bird’s-Eye View
![[1_jvCf_KxQbegKuiG_r0gcnA.webp]]
Birds-eye view of the transformer model’s process

## **Encoder: Under the Hood**
**Guiding Question:** **How does the encoder understand and translate the user’s input into something the decoder can use to generate a response?**

When we converse with each other, we understand grammar, syntax, and vocabulary. Similarly, the encoder determines these relationships between words and sends them to the decoder.

**STEP 1 : POSITIONAL ENCODING**
The encoder cares about word order. From here on out, let’s use the following sentence as an example of an input into our transformer model: **“What color is the sky?”**

Each word of a sentence is called a **token**, and each token is represented by a **vector embedding, E,** a numerical representation of the word**.** To those of you not familiar with linear algebra, no worries! Think of a vector as a column of numbers; in the figure below, I chose random numbers to illustrate. Here’s a useful analogy: a token is to a grocery item, as a vector is to the item’s serial number.

The **dimension, d,** of a vector simply represents its length, and all vectors in this scenario will have the same length. The subscript **i** simply refers to where the value stands in the input sequence.

![[1_vA-P1JShT-lr-DOg7_6Uiw.webp]]

**d** is defined at the onset and is chosen for the model. For example, this value could be **d = 512.** The value **i** represents the token’s position in the sentence. The word “color” in our original sentence is at position **i=2.** The k value is intriguing because **it _ranges_ from 1 to d**; if d = 512, then k ranges from 1 to 512. Before you proceed, make sure you understand what values **i, d,** and **k** can take on. The next figure has an example of the range of k values.

Now, to indicate the positioning of each word (which we will call “tokens” from now on) with a vector representation of each word that _includes positional information_, the encoder adds a **positional encoding** value, **PE**, to each token’s vector. The PE value for each token is determined by a function that I exclude here. All you need to know is that we use the **i, d,** and **k** values to calculate this PE value. **d** is constant, **i** changes depending on the token we’re currently looking at, and for every word, we iterate through all **k** **= 1 to d**. After every iteration, we produce a value that is added into our PE vector until we have reached d = 512. Once we get the PE vector embedding for “color,” we move to i=3 (the next token), and repeat the same process for k=1 to 512 to find this next token’s associated PE. We do this for all of the words/tokens in the input sequence (see below visual)

Adding E and PE _for each token_ yields an **X**ₚ**ₒ**ₛ vector that neatly incorporates the positional information about each word in the input sentence (see below visual). Once I write a blog about training, I hope to write _another_ blog about the deeper mathematical intuition behind this.

![[1_XZIys2Y6jukK1eAEAwRHLA.webp]]

**STEP 2 : MULTI-HEAD ATTENTION**
When you hear sentences, you first quickly understand the positioning of words, and then instantaneously focus on the sentence as a whole to understand it. Similarly, the transformer model uses **Multi-Head Attention** to focus on multiple parts of the input sequence simultaneously (in parallel). The transformer model uses multiple heads, and each head focuses on a different aspect of the sentence, like how you might note a friend’s grammar, diction, and tone.

Previously, we came up with a neat **X**ₚ**ₒ**ₛ vector embedding for each token in the input sequence. _Each head_ uses three sets of learned parameters (**weight matrices, Wq, Wₖ, Wᵥ**) to transform the input sequence into three different sets of vectors. We will keep things simple and focus on one of the heads.

> _Remark: There is currently no way to format Wq’s “q” as a subscript; my apologies._

To get the three different sets of vectors, Q, K, and V, we multiply each **X**ₚ**ₒ**ₛ by Wq, Wₖ, and W**ᵥ**. This is matrix-vector multiplication, so Q, K, and V are vectors with the same dimensions as **X**ₚ**ₒ**ₛ.
![](https://miro.medium.com/v2/resize:fit:1094/1*ov6Bk4a43OOzr7h_OirgGw.png)

![[1_ov6Bk4a43OOzr7h_OirgGw.webp]]

- **Q vectors** represent **queries** that define what to look for in the input sequence.
- **K vectors** represent **keys** that define the relationship between each query and every token in the input sequence.
- **V vectors** represent values that provide information about each token’s content.

Here’s a useful analogy: Imagine you are going to a library to get a book about medieval history. You go to the librarian and ask them a question (Q), they look around for the most similar book (K) to your question, and then bring it back to you. You use the information inside the book (V) to learn its contents.

For the head to develop an understanding of tokens’ relative importance to each other, it calculates **attention scores** for each token. Once again, let’s use the “color” token of the input sequence. As we saw above, the “color” token has **one Xₚₒₛ**, **one Q, one K, and one V** **vector** (again, the other tokens in the sequence also have these four vectors). For a head to determine which of the other tokens is most relevant to the “color” token, it compares our current token’s Q vector with every other token’s K vector (using a dot product). It then applies a scaling factor (the square root of our **d** value) to all of these Q•K values.

So now each token from our sentence has four scaled attention scores. The penultimate step here is to apply a **softmax function** to each token’s attention scores to get **attention weights** _for each token_**.** The softmax function ensures that the token’s attention weights add up to one and represents a normalized distribution of each other token’s relative importance to our current token. Here is a rough example. After applying the softmax function to the “color” token’s attention scores, we can interpret the attention weights as follows: let’s say “sky” is somehow 50% similar to “color,” and the other tokens collectively make up the remaining 50%. Thus, “sky” is the most similar to “color,” at least from our point of view from the “color” token. Again, this is a very rough example for high level conceptualization. We then move on to the next token and do the same thing to gain similar insight.

Finally, for each token, we multiply the attention weights by the corresponding V vectors and sum all of them up to get one **Attention-Weighted Sum** for each token (below).


![[1_cnriu7dHEqqCfzouSdjv_g.webp]]
Big Idea: The attention-weighted sums capture the model’s attention towards different parts of the input sequence. Remember that this is just for _one head_ that focuses on a certain aspect of the input sequence. Quite remarkable, right?

> Remark: For those familiar with matrices, consider a matrix Q that contains all Q vectors and a matrix K that contains all K vectors. We can take the dot product of Q and K^T (K transpose), apply the scaling to all the values, and finally use the softmax function to create an **attention weight matrix.** We finally sum the attention weights times V as described above to get each token’s attention-weighted sum.

**STEP 3 : FEED FORWARD NEURAL NETWORK (FFNN), etc.**

I won’t go into technical detail about FFNNs here because I want to get to the decoder, but here is the general gist. The attention score is the output of the encoder, and this serves as input for the FFNN, which exists to learn more granular patterns and dependencies (both local and global) about the input sequence. The output of the FFNN and other processing is a set of more refined representations of the tokens from the input sequence. I’ll probably link another blog about this stage between the encoder and the decoder. After this step, the output is sent directly to the decoder to generate a relevant output to return to the user.

## Concluding Thoughts
Let’s quickly sum up the entire encoder process that powers LLMs to understand input and ultimately generate output.

- **Positional Encoding** creates positional information about tokens’ positioning in the input sequence.
- **Multi-Head Attention** captures detailed information about the relationships between tokens. It does this in multiple ways at once (multiple heads) from multiple angles to learn as much about the relationships as possible.
- **FFNN, etc.** refines the representation of the input before passing it to the decoder, which then assists in producing our output. As mentioned above, I’ll write an additional article describing the decoder and link it here.

I hope this article provides an intuitive mathematical foundation regarding the LLMs and transformer model that most of us now use regularly. It’s amazing that this is only half of the process used in the transformer model, and our example sentence/input sequence is only five tokens/words.

How many words did you include in your last ChatGPT prompt? Now consider the above process with respect to your large prompt and the lightning fast speed at which ChatGPT responds. Absolutely amazing.
