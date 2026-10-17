# Claude Code

Claude Code és Claude treballant directament al teu ordinador, dins d'una carpeta de codi. Llegeix els teus fitxers, els edita, executa ordres i tests, i fa servir git. Està inclòs a Pro i comparteix els mateixos límits d'ús que el xat.

Fes-lo servir en lloc del xat quan la tasca tracti del **teu propi codi**: un pipeline, un repositori d'anàlisi, una simulació, un article en LaTeX.

!!! tip "Per a la majoria d'investigadors: l'aplicació d'escriptori"
    La manera més fàcil de fer servir Claude Code és la pestanya **Code** de l'aplicació d'escriptori de Claude. Sense terminal i sense res més per instal·lar: tries una carpeta, descrius què vols i revises els canvis a la pantalla. La resta d'aquesta pàgina parla de l'aplicació d'escriptori; la [versió de terminal](#terminal-version) és al final.

## On executar-lo

- **Aplicació d'escriptori** (macOS, Windows, Linux beta): la pestanya **Code**. Recomanat. Instruccions més avall.
- **VS Code** i **JetBrains**: instal·la l'extensió Claude Code. Mostra els canvis com a diffs a l'editor. Consulta [Claude a VS Code](vs-code.md).
- **Terminal**: l'ordre `claude`. Útil en un clúster per SSH o si ja treballes al terminal. Consulta la [versió de terminal](#terminal-version).
- **Web** ([claude.ai/code](https://claude.ai/code)): treballa sobre un repositori de GitHub al núvol, no al teu portàtil.

Totes són el mateix assistent, amb el mateix `CLAUDE.md` i la mateixa configuració.

## Instal·la l'aplicació d'escriptori { #install-the-desktop-app }

1. Descarrega Claude per al teu sistema:
    - **macOS** (Intel i Apple Silicon): [descàrrega](https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect)
    - **Windows** (x64): [descàrrega](https://claude.ai/api/desktop/win32/x64/setup/latest/redirect). Per a portàtils ARM: [instal·lador ARM64](https://claude.ai/api/desktop/win32/arm64/setup/latest/redirect)
    - **Linux** (beta, Ubuntu/Debian): consulta [Claude Desktop on Linux](https://code.claude.com/docs/en/desktop-linux)

    Totes les descàrregues també són a [claude.com/download](https://claude.com/download).

2. Instal·la i obre Claude, i inicia la sessió amb el teu compte de **Claude Pro**.
3. Fes clic a la pestanya **Code**, a dalt al centre. (Les altres pestanyes són **Chat**, la conversa normal, i **Cowork**, per a tasques més llargues que s'executen en segon pla.)

L'aplicació ja porta Claude Code a dins: no necessites Node.js ni la versió de terminal.

## La teva primera sessió { #your-first-session }

1. **Tria on s'executa.** Selecciona **Local** per treballar amb fitxers del teu ordinador, fes clic a **Select folder** i tria la carpeta del projecte. Comença amb un projecte petit que coneguis bé.
2. **Tria un model** al desplegable que hi ha al costat del botó d'enviar.
3. **Tria un mode de permisos** al selector que hi ha al costat del botó d'enviar. Mentre n'aprens, tria **Manual**: Claude pregunta abans d'editar un fitxer o d'executar una ordre.
4. **Descriu la tasca** al quadre de text, com ho faries al xat. Consulta [Bones primeres tasques](#good-first-tasks).
5. **Revisa els canvis.** En mode **Manual**, cada canvi apareix com un diff amb els botons **Accept** i **Reject**. En els altres modes, Claude aplica les edicions i apareix un indicador com `+12 -1`: fes-hi clic per veure tots els canvis fitxer per fitxer. Pots comentar una línia concreta i Claude la revisarà.

No cal que esperis que Claude acabi: fes clic al botó d'aturar per interrompre'l, o escriu una correcció i prem **Enter** per redirigir-lo mentre treballa.

### Modes de permisos { #permission-modes }

| Mode | Què fa Claude |
|---|---|
| **Manual** | Pregunta abans d'editar fitxers o d'executar ordres. El millor per començar. |
| **Accept edits** | Edita fitxers sense preguntar, però encara pregunta abans d'executar ordres. |
| **Plan** | Només proposa un pla, no canvia res. Útil abans d'un canvi gran. |
| **Auto** | Treballa sense preguntar; les accions arriscades es bloquegen automàticament. |

### Coses útils a la pestanya Code { #useful-things-in-the-code-tab }

- **Afegeix context**: escriu `@` i el nom d'un fitxer per assenyalar-lo a Claude, o arrossega-hi PDF, imatges i gràfics.
- **Terminal**: prem `` Ctrl+` `` per obrir un terminal a la carpeta del projecte i executar-hi coses tu mateix.
- **Diverses tasques alhora**: **+ New session** a la barra lateral. Cada sessió té la seva pròpia conversa i carpeta.
- **Pregunta lateral**: prem `Cmd+;` (macOS) o `Ctrl+;` (Windows) per preguntar alguna cosa sense destorbar la tasca principal.
- **Ordres i skills**: escriu `/` al quadre de text, per exemple `/init` (consulta [més avall](#make-it-know-your-project)) o `/code-review`.
- **Màquines remotes**: en lloc de **Local**, tria **SSH** per treballar en un servidor o clúster on tinguis compte, o **Cloud** per executar una tasca llarga que continua encara que tanquis l'aplicació.
- **Git**: no cal per a una sessió senzilla, però és molt recomanable (consulta [Mantén el control](#stay-in-control)). Algunes funcions, com executar cada sessió en el seu propi worktree, el necessiten. A Windows, instal·la [Git for Windows](https://git-scm.com/downloads/win).

Referència completa: [documentació de Claude Code a l'escriptori](https://code.claude.com/docs/en/desktop) i la [guia ràpida d'escriptori](https://code.claude.com/docs/en/desktop-quickstart).

## Bones primeres tasques { #good-first-tasks }

Comença deixant que llegeixi abans que escrigui:

- *"Què fa aquest projecte? Explica'm l'estructura de carpetes."*
- *"On es calcula la distorsió en l'espai de redshift, i quines són les seves entrades?"*

Després, canvis petits i fàcils de comprovar:

- *"Escriu tests per a `cosmology.py` i després executa'ls."*
- *"Aquest script falla amb l'error adjunt. Troba'n la causa i arregla-la."*
- *"Converteix aquesta rutina de Fortran 77 a Python amb numpy, i comprova que totes dues donen la mateixa sortida amb el fitxer de prova."*
- *"Arregla els avisos de LaTeX de `paper.tex` i fes que l'estil de les referències sigui coherent."*
- *"Revisa els meus canvis sense commit i assenyala'n els errors."*

## Mantén el control { #stay-in-control }

- **Fes servir git.** Fes un commit abans de demanar canvis grans, perquè sempre puguis tornar enrere. Revisa el diff (o demana a Claude *"mostra'm què has canviat"*) abans de fer el commit.
- **Permisos.** Segons el mode de permisos, Claude Code pot executar ordres i editar fitxers sense preguntar cada vegada. Comença en **Manual** i canvia només quan confiïs en la tasca.
- **No l'executis en carpetes amb secrets o amb dades que no pots compartir** (consulta [Dades i privadesa](../getting-started/data-and-privacy.md)). Llegeix el que necessita de la carpeta que obres.
- **Comprova els resultats**: executa els tests i mira els gràfics. Claude Code es pot equivocar amb tota la seguretat del món en detalls científics.

## Fes que conegui el teu projecte { #make-it-know-your-project }

Crea un fitxer anomenat `CLAUDE.md` a l'arrel del teu repositori. Claude Code el llegeix al començament de cada sessió. Posa-hi el que hauria de saber un estudiant nou:

```markdown
# Notes del projecte per a Claude
- Python 3.11, numpy/scipy/astropy. Executa els tests amb `pytest tests/`.
- Unitats: distàncies en Mpc/h, masses en Msun/h.
- No modifiquis mai els fitxers de `data/raw/`.
- El punt d'entrada principal del pipeline és `run_pipeline.py`.
```

Escriu `/init` a Claude Code perquè te'n prepari un esborrany.

## Versió de terminal { #terminal-version }

El mateix Claude Code també funciona com l'ordre `claude` en un terminal. És pràctic en un clúster per SSH, o si prefereixes la línia d'ordres.

macOS, Linux o WSL:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Windows PowerShell:

```powershell
irm https://claude.ai/install.ps1 | iex
```

O amb Homebrew: `brew install --cask claude-code`. Comprova que ha funcionat amb `claude --version`.

Després ves a la carpeta d'un projecte i inicia'l:

```bash
cd ~/work/my-analysis
claude
```

La primera vegada, obre el navegador perquè iniciïs la sessió. Tria el teu compte de **Claude Pro**. Prem `Shift+Tab` per canviar de mode de permisos.

| Ordre | Què fa |
|---|---|
| `claude` | Inicia una sessió a la carpeta actual |
| `claude -c` | Continua l'última sessió d'aquesta carpeta |
| `/clear` | Comença una conversa nova (fes-la servir quan canviïs de tasca) |
| `/help` | Mostra la llista d'ordres |
| `Esc` | Interromp Claude |

Instruccions completes: [Claude Code quickstart](https://code.claude.com/docs/en/quickstart).

Per aprendre'n més, el curs gratuït [Claude Code 101](https://academy.claude.com/courses/claude-code-101) és un bon pas següent.
