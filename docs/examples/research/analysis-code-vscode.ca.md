---
tags:
  - Recerca
  - Claude Code
  - Programació
---

# Accelerar el codi d'un article publicat

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | 2026-10-09 |
| **Àrea** | Física hadrònica (teoria) |
| **Eines utilitzades** | Claude Code, Google Antigravity (Gemini) i un model local, cadascun amb accés a la carpeta del codi |
| **Temps estalviat** | Revisió feta en una mitja hora; ara el codi és més de 10 vegades més ràpid |
| **Article** | [High-energy η(′)π photoproduction and the nature of exotic waves](https://inspirehep.net/literature/3070423), G. Montaña, V. Mathieu et al., Phys. Lett. B 872 (2026) 140101 ([arXiv:2510.14549](https://arxiv.org/abs/2510.14549)) |

## Objectiu

El 2025 vam publicar un article amb la Gloria Montaña i altres col·legues sobre la producció d'ηπ a alta energia. El model té cinc variables, i calcular els observables volia dir integrar sobre quatre d'elles.

Vaig escriure el codi de Monte Carlo jo mateix, força de pressa, en part mentre viatjava. Vaig decidir no fer servir **cap llibreria**: volia entendre cada pas, així que totes les rutines estaven escrites a mà, des de la integració de Monte Carlo fins al determinant d'una matriu 6×6 que serveix per comprovar els límits de la regió física. Funcionava, i es va fer servir per a l'article, però un càlcul complet trigava hores.

Un any després, quan vaig començar a fer servir eines de programació amb IA, vaig voler saber si aquest codi es podia fer més ràpid.

## Què vaig fer

1. **Vaig donar a l'eina accés a la carpeta** amb el codi que havia produït els resultats publicats.
2. **Vaig explicar el context**: l'article, i que aquest era el codi que s'hi havia fet servir.
3. **Vaig demanar una revisió**, en essència: *"Aquest és el codi que es va fer servir per publicar aquest article. Revisa tots els fitxers i mira si el podem optimitzar."*
4. **Vaig repetir l'exercici amb tres eines**: Google Antigravity (amb Gemini), Claude (Sonnet, a Claude Code) i un model local, per veure si arribaven a les mateixes conclusions.

## Resultat

La revisió va durar una mitja hora. Va trobar:

- **Feina duplicada**: diversos llocs on es calculava la mateixa quantitat dues vegades, cadascun un factor 2.
- **Rutines poc eficients**: la meva rutina feta a mà per al determinant no era eficient.

Tot plegat va donar **una acceleració de més d'un factor 10**. Un any després de l'article, el mateix codi va molt, molt més ràpid.

Les tres eines (Antigravity, Claude i el model local) van portar a la mateixa conclusió: el codi va ser molt més eficient després de la revisió amb IA.

## Què cal vigilar

- **Escriu-lo tu primer.** Crec que és bona idea començar programant cada funció tu mateix, sense llibreries, per entendre tant la física com el codi.
- **Després optimitza amb IA.** Quan el codi funciona i està comprovat, i el necessites eficient per produir els resultats definitius, demana a una IA que l'optimitzi. Mantens la comprensió *i* tens un codi eficient.
- **Comprova que els resultats no canvien.** Compara la sortida del codi optimitzat amb els resultats publicats abans de fer-lo servir.
- **Qualsevol eina serveix.** Aquí una eina al núvol i un model local van trobar les mateixes millores; si el teu codi no pot sortir de la teva màquina, consulta [Executar un LLM local al teu portàtil](local-llm-laptop.md).
