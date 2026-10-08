---
tags:
  - Divulgació
  - Artifacts
---

# Una pàgina web animada per a un acte públic

!!! info "Exemple il·lustratiu"
    Aquest exemple l'han escrit els editors del lloc per mostrar el flux de treball. Encara no és una experiència real de l'ICCUB. Si el proves, [envia'ns la teva versió](../../contribute/index.md) i el substituirem.

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Editors de la Guia de Claude de l'ICCUB |
| **Data** | 2026-10-06 |
| **Àrea** | Divulgació |
| **Eines utilitzades** | Artifacts de claude.ai i, després, Claude Code per a la versió final |
| **Temps estalviat** | Dies de desenvolupament web, per a algú que no fa llocs web (estimació) |

## Objectiu

Per a l'estand d'una jornada de portes obertes, fer una pàgina interactiva amb què els visitants puguin jugar en una tauleta: **"Construeix un sistema solar"**, on col·loques planetes al voltant d'una estrella i en veus les òrbites, amb una breu explicació de les lleis de Kepler. Sense necessitat de saber desenvolupament web.

## Què vaig fer

1. **Ho vaig descriure en un xat**, demanant un Artifact (artefacte):

    > *Fes una pàgina web interactiva per a una fira de ciència, per a visitants a partir de 10 anys. Una estrella al centre; els visitants toquen la pantalla per afegir planetes a diferents distàncies; els planetes orbiten amb velocitats realistes segons Kepler (els interiors, més ràpid). Mostra el període orbital de cada planeta. Un botó "Explica" obre una explicació de tres frases de la tercera llei de Kepler. Botons grans, que funcioni en una tauleta, amb colors vius però no infantil. Text en català, castellà i anglès amb un selector d'idioma.*

2. **Vaig iterar jugant-hi**, en el mateix xat:

    > *Els planetes són massa petits en una tauleta. Afegeix estela darrere dels planetes. Afegeix un botó de "reinicia". Quan dos planetes siguin massa a prop, mostra un avís "Òrbita inestable!".*

3. **Vaig comprovar la física**: *"Mostra'm la fórmula que fas servir per al període i les unitats."* Vaig verificar que, en doblar la distància, el període es multiplica per 2,83.

4. **El vaig publicar** amb el botó **Publish** de l'Artifact per obtenir un enllaç i un codi QR per a l'estand. Per tenir-ne una versió permanent al web de l'ICCUB, vaig descarregar el fitxer HTML i el vaig passar a l'equip web.

## Resultat

Una pàgina funcional, bilingüe i adaptada a pantalles tàctils en aproximadament una hora, utilitzada en una tauleta a l'estand. Els nens hi jugaven; els pares llegien l'explicació.

## Què cal vigilar

- **Dreceres en la física**: les animacions sovint falsegen la física (òrbites circulars, proporcions de velocitat incorrectes). Pregunta què es calcula i comprova-ho.
- **Traduccions**: fes que un parlant nadiu revisi els textos en català i en castellà.
- **Els Artifacts publicats són públics**: qualsevol persona amb l'enllaç els pot veure. No hi posis res confidencial.
- **Prova-ho al dispositiu real** abans de l'acte: les tauletes tenen mides de pantalla i comportaments tàctils diferents.
- Per a una cosa més gran (diverses pàgines, mantingudes durant anys), fes servir [Claude Code](../../using-claude/claude-code.md) en un repositori com cal en lloc d'un Artifact.
