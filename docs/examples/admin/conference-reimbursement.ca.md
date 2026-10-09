---
tags:
  - Gestió
  - Connectors
  - Correu electrònic
---

# Reemborsament d'un viatge a un congrés a partir del correu electrònic

!!! info "Exemple il·lustratiu"
    Aquest exemple l'han escrit els editors del lloc per mostrar el flux de treball. Encara no és una experiència real de l'ICCUB. Si el proves, [envia'ns la teva versió](../../contribute/index.md) i el substituirem.

| Sobre aquest exemple | |
| --- | --- |
| **Autor/a** | Editors de la Guia de Claude de l'ICCUB |
| **Data** | 2026-10-06 |
| **Àrea** | Gestió |
| **Eines utilitzades** | Connectors de Gmail i Google Drive (o Microsoft 365), Claude in Chrome (opcional) |
| **Temps estalviat** | Aproximadament una hora per viatge (estimació) |

## Objectiu

En tornar d'un congrés, reunir tot el que cal per al reemborsament del viatge: el rebut de la inscripció, els vols, l'hotel, el transport local i les dates per a les dietes. Després, omplir el full de despeses del departament i redactar el correu per a l'administració, sense haver de remenar desenes de correus.

## Què vaig fer

1. **Vaig connectar la bústia** una sola vegada (consulta [Correu electrònic, calendari i documents](../../using-claude/email-calendar.md)) i vaig activar els connectors de correu i de Drive en un xat nou.

2. **Vaig reunir els documents:**

    > *Vaig assistir a un congrés a Lisboa del 29 de juny al 3 de juliol de 2026. Cerca al meu correu el rebut de la inscripció, les reserves de vols, la confirmació de l'hotel i qualsevol altre pagament relacionat amb aquest viatge. Fes una taula: data, concepte, proveïdor, import, moneda, mètode de pagament i un enllaç al correu. Assenyala tot el que falti.*

    Va trobar cinc conceptes i va assenyalar que la factura de l'hotel era una confirmació de reserva, no una factura.

3. **Vaig omplir el formulari.** Vaig pujar la plantilla de despeses del departament (Excel) i la llista de normes:

    > *Omple aquest full de despeses amb els conceptes de la taula. Aplica les normes de dietes del document adjunt per als dies de viatge. Converteix els imports que no siguin en euros amb el tipus de canvi de la data del pagament i indica quin tipus has fet servir.*

4. **Vaig redactar el correu:**

    > *Redacta un correu en català per a l'administració del departament, adjuntant-hi el full omplert, amb la llista dels rebuts, i preguntant quin és el procediment per a la factura de l'hotel que falta. No l'enviïs.*

5. **Ho vaig comprovar tot** amb els rebuts, vaig descarregar els adjunts i vaig enviar el correu jo mateix.

6. *(Opcional)* Per a la factura de l'hotel, vaig fer servir [Claude in Chrome](../../using-claude/chrome.md) per iniciar sessió al web de reserves de l'hotel i trobar la pàgina de descàrrega de la factura. Vaig fer clic a "descarregar" jo mateix.

## Resultat

Tots els rebuts trobats, un full de despeses omplert i un esborrany de correu, en uns 15 minuts en lloc d'una hora i mitja. Un document que faltava es va detectar abans de fer la sol·licitud i no després.

## Què cal vigilar

- **Imports i dates**: comprova cada xifra amb els rebuts. Estem parlant de diners.
- **Rebuts o confirmacions**: l'administració normalment necessita factures. Demana a Claude que assenyali la diferència.
- **Adjunts**: els connectors poden llegir adjunts, però és possible que les eines d'escriptura no puguin adjuntar fitxers als correus. Adjunta'ls tu mateix.
- **No el deixis enviar.** Demana-li esborranys.
- **Dades personals**: la teva bústia conté dades d'altres persones. Limita la cerca al viatge en qüestió.
- **Les normes de la UB canvien**: dona-li el document de normes vigent en lloc de refiar-te del que "sap".
