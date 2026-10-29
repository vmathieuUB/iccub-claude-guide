# Correu electrònic, calendari i documents

Amb els [connectors](connectors.md), Claude pot cercar al teu correu, llegir fitxers adjunts del teu Drive, consultar el teu calendari i redactar esborranys de respostes. És la configuració més útil per a la feina de gestió: viatges, reemborsaments, planificació de reunions, informes.

## Quin connector

| El teu compte | Connector | Què pot fer Claude |
|---|---|---|
| Gmail / compte de Google | **Gmail**, **Google Calendar**, **Google Drive** | Cercar i llegir correus, redactar, respondre i enviar (abans t'ho pregunta); veure, crear i modificar esdeveniments; trobar franges lliures; cercar, llegir i desar fitxers del Drive |
| Compte de Google | **Google Docs**, **Google Sheets**, **Google Slides** | Editar un fitxer en directe en un panell al costat del xat, crear-ne de nous, treballar amb els comentaris i suggeriments de Docs |
| Microsoft 365 de la UB (Outlook, OneDrive, SharePoint, Teams) | **Microsoft 365** | Cercar al correu, al calendari, a OneDrive, a SharePoint i a Teams. Des de juliol de 2026 també pot redactar i enviar correus, gestionar esdeveniments i editar fitxers d'OneDrive/SharePoint, però només un cop l'administrador ha habilitat aquestes eines d'escriptura |

!!! warning "Microsoft 365 necessita els serveis informàtics de la UB"
    El connector de Microsoft 365 només funciona amb un compte de feina, un cop un administrador de Microsoft de l'organització l'ha aprovat una vegada (les eines d'escriptura necessiten una segona aprovació). Els comptes personals com @outlook.com no són compatibles. Si et diu que cal aprovació per al teu compte de la UB, posa't en contacte amb els serveis informàtics de la UB; mentrestant, fes servir el connector de Gmail amb un compte de Google, o reenvia els correus rellevants i puja els fitxers adjunts a mà.

## Connecta

1. En un xat, fes clic a **+** i després a **Connectors** (o ves a **Customize → Connectors**).
2. Fes clic a **Connect** al costat de Gmail, Google Calendar, Google Drive, Google Docs/Sheets/Slides o Microsoft 365.
3. Inicia la sessió amb el compte que vols que Claude faci servir i aprova l'accés.
4. A cada xat, fes servir **+** per activar o desactivar connectors. Deixa activat només el que necessiti aquell xat.

## Què li pots demanar

**Correu electrònic**

- *"Troba tots els correus del SOC del congrés de Lisboa i fes una llista del que em demanen que faci, amb els terminis."*
- *"Resumeix el fil sobre el nou node de GPU i digues-me qui està esperant una resposta meva."*
- *"Redacta un esborrany de resposta educada per declinar la petició de revisió, suggerint el Dr. X en el meu lloc. No l'enviïs."*

**Calendari**

- *"Com tinc la setmana? Avisa'm de qualsevol cosa que coincideixi amb les meves classes de dimarts i dijous."*
- *"Troba tres franges d'1 hora en les dues setmanes vinents en què l'Anna, en Marc i jo estiguem lliures."* (funciona si et comparteixen els seus calendaris)
- *"Crea un esdeveniment divendres de 15:00 a 16:00, 'Reunió de grup', sala 503, i afegeix-hi l'ordre del dia del meu últim correu a en Pau."*

**Combinat**

- *"Cada divendres a les 16:00, fes una llista dels correus d'aquesta setmana que encara esperen una resposta meva."* (una [tasca programada](tasks.md#scheduled-tasks))
- *"He tornat del congrés de Lisboa. Troba al meu correu el rebut de la inscripció i les confirmacions del vol i de l'hotel, fes una llista dels imports i les dates, i redacta l'esborrany del correu de reemborsament per a l'administració del departament."* Consulta l'exemple complet: [Reemborsament d'un viatge a un congrés](../examples/admin/conference-reimbursement.md).

## Claude dins d'Office: els complements de Microsoft 365

A part del connector, **Claude for Microsoft 365** posa Claude en un panell lateral dins d'**Excel**, **Word** i **PowerPoint** (i d'**Outlook**, en beta). Instal·la'ls des de [claude.com/claude-for-microsoft-365](https://claude.com/claude-for-microsoft-365) i inicia la sessió amb el teu compte de Claude.

- **Excel**: pregunta per cel·les i fórmules, actualitza un model sense trencar-lo.
- **Word**: els canvis apareixen com a **control de canvis**; Claude pot respondre fils de comentaris. Pràctic per a propostes escrites a diverses mans.
- **PowerPoint**: crea o edita diapositives amb la teva pròpia plantilla.
- **Outlook** (beta): classifica la safata d'entrada i redacta respostes que esperen que les enviïs tu.

A la UB, instal·lar complements d'Office també pot necessitar l'aprovació dels serveis informàtics.

## Fes-ho amb seguretat

- Claude **pregunta abans d'enviar, esborrar o crear** res. Llegeix el que et proposa abans d'aprovar-ho. Encara millor: demana-li esborranys i envia'ls tu mateix.
- La teva bústia conté **dades personals d'altres persones**. Pregunta per fils o remitents concrets en lloc de "cerca a tot el meu correu", i no enganxis els resultats enlloc que sigui públic.
- Els correus poden contenir text escrit per manipular assistents d'IA. No deixis que Claude actuï automàticament segons instruccions que trobi dins d'un correu.
- Desconnecta els serveis que ja no facis servir: **Customize → Connectors → Disconnect**.

Consulta també [Dades i privadesa](../getting-started/data-and-privacy.md).
