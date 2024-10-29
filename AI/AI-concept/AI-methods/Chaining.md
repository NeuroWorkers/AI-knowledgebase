---
aliases:
  - Inference chaining, LLM chaining
up:
  - [[AI-concept]]
---
up:  [[AI-concept]]

See: [[AI-concept#Inference (Model Inference)|Inference (Model Inference)]]
### Chaining, Inference chaining, LLM chaining

is commonly referred to as "chaining" or more specifically, "inference chaining" or "LLM chaining." Here are some related terms and concepts:

1. Chain-of-Thought (CoT) Prompting: This involves breaking down a complex task into smaller, sequential steps, each potentially requiring a separate LLM inference.
2. Multi-step Reasoning: Similar to CoT, this involves using multiple LLM calls to solve complex problems that require intermediate steps or reasoning.
3. Recursive LLM Calls: When an LLM's output is used as input for subsequent LLM calls, potentially multiple times.
4. Cascading Inference: A process where the output of one inference step triggers or informs the next, creating a cascade of LLM calls.
5. Iterative Refinement: Using multiple LLM calls to progressively refine an answer or solution.
6. Decomposition and Recomposition: Breaking a complex query into simpler sub-queries, solving each with an LLM call, then combining the results.
7. LangChain: While this is a framework, it's worth mentioning as it's designed specifically for creating these kinds of multi-step LLM processes. The term "LangChain" is sometimes used informally to describe this type of chained LLM usage.

In the context of conversational AI and chatbots, this approach is often used to handle complex queries that require multiple steps of processing or reasoning. It allows the bot to break down a user's request into manageable parts, potentially consult different knowledge sources or perform various types of analysis, and then synthesize the results into a coherent response.
