---
tags:
  - Research
  - Local models
  - Coding
---

# Run a local LLM on your laptop

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | to confirm |
| **Tools used** | Ollama, Gemma 2, Hermes Agent, VS Code with the Continue extension |
| **Why local** | Data never leaves your machine, no token costs, works offline |

## Goal

Run an open-weight language model entirely on a personal laptop, use it as a chat assistant in the terminal, and plug it into VS Code as a coding assistant, so that sensitive code and data never go to a cloud service.

## What I did

### 1. Pick a model that fits your RAM

Open-weight models come in sizes measured in billions of parameters (2B, 8B, 27B). They are usually distributed 4-bit quantized (Q4), which cuts memory needs a lot with little loss in quality.

| Laptop RAM | Recommended models | Command | Good for |
| --- | --- | --- | --- |
| 8 GB | Gemma 2 2B, Phi-3 Mini 3.8B | `ollama run gemma2:2b` | Quick chat, code snippets, offline drafting |
| 16 GB | Gemma 2 9B, Llama 3.1 8B, Qwen 2.5 7B | `ollama run gemma2:9b` | The sweet spot: reasoning, coding help, analysis |
| 32 GB or more | Gemma 2 27B, Qwen 2.5 14B or 32B | `ollama run gemma2:27b` | Harder reasoning, larger refactors, agent tasks |

### 2. Install Ollama

Ollama runs in the background, downloads models and serves them through a local API on `http://localhost:11434`.

- **macOS**: download from [ollama.com/download](https://ollama.com/download), or `brew install ollama`
- **Windows**: download and run `OllamaSetup.exe` from [ollama.com/download](https://ollama.com/download)
- **Linux**: `curl -fsSL https://ollama.com/install.sh | sh`

Essential commands:

```bash
ollama run gemma2:9b   # download the model if needed and start a chat
ollama list            # models stored on this machine
ollama ps              # model currently loaded in memory
ollama rm gemma2:9b    # delete a model to free disk space
```

### 3. Optional: a terminal agent (Hermes Agent)

`ollama run` gives a plain chatbot. An agent harness such as Hermes Agent turns the terminal into a workspace where the model can read and run files and call tools.

1. On first launch, Hermes asks which inference backend to use: choose **Ollama**.
2. It detects the models you have pulled (for example `gemma2:9b`) on `localhost:11434`.

```bash
hermes agent --model gemma2:9b
```

### 4. VS Code with the Continue extension

1. Open the Extensions tab (++cmd+shift+x++ or ++ctrl+shift+x++).
2. Install **Continue**.
3. Continue detects Ollama on `localhost:11434` and lists your models. To set one explicitly, add to its config:

```json
{ "models": [ { "title": "Local Gemma 2 (9B)", "provider": "ollama", "model": "gemma2:9b" } ] }
```

Shortcuts: ++cmd+l++ / ++ctrl+l++ opens the chat about your open files; ++cmd+i++ / ++ctrl+i++ edits selected code inline; ++tab++ accepts completions.

## Result

A working local assistant in the terminal and in VS Code. Two quick tests that worked:

- In the terminal: `ollama run gemma2:9b`, then *"Write a Python function to validate email addresses using regex."*
- In VS Code: select a block of code, press ++cmd+i++, and ask *"Add docstrings, type annotations, and handle potential ZeroDivisionError."* Review the diff, then accept.

## What to watch for

- **Fan noise or slow answers**: run `ollama ps`. On 8 or 16 GB machines, make sure only one large model is loaded. Ollama unloads idle models after about 5 minutes.
- **Quality**: small local models are well behind Claude on hard reasoning. Use them where privacy or offline use matters, not as a drop-in replacement.

Next step: [share one machine's models with colleagues over the network](local-llm-remote-access.md).
