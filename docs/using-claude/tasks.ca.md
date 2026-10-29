# Tasques llargues i programades

Claude ja no només respon preguntes. A la mateixa conversa li pots encarregar una feina més gran (un informe, un full de càlcul, una presentació, una taula bibliogràfica) i ell planifica els passos, els fa i et lliura fitxers acabats. Abans era un mode separat anomenat **Cowork**; des de setembre de 2026 forma part de tots els xats a Pro, i arriba de manera gradual.

!!! note "Ja el tens?"
    Si el quadre de missatge encara mostra les opcions **Chat** i **Cowork** per separat, el teu compte té la disposició antiga. Tot el que hi ha a continuació també funciona, al mode **Cowork**.

## Encarrega una tasca

Descriu el resultat que vols, el material que cal fer servir i com ha de ser un bon resultat, com ho faries amb un col·lega:

- *"A partir dels tres articles adjunts, fes una taula que compari les mostres, els mètodes i les restriccions sobre σ8, i després escriu un resum d'una pàgina per a la reunió del grup com a document Word."*
- *"Llegeix el CSV amb les notes de l'examen del semestre passat (anonimitzat), calcula la distribució per pregunta i fes cinc diapositives sobre quines preguntes han funcionat i quines no."*
- *"Repassa els PDF de la meva carpeta 'Referee guidelines' i fes un esborrany de llista de comprovació que pugui reutilitzar."*

És possible que Claude et faci primer algunes preguntes, i després treballarà uns minuts. Pots:

- **Seguir-lo, aturar-lo o redirigir-lo** en qualsevol moment.
- **Fer diverses tasques en paral·lel** en converses diferents.
- **Tancar el portàtil**: les tasques començades a la web o al mòbil continuen al núvol, i el resultat apareix a la conversa. Pots consultar el progrés i respondre preguntes des de l'aplicació mòbil.

Els resultats arriben com a fitxers de veritat: documents Word, fulls de càlcul amb fórmules que funcionen, presentacions compatibles amb PowerPoint, PDF o [Artifacts](artifacts.md) (Docs, Slides, Design).

## Fins a quin punt Claude treballa sol

El **control de permisos** del quadre de missatge decideix si Claude pregunta abans de cada pas:

| Opció | Què passa |
|---|---|
| **Auto** (predeterminada a Pro) | Claude avança sense preguntar a cada pas; abans de cada acció s'executen comprovacions de seguretat automàtiques. |
| **Manual** | Claude pregunta abans de cada acció. |

!!! tip "Recomanat mentre n'aprens"
    Canvia a **Manual** per a tot el que toqui el teu correu, el calendari, els teus fitxers o webs on tens la sessió iniciada. Llegeix què proposa Claude abans d'aprovar-ho.

## Fitxers del teu ordinador (aplicació d'escriptori) {#files-on-your-computer-desktop-app}

A l'**aplicació d'escriptori** pots donar a Claude accés a una carpeta perquè hi llegeixi, organitzi i creï fitxers. Configura-ho a **Settings** (busca **Storage folder** i **Trusted folders**). Per defecte, Claude pregunta abans d'esborrar res de manera permanent.

- Dona accés només a carpetes que compartiries de bon grat. No tota la carpeta personal, ni carpetes amb dades d'estudiants o material intern d'una col·laboració. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).
- Les carpetes locals, el navegador integrat i el computer use només funcionen mentre l'aplicació d'escriptori està oberta.
- **Computer use** (beta a Pro): Claude pot fer clic, escriure i moure's entre aplicacions de la teva pantalla. És potent però lent i arriscat; reserva'l per a tasques on no funciona res més.

## Tasques programades {#scheduled-tasks}

Demana a Claude que repeteixi una tasca periòdicament: *"Cada dilluns a les 8:00, resumeix els articles nous d'arXiv astro-ph.CO que parlin de lents febles i envia'm la llista per correu."* Les tasques programades s'executen al núvol, de manera que continuen encara que l'ordinador estigui apagat. Consulta l'exemple del [resum setmanal d'arXiv](../examples/research/weekly-arxiv-digest.md).

Cada execució gasta quota. Revisa de tant en tant les teves tasques programades i esborra les que ja no necessitis.

## Skills {#skills}

Una **skill** és un conjunt d'instruccions (i de vegades scripts) que ensenya a Claude com vols que faci un tipus de tasca. Claude la fa servir automàticament quan surt aquella tasca.

- Les **skills integrades** creen i editen fitxers Word, Excel, PowerPoint i PDF. Estan activades per defecte.
- **Les teves skills**: per exemple "com formato els fulls d'exercicis de la meva assignatura" o "la plantilla de l'ICCUB per anunciar seminaris". Demana a Claude, en un xat, que converteixi en skill una manera de treballar que acabeu de fer, o puja'n una.
- Gestiona-les a **Customize → Skills**. Les skills necessiten que **Create and edit files** (abans *Code execution and file creation*) estigui activat a **Settings → Capabilities**.
- Els **plugins** agrupen skills i connectors per a un perfil professional. Els trobaràs al directori de **Customize**. Instal·la només plugins i skills de fonts de confiança: contenen instruccions que Claude seguirà.

Compartir skills amb col·legues només és possible als plans Team. A Pro, comparteix el fitxer de la skill.

## Ús

Les tasques llargues gasten molta més quota que una pregunta ràpida. Consulta **Settings → Usage** i [Límits d'ús](../getting-started/what-is-claude.md#usage-limits).

## Limitacions actuals

- Els **xats d'incògnit** s'obren amb l'experiència antiga: Claude no hi pot crear fitxers ni executar codi.
- Les tasques antigues de Cowork són a **Recents**, però no surten a la cerca de xats.

Referència: [Claude Cowork and chat are one Claude](https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude) (centre d'ajuda d'Anthropic).
