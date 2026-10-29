# Claude in Chrome

**Claude in Chrome** és una extensió del navegador que permet que Claude llegeixi pàgines web, hi faci clic i hi escrigui, des d'un panell lateral al costat de la pàgina. Pot fer per tu tasques de diversos passos en llocs web: omplir un formulari, recollir informació de diverses pestanyes, navegar per un portal web complicat. Està inclosa a Pro, només per a Google Chrome d'escriptori (no per a altres navegadors Chromium ni per al mòbil).

## Instal·lació

1. A Google Chrome (escriptori), ves a la Chrome Web Store i cerca **Claude** d'Anthropic.
2. Fes clic a **Add to Chrome**.
3. Inicia la sessió amb el teu compte de Claude Pro.
4. Fixa-la: fes clic a la icona del trencaclosques de la barra d'eines i després a la xinxeta al costat de Claude.
5. Fes clic a la icona de Claude per obrir el panell lateral.

!!! info "Què ha canviat a la tardor de 2026"
    - El panell lateral s'està convertint en una sessió completa de Claude (abans en deien sessió de *Cowork*): les converses es desen, se sincronitzen amb els teus altres dispositius i poden fer servir les teves skills i connectors. Arriba als comptes Pro de manera gradual. Per tornar enrere, fes clic als tres punts de la part superior dreta del panell i tria **Switch back to classic**.
    - **Tasques programades**: la icona del rellotge de la part superior dreta del panell executa una tasca al navegador cada dia, cada setmana o cada mes.
    - **Dreceres** (shortcuts): desa un prompt que reutilitzes i crida'l escrivint `/`.
    - L'**aplicació d'escriptori** ara té el seu propi navegador integrat, que Claude pot fer servir en lloc de Chrome durant les [tasques llargues](tasks.md). Tria quin a **Settings → Cowork → Preferred browser**. Perquè l'aplicació d'escriptori pugui fer servir Chrome, ves a **Customize → Connectors**, fes clic a **Configure** al costat de Claude in Chrome i activa-ho.

## Per a què és útil

- **Recollir informació**: *"Obre les pàgines d'inscripció d'aquests tres congressos i fes una taula amb les dates, les quotes, el termini d'enviament de resums i el termini de la tarifa reduïda (early bird)."*
- **Portals feixucs**: *"Segueix els passos d'aquesta pàgina per descarregar el registre d'observació de la proposta 2026A-017."* (la sessió la inicies tu)
- **Llegir el que estàs mirant**: *"Resumeix la pàgina del resum d'aquest article i digues-me si fan servir el mateix conjunt de simulacions que nosaltres."*
- **Formularis**: *"Omple aquest formulari de viatge amb les dades del correu de confirmació que tinc obert a l'altra pestanya. No l'enviïs."*

## La seguretat, primer

Claude in Chrome actua **com si fossis tu**, als llocs on tens la sessió iniciada. Pensa-ho com si deixessis el teu portàtil a algú durant uns minuts.

- **Comprova el mode de permisos.** El panell lateral comença en **Automatically approve**, en què Claude només s'atura quan una acció necessita aprovació. Mentre n'aprens, canvia a un mode que pregunti abans de cada acció; el panell recorda la teva tria.
- **Comença amb tasques només de lectura.** Deixa que reculli informació i la resumeixi abans de deixar-lo escriure o fer clic a *Submit*.
- **Demana-li que s'aturi abans d'enviar**: afegeix *"No l'enviïs, ho revisaré primer"* a qualsevol tasca amb formularis.
- **Permisos per lloc web**: Claude pregunta abans d'actuar en un lloc nou. Permet només els llocs que necessitis. Evita la banca en línia, les nòmines de la UB i els portals de recursos humans.
- **Les pàgines no fiables poden contenir instruccions amagades** adreçades a assistents d'IA ("prompt injection"). No deixis que Claude actuï en pàgines de les quals no et fiïs, i vigila què fa.
- Tot el que Claude llegeix en una pàgina passa a formar part del teu xat. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).

## Extensió de Chrome o connectors?

Si un servei té un [connector](connectors.md) (Gmail, Google Drive, Google Calendar, GitHub…), fes servir el connector: és més ràpid i més fiable. Fes servir Chrome per a llocs web que no tenen connector, com ara webs de congressos, sistemes d'enviament d'articles a revistes o portals universitaris.

Referència: [Getting started with Claude in Chrome](https://support.claude.com/en/articles/12012173-getting-started-with-claude-in-chrome) (centre d'ajuda d'Anthropic).
