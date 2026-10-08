---
tags:
  - Recerca
  - Models locals
  - Programació
---

# Compartir un LLM local a través de la xarxa

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | 2026-09-26 |
| **Eines utilitzades** | Ollama, LM Studio, VS Code amb l'extensió Continue |
| **Configuració** | Un MacBook Pro més nou com a servidor, un MacBook Pro més antic com a client, a la mateixa xarxa local |

## Objectiu

Comprovar que els models locals que s'executen en un Mac (el servidor) es poden fer servir des d'un segon Mac (el client) a la mateixa xarxa, tant com a model de xat com a agent de programació a VS Code. És una prova de concepte per a una estació de treball compartida que doni servei a diversos investigadors, sense costos d'API al núvol i sense que cap dada surti de la xarxa local.

Models al servidor: `qwen3-coder:30b`, `qwen2.5-coder:7b`, `gemma4:e4b`, `gemma4:e2b`, `gemma4:12b-mlx`.

## Què vaig fer

### 1. Servidor: exposar Ollama i LM Studio a la xarxa

Troba l'adreça IP del servidor:

```bash
ipconfig getifaddr en0
```

Per defecte, Ollama només escolta a `localhost`. Fes que escolti a la xarxa:

```bash
launchctl setenv OLLAMA_HOST "0.0.0.0:11434"
```

Tanca Ollama del tot i torna'l a obrir, i després comprova que mostra la llista dels teus models:

```bash
curl http://localhost:11434/api/tags
```

Per a LM Studio: pestanya Developer (Server), carrega un model, inicia el servidor i configura'l perquè serveixi a la xarxa local en lloc de `127.0.0.1`. El port per defecte és `1234`.

### 2. Servidor: tallafoc

A System Settings, Network, Firewall: si el tallafoc està activat, accepta els avisos de connexió entrant per a Ollama i LM Studio el primer cop que s'hi connecti un client, o afegeix-los a Firewall Options.

### 3. Client: comprova la connexió i xateja des del terminal

Substitueix `<server-ip>` per l'adreça del servidor:

```bash
ping <server-ip>
curl http://<server-ip>:11434/api/tags
curl http://<server-ip>:1234/v1/models
```

Xateja amb un model que s'executa al servidor (el client necessita tenir Ollama instal·lat, però cap model):

```bash
OLLAMA_HOST=http://<server-ip>:11434 ollama run qwen3-coder:30b
```

Aquesta va ser la primera prova que l'accés remot funciona.

### 4. Client: VS Code amb l'extensió Continue

1. Instal·la **Continue** (l'agent de codi amb IA de codi obert) a VS Code.
2. Instal·la també l'extensió **YAML** de Red Hat. Sense aquesta extensió, Continue no aconsegueix llegir la seva configuració i no avisa de l'error.
3. Fes una còpia de seguretat de qualsevol `~/.continue/config.yaml` existent i després escriu:

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

4. Executa ++cmd+shift+p++ i després **Developer: Reload Window**.
5. Obre el panell de Continue, tria un model i envia un missatge de prova.

### 5. Proves

Des d'una carpeta buida, en el mode Agent de Continue:

1. **Comprovació de la connexió**: *"Quin model ets i quant fa 17 × 24?"*
2. **Ús d'eines**: *"Crea en aquesta carpeta un fitxer anomenat hello.py que imprimeixi 'Hello from the remote model' i després executa'l."*
3. **Edició en diversos passos**: *"Afegeix a hello.py una funció que calculi la successió de Fibonacci fins a n=10 i torna'l a executar."*

## Resultat

Funciona de punta a punta: tant el xat al terminal com el mode Agent de VS Code van funcionar amb el model remot, i el mateix model va crear i executar `hello.py`. Clarament més lent que executar-lo en local, sobretot amb el model de 30B, però correcte.

## Què cal vigilar

- **El mode Agent mostra les crides a eines en lloc d'executar-les**: és un error conegut de Continue amb `provider: ollama` als modes Agent i Plan (el xat normal funciona bé). Canvia aquest model a `provider: openai`, amb `apiBase: http://<server-ip>:11434/v1` i una `apiKey: "ollama"` de marcador de posició.
- **La configuració s'ignora sense avisar**: instal·la l'extensió YAML de Red Hat.
- **Velocitat**: el model de 30B és lent a través de la xarxa. Fes servir el model de 7B quan importi la rapidesa de resposta.
- **Canvis d'adreça IP**: assigna al servidor una IP fixa o un nom d'amfitrió `.local` abans que diverses persones en depenguin, o totes les configuracions dels clients deixaran de funcionar quan canviï l'adreça.

## Consells per a una demostració

Mostra primer el xat al terminal (el més senzill) i després la prova de creació de fitxers a VS Code, que és el moment més convincent d'"agent de programació de veritat". Tria el model de 7B si la demostració ha de semblar ràpida, o explica el compromís: privadesa i cost zero a canvi de velocitat.
