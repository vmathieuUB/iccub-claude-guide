---
tags:
  - Recerca
  - Models locals
  - Programació
---

# Executar un LLM local al teu portàtil

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | per confirmar |
| **Eines utilitzades** | Ollama, Gemma 2, Hermes Agent, VS Code amb l'extensió Continue |
| **Per què en local** | Les dades no surten mai de la teva màquina, sense cost per tokens, funciona sense connexió |

## Objectiu

Executar un model de llenguatge de pesos oberts completament en un portàtil personal, fer-lo servir com a assistent de xat al terminal i connectar-lo a VS Code com a assistent de programació, de manera que el codi i les dades sensibles no vagin mai a un servei al núvol.

## Què vaig fer

### 1. Tria un model que càpiga a la teva RAM

Els models de pesos oberts tenen mides que es mesuren en milers de milions de paràmetres (2B, 8B, 27B). Normalment es distribueixen quantitzats a 4 bits (Q4), cosa que redueix molt la memòria necessària amb poca pèrdua de qualitat.

| RAM del portàtil | Models recomanats | Ordre | Útil per a |
| --- | --- | --- | --- |
| 8 GB | Gemma 2 2B, Phi-3 Mini 3.8B | `ollama run gemma2:2b` | Xat ràpid, fragments de codi, redacció sense connexió |
| 16 GB | Gemma 2 9B, Llama 3.1 8B, Qwen 2.5 7B | `ollama run gemma2:9b` | El punt òptim: raonament, ajuda amb el codi, anàlisi |
| 32 GB o més | Gemma 2 27B, Qwen 2.5 14B o 32B | `ollama run gemma2:27b` | Raonament més difícil, refactoritzacions més grans, tasques d'agent |

### 2. Instal·la Ollama

Ollama s'executa en segon pla, descarrega models i els serveix a través d'una API local a `http://localhost:11434`.

- **macOS**: descarrega'l des de [ollama.com/download](https://ollama.com/download), o `brew install ollama`
- **Windows**: descarrega i executa `OllamaSetup.exe` des de [ollama.com/download](https://ollama.com/download)
- **Linux**: `curl -fsSL https://ollama.com/install.sh | sh`

Ordres essencials:

```bash
ollama run gemma2:9b   # download the model if needed and start a chat
ollama list            # models stored on this machine
ollama ps              # model currently loaded in memory
ollama rm gemma2:9b    # delete a model to free disk space
```

### 3. Opcional: un agent de terminal (Hermes Agent)

`ollama run` ofereix un simple xatbot. Un entorn d'agent com Hermes Agent converteix el terminal en un espai de treball on el model pot llegir i executar fitxers i cridar eines.

1. En el primer inici, Hermes et pregunta quin backend d'inferència vols fer servir: tria **Ollama**.
2. Detecta els models que has descarregat (per exemple `gemma2:9b`) a `localhost:11434`.

```bash
hermes agent --model gemma2:9b
```

### 4. VS Code amb l'extensió Continue

1. Obre la pestanya d'extensions (++cmd+shift+x++ o ++ctrl+shift+x++).
2. Instal·la **Continue**.
3. Continue detecta Ollama a `localhost:11434` i mostra la llista dels teus models. Per fixar-ne un explícitament, afegeix a la seva configuració:

```json
{ "models": [ { "title": "Local Gemma 2 (9B)", "provider": "ollama", "model": "gemma2:9b" } ] }
```

Dreceres: ++cmd+l++ / ++ctrl+l++ obre el xat sobre els fitxers que tens oberts; ++cmd+i++ / ++ctrl+i++ edita el codi seleccionat en línia; ++tab++ accepta les compleccions.

## Resultat

Un assistent local que funciona al terminal i a VS Code. Dues proves ràpides que van funcionar:

- Al terminal: `ollama run gemma2:9b`, i després *"Escriu una funció de Python que validi adreces de correu electrònic amb una expressió regular."*
- A VS Code: selecciona un bloc de codi, prem ++cmd+i++ i demana *"Afegeix docstrings i anotacions de tipus, i gestiona el possible ZeroDivisionError."* Revisa el diff i després accepta'l.

## Què cal vigilar

- **Soroll del ventilador o respostes lentes**: executa `ollama ps`. En màquines de 8 o 16 GB, assegura't que només hi ha un model gran carregat. Ollama descarrega de la memòria els models inactius al cap d'uns 5 minuts.
- **Qualitat**: els models locals petits queden molt per darrere de Claude en raonament difícil. Fes-los servir quan la privadesa o l'ús sense connexió siguin importants, no com a substitut directe.

Pas següent: [comparteix els models d'una màquina amb els col·legues a través de la xarxa](local-llm-remote-access.md).
