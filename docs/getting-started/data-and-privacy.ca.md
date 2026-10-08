# Dades i privadesa

Què passa amb el que escrius i puges, i què no hauries de posar a Claude.

!!! info "No és assessorament jurídic"
    Aquesta pàgina resumeix les polítiques públiques d'Anthropic a octubre de 2026. Per a qualsevol cosa important, consulta l'[Anthropic Privacy Center](https://privacy.claude.com) i la normativa de protecció de dades de la UB.

## Què passa amb les teves dades

Claude Pro és un pla **de consum**. Les teves converses es regeixen per les [Consumer Terms](https://www.anthropic.com/legal/consumer-terms) (condicions de consum) i la [Privacy Policy](https://www.anthropic.com/legal/privacy) (política de privadesa) d'Anthropic, no per un contracte amb la UB.

**L'entrenament de models depèn de tu.** L'opció **Help improve Claude** (Settings → Privacy) determina si les teves converses i sessions de Claude Code es poden fer servir per entrenar models futurs.

| Opció | S'utilitza per entrenar? | Quant de temps conserva Anthropic les teves converses |
|---|---|---|
| **Desactivada** (recomanat) | No | Fins a 30 dies després que les esborris |
| **Activada** | Sí | Fins a 5 anys |

Alguns detalls:

- Les **converses esborrades** no es fan servir per a futurs entrenaments, sigui quina sigui l'opció.
- Les **converses d'incògnit** (una opció en començar un xat nou) no es fan servir mai per entrenar i no apareixen a l'historial.
- La **valoració amb polze amunt / avall** envia tota aquella conversa a Anthropic, que la pot conservar fins a 5 anys i fer-la servir per entrenar, encara que tinguis l'opció desactivada. No valoris converses que continguin material sensible.
- Les **converses marcades per a revisió de seguretat** es poden conservar més temps.
- Els **connectors** (Google Drive, Gmail, etc.) permeten que Claude llegeixi el que li indiquis en aquell xat. Aquest contingut passa a formar part de la conversa.

## Què pots compartir

Una regla senzilla: **puja només allò que t'estaria bé enviar per correu a un col·lega de fora de la UB.** Després, fes servir la taula següent.

| Material | D'acord? | Notes |
|---|---|---|
| Articles publicats, dades públiques, llibres de text | Sí | |
| El teu propi codi i els teus scripts d'anàlisi | Sí | Elimina-hi abans contrasenyes, tokens i claus d'API. |
| Els teus esborranys i resultats no publicats | Normalment | Amb l'entrenament desactivat. Comprova que no estiguis subjecte a cap embargament. |
| Dades i documents interns de col·laboracions (Gaia, LSST, Euclid, LHCb, CTA…) | **Comprova-ho primer** | Moltes col·laboracions tenen les seves pròpies normes sobre IA o sobre compartir dades. Si tens dubtes, pregunta a la col·laboració. |
| Informes de revisió i articles que estàs revisant | **No** | La majoria de revistes prohibeixen pujar manuscrits en revisió. |
| Propostes de projectes que estàs avaluant | **No** | L'avaluació és confidencial; consulta les normes del finançador. |
| Treballs d'estudiants, notes, correus amb noms | **No**, tret que estiguin anonimitzats | Les dades personals estan subjectes al RGPD. Elimina-hi noms i identificadors. |
| Dades personals de qualsevol persona (CV, salut, RH) | **No** | |
| Contrasenyes, claus SSH, tokens d'API | **Mai** | |

## Bons hàbits

1. **Desactiva l'entrenament** a Settings → Privacy, tret que tinguis algun motiu per no fer-ho.
2. **Anonimitza** abans d'enganxar: substitueix els noms per *Estudiant A*, elimina adreces de correu i identificadors.
3. **Fes servir un xat d'incògnit** per a preguntes puntuals sobre alguna cosa sensible.
4. **Esborra les converses** que ja no necessitis.
5. **Declara l'ús de la IA.** Moltes revistes et demanen que indiquis com s'ha fet servir la IA. Consulta [Consells i errors habituals](../tips/index.md).

## Quan convé fer servir un model local

Si les dades no poden sortir de cap manera de l'ICCUB, executa un model obert al teu propi ordinador o en un servidor de l'ICCUB. No s'envia res a cap empresa externa. Els models són menys potents que Claude, però sovint n'hi ha prou per resumir, canviar el format o ajudar amb el codi.

- [Executa un LLM local al teu portàtil](../examples/research/local-llm-laptop.md)
- [Comparteix un LLM local a través de la xarxa](../examples/research/local-llm-remote-access.md)

## Fonts

- [Es fan servir les meves dades per entrenar models?](https://privacy.claude.com/en/articles/10023580-is-my-data-used-for-model-training) (Anthropic Privacy Center)
- [Actualitzacions de les condicions de consum i de la política de privadesa](https://www.anthropic.com/news/updates-to-our-consumer-terms) (Anthropic, 2025)
