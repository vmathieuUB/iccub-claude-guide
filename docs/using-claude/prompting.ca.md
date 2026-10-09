# Xat i prompts

La major part del que faràs amb Claude és un xat normal. Uns quants hàbits hi marquen una gran diferència.

## Dona context

Claude sap física i Python, però no et coneix a tu, ni el teu projecte, ni el teu públic. Explica-li:

- **Qui ets** i a qui va dirigit el resultat.
- **Quina és la tasca**, i què faràs amb el resultat.
- **Com ha de ser un bon resultat**: extensió, format, nivell, llengua.

| En lloc de | Prova |
|---|---|
| *Explica la matèria fosca.* | *La setmana que ve faig una xerrada de 20 minuts per a estudiants de batxillerat. Explica les proves de l'existència de la matèria fosca en punts per a l'equivalent de cinc diapositives, sense equacions i amb una analogia de la vida quotidiana.* |
| *Arregla el meu codi.* | *Aquesta funció hauria de retornar la distància de lluminositat en Mpc per a una cosmologia ΛCDM plana, però dona valors un 10% massa alts a z = 1. Troba l'error.* (i després enganxa el codi) |
| *Escriu un correu als estudiants.* | *Escriu un correu breu i amable en català als meus estudiants de Física Quàntica per dir-los que l'examen passa del 12 al 19 de gener, a la mateixa aula.* |

Les preferències personals que defineixis a **Settings → Profile** s'afegeixen a cada xat, de manera que no cal que repeteixis qui ets cada vegada (consulta [Els teus primers 30 minuts](../getting-started/first-steps.md)).

## Itera, no tornis a començar

La primera resposta és un esborrany. Respon dient què cal canviar: *"més curt"*, *"més formal"*, *"fes servir numpy en lloc de bucles"*, *"el segon punt és incorrecte perquè…"*. Claude té present tota la conversa.

Comença un **xat nou** quan canviïs de tema. Els xats molt llargs van més lents, consumeixen més dels teus límits d'ús i Claude pot perdre de vista detalls del principi.

## Mostra un exemple

Si vols un format concret, enganxa'n un. *"Dona format a les referències així: …"* o *"Escriu l'exercici amb el mateix estil que aquest: …"* funciona millor que descriure l'estil.

## Demana a Claude que revisi la seva feina

- *"Revisa aquesta derivació pas a pas i digues-me on estàs menys segur."*
- *"Fes una llista de les hipòtesis que hagis fet."*
- *"De quines d'aquestes referències estàs segur que existeixen?"*

Sovint Claude detecta els seus propis errors quan l'hi demanes. No els detectarà tots: igualment has de verificar els números, les derivacions i les cites. Consulta [Consells i errors habituals](../tips/index.md).

## Trucs útils

- **Extended thinking** (menú de models sota el quadre de missatge): activa'l per a derivacions, depuració de codi i qualsevol cosa en què una resposta acurada importi més que una de ràpida.
- **Edita el teu missatge**: passa el ratolí per sobre d'un missatge que hagis enviat i fes clic al llapis per canviar-lo i obtenir una resposta nova, en lloc d'afegir-hi una correcció.
- **Torna-ho a provar**: el botó de reintentar que hi ha sota una resposta et dona una versió diferent.
- **Demana-li primer que et faci preguntes**: *"Abans de començar, pregunta'm tot el que necessitis saber."* és útil per a tasques més grans, com l'esquema d'una assignatura o una secció d'una proposta.
- **Llengua**: Claude funciona bé en anglès, castellà i català. Pregunta en una llengua i demana la resposta en una altra si et cal.
