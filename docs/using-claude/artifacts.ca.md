# Artifacts

Quan Claude produeix alguna cosa substancial i autònoma (un document, un fragment de codi, un diagrama, una petita pàgina interactiva), l'obre en un panell al costat del xat. Això és un Artifact.

## Per a què són útils

- **Documents**: un full informatiu per a una assignatura, un resum d'una pàgina d'un projecte, unes preguntes freqüents.
- **Diagrames**: un diagrama de flux del teu pipeline de dades, una cronologia de l'Univers (SVG o Mermaid).
- **Pàgines interactives**: un control lliscant que mostra com canvia l'espectre de Planck amb la temperatura, un qüestionari per als estudiants, una calculadora senzilla.
- **Codi**: un script que copiaràs al teu projecte.

Claude decideix quan en crea un, però l'hi pots demanar: *"Fes-ne un artifact."*

## Com treballar-hi

- **Canvia'l demanant-ho**: *"Afegeix un segon control lliscant per al redshift"*, *"Fes la lletra més gran."* Claude actualitza l'Artifact i en conserva les versions anteriors; fes servir les fletxes del panell per tornar enrere.
- **Copia o descarrega**: botons a la cantonada superior del panell.
- **Publica**: el botó **Publish** o **Share** et dona un enllaç públic. Qualsevol persona amb l'enllaç el pot veure (i fer servir) sense compte. No publiquis res que no posaries en una pàgina web pública.

Si no apareixen Artifacts, comprova que **Code execution and file creation** estigui activat a Settings → Capabilities.

## Exemples

!!! example "Un gràfic interactiu per a una classe"
    *"Fes una pàgina interactiva amb un control lliscant per a la temperatura d'un cos negre de 3 K a 30 000 K. Mostra l'espectre de Planck en un gràfic log-log, marca el pic de Wien i escriu la longitud d'ona del pic. Afegeix un selector per canviar entre longitud d'ona i freqüència."*

!!! example "Un qüestionari"
    *"Fes un qüestionari de 10 preguntes tipus test sobre evolució estel·lar per a estudiants de primer. Després de cada resposta, mostra la resposta correcta i una explicació d'una línia. Mostra la puntuació al final."*

!!! example "Un resum d'una pàgina"
    *"Converteix la proposta adjunta en un resum d'una pàgina per al web de l'ICCUB, amb un títol, tres paràgrafs breus i un requadre de 'Xifres clau'."*

## Limitacions

- Els Artifacts interactius s'executen al navegador. No substitueixen un codi d'anàlisi de veritat.
- Comprova la física i els números d'un Artifact igual que ho faries amb una resposta del xat: un control lliscant amb bon aspecte pot fer servir igualment una fórmula equivocada.
