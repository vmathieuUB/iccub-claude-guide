# Correu electrònic, calendari i documents

Amb els [connectors](connectors.md), Claude pot cercar al teu correu, llegir fitxers adjunts del teu Drive, consultar el teu calendari i redactar esborranys de respostes. És la configuració més útil per a la feina de gestió: viatges, reemborsaments, planificació de reunions, informes.

## Quin connector

| El teu compte | Connector | Què pot fer Claude |
|---|---|---|
| Gmail / compte de Google | **Gmail**, **Google Calendar**, **Google Drive** | Cercar i llegir correus, redactar, respondre i enviar (abans t'ho pregunta); veure, crear i modificar esdeveniments; trobar franges lliures; cercar i llegir fitxers del Drive |
| Microsoft 365 de la UB (Outlook, OneDrive, Teams) | **Microsoft 365** | Cercar al correu, al calendari, a OneDrive, a SharePoint i a Teams. Escriure (esborranys, esdeveniments) només si l'administrador ho ha habilitat |

!!! warning "Microsoft 365 necessita els serveis informàtics de la UB"
    El connector de Microsoft 365 només funciona un cop un administrador de Microsoft de l'organització l'ha aprovat una vegada. Si et diu que cal aprovació per al teu compte de la UB, posa't en contacte amb els serveis informàtics de la UB; mentrestant, fes servir el connector de Gmail amb un compte de Google, o reenvia els correus rellevants i puja els fitxers adjunts a mà.

## Connecta

1. En un xat, fes clic a **+** i després a **Connectors** (o ves a **Settings → Connectors**).
2. Fes clic a **Connect** al costat de Gmail, Google Calendar, Google Drive o Microsoft 365.
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

- *"He tornat del congrés de Lisboa. Troba al meu correu el rebut de la inscripció i les confirmacions del vol i de l'hotel, fes una llista dels imports i les dates, i redacta l'esborrany del correu de reemborsament per a l'administració del departament."* Consulta l'exemple complet: [Reemborsament d'un viatge a un congrés](../examples/admin/conference-reimbursement.md).

## Fes-ho amb seguretat

- Claude **pregunta abans d'enviar, esborrar o crear** res. Llegeix el que et proposa abans d'aprovar-ho. Encara millor: demana-li esborranys i envia'ls tu mateix.
- La teva bústia conté **dades personals d'altres persones**. Pregunta per fils o remitents concrets en lloc de "cerca a tot el meu correu", i no enganxis els resultats enlloc que sigui públic.
- Els correus poden contenir text escrit per manipular assistents d'IA. No deixis que Claude actuï automàticament segons instruccions que trobi dins d'un correu.
- Desconnecta els serveis que ja no facis servir: **Settings → Connectors → Disconnect**.

Consulta també [Dades i privadesa](../getting-started/data-and-privacy.md).
