# Claude Code

Claude Code és Claude treballant directament al teu ordinador, dins d'una carpeta de codi. Llegeix els teus fitxers, els edita, executa ordres i tests, i fa servir git. Està inclòs a Pro i comparteix els mateixos límits d'ús que el xat.

Fes-lo servir en lloc del xat quan la tasca tracti del **teu propi codi**: un pipeline, un repositori d'anàlisi, una simulació, un article en LaTeX.

## On executar-lo

- **Terminal** (macOS, Linux, Windows): la versió completa. Instruccions més avall.
- **VS Code** i **JetBrains**: instal·la l'extensió Claude Code. Mostra els canvis com a diffs a l'editor. Consulta [Claude a VS Code](vs-code.md).
- **Aplicació d'escriptori** i **web** ([claude.ai/code](https://claude.ai/code)): no cal instal·lar res. La versió web treballa sobre un repositori de GitHub al núvol, no al teu portàtil.

## Instal·lació (terminal)

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

La primera vegada, obre el navegador perquè iniciïs la sessió. Tria el teu compte de **Claude Pro**.

Instruccions completes i actualitzades: [Claude Code quickstart](https://code.claude.com/docs/en/quickstart).

## Bones primeres tasques

Comença deixant que llegeixi abans que escrigui:

- *"Què fa aquest projecte? Explica'm l'estructura de carpetes."*
- *"On es calcula la distorsió en l'espai de redshift, i quines són les seves entrades?"*

Després, canvis petits i fàcils de comprovar:

- *"Escriu tests per a `cosmology.py` i després executa'ls."*
- *"Aquest script falla amb l'error adjunt. Troba'n la causa i arregla-la."*
- *"Converteix aquesta rutina de Fortran 77 a Python amb numpy, i comprova que totes dues donen la mateixa sortida amb el fitxer de prova."*
- *"Arregla els avisos de LaTeX de `paper.tex` i fes que l'estil de les referències sigui coherent."*
- *"Revisa els meus canvis sense commit i assenyala'n els errors."*

## Mantén el control

- **Fes servir git.** Fes un commit abans de demanar canvis grans, perquè sempre puguis tornar enrere. Demana a Claude *"mostra'm què has canviat"* abans de fer el commit.
- **Permisos.** Claude Code pot executar ordres i editar fitxers sense preguntar cada vegada, segons el mode de permisos. Prem `Shift+Tab` per canviar de mode, per exemple a un que pregunti abans de cada canvi mentre n'aprens.
- **No l'executis en carpetes amb secrets o amb dades que no pots compartir** (consulta [Dades i privadesa](../getting-started/data-and-privacy.md)). Llegeix el que necessita de la carpeta on l'inicies.
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

## Ordres útils

| Ordre | Què fa |
|---|---|
| `claude` | Inicia una sessió a la carpeta actual |
| `claude -c` | Continua l'última sessió d'aquesta carpeta |
| `/clear` | Comença una conversa nova (fes-la servir quan canviïs de tasca) |
| `/help` | Mostra la llista d'ordres |
| `Esc` | Interromp Claude |

Per aprendre'n més, el curs gratuït [Claude Code 101](https://academy.claude.com/courses/claude-code-101) és un bon pas següent.
