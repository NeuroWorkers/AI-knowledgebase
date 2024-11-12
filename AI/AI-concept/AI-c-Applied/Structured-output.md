---
aliases:
  - Structured output (AI)
  - Structured outputs
up:
  - 
---
up:  [[AI-concept#Structured Output]]
# Structured output
It is often crucial to have LLMs return structured output. 
How: Prompting ; Function calling ; Tool calling; JSON mode

Prompting: This is when you ask the LLM (very nicely) to return output in the desired format (JSON, XML). This is nice because it works with all LLMs. It is not nice because there is no guarantee that the LLM returns the output in the right format.
Function calling: This is when the LLM is fine-tuned to be able to not just generate a completion, but also generate a function call. The functions the LLM can call are generally passed as extra parameters to the model API. The function names and descriptions should be treated as part of the prompt (they usually count against token counts, and are used by the LLM to decide what to do).
Tool calling: A technique similar to function calling, but it allows the LLM to call multiple functions at the same time.
JSON mode: This is when the LLM is guaranteed to return JSON.

##### Awesome LLM JSON List (@external_resource_list)
https://github.com/imaurer/awesome-llm-json
Resource list for generating JSON using LLMs via function calling, tools, CFG. Libraries, Models, Notebooks, etc.

