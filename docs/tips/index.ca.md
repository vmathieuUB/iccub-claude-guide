# Consells i errors habituals

Els paranys més freqüents i com evitar-los. La majoria es redueixen a una sola regla: **Claude és un assistent ràpid i amb molts coneixements que de vegades s'equivoca amb tota la seguretat del món. Tu continues sent responsable del que fas servir.**

## Coses que cal comprovar sempre

### Referències i citacions

Claude pot inventar-se referències que semblen reals (autors, revista i any versemblants) o atribuir una afirmació a l'article equivocat.

- Comprova cada referència a [ADS](https://ui.adsabs.harvard.edu) o a arXiv abans de fer-la servir.
- Pregunta *"De quines d'aquestes referències estàs segur que existeixen?"*, i interpreta "no n'estic segur" com "probablement inventada".
- Amb la [cerca web o Research](../using-claude/research.md) activats, Claude cita pàgines reals, però comprova que la pàgina digui el que Claude afirma.

### Números, deduccions i unitats

- Torna a fer tu mateix els passos clau. Els errors s'amaguen en factors de 2, π, signes i convencions de *h*.
- Demana les **unitats a cada pas** i una **comprovació de coherència** (ordre de magnitud, un límit conegut).
- Per a l'anàlisi de dades, demana el **codi** que ha produït un número i executa'l tu mateix.

### Codi

- Executa'l. Prova'l amb un cas en què coneguis la resposta.
- Llegeix els diffs abans d'acceptar canvis a [Claude Code](../using-claude/claude-code.md) o a [VS Code](../using-claude/vs-code.md).
- Vigila el codi que "funciona" perquè se salta dades sense dir res, captura totes les excepcions o té un resultat posat a mà.

### Afirmacions sobre les teves pròpies dades o el teu codi

Claude pot descriure el teu fitxer o el teu codi amb molta seguretat i equivocar-se, sobretot amb fitxers llargs. Demana-li que **citi la línia o la cel·la** de què parla.

## Com obtenir millors resultats

- **Dona context**: qui ets, per a qui és, com seria un bon resultat. Consulta [Xat i prompts](../using-claude/prompting.md).
- **Itera dins del mateix xat**, però **comença un xat nou** quan canviïs de tema.
- **Demana primer un pla** per a qualsevol cosa gran: un esquema abans d'un article, un pla abans de refactoritzar.
- **Treballa a passos petits**: una secció, una funció, un capítol cada vegada.
- **Demana una segona opinió**: enganxa la resposta en un xat nou i demana una revisió independent.
- **Fes servir Projects i `CLAUDE.md`** per no haver de repetir instruccions. Consulta [Projects](../using-claude/projects.md).

## Dades, privadesa i seguretat

- No pugis informes de revisió, propostes que estiguis avaluant, dades d'estudiants amb noms ni contrasenyes. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).
- Amb els [connectors](../using-claude/connectors.md) i [Claude in Chrome](../using-claude/chrome.md), Claude actua en nom teu. Demana-li **esborranys** i aprova tu mateix les accions.
- El text de correus, pàgines web o documents pot contenir instruccions adreçades a la IA ("prompt injection"). No deixis que Claude actuï segons instruccions que ha trobat dins d'un contingut.

## Declarar l'ús de la IA

- **Articles**: la majoria de revistes (A&A, MNRAS, ApJ, Physical Review…) et demanen que declaris com has fet servir les eines d'IA, normalment als agraïments o a la secció de mètodes. La IA no pot ser autora. Consulta la política actual de la teva revista.
- **Col·laboracions**: moltes tenen les seves pròpies normes sobre la IA i sobre compartir material intern. Comprova-ho abans de fer servir Claude amb documents d'una col·laboració.
- **Material docent**: indica quan els apunts o els exercicis s'han preparat amb ajuda de la IA.
- **Estudiants**: explica'ls clarament quin ús de la IA es permet a la teva assignatura, i dona per fet que la fan servir per a les tasques que fan a casa.

## Límits d'ús

- Els xats llargs, els fitxers grans, Opus i l'extended thinking consumeixen la teva quota més de pressa.
- Posa els fitxers que reutilitzes en un [Project](../using-claude/projects.md) en lloc de tornar-los a pujar.
- Si arribes al límit, es mostra l'hora en què es restableix. Consulta [Què inclou Claude Pro](../getting-started/what-is-claude.md#usage-limits).

## Sorpreses habituals

| Sorpresa | Per què | Què cal fer |
|---|---|---|
| Claude no coneix un article recent o una versió recent d'un programari | El seu coneixement s'atura en una data de tall de l'entrenament | Activa la cerca web o puja l'article |
| Ha oblidat alguna cosa del començament d'un xat llarg | Els xats llargs es resumeixen o perden detalls | Comença un xat nou amb un breu resum del que és important |
| Està d'acord amb tot el que dius | Tendeix a complaure l'usuari | Demana-li que argumenti en contra de la teva idea o que en trobi el punt més feble |
| La mateixa pregunta dona respostes diferents | Les respostes no són deterministes | Demana el raonament, compara i comprova |
| Es nega a fer una cosa inofensiva | Filtres de seguretat massa prudents | Reformula-ho amb context: qui ets i per què ho necessites |

Tens algun parany per afegir? [Explica-ns'ho](../contribute/index.md).
