---
tags:
  - Recerca
  - LaTeX
  - Redacció
---

# Escriure uns proceedings d'un congrés

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | 2026-09-28 |
| **Àrea** | Física hadrònica (teoria) |
| **Eines utilitzades** | Claude amb accés a una carpeta local del projecte |
| **Temps estalviat** | Els proceedings es van escriure en una mitja hora |
| **Resultat** | [Meson photoproduction at Jefferson Lab: from two-meson final states to meson-baryon spin-density matrices](https://inspirehep.net/literature/3208903) (INSPIRE) |

## Objectiu

Dos mesos abans havia fet una xerrada plenària al congrés MESON a Cracòvia. Normalment no escric proceedings, però aquesta vegada els meus col·legues experimentals de la col·laboració GlueX en necessitaven. Havien fet servir fórmules que jo havia derivat i que encara no estan publicades, perquè l'article no està acabat. Un estudiant de doctorat que havia fet l'anàlisi volia presentar els seus resultats preliminars en uns proceedings propis, i necessitava una referència per al formalisme. Així que em van demanar que escrivís uns proceedings que poguessin citar.

La petició em va arribar per Slack mentre era en un altre congrés, escoltant xerrades. No tenia temps d'escriure'ls jo mateix.

## Què vaig fer

1. **Vaig crear una carpeta nova** per als proceedings i hi vaig posar:
    - les diapositives de la meva xerrada al MESON,
    - la meva nota d'anàlisi, la que faré servir més endavant per escriure l'article complet,
    - la plantilla de LaTeX descarregada del web del congrés.

2. **Vaig donar accés a Claude a tot** el que hi havia a la carpeta.

3. **Vaig escriure un prompt llarg** explicant a Claude tota la història:
    - Vaig fer una xerrada plenària en aquest congrés, amb l'enllaç al web del congrés.
    - Les diapositives són el contingut de la xerrada, i la nota d'anàlisi conté el formalisme.
    - Per què calen els proceedings: els meus col·legues de GlueX i el seu estudiant de doctorat han de poder citar el formalisme abans que surti l'article.
    - Els proceedings han de seguir la plantilla del congrés.

4. **Vaig llegir l'esborrany.** Al cap d'una mitja hora els proceedings ja estaven escrits.

5. **Els vaig acabar a mà:**
    - vaig treure una frase que no era adequada,
    - vaig afegir el meu correu electrònic i els números dels meus projectes de finançament,
    - els vaig enviar a arXiv i a les actes del congrés.

## Resultat

Els proceedings eren clars, concisos, exactament el que volia, i amb el format que demanava el congrés. Llevat de la frase que vaig treure, vaig mantenir el text tal com l'havia escrit Claude.

Són a arXiv i a INSPIRE: [Meson photoproduction at Jefferson Lab: from two-meson final states to meson-baryon spin-density matrices](https://inspirehep.net/literature/3208903). Ara els meus col·legues poden citar el formalisme en els seus propis proceedings.

## Què cal vigilar

- **Dona tot el context.** El prompt llarg amb tota la història (qui ho necessita, per què i què ha de contenir) és el que va fer que el primer esborrany fos aprofitable.
- **Posa les fonts reals a la carpeta.** Les diapositives, la nota d'anàlisi i la plantilla oficial van fer que Claude treballés a partir del meu material i no de coneixement general.
- **Llegeix cada frase.** Una frase no era adequada i vaig haver de treure-la. L'autor continues sent tu.
- **Treball no publicat.** La nota d'anàlisi contenia resultats que encara no estan publicats. Comprova què pots compartir abans de donar-hi accés a Claude. Consulta [Dades i privadesa](../../getting-started/data-and-privacy.md).
- **Els detalls els has d'afegir tu**: correu electrònic de l'autor, afiliacions, números de projectes de finançament, agraïments.
