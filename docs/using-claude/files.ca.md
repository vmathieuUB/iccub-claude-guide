# Pujar fitxers

Arrossega fitxers al xat, o fes clic a **+** al costat del quadre de missatge. Aleshores Claude els llegeix com a part de la conversa.

## Què pots pujar

| Tipus | Formats | Què veu Claude |
|---|---|---|
| Documents | PDF, DOCX, TXT, RTF, ODT, HTML, EPUB | El text. En els PDF de menys de 100 pàgines, també les figures, els gràfics i les taules. |
| Dades | CSV, JSON, XLSX | El contingut. Amb l'execució de codi activada, Claude també les pot analitzar amb Python. |
| Codi | `.py`, `.ipynb`, `.c`, `.f90`, `.tex` i altres fitxers de text | El text |
| Imatges | PNG, JPEG, GIF, WebP | La imatge: gràfics, fotos d'una pissarra, captures de pantalla, notes escrites a mà |

Límits: fins a **30 MB per fitxer** i **20 fitxers per xat**. Dels PDF de més d'unes 1000 pàgines només se'n llegeix el text. Les imatges funcionen millor amb 1000 px o més per costat.

!!! warning "Abans de pujar res"
    Consulta [Dades i privadesa](../getting-started/data-and-privacy.md). Res d'informes de revisió (referee reports), res de dades d'estudiants amb noms, res de material intern d'una col·laboració si no has comprovat les normes.

## Articles

- *"Resumeix el mètode i fes una llista de les hipòtesis principals."*
- *"Què fan servir per a la funció de massa dels halos, i en què es diferencia de Tinker et al.?"* (puja els dos articles)
- *"Explica la figura 4 a un estudiant de màster."*
- *"Escriu un resum de 150 paraules per a l'anunci del journal club del nostre grup."*

Claude llegeix les figures d'un PDF, així que pots preguntar directament pels gràfics. Comprova qualsevol cosa que pensis citar: Claude pot llegir malament un valor d'un gràfic.

## Dades

Amb **Code execution and file creation** activat (Settings → Capabilities), Claude pot executar Python sobre un fitxer CSV o Excel que hagis pujat: calcular estadístiques, ajustar un model, fer un gràfic i donar-te el fitxer resultant.

- *"Representa la columna `flux` en funció de `mjd`, amb barres d'error a partir de `flux_err`, i marca en vermell els punts amb `flag == 1`."*
- *"Ajusta una llei de potències a aquest espectre entre 1 i 10 keV i dona'm l'índex amb la seva incertesa."*

Demana-li també el codi, perquè el puguis tornar a executar i comprovar al teu ordinador.

## Imatges i captures de pantalla

- Una foto d'una pissarra: *"Passa això a LaTeX."*
- Un gràfic d'un col·lega: *"Què no està bé d'aquesta figura per a un article?"*
- Una captura de pantalla d'un missatge d'error: *"Què vol dir això i com ho arreglo?"*

## Fitxers que fas servir una vegada i una altra

Si sempre tornes a pujar el mateix pla docent, el mateix article o la mateixa guia d'estil, posa'ls en un [Project](projects.md). Tots els xats del Project els veuen, i consumeix menys dels teus límits d'ús que tornar-los a pujar.
