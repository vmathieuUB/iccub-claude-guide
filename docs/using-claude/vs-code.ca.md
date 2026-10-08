# Claude a VS Code

Molts de nosaltres escrivim codi, LaTeX i notes a **Visual Studio Code**. L'**extensió Claude Code** posa Claude en un panell dins de VS Code, on pot llegir el teu projecte, proposar canvis com a diffs que acceptes o rebutges, i executar ordres. Funciona amb el teu compte Pro; no cal cap clau d'API.

## Instal·lació

1. Obre VS Code (versió 1.94 o posterior).
2. Obre la vista d'extensions: `Cmd+Shift+X` (Mac) o `Ctrl+Shift+X` (Windows/Linux).
3. Cerca **Claude Code** (editor: Anthropic) i fes clic a **Install**.
4. Fes clic a la **icona de l'espurna** que apareix a dalt a la dreta d'un fitxer obert, o a la barra d'activitat de l'esquerra.
5. Inicia la sessió amb el teu compte de **Claude Pro** quan t'ho demani.

Si la icona no apareix, executa **Developer: Reload Window** des de la paleta d'ordres (`Cmd/Ctrl+Shift+P`).

## Obre el teu projecte de la manera correcta

Claude treballa sobre la **carpeta que obres** a VS Code. Obre la carpeta del teu article, de la teva assignatura o de la teva anàlisi (**File → Open Folder**), no un sol fitxer. Aleshores Claude pot llegir-ne tot el contingut, i només això.

## Ús quotidià

| Vols… | Fes això |
|---|---|
| Preguntar per un fragment de codi | Selecciona les línies. Claude veu la selecció automàticament. Després pregunta *"Què fa això?"* |
| Indicar un fitxer a Claude | Escriu `@` i el nom del fitxer: *"Compara `@fit_spectrum.py` amb `@fit_spectrum_old.py`"*. `Option+K` / `Alt+K` insereix la selecció actual com a referència. |
| Que Claude canviï codi | Descriu el canvi. Claude mostra cada edició com un **diff**; accepta-la o rebutja-la. |
| Planificar abans de canviar res | Escriu `/plan` seguit de la tasca. Claude proposa un pla que pots editar abans que toqui cap fitxer. |
| Treballar en diverses coses alhora | Obre diverses converses en pestanyes separades. |
| Pensar més a fons | Activa l'**extended thinking** des del menú `/` per a errors complicats i derivacions. |

## No només codi

VS Code + Claude també és una bona manera de treballar en **articles en LaTeX, apunts i Markdown**:

- *"Arregla tots els avisos de LaTeX de `main.tex` i fes que l'estil de les cites sigui coherent."*
- *"Llegeix els meus comentaris `% TODO` de `chapter3.tex` i resol-los un per un."*
- *"Converteix `notes.md` en un esquema estructurat per a la secció 2 de l'article."*

Consulta els exemples desenvolupats: [Escriure uns proceedings d'un congrés](../examples/research/conference-proceeding.md) i [Apunts a partir de diapositives](../examples/teaching/lecture-notes-from-slides.md).

## Explica a Claude el teu projecte

Posa un fitxer `CLAUDE.md` a l'arrel de la carpeta: què és el projecte, com s'executa, quines convencions segueix, què no s'ha de tocar. Claude el llegeix al començament de cada conversa. Escriu `/init` perquè Claude te'n prepari un esborrany. Més informació a [Claude Code](claude-code.md#make-it-know-your-project).

## Mantén el control

- **Fes servir git** (VS Code l'inclou de sèrie, al panell Source Control). Fes un commit abans d'un canvi gran perquè el puguis desfer.
- **Llegeix els diffs** abans d'acceptar-los. Claude es pot equivocar amb tota la seguretat del món.
- **Mode de permisos**: per defecte, Claude pot editar i executar coses preguntant menys. Mentre n'aprens, canvia a un mode que pregunti abans de cada canvi (mira el selector de mode al panell, o `Shift+Tab` a la versió de terminal).
- No obris carpetes que continguin secrets o dades que no tens permís per compartir. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).

## Extensió o terminal?

L'extensió i la versió de terminal (`claude` en un terminal, consulta [Claude Code](claude-code.md)) són el mateix assistent. L'extensió és més còmoda si ja passes el dia a VS Code; el terminal funciona a tot arreu, fins i tot per SSH en un clúster. Les converses es comparteixen entre totes dues.

Referència: [Claude Code in VS Code](https://code.claude.com/docs/en/vs-code) (documentació d'Anthropic).
