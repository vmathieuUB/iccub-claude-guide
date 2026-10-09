# Connectors

Els Connectors (connectors) permeten que Claude llegeixi (i de vegades actuï en) altres serveis que fas servir: Google Drive, Gmail, Google Calendar, Microsoft 365, GitHub, Notion i d'altres.

## Quan són útils

- *"Troba l'última versió de la proposta ERC al meu Drive i fes una llista del que encara hi falta."*
- *"Quines reunions tinc la setmana que ve, i quines coincideixen amb les meves classes?"*
- *"Resumeix les issues obertes del repositori de GitHub del nostre pipeline."*
- *"Troba el correu de la revista sobre el termini de la meva revisió."*

Sense connectors, hauries de descarregar i pujar cada fitxer tu mateix.

## Connecta un servei

1. Obre **Settings → Connectors** (també hi pots accedir des de **+** en un xat).
2. Busca el servei i fes clic a **Connect**.
3. Inicia la sessió en aquest servei i aprova l'accés que et demana.

Fes servir el teu **compte de la UB** per als serveis de Google o Microsoft de la UB, perquè Claude vegi els fitxers de feina i no els personals (o al revés, si és el que vols).

En un xat, obre **+** per activar o desactivar connectors concrets. Deixa activats només els que necessiti aquell xat.

## Què pot veure Claude

- Claude pot accedir a tot allò a què pot accedir **el teu compte** en aquell servei, però només llegeix el que és rellevant per a la teva petició.
- El que llegeix passa a formar part d'aquell xat, amb les mateixes normes que un fitxer que hagis pujat. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).
- Alguns connectors també poden **actuar**: crear un esdeveniment al calendari, redactar un esborrany de correu. Claude et demana confirmació abans de fer-ho. Llegeix la confirmació abans d'aprovar-la.

!!! warning
    Connectar el teu correu o el teu Drive de la UB dona a Claude accés a tot el que hi ha, incloses dades d'altres persones. Indica-li fitxers o carpetes concrets, i desconnecta els serveis que ja no facis servir (Settings → Connectors → **Disconnect**).

## Més informació

- [Correu electrònic, calendari i documents](email-calendar.md): Gmail, Google Calendar, Drive i Microsoft 365 en detall.
- [Claude in Chrome](chrome.md): per a llocs web que no tenen connector.

## Consells

- Concreta on ha de buscar: *"a la carpeta 'Docència 2026'"* és més ràpid i més segur que *"al meu Drive"*.
- Combina'ls amb [Research](research.md): Claude pot cercar al web i al teu Drive en una mateixa investigació.
- Per a GitHub, el connector permet que Claude llegeixi repositoris. Perquè Claude canviï codi, fes servir [Claude Code](claude-code.md).
