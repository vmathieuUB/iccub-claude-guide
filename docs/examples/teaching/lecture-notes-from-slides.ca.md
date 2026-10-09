---
tags:
  - Docència
  - LaTeX
  - Redacció
---

# Converteix les teves diapositives en apunts, capítol a capítol

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | 2026-10-08 |
| **Àrea** | Docència (assignatura universitària) |
| **Eines utilitzades** | Claude amb accés a una carpeta local, LaTeX |
| **Resultat** | Apunts en català i en castellà, publicats al Campus Virtual de la UB |

## Objectiu

Escriure uns apunts com cal per a la meva assignatura a partir de les diapositives de classe, en les dues llengües en què s'imparteix (català i castellà), i publicar-los per als estudiants al Campus Virtual de la UB.

## Què vaig fer

### 1. Posar-ho tot en una sola carpeta

Vaig obrir Claude, vaig crear una carpeta nova i hi vaig posar:

- les diapositives de les meves classes,
- referències: alguns llibres que tenia,
- el *pla docent* (el pla docent oficial de l'assignatura).

Com més context li dones, millor i més polit és el resultat.

### 2. Fer primer la plantilla

Abans d'escriure cap contingut, vam crear junts una plantilla de LaTeX amb l'estil que volia: tipus de lletra, colors, disseny, tot. No vaig passar a la següent fase fins que la plantilla em va agradar.

També funciona bé **donar-li tu mateix l'estructura**: esbossa l'esquelet de LaTeX amb els capítols i les seccions que vulguis, i Claude l'omple.

### 3. Escriure capítol a capítol

Després vaig demanar a Claude que escrivís els apunts capítol a capítol, a partir de les meves diapositives i seguint el *pla docent*.

### 4. Revisar escrivint comentaris directament al fitxer .tex

Per a cada capítol, Claude escrivia una primera versió. Jo obria el fitxer `.tex` i hi escrivia els meus comentaris directament, allà on calia el canvi. Per exemple:

```latex
% Here I want an example.
% Here I want a figure.
% This figure is not correct.
```

Després tornava al xat amb Claude i li deia: *"He posat comentaris al fitxer, revisa'ls."*

Ho vaig repetir durant diverses iteracions, fins que el capítol em va agradar, i llavors passava al següent.

### 5. Primer una llengua, després traduir

Vaig treballar només en una llengua. Quan un capítol era definitiu en aquella llengua, demanava a Claude que el traduís a l'altra (català ↔ castellà).

### 6. Publicar

Els apunts acabats, en les dues llengües, es van publicar a la pàgina de l'assignatura al Campus Virtual de la UB.

## Resultat

Uns apunts complets, amb el meu estil i seguint les meves diapositives i el *pla docent*, tant en català com en castellà, disponibles per als estudiants al Campus Virtual.

## Què cal vigilar

- **Primer, la plantilla.** Fixar l'estil abans d'escriure estalvia haver de tornar a donar format a cada capítol més endavant.
- **Dona-li estructura i context.** Un esquelet de LaTeX, les diapositives, els llibres i el *pla docent* van fer que els esborranys s'acostessin més al que volia.
- **Els comentaris dins del fitxer funcionen millor que els missatges llargs al xat.** Cada comentari és exactament on cal el canvi.
- **Itera per capítols.** Acaba un capítol abans de començar el següent.
- **Acaba una llengua abans de traduir.** Si no, cada correcció s'ha de fer dues vegades.
- **Revisa la física.** Llegeix cada deducció i cada exemple: el responsable del contingut continues sent tu.
