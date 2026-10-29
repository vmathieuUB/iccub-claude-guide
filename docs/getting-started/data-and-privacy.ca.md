# Dades i privadesa

Què passa amb el que escrius i puges, i què no hauries de posar a Claude.

!!! info "No és assessorament jurídic"
    Aquesta pàgina resumeix les polítiques públiques d'Anthropic a octubre de 2026. Per a qualsevol cosa important, consulta l'[Anthropic Privacy Center](https://privacy.claude.com) i la normativa de protecció de dades de la UB.

## Què passa amb les teves dades

Claude Pro és un pla **de consum**. Les teves converses es regeixen per les [Consumer Terms](https://www.anthropic.com/legal/consumer-terms) (condicions de consum) i la [Privacy Policy](https://www.anthropic.com/legal/privacy) (política de privadesa) d'Anthropic, no per un contracte amb la UB.

**L'entrenament de models depèn de tu.** L'opció de **millora del model** (Settings → Privacy, amb l'etiqueta **Help Improve our AI models**) determina si les teves converses i sessions de Claude Code es poden fer servir per entrenar models futurs.

| Opció | S'utilitza per entrenar? | Quant de temps conserva Anthropic les teves converses |
|---|---|---|
| **Desactivada** (recomanat) | No | Les converses esborrades s'eliminen en un termini de 30 dies |
| **Activada** | Sí | Fins a 5 anys, de forma desidentificada |

Alguns detalls:

- Les **converses esborrades** no es fan servir per a futurs entrenaments, sigui quina sigui l'opció.
- Les **converses d'incògnit** (una opció en començar un xat nou) no es fan servir mai per entrenar i no apareixen a l'historial.
- La **valoració amb polze amunt / avall** envia tota aquella conversa a Anthropic, que la pot conservar fins a 5 anys i fer-la servir per entrenar, encara que tinguis l'opció desactivada. No valoris converses que continguin material sensible.
- Les **converses marcades per a revisió de seguretat** es poden conservar més temps (fins a 2 anys).
- Els **connectors** (Google Drive, Gmail, etc.) permeten que Claude llegeixi el que li indiquis en aquell xat. Aquest contingut passa a formar part de la conversa.
- Les **carpetes del teu ordinador** que obres a Claude a l'aplicació d'escriptori, a [Claude Code](../using-claude/claude-code.md) o a [Claude Science](../using-claude/science.md): el que Claude en llegeix s'envia a Anthropic com si fos un fitxer pujat.

## Memòria {#memory}

Claude conserva una **memòria** del context útil de les teves converses (el teu camp, les teves assignatures, com t'agraden les respostes), desada en temes separats. A Pro està activada per defecte.

- **Consulta-la i edita-la**: **Settings → Your Claude** i després **Manage** al costat de *Your memory*. Obre un tema per llegir-lo, editar-lo o esborrar-lo. També pots dir a Claude, en un xat, que recordi o oblidi alguna cosa.
- **Desactiva-la**: l'interruptor **Memory from chats**, al mateix lloc. Si la poses en pausa, es conserva el que hi ha desat; si la restableixes, s'esborra tot.
- **Un xat sense memòria**: fes clic a **+** i desactiva Memory abans del primer missatge, o fes servir un xat d'incògnit.
- Els **Projects** tenen la seva pròpia memòria. Per mantenir un Project del tot separat de la resta, desactiva **Use account memory** a la pàgina del Project.
- Els **temes sensibles** (salut, política, religió…) no es desen tret que activis **Include sensitive topics in memory**. Deixa-ho desactivat.
- **Cerca de xats**: Claude també pot buscar a les teves converses anteriors quan li és útil. Desactiva-ho amb **Search and reference chats** a **Settings → Your Claude**.

La memòria és pràctica, però també vol dir que una cosa d'un xat pot aparèixer en un altre. Desactiva-la en un xat sobre un tema confidencial.

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

1. **Desactiva la millora del model** a Settings → Privacy, tret que tinguis algun motiu per no fer-ho.
2. **Anonimitza** abans d'enganxar: substitueix els noms per *Estudiant A*, elimina adreces de correu i identificadors.
3. **Fes servir un xat d'incògnit** per a preguntes puntuals sobre alguna cosa sensible. No es desa ni a l'historial ni a la memòria.
4. **Esborra les converses** que ja no necessitis.
5. **Declara l'ús de la IA.** Moltes revistes et demanen que indiquis com s'ha fet servir la IA. Consulta [Consells i errors habituals](../tips/index.md).

## Quan convé fer servir un model local

Si les dades no poden sortir de cap manera de l'ICCUB, executa un model obert al teu propi ordinador o en un servidor de l'ICCUB. No s'envia res a cap empresa externa. Els models són menys potents que Claude, però sovint n'hi ha prou per resumir, canviar el format o ajudar amb el codi.

- [Executa un LLM local al teu portàtil](../examples/research/local-llm-laptop.md)
- [Comparteix un LLM local a través de la xarxa](../examples/research/local-llm-remote-access.md)

## Fonts

- [Es fan servir les meves dades per entrenar models?](https://privacy.claude.com/en/articles/10023580-is-my-data-used-for-model-training) (Anthropic Privacy Center)
- [Quant de temps es conserven les meves dades?](https://privacy.claude.com/en/articles/10023548-how-long-do-you-store-my-data) (Anthropic Privacy Center)
- [Cerca de xats i memòria](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context) (centre d'ajuda d'Anthropic)
- [Actualitzacions de les condicions de consum i de la política de privadesa](https://www.anthropic.com/news/updates-to-our-consumer-terms) (Anthropic, 2025)
