---
tags:
  - Recerca
  - Claude Code
  - VS Code
  - Programació
---

# Endreçar i provar un pipeline d'anàlisi a VS Code

!!! info "Exemple il·lustratiu"
    Aquest exemple l'han escrit els editors del web per mostrar el flux de treball. Encara no és una experiència real de l'ICCUB. Si el proves, [envia'ns la teva versió](../../contribute/index.md) i el substituirem.

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Editors de la guia de Claude de l'ICCUB |
| **Data** | 2026-10-06 |
| **Àrea** | Qualsevol treball computacional |
| **Eines utilitzades** | Extensió de Claude Code a VS Code, Python, pytest, git |
| **Temps estalviat** | Uns dos dies (estimació) |

## Objectiu

Un estudiant de doctorat se'n va i traspassa a un nou estudiant una anàlisi en Python de 3000 línies (un gran script més uns quants notebooks). Volem que sigui comprensible, que tingui tests i que sigui reproduïble abans del traspàs, sense canviar els resultats científics.

## Què vaig fer

1. **Vaig obrir la carpeta del repositori a VS Code** i em vaig assegurar que tot estava desat amb commit a git.

2. **Vaig demanar un recorregut, sense canvis:**

    > *Explica què fa aquest projecte, el flux de dades des dels fitxers en brut fins als gràfics finals i quines funcions són les més fràgils. No canviïs res.*

3. **Primer vaig congelar els resultats actuals.** Abans de qualsevol refactorització:

    > *Escriu un script `tests/make_reference.py` que executi tot el pipeline sobre `data/sample/` i desi cada array de sortida a `tests/reference/`. Després escriu un test de pytest que torni a executar el pipeline i comprovi que les sortides coincideixen amb la referència fins a 1e-10.*

    El vaig executar un cop, vaig revisar a ull les sortides de referència i en vaig fer commit.

4. **Vaig refactoritzar a petits passos amb `/plan`:**

    > */plan Divideix analysis.py en mòduls (io, cleaning, fitting, plotting) sense canviar-ne el comportament. Proposa primer la divisió.*

    Un cop acordat el pla: *"Fes només el pas 1 i després executa els tests."* Ho vaig repetir pas a pas, llegint cada diff.

5. **Vaig afegir tests unitaris** per a les funcions principals: *"Escriu tests per a `fit_profile` que incloguin casos límit: entrada buida, NaN, un sol punt."* Dos tests van fallar i van revelar un error real en el tractament dels NaN, que vam corregir per separat i documentar.

6. **Vaig escriure documentació**: un `README.md` amb instruccions d'instal·lació i execució, docstrings i un `CLAUDE.md` per a qui faci servir Claude amb el codi després.

## Resultat

Els mateixos resultats numèrics (el test de regressió passa), cinc mòduls en lloc d'un sol script, 25 tests unitaris, un README i un error real trobat i corregit.

## Què cal vigilar

- **Congela els resultats abans de refactoritzar.** Sense el test de regressió, petits canvis de comportament (ordenació, precisió de coma flotant, arguments per defecte) passen desapercebuts.
- **Petits passos.** "Refactoritza-ho tot" produeix un diff massa gran per revisar-lo.
- **Els tests escrits per Claude també poden estar malament**: un test que comprova el comportament erroni només consolida l'error. Llegeix-los.
- **No deixis que "arregli" la física** mentre refactoritza. Demana-li que faci una llista a part de la física sospitosa en lloc de canviar-la.
