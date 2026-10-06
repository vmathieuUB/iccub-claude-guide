---
tags:
  - Research
  - Local models
  - Coding
---

# Share a local LLM over the network

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | 2026-09-26 |
| **Tools used** | Ollama, LM Studio, VS Code with the Continue extension |
| **Setup** | A newer MacBook Pro as server, an older MacBook Pro as client, same local network |

## Goal

Check that local models running on one Mac (the server) can be used from a second Mac (the client) on the same network, both as a chat model and as a coding agent in VS Code. This is a proof of concept for one shared workstation serving several researchers, with no cloud API costs and no data leaving the local network.

Models on the server: `qwen3-coder:30b`, `qwen2.5-coder:7b`, `gemma4:e4b`, `gemma4:e2b`, `gemma4:12b-mlx`.

## What I did

### 1. Server: expose Ollama and LM Studio on the network

Find the server's IP address:

```bash
ipconfig getifaddr en0
```

Ollama only listens on `localhost` by default. Make it listen on the network:

```bash
launchctl setenv OLLAMA_HOST "0.0.0.0:11434"
```

Quit Ollama completely and start it again, then check that it lists your models:

```bash
curl http://localhost:11434/api/tags
```

For LM Studio: Developer (Server) tab, load a model, start the server, and set it to serve on the local network rather than `127.0.0.1`. The default port is `1234`.

### 2. Server: firewall

In System Settings, Network, Firewall: if the firewall is on, accept the incoming-connection prompts for Ollama and LM Studio the first time a client connects, or add them under Firewall Options.

### 3. Client: check the connection and chat from the terminal

Replace `<server-ip>` with the server's address:

```bash
ping <server-ip>
curl http://<server-ip>:11434/api/tags
curl http://<server-ip>:1234/v1/models
```

Chat with a model running on the server (the client needs Ollama installed but no models):

```bash
OLLAMA_HOST=http://<server-ip>:11434 ollama run qwen3-coder:30b
```

This was the first proof that remote access works.

### 4. Client: VS Code with the Continue extension

1. Install **Continue** (the open-source AI code agent) in VS Code.
2. Also install the **YAML** extension by Red Hat. Without it, Continue silently fails to read its config.
3. Back up any existing `~/.continue/config.yaml`, then write:

```yaml
name: Remote LAN Models
version: 1.0.0
schema: v1

models:
  - name: "Qwen3 Coder 30B (remote)"
    provider: ollama
    model: qwen3-coder:30b
    apiBase: http://<server-ip>:11434
    roles: [chat, edit, apply]
    capabilities: [tool_use]
    defaultCompletionOptions:
      contextLength: 32768

  - name: "Qwen2.5 Coder 7B (remote, faster)"
    provider: ollama
    model: qwen2.5-coder:7b
    apiBase: http://<server-ip>:11434
    roles: [chat, edit, apply]
    capabilities: [tool_use]

  - name: "Gemma4 e4b (remote, general)"
    provider: ollama
    model: gemma4:e4b
    apiBase: http://<server-ip>:11434
    roles: [chat]
```

4. Run ++cmd+shift+p++, then **Developer: Reload Window**.
5. Open the Continue panel, pick a model, and send a test message.

### 5. Tests

From an empty folder, in Continue's Agent mode:

1. **Connection check**: *"What model are you and what's 17 × 24?"*
2. **Tool use**: *"Create a file called hello.py in this folder that prints 'Hello from the remote model' and then run it."*
3. **Multi-step edit**: *"Add a function to hello.py that computes the Fibonacci sequence up to n=10, then run it again."*

## Result

Working end to end: terminal chat and VS Code Agent mode both ran against the remote model, and `hello.py` was created and run by it. Noticeably slower than running locally, especially with the 30B model, but correct.

## What to watch for

- **Agent mode prints tool calls instead of running them**: a known Continue bug with `provider: ollama` in Agent and Plan modes (plain chat is fine). Switch that model to `provider: openai`, with `apiBase: http://<server-ip>:11434/v1` and a placeholder `apiKey: "ollama"`.
- **Config silently ignored**: install the Red Hat YAML extension.
- **Speed**: the 30B model is slow over the network. Use the 7B model when responsiveness matters.
- **IP address changes**: give the server a fixed IP or a `.local` hostname before several people depend on it, or every client config breaks when the address changes.

## Demo tips

Show the terminal chat first (simplest), then the VS Code file-creation test, which is the more convincing "real coding agent" moment. Pick the 7B model if the demo needs to feel fast, or explain the trade-off: privacy and no cost against speed.
