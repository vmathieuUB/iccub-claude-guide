---
tags:
  - Docència
  - Projects
---

# Fulls d'exercicis amb solucions, en un Project

!!! info "Exemple il·lustratiu"
    Aquest exemple l'han escrit els editors del lloc per mostrar el flux de treball. Encara no és una experiència real de l'ICCUB. Si el proves, [envia'ns la teva versió](../../contribute/index.md) i el substituirem.

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Editors de la Guia de Claude de l'ICCUB |
| **Data** | 2026-10-06 |
| **Àrea** | Docència |
| **Eines utilitzades** | Projects de claude.ai, raonament estès (extended thinking) |
| **Temps estalviat** | Unes 2 hores per full (estimació) |

## Objectiu

Preparar els fulls de problemes setmanals d'una assignatura, al nivell adequat, amb solucions completes per als professors de pràctiques, i sense repetir els problemes de l'any passat.

## Què vaig fer

1. **Vaig crear un Project** (projecte) "Electromagnetisme, fulls de problemes" i hi vaig pujar: el programa de l'assignatura, els apunts, i els fulls i exàmens de l'any passat (perquè pugui evitar repetir-los).

2. **Instruccions del Project:**

    ```text
    Assignatura: Electromagnetisme, 2n de Física, UB. Fulls de problemes en català.
    Cada full: 5 problemes, de dificultat creixent, que cobreixin només la matèria explicada fins a aquella setmana.
    Format: LaTeX, amb la classe exam. Les solucions, en un fitxer a part.
    No reutilitzis problemes dels fulls i exàmens anteriors que t'he pujat.
    Les solucions han de ser completes, amb tots els passos, i una comprovació numèrica final.
    ```

3. **Cada setmana**, amb el raonament estès activat:

    > *La setmana 6 vam veure la llei de Gauss en medis materials i les condicions de contorn (apunts, cap. 6). Prepara el full i les solucions.*

4. **Vaig comprovar les solucions** demanant una verificació independent en un **xat nou** (perquè no es limiti a donar-se la raó a si mateix):

    > *Aquí tens un problema i una proposta de solució. Resol-lo de manera independent, després compara-ho i assenyala qualsevol error.*

5. Vaig corregir a mà i compilar.

## Resultat

Un full i un fitxer de solucions cada setmana, amb uns 30 minuts de revisió en lloc de 2 o 3 hores de redacció.

## Què cal vigilar

- **Les solucions contenen errors** amb una freqüència sorprenent en els problemes més difícils: unitats, signes, un límit equivocat. La verificació independent en detecta alguns; la resta els has de detectar tu.
- **Alguns problemes poden no tenir solució** tal com estan plantejats (dades que falten, nombres incoherents). Resol-los tu mateix o fes que els resolgui un professor de pràctiques abans de publicar-los.
- **Originalitat**: els problemes poden assemblar-se a d'altres de coneguts dels llibres de text. Normalment no és cap problema per practicar, però sí per als exàmens.
