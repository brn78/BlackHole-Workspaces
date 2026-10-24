[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="pratiche"></a>Pratiche

**Progettazione → Pratiche** (dalla 1.121.0) segue le **pratiche con gli enti** che accompagnano un impianto: la connessione alla rete, Terna Gaudì, il GSE, l'ENEA, il Comune, le Dogane, la wallbox. Ogni pratica ha i suoi **passi**, ognuno con la sua **scadenza**: i passi da fare vanno nello [scadenzario](scadenze.md) (anche nel calendario del telefono di chi lo abbona) e chi segue la pratica riceve il promemoria. La pagina compare a chi vede gli impianti; le pratiche si compilano con *Modificare gli impianti*, si eliminano con *Eliminare gli impianti* e i tipi si gestiscono con *Gestire i tipi di impianto*.

Le linguette: **In corso** (con la scadenza più vicina, rossa se passata, gialla se vicina, e **Fatto** per segnare in un clic il prossimo passo), **Chiuse** e **Tutte**; i **tipi di pratica** (con quelli proposti) stanno in **⋯ Altro → Tipi di pratica**, nel pannello a destra. Si filtra per tipo e con *Solo quelle che seguo io*. In alto: le pratiche in corso, i passi scaduti, quelli in scadenza e le concluse dell'anno.

## <a id="pratiche-tipi"></a>I tipi di pratica

- Un'installazione nuova non ha tipi: **Tipi proposti** aggiunge quelli che fai, pronti da adattare: *Connessione alla rete (TICA)*, *Modello unico (piccoli impianti)*, *Terna Gaudì*, *GSE: ritiro dedicato*, *GSE: comunità energetica o autoconsumo*, *ENEA: detrazioni fiscali*, *Dogane: officina elettrica*, *Comune: titolo edilizio*, *Wallbox: potenza e incentivi*. I giorni dei passi proposti sono **indicativi**: i termini veri sono quelli dell'ente e cambiano con le regole, quindi controllali e correggili.
- Un tipo ha il nome, l'**ente**, l'icona e il colore, la descrizione, il **preavviso** (quanti giorni prima arriva il promemoria), i **tipi d'impianto** per cui si propone (per esempio Fotovoltaico: connessione, Gaudì, GSE, ENEA) e **per quali clienti** (dalla 1.125.0): tutti, le **persone fisiche e i condomini** (l'ENEA delle detrazioni, così è proposta) oppure le **aziende**. In «Avvia le pratiche» un tipo che non vale per quel cliente resta nell'elenco non spuntato, con il perché: si può sempre spuntare a mano. Un condominio si riconosce dalla forma giuridica *Condominio* o dal nome che comincia con «Condominio».
- I **passi**, in ordine: che cosa va fatto, entro quanti **giorni** e **da quando**: dall'avvio della pratica, dal passo prima (quando è fatto), dalla fine dei lavori, dall'entrata in esercizio, oppure senza scadenza (da spuntare e basta). Il suggerimento sotto il passo ricorda documenti, portali, termini da controllare.
- Cambiare un tipo vale per le pratiche nuove: quelle già aperte tengono i loro passi. Un tipo usato non si elimina: si **archivia** e non si propone più.

## <a id="pratiche-scheda"></a>La pratica

- **Nuova pratica**: il tipo (con l'anteprima dei passi), il **cliente**, l'**impianto** (la sua data di installazione si propone come fine dei lavori), il titolo se servono più pratiche dello stesso tipo, il **codice dell'ente** (codice di rintracciabilità, CENSIMP, numero della pratica GSE o ENEA, protocollo del Comune: si trova anche con la ricerca), **chi la segue**, le date e le note.
- Più comodo dalla pagina dell'impianto, linguetta **Pratiche**: **Avvia le pratiche** le crea tutte insieme, con già spuntate quelle proposte per il suo tipo.
- Fatti tutti i passi, la pratica è **conclusa** da sola. **Esito…** la chiude a mano: conclusa, **respinta** dall'ente o **annullata**, con una nota. **Riapri** la rimette in corso. Eliminata, va nel [cestino](cestino.md) con i passi e lo storico.
- Lo **storico** tiene ogni modifica, ogni passo fatto o rifatto, con chi e quando.

## <a id="pratiche-da-testo"></a>Una pratica da un testo

Dalla 1.123.0, con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (in alto nella pagina Pratiche, quando ci sono i tipi) apre un pannello dove incollare l'**email** o la **ricevuta** dell'ente (gestore di rete, Terna, GSE, ENEA, Comune, Dogane) o del cliente. L'assistente sceglie il **tipo di pratica** tra i vostri, propone il **codice dell'ente** (rintracciabilità, CENSIMP, numero della pratica, protocollo), le date di avvio, fine dei lavori ed entrata in esercizio e le **note** (POD, potenza, documenti chiesti). Con **Da un file** il testo si legge anche da un PDF o da una scansione. **Proponi i dati** chiede all'assistente i dati e la piattaforma cerca il **cliente** tra quelli che vedi (partita IVA, email anche dei referenti, telefono, nome, poi un nome simile da controllare) e, con il cliente, il suo **impianto** dalle parole del testo. Si apre la scheda nuova **già compilata**, con in cima la nota dell'assistente: controlla, correggi e salva come sempre. Niente si salva da solo e il testo non si conserva. Se il cliente non è in anagrafica, la nota lo dice: lo scegli tu.

## <a id="pratiche-passi"></a>I passi e le scadenze

- Le scadenze si calcolano dalle date della pratica: l'**avvio**, la **fine dei lavori** e l'**entrata in esercizio** (il giorno dell'attivazione). Finché una data manca, i passi che ne dipendono aspettano (); così i passi «dal passo prima», finché quello prima non è fatto.
- **Fatto** segna il passo oggi, dopo un avviso che dice che cosa succede (il passo esce dallo scadenzario; se è l'ultimo, la pratica si conclude) e chiede conferma; lo stesso da **Fatto oggi** nell'elenco e nello scadenzario. Dal menu ⋯ anche **in un altro giorno, con una nota** (il protocollo, il codice ricevuto), **Modifica il passo** (titolo, giorni, una **scadenza scritta a mano** quando l'ente dà un termine preciso, vuota per tornare a quella calcolata), sposta su o giù, togli. lo rimette da fare (una pratica conclusa torna in corso).
- Ogni passo si vede fatto, scaduto (in rosso, con i giorni di ritardo), in scadenza (entro il preavviso), da fare o in attesa. **Aggiungi un passo** ne mette uno solo in questa pratica.
- Nello [scadenzario](scadenze.md) le pratiche hanno il loro filtro; dal menu della riga **Fatto oggi**. Il promemoria va a chi segue la pratica; se non la segue nessuno, a chi modifica gli impianti (le pratiche dei clienti privati solo al proprietario).

---

[← Manutenzioni](manutenzioni.md) · [Indice](README.md) · [Assistenza →](assistenza.md)
