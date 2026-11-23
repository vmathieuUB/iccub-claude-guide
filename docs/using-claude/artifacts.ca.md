# Artifacts

Quan Claude produeix alguna cosa substancial (un document, una presentació, un disseny, una petita pàgina interactiva), l'obre en un panell al costat del xat. Això és un Artifact. Tots els teus Artifacts es guarden a la pestanya **Artifacts** de la barra lateral esquerra.

## Tipus d'Artifact

Des de setembre de 2026, els Artifacts són de diversos tipus, i Sheets i Whiteboards (tots dos en beta) són els més nous. No cal que en triïs cap: demana el que vols i Claude tria. També pots començar a partir d'una plantilla a la pestanya **Artifacts**.

| Tipus | Útil per a | Exporta a |
|---|---|---|
| **Docs** | Un full informatiu per a una assignatura, un resum d'una pàgina d'un projecte, un informe, unes actes | Word, PDF, Markdown, Google Docs |
| **Slides** | Una xerrada, un seminari, diapositives de classe a partir de les teves notes | PowerPoint, PDF, Google Slides |
| **Design** | Un pòster, un full d'una pàgina, una pàgina web per a un esdeveniment, una maqueta | PDF, PowerPoint, HTML, .zip |
| **Sheets** (beta) | Un full de càlcul que edites amb Claude: un full de notes, un registre d'observacions, un pressupost amb fórmules que funcionen | .xlsx, CSV |
| **Whiteboards** (beta) | Pensar una idea: Claude organitza les notes en diagrames, fluxos i grups (l'esquema d'un article, el pla d'un projecte) | PNG |
| **Data** (abans *Dashboards*) | Taulers i petites històries de dades a partir d'una font de dades connectada (una base de dades o una aplicació com Salesforce). Pensat sobretot per a dades d'empresa; per als teus propis fitxers de dades, puja'ls a un xat. | |
| **Pàgines interactives** | Un control lliscant que mostra com canvia l'espectre de Planck amb la temperatura, un qüestionari per als estudiants, una calculadora senzilla | |

Els Artifacts creats abans de setembre de 2026 continuen funcionant i encara es poden publicar, però els nous fan servir els tipus d'aquesta taula.

## Com treballar-hi

- **Canvia'l demanant-ho**: *"Afegeix un segon control lliscant per al redshift"*, *"Fes la diapositiva 4 menys atapeïda."*
- **Edita'l tu mateix**: escriu directament en un document, edita qualsevol diapositiva o mou elements d'un disseny.
- **Edita'n una part amb Claude**: selecciona text en un document, fes clic a **Edit with Claude** i digues què cal canviar. Claude només toca aquella part.
- **Presenta** les diapositives directament des de Claude amb **Present**, o descarrega-les.
- **Torna enrere**: si edites un missatge anterior del xat, es crea una branca nova amb els seus propis Artifacts, i l'original es manté intacte.

Si no apareixen Artifacts, comprova que **Create and edit files** (abans *Code execution and file creation*) estigui activat a **Settings → Capabilities**.

## Compartir

- Els Artifacts nous són **privats** fins que els comparteixes.
- **Share** et dona un enllaç. Comprova qui el pot obrir abans d'enviar-lo, i no comparteixis res que no posaries en una pàgina web pública.
- Els Artifacts antics (d'abans de setembre de 2026) s'han de **publicar** per compartir-los; qualsevol persona amb l'enllaç els pot veure i fer servir sense compte.
- Alguns Artifacts interactius guarden dades. Si un Artifact fa servir **emmagatzematge compartit**, tothom qui l'obre veu el que s'hi introdueix. No hi escriguis dades sensibles.

## Exemples

!!! example "Diapositives per a un seminari"
    *"A partir de l'article adjunt, fes 12 diapositives per a un seminari de 30 minuts a l'ICCUB: motivació, mètode, tres resultats clau amb les figures de l'article i una diapositiva de perspectives. Fes servir un estil blanc i senzill amb lletra grossa."*

!!! example "Un gràfic interactiu per a una classe"
    *"Fes una pàgina interactiva amb un control lliscant per a la temperatura d'un cos negre de 3 K a 30 000 K. Mostra l'espectre de Planck en un gràfic log-log, marca el pic de Wien i escriu la longitud d'ona del pic. Afegeix un selector per canviar entre longitud d'ona i freqüència."*

!!! example "Un qüestionari"
    *"Fes un qüestionari de 10 preguntes tipus test sobre evolució estel·lar per a estudiants de primer. Després de cada resposta, mostra la resposta correcta i una explicació d'una línia. Mostra la puntuació al final."*

!!! example "Un resum d'una pàgina"
    *"Converteix la proposta adjunta en un document resum d'una pàgina per al web de l'ICCUB, amb un títol, tres paràgrafs breus i un requadre de 'Xifres clau'. Exporta'l a Word."*

## Limitacions

- Els Artifacts interactius s'executen al navegador. No substitueixen un codi d'anàlisi de veritat.
- Comprova la física i els números d'un Artifact igual que ho faries amb una resposta del xat: una diapositiva o un control lliscant amb bon aspecte poden fer servir igualment una fórmula equivocada.
- Els fitxers PowerPoint o Word exportats poden necessitar retocs de format; obre'ls abans de presentar-los o enviar-los.

Referències: [What are artifacts and how do I use them?](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them), [Claude Sheets](https://support.claude.com/en/articles/18324300-get-started-with-claude-sheets), [Claude Whiteboards](https://support.claude.com/en/articles/18324319-get-started-with-claude-whiteboards), [Claude Data](https://support.claude.com/en/articles/17454700-get-started-with-claude-data) (centre d'ajuda d'Anthropic).
