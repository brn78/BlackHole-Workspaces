[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="acquisti"></a>Ordini fornitori

**Magazzino → Ordini fornitori** segue tutto quello che si compra dai fornitori: le **richieste d'offerta** per confrontare i prezzi, gli **ordini**, la loro conferma, i **solleciti**, l'**arrivo della merce** (anche a più riprese) e il **controllo dei prezzi d'acquisto**. Le linguette sono Ordini, Richieste d'offerta, Da ricevere, Prezzi da verificare e Fornitori; in alto **Nuovo ordine**, **Richiesta d'offerta**, **Arrivo merce**, **Impostazioni** e **Stampa**. I prezzi d'acquisto sono dati riservati: li vede chi ha il permesso degli acquisti.

## <a id="acquisti-ordini"></a>Gli ordini

**Nuovo ordine** apre il pannello a destra: il **fornitore** (dall'anagrafica; l'email per l'ordine è la prima della sua scheda e si può cambiare), la data, la **consegna richiesta**, l'oggetto, il magazzino dove arriva la merce, la commessa e, più sotto, consegna, pagamento e note per il fornitore (proposti dalle impostazioni) e le note interne. Le righe si aggiungono cercando nel listino (anche per codice del fornitore o leggendo uno o più codici a barre), come **riga libera** (una descrizione senza voce del listino) o come **testo**. Il prezzo proposto per quel fornitore è, nell'ordine: l'ultimo pagato a lui, l'ultimo ordinato a lui, il suo listino (METEL) con lo sconto della famiglia, il listino della voce, il costo; accanto c'è da dove viene. Lo sconto si scrive anche in cascata (50+10).

Salvato, l'ordine è in **bozza**; poi **Invia**: per email (con la posta configurata) o segnato come stampato, telefonato o mandato in altro modo. L'email parte **a nome di chi la manda**: il suo nome come mittente, il suo indirizzo (se è dello stesso dominio della posta dell'azienda, anche come indirizzo del mittente), le risposte del fornitore vanno a lui e ne riceve una copia; per questo serve la propria email nel profilo. L'email contiene le righe con i prezzi, il totale imponibile, la consegna e il pagamento; **Stampa** apre l'anteprima dei fogli con il [modello di stampa](modelli-stampa.md) degli acquisti (si possono scegliere un altro modello e i colori) e da lì la stampa del browser, anche in PDF. Gli stati: **Bozza**, **Inviato**, **Confermato**, **Arrivato in parte**, **Arrivato**, **Chiuso** (con un residuo che non arriverà) e **Annullato**. Nel menu **Azioni** ci sono anche **Duplica**, **Storico** (chi ha fatto che cosa) ed **Elimina** (una bozza; un ordine inviato solo chi gestisce gli acquisti, e mai se è arrivata della merce).

## <a id="acquisti-solleciti"></a>Conferme, ritardi e solleciti

Quando il fornitore conferma, **Confermato** registra la data, il numero della sua conferma e la **consegna prevista**. Un ordine inviato e non confermato dopo i giorni delle impostazioni risulta **da confermare**; uno con la consegna prevista passata e merce ancora da arrivare **in ritardo**, con i giorni. **Sollecita** manda al fornitore un'email con le righe ancora da consegnare (o la conferma che manca), oppure registra una telefonata o una nota, e fissa quando risentirlo. Gli ordini da confermare, da risentire o in ritardo compaiono nello [scadenzario](scadenze.md) e nei promemoria di chi gestisce gli acquisti, con i filtri della linguetta Ordini.

## <a id="acquisti-arrivi"></a>L'arrivo della merce

La merce arriva con un **carico da fornitore** del [magazzino](magazzino.md) legato alle righe dell'ordine: **Arrivo merce** (dall'ordine o dalla pagina, scegliendo il fornitore e le righe arrivate, anche di più ordini) apre il carico già compilato con le quantità mancanti e i prezzi dell'ordine. Si correggono le quantità arrivate, si scrivono il DDT del fornitore e le matricole; accanto al costo c'è il prezzo ordinato, e una differenza si vede subito. Registrato il carico, l'ordine si aggiorna da solo: arrivato in parte o arrivato. La linguetta **Da ricevere** elenca le righe ancora attese, le più vecchie prima. Per le prestazioni (trasporti, lavorazioni) e il materiale consegnato direttamente in cantiere c'è **Arrivato senza magazzino**; per quello che non arriverà più, **Chiudi il residuo** (con il motivo). Una riga già arrivata non si toglie e la sua quantità non scende sotto quella arrivata.

Dalla 1.103.0, con l'assistente attivo, **Arrivo merce** ha anche **Da un documento**: dalla scansione o dal PDF del DDT del fornitore l'assistente legge le righe e le abbina alle righe degli ordini aperti, come il [carico da un documento](magazzino.md#magazzino-da-documento) del magazzino.

## <a id="acquisti-rdo"></a>Richieste d'offerta

**Richiesta d'offerta** prepara la stessa richiesta per uno o più fornitori (le righe con le quantità, senza prezzi) con la data entro cui si vuole la risposta. **Invia** la manda per email a ognuno (o la segna inviata). Quando rispondono, **Risposte** registra per ogni fornitore prezzo, sconto e giorni di consegna di ogni riga. **Confronta e ordina** mette le offerte una accanto all'altra con il prezzo netto, propone per ogni riga il più basso e mostra il totale di ogni fornitore; si sceglie da chi comprare riga per riga (o di non ordinarla) e **Crea gli ordini** prepara un ordine in bozza per ogni fornitore scelto, con i suoi prezzi e la consegna offerta.

Dalla 1.103.0, con l'assistente attivo, nelle **Risposte** c'è **Dall'offerta (PDF o scansione)**: scegli il file dell'offerta del fornitore e l'assistente mette, per ogni riga della richiesta, prezzo, sconto e giorni di consegna (abbinando per codice, poi per descrizione), più numero e data dell'offerta; le righe compilate si colorano. Un articolo equivalente proposto al posto di quello chiesto, o una confezione diversa, va nelle note della risposta. Controlla e **Salva la risposta**: niente si salva da solo.

## <a id="acquisti-proposte"></a>Ordini proposti: scorte e preventivi

- Dal [magazzino](magazzino.md#magazzino-riordino), **Da riordinare → Crea gli ordini** prepara un ordine in bozza per ogni fornitore (quello della voce, altrimenti quello dell'ultimo acquisto) con le quantità proposte; le voci senza fornitore si saltano e vengono elencate.
- Da un [preventivo](preventivi.md) inviato o accettato, nel menu **⋯**, **Ordina il materiale** elenca il materiale del listino del preventivo con quanto c'è in magazzino e quanto è già ordinato per quel preventivo, propone solo quello che manca (o tutto) e crea gli ordini, legati al preventivo e alla sua commessa.

## <a id="acquisti-prezzi"></a>Prezzi da verificare

La linguetta **Prezzi da verificare** controlla i carichi da fornitore del periodo scelto e segnala quelli con un prezzo da guardare: **più caro dell'ordine**, **aumentato** rispetto all'acquisto precedente dallo stesso fornitore oltre la soglia delle impostazioni, **sopra il listino del fornitore** con lo sconto della sua famiglia (per le voci legate a un listino METEL), oppure pagato più di quanto lo ha fatto pagare **un altro fornitore** negli ultimi sei mesi. Per ognuno il motivo, il riferimento e la differenza in percentuale; un clic apre il carico. Chi gestisce gli acquisti lo segna **Verificato** con una nota (per esempio «aumento concordato»): sparisce dall'elenco, ma si ritrova con **Anche i verificati**. Già nel carico, accanto al costo scritto, si vede la differenza con l'ordine o con l'ultimo acquisto.

## <a id="acquisti-fornitori"></a>Fornitori

La linguetta **Fornitori** riassume come lavora ogni fornitore nel periodo: ordini e valore ordinato, ordini aperti e in ritardo, acquistato con i carichi, **puntualità** (le righe arrivate del tutto entro la consegna prevista), **ritardo medio**, solleciti e prezzi da verificare.

## <a id="acquisti-importa"></a>Importare ed esportare

**Esporta** scarica gli ordini (dalla linguetta Ordini) o le richieste d'offerta (dalla loro linguetta) in **Excel** o **CSV**, con una riga per ogni riga del documento: numero, data, fornitore, oggetto, riferimento del fornitore, consegna prevista, pagamento, resa e note, poi codice, codice del fornitore, descrizione, unità di misura, quantità, prezzo, sconto (anche in cascata, *50+10*), IVA, consegna e note della riga. **Importa** li porta da un foglio fatto così: le righe con lo stesso numero fanno un documento. Il fornitore deve essere in anagrafica (per le richieste d'offerta si può lasciare vuoto). I documenti si importano **in bozza**, con il numero della piattaforma (quello del file va nelle note): si controllano e si mandano come gli altri. Una riga con il **codice di una voce del listino** (o il suo codice del fornitore) si collega alla voce, così all'arrivo la merce entra in magazzino. Vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export).

## <a id="acquisti-impostazioni"></a>Impostazioni e permessi

Le **Impostazioni** (chi gestisce gli acquisti) fissano dopo quanti giorni un ordine è da confermare, ogni quanti giorni risentire il fornitore, la soglia dei prezzi da verificare e i testi proposti: messaggio dell'ordine e della richiesta d'offerta, pagamento, consegna e note.

| Vedere gli acquisti | Riservato: ordini e richieste d'offerta con i prezzi d'acquisto, la merce da ricevere, i prezzi da verificare e l'andamento dei fornitori; vede anche i costi nei carichi di magazzino. |
| --- | --- |
| Gestire ordini e richieste d'offerta | Crearli e modificarli (anche dalle scorte e dai preventivi), inviarli, registrare conferme, risposte e solleciti, chiudere i residui. Per ricevere la merce serve anche *Registrare i movimenti* del magazzino. |
| Gestire gli acquisti | Annullare ed eliminare gli ordini inviati, le impostazioni, segnare i prezzi come verificati. |

---

[← Magazzino](magazzino.md) · [Indice](README.md) · [Fatturazione →](vendite.md)
