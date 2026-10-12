---
tags:
  - Recerca
  - Scheduled tasks
---

# Un resum setmanal d'arXiv, cada dilluns

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Vincent Mathieu |
| **Data** | 2026-10-12 |
| **Àrea** | Física hadrònica (teoria) |
| **Eines utilitzades** | Una scheduled task de Claude, l'API pública d'INSPIRE-HEP |
| **Temps estalviat** | La revisió dels articles nous del dilluns, cada setmana |

## Objectiu

Cada setmana surten desenes d'articles a hep-ph, nucl-th i hep-lat. Volia una llista curta el dilluns al matí amb dues coses: els articles nous que citen la meva feina i els articles nous sobre els meus temes (teoria de Regge, fotoproducció, anàlisi d'amplituds, hadrons exòtics, glueballs, regles de suma, espectroscòpia en el reticle), cadascun amb una o dues frases sobre per què m'interessa.

En lloc de demanar-ho a Claude cada setmana, vaig escriure la petició una sola vegada i en vaig fer una **scheduled task** (tasca programada): Claude executa el mateix prompt tot sol a una hora fixa i em deixa el resultat per llegir.

## Què vaig fer

1. **Vaig triar la font.** [INSPIRE-HEP](https://inspirehep.net) té una API pública i gratuïta que no demana iniciar sessió. Sap qui cita qui, cosa que els llistats d'arXiv sols no saben. M'identifico amb el meu identificador d'autor d'INSPIRE (`V.Mathieu.1`, que surt a la teva pàgina d'autor d'INSPIRE).

2. **Vaig escriure les consultes com a URL completes.** Una per a les citacions de la meva feina i tres per als meus temes. Cada URL està escrita sencera al prompt (mira l'avís de més avall per saber per què).

3. **Vaig escriure el prompt.** Diu qui soc, què cal descarregar, què cal conservar i com ha de ser el resum. Una versió escurçada que pots adaptar:

    ```text
    Aquesta és una execució automàtica d'una tasca programada. L'usuari no hi
    és per respondre preguntes. No facis preguntes aclaridores ni cap acció
    d'"escriptura"; si dubtes, informa del que hagis trobat.

    Prepares un resum setmanal de bibliografia per a <el teu nom>, que treballa
    en <els teus temes>, identificador d'autor d'INSPIRE "<el teu ID>",
    sobretot a les categories d'arXiv <les teves categories>.

    Fes servir l'API pública d'INSPIRE-HEP. Descarrega cada URL de sota
    exactament tal com està escrita.

    Pas 1, articles que citen la meva feina. Descarrega:
    https://inspirehep.net/api/literature?sort=mostrecent&size=25&q=refersto:a%20<el teu ID>&fields=titles,abstracts,arxiv_eprints,authors,earliest_date
    Conserva només les entrades amb earliest_date dels últims 7 dies.
    Si aquesta consulta falla, digues-ho en lloc d'informar que "no hi ha citacions".

    Pas 2, articles nous sobre els meus temes. Descarrega:
    https://inspirehep.net/api/literature?sort=mostrecent&size=20&q=(t%20<tema 1>%20or%20t%20<tema 2>)&fields=titles,abstracts,arxiv_eprints,authors,earliest_date
    (una URL per a cada grup de temes)
    Conserva els últims 7 dies, apunta a entre 10 i 15 articles i prioritza
    els que s'hi ajustin més.

    Pas 3, elimina els duplicats entre els passos 1 i 2.

    Pas 4, presenta dues seccions: "Articles que citen la teva feina" i
    "Articles nous sobre els teus temes". Per a cada article: títol, primer
    autor (et al. si n'hi ha més de 3), enllaç d'arXiv i 1 o 2 frases sobre
    per què és rellevant per a mi. Fes-ho curt i fàcil de llegir.
    ```

4. **El vaig executar una vegada a mà** i vaig comprovar el resultat amb INSPIRE abans de programar res.

5. **El vaig programar**: cada dilluns a les 08:00, hora de Madrid. Ho pots demanar directament a Claude, *"Converteix això en una tasca programada que s'executi cada dilluns a les 8:00"*, i apareix a la teva llista de tasques programades, on la pots aturar, editar o executar quan vulguis.

## Resultat

El dilluns obro l'execució i hi trobo el resum. Aquesta setmana hi havia onze articles que citaven la meva feina, entre ells una reanàlisi de la X(2370) en desintegracions radiatives de la J/ψ i un estudi en el reticle de tetraquarks totalment encantats, cadascun amb l'enllaç d'arXiv i un resum de dues línies. També deia clarament que cap de les consultes de temes no tenia res posterior a setembre, així que sabia que la secció era buida, no que estigués trencada.

## Què cal vigilar

- **No hi ha ningú per clicar "Allow".** Una tasca programada s'executa quan no hi ets. La primera execució automàtica d'aquesta va fallar: cada petició web necessitava un permís que jo no hi era per donar, i Claude va informar que no tenia articles en lloc d'inventar-se'n. Executa la tasca una vegada a mà, accepta els permisos que et demani i revisa la següent execució automàtica.
- **Escriu les URL senceres.** L'eina de descàrrega web només obre URL que apareixen exactament al prompt, així que Claude no pot construir una consulta a partir d'una plantilla durant l'execució. Les URL molt llargues també es rebutgen, així que divideix les llistes de temes llargues en diverses consultes curtes.
- **Demana-li que informi dels errors.** "Si aquesta consulta falla, digues-ho" converteix una secció buida silenciosa en un missatge clar.
- **Comprova el que resumeix.** Els resultats passen per un resumidor, i alguns articles "que citen" no hi tenien res a veure (PDF nuclears, programari d'acceleradors). Obre INSPIRE abans de citar res.
- **Una execució, un informe.** Demana un missatge al xat, no un fitxer, i cap acció d'"escriptura": una tasca sense supervisió ha de llegir i informar, no canviar coses per tu.
- **Fa servir la teva quota de Pro.** Cada execució compta com una conversa normal. Un cop per setmana és poc; cada hora no.
