# Local Small Language Agent

Language model-based agents promise the ability to introduce flexibility
and adaptability in order to answer requests from users expressed in
natural language.

Language model-based agents can answer by solely recalling
information that was in their training data, or identify (software) tools
as intermediate steps to answer a request. Since agents are programs,
their ability to generate code combined makes them metaprograms:
they can generate code. However, that added
flexibility and adaptability compared to traditional software
means that predictability or safety will likely require particular
attention.

At the time of writing, creating agentic systems using language models
relies on empiricism and experimentation. Building an intuition about
how they work is arguably important to let teams better understand
what can be achieved with them, and anticipate what is going to be easy and
what is going to be hard to implement. To achieve this,
it should be easy for anyone to build experimental agents. 

The good news is that many language models are available with open weights,
do not have to be large, and do not rely on calling external services.

This tutorial will walk a user through
building a small local agentic solution that can query a database when needed,
chaining steps or calls when required to obtain the final answer.
Several language models can be compared, no GPU is needed, and all
code can run from a Jupyter notebook.

## Prerequisites

- Python (likely >= 3.10)
- `podman` (or own install of `ollama`)
- internet connection to fetch language models using `ollama`
- Python packages such as `langchain`, `langchain_ollama`, and `ollama`

## Quick start


```bash
python3 -m venv small-language-agent_env
source small-language-agent_env/bin/activate
python3 -m pip install uv
uv pip install langchain langchain_ollama ollama jupyterlab
```
