[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="scadenze"></a>Scadenze

**Azienda → Scadenze** è lo **scadenzario**: in un elenco solo le scadenze del personale, dei mezzi e delle attrezzature, delle manutenzioni degli impianti e quelle dell'azienda. Del personale in forza: la voce più recente di ogni corso, documento e visita con la sua scadenza, la **fine dei contratti a termine** e le voci **obbligatorie mancanti** (dal [catalogo](personale.md#personale-catalogo)). Dei [mezzi e delle attrezzature](mezzi.md) in uso o in riparazione: revisioni, bolli, assicurazioni, tagliandi e verifiche, anche a km. Delle [manutenzioni](manutenzioni.md) degli impianti in servizio: la prossima scadenza di ogni voce del piano e la fine dei contratti di manutenzione. Dei [preventivi](preventivi.md) aperti: il giorno in cui **risentire il cliente**. Delle [trattative](trattative.md) in corso: il **prossimo passo** con la sua data. Delle [pratiche](pratiche.md) in corso: i **passi da fare** con la scadenza e l'icona del tipo di pratica (un clic apre la pratica nel pannello, sopra lo scadenzario). Degli [ordini ai fornitori](acquisti.md#acquisti-solleciti): la conferma da sollecitare, il giorno per risentire il fornitore e la consegna prevista passata (con il permesso degli acquisti). Delle [fatture](vendite.md#vendite-incassi): le rate da incassare scadute o in scadenza entro una settimana (con il permesso delle vendite). Dell'azienda: certificazioni e attestazioni, polizze, contributi, contratti, autorizzazioni… Ciascuno vede quelle che i suoi permessi gli lasciano vedere: le scadenze del personale con **Vedere il personale** (documenti e visite solo con il loro permesso), quelle dei beni con **Vedere mezzi e attrezzature**, quelle delle manutenzioni con **Vedere le manutenzioni**, quelle dei preventivi con **Vedere i preventivi** (di un contatto privato solo il suo proprietario), quelle dell'azienda con **Vedere le scadenze dell'azienda**.

## <a id="scadenze-elenco"></a>Lo scadenzario

- **Da gestire**: le scadenze passate, quelle entro il preavviso e le voci mancanti, le più urgenti prima.
- **Tutte**: anche quelle lontane, in ordine di data.
- **Dell'azienda**: le scadenze dell'azienda, anche quelle chiuse, con la data, ogni quanto si ripetono, lo stato e l'ultima volta che sono state fatte.

Sotto le linguette si sceglie **Tutte**, solo il **Personale**, solo **Mezzi e attrezzature**, solo le **Manutenzioni**, solo **Preventivi e trattative**, solo l'**Azienda** e gli altri gruppi che vedi (Acquisti, Incassi, Pagamenti e, per gli amministratori, la **Privacy**: richieste degli interessati aperte e violazioni da notificare al Garante); la ricerca e l'elenco delle categorie restringono ancora. Ogni riga ha la data con quanto manca (o da quanto è passata; per una scadenza a km i km e quanti ne mancano), che cosa scade con la sua categoria, a chi o a che cosa si riferisce (per un bene, anche a chi è consegnato) e lo stato: **Scaduta**, **Mancante**, **In scadenza**, **In regola**. Un clic apre la [scheda della persona](personale.md#personale-scheda) alla linguetta giusta, la [scheda del bene](mezzi.md#mezzi-scadenze) alle sue scadenze, la manutenzione (nella pagina Manutenzioni) oppure la scadenza dell'azienda; dal menu della riga di un bene, **Segna come fatta**, e di una manutenzione, **Registra il rapporto**. Un preventivo da risentire è **in scadenza** il giorno prima e il giorno stesso, **scaduto** dopo: un clic apre il preventivo, e dal menu della riga **Cliente sentito…** (per chi compila i preventivi) registra il contatto e sposta il giorno; un preventivo accettato, rifiutato o annullato esce dallo scadenzario. Il promemoria nella campanella arriva al **commerciale** del preventivo (senza, a chi gestisce i preventivi). **Stampa** stampa l'elenco come lo stai guardando.

## <a id="scadenze-azienda"></a>Le scadenze dell'azienda

**Nuova scadenza**, per chi può **Gestire le scadenze dell'azienda**: che cosa scade (per esempio *Certificazione UNI EN ISO 9001 – sorveglianza annuale*, *Attestazione SOA – verifica triennale*, *DURC*, *Polizza RC*), la categoria, l'azienda del gruppo, la data, **ogni quanto si ripete** (una volta sola, ogni mese, 3, 4 o 6 mesi, ogni anno, 2, 3 o 5 anni, oppure un numero di mesi a scelta), il preavviso in giorni e le note.

- **Fatta**, con la data e una nota (per esempio il numero della nuova polizza): una scadenza che si ripete passa da sola alla **successiva** (la data più il periodo, fino a superare il giorno in cui è stata fatta); una che non si ripete si **chiude** e resta nella linguetta Dell'azienda, con **Riapri**.
- Lo **storico** della scadenza ricorda quando è stata creata, cambiata e fatta, da chi e con quale nota.

## <a id="scadenze-da-testo"></a>Una scadenza da un testo

Dalla 1.123.0, con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (in alto nella pagina Scadenze, per chi gestisce le scadenze dell'azienda) apre un pannello dove incollare la **polizza**, il **certificato**, il **contratto** o l'**avviso** di un ente (anche da un PDF o da una scansione, con **Da un file**). L'assistente propone che cosa scade, la categoria, la **data**, ogni quanto si **ripete** (ogni anno per un tacito rinnovo annuale), il **preavviso** se il testo lo dice (per esempio la disdetta 60 giorni prima) e le note (numero della polizza, ente, importo). Si apre la scadenza nuova già compilata, da controllare e salvare.

## <a id="scadenze-promemoria"></a>I promemoria

Ogni scadenza manda una [notifica](notifiche.md) quando **entra nel preavviso** e una quando **passa** senza essere rinnovata, una volta sola per data (o per km), dalle 7 del mattino; come le altre notifiche arrivano anche per email a chi le vuole. Le ricevono chi può **Gestire il personale** (per documenti e visite serve anche **Documenti personali e visite mediche**), chi può **Gestire mezzi e attrezzature** (e la persona che ha il bene in consegna, se ha la scheda collegata a un utente), chi può **Gestire le manutenzioni** (quelle dei contatti privati solo il proprietario e gli amministratori) e chi può **Gestire le scadenze dell'azienda**. Le voci mancanti non mandano notifiche: compaiono nello scadenzario e nelle schede. Si possono disattivare dalle [preferenze delle notifiche](notifiche.md#notifiche-preferenze).

## <a id="scadenze-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere le scadenze dell'azienda | Lo scadenzario con le scadenze dell'azienda. |
| Gestire le scadenze dell'azienda | Aggiungerle, modificarle, eliminarle, segnarle come fatte e riaprirle; ricevere i loro promemoria. |

Le scadenze del personale seguono i [permessi del personale](personale.md#personale-permessi), quelle dei mezzi e delle attrezzature i [loro permessi](mezzi.md#mezzi-permessi), quelle delle manutenzioni i [permessi delle manutenzioni](manutenzioni.md#manutenzioni-permessi).

---

[← Contabilità](contabilita.md) · [Indice](README.md) · [Documenti →](documenti.md)
