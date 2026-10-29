# Claude Science

**Claude Science** és l'aplicació d'escriptori d'Anthropic per a la recerca científica, en **beta** des de juny de 2026 i inclosa a Pro. Descrius una anàlisi amb paraules; Claude escriu i executa el codi en un entorn aïllat (sandbox), llegeix les carpetes que li dones, es pot connectar a bases de dades científiques i als teus propis recursos de càlcul, i desa cada resultat amb un registre de com s'ha obtingut.

!!! note "De moment, pensat sobretot per a les ciències de la vida"
    Les skills i els connectors de bases de dades que inclou estan orientats a la biologia i la química (genòmica, proteïnes, PubMed…). Encara no hi ha res específic per a física o astronomia, com ara eines que coneguin ADS o astropy. Per a la majoria de la feina de l'ICCUB, [Claude Code](claude-code.md) al terminal o a [VS Code](vs-code.md) és l'opció més madura. Val la pena provar Claude Science si vols els seus registres de procedència o l'enviament de feines a un clúster.

## Instal·lació

1. Descarrega-la de la [pàgina de Claude Science](https://claude.com/product/claude-science). Funciona a macOS 13 o posterior, Windows 11 (x64) i Linux x64.
2. Inicia la sessió amb el teu compte de Claude Pro.

Si formes part del **pla Team per a científics** d'un grup, ja està activada per defecte. En altres plans Team, l'activa qui administra el pla.

## Què fa

- **Fa anàlisis de cap a cap**: escriu i executa Python en un sandbox, sobre els fitxers d'una carpeta que li dones.
- **Conserva la procedència**: cada figura o taula es desa amb el seu codi, l'entorn i la conversa, perquè tu (o un revisor) la puguis reproduir més endavant, i hi puguis demanar canvis amb paraules.
- **Fa servir els teus recursos de càlcul**: prepara un pla, pregunta abans de fer servir recursos nous i pot enviar feines a un clúster HPC per SSH.
- **Revisa la seva pròpia feina**: un agent revisor comprova les referències i els càlculs i n'assenyala els errors. Comprova-ho igualment tu.
- **Bifurca una sessió** perquè puguis comparar dues estratègies.

## Idees per a l'ICCUB

- *"Carrega les corbes de llum de `data/`, ajusta un damped random walk a cadascuna i fes una taula amb les escales de temps òptimes i les seves incerteses."*
- *"Reprodueix la figura 3 de l'article adjunt a partir del catàleg públic i digues-me en què difereix del nostre resultat."*
- *"Prepara i envia al nostre clúster un job array que executi `run_mcmc.py` per a cadascun dels 20 fitxers de paràmetres, i després recull les cadenes quan acabin."*

## Mantén-ne el control

- Fes-la treballar sobre una **còpia** de les teves dades, o sobre una carpeta que puguis compartir. Les dades es queden al teu ordinador o al clúster, però les parts necessàries per a cada pas s'envien a Claude. Consulta [Dades i privadesa](../getting-started/data-and-privacy.md).
- Llegeix el pla abans que faci servir temps de clúster.
- És una beta: espera-hi imperfeccions i comprova els resultats com ho faries amb la primera anàlisi d'un estudiant.

Referència: [Get started with Claude Science](https://support.claude.com/en/articles/16563838-get-started-with-claude-science) (centre d'ajuda d'Anthropic).
