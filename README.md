# Chat Prompt Templates

Collection of Basic Prompt Templates for Various Chat LLMs

**Motivation**: The basic prompt template will significantly affect the effectiveness of instruction following. Models of different architectures may use different prompt templates during training. However, at present, these templates can be challenging to locate; sometimes they are embedded in example codes, hidden within GitHub issues, or occasionally found in official blogs...

(Alphabetical order by architecture)

## Baichuan Prompt Template

```python
template = """<reserved_195>{query}<reserved_196>"""
```

* References:
  * https://huggingface.co/baichuan-inc/Baichuan2-13B-Chat/blob/main/generation_config.json
  * https://github.com/baichuan-inc/Baichuan2/issues/227
* Model Site: https://huggingface.co/baichuan-inc

## ChatGLM3 Prompt Template

```python
template = """<|system|>
You are ChatGLM3, a large language model trained by Zhipu.AI. Follow the user's instructions carefully. Respond using markdown.
<|user|>
{query}
<|assistant|>
"""
```

* References:
  * https://github.com/THUDM/ChatGLM3/blob/main/PROMPT_en.md
* Model Site: https://huggingface.co/THUDM/chatglm3-6b
* Note: If no special template is provided, the instruction following still works very well.

## LLaMA2 Prompt Template

```python
template = """<s>[INST] <<SYS>>
You are a helpful, respectful and honest assistant.
<</SYS>> {query} [/INST] Sure, I'd be happy to help. Here is the answer:"""
```

* References:
  * https://huggingface.co/blog/llama2#how-to-prompt-llama-2
  * https://www.reddit.com/r/LocalLLaMA/comments/16x4733/how_to_stop_llama_2_13b_from_starting_each/
* Model Site: https://huggingface.co/meta-llama/Llama-2-13b-chat
* Note: `Sure, I'd be happy to help. Here is the answer:` avoids verbose model outputs.

## Phi-2 Prompt Template

```python
template = """Instruct: {query}\nOutput:"""
# or template = """Alice: {query}\nBob:"""
```

* References:
  * https://huggingface.co/microsoft/phi-2
* Model Site: https://huggingface.co/microsoft/phi-2

## Qwen Prompt Template

```python
template = """<|im_start|>system
You are a helpful assistant.<|im_end|>
<|im_start|>user
{query}<|im_end|>
<|im_start|>assistant
"""
```

* References:
  * https://github.com/QwenLM/Qwen/blob/5aa84bdfd3237b37f01bc88cd49b3279b9a71d0b/examples/vllm_wrapper.py#L32
  * https://github.com/vllm-project/vllm/issues/901
* Model Site: https://huggingface.co/Qwen/Qwen-7B-Chat

## XXX Prompt Template

```python
template = 
```

* References:
* Model Site: 
* Note: 
