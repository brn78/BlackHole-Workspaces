[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="posta"></a>Posta

**Il mio spazio → Posta** legge e invia la posta delle tue caselle, dentro BlackHole: i messaggi restano nell'archivio, si cercano in tutta la casella e vanno nei backup. A sinistra ci sono le caselle con le loro cartelle, al centro l'elenco dei messaggi, accanto o sotto il messaggio aperto.

- **Scrivi** è il solo pulsante blu della pagina (tasto <kbd>N</kbd>).
- **Controlla la posta adesso** è l'icona ↻ accanto al nome della cartella, sopra l'elenco (tasto <kbd>F9</kbd>, come in Outlook): gira finché il controllo non è finito. Di solito non serve, perché la posta si controlla da sola.
- In **⋯ Altro** della pagina ci sono la scelta della visualizzazione e, quando hai già delle caselle, **Aggiungi una casella**. Senza caselle la pagina mostra solo l'invito ad aggiungerne una.
- Le impostazioni di una casella non servono nel lavoro di ogni giorno: stanno nel suo **⋯**, a sinistra.
- Nel menu a sinistra, accanto a **Posta**, c'è il numero dei messaggi da leggere di tutte le tue caselle: la posta nuova si vede da ogni pagina. Non contano Posta inviata, Bozze, Cestino e Spam.

## <a id="posta-caselle"></a>Caselle e cartelle

- Ogni casella è una riga con l'avatar, il nome e il numero dei messaggi non letti. Sotto ci sono le sue cartelle, annidate come sul server.
- La freccia accanto apre o chiude la casella o la cartella. Il programma ricorda che cosa hai aperto, in questo browser.
- Un clic su una cartella mostra i suoi messaggi, anche se è di un'altra casella.
- Il **⋯** della casella, o il tasto destro sulla casella, offre **Nuova cartella…** e **Impostazioni della casella…**, che apre la sua scheda (vedi [La scheda della casella](#posta-casella)). Chi può solo scrivere vede la sua firma al posto delle impostazioni; chi può solo leggere non ha il ⋯.
- Il tasto destro su una cartella, o il suo **⋯** (compare passandoci sopra), offre:
   - **Nuova sottocartella…**, per creare una cartella dentro quella: nella Posta in arrivo e nelle cartelle create da te, non nel Cestino, nello Spam, nelle Bozze o nella Posta inviata;
   - **Rinomina…** ed **Elimina la cartella…**, solo per le cartelle create da te, non per Posta in arrivo, Posta inviata, Bozze, Cestino, Spam e Archivio, né per le cartelle speciali del server (su Gmail Tutti i messaggi, Speciali e Importanti) e quelle di altri utenti o condivise. Eliminando una cartella i messaggi che contiene vanno nel Cestino; se dentro ci sono altre cartelle, prima si eliminano quelle;
   - **Segna tutti come letti**;
   - sul Cestino, **Svuota il cestino…** (vedi [Cestino ed eliminazione](#posta-eliminare)).
- Nelle cartelle nuove si spostano i messaggi come nelle altre: trascinandoli, o con **Sposta in…**. Con una casella **IMAP** le cartelle si creano, si rinominano e si eliminano anche sul server della posta, e le ritrovi uguali sul telefono e negli altri programmi; con **POP3**, che sul server non ha cartelle, esistono solo in BlackHole.
- Una cartella nuova non può chiamarsi come una di sistema (Posta in arrivo, Posta inviata, Bozze, Cestino, Spam, Archivio, anche in inglese): si confonderebbe con quella vera. Se una cartella con uno di questi nomi c'è già sul server, creata da un altro programma, resta una cartella tua e il cestino resta quello del server.
- Se il server della posta non accetta una cartella nuova (per esempio dentro una cartella che non ne ammette altre), la cartella sparisce e i messaggi che ci avevi spostato tornano dov'erano. Se rinomini una cartella con un nome che sul server è già di un'altra, creata nel frattempo da un altro programma, la tua riprende il nome di prima. In tutti e due i casi il segno accanto alla casella dice che cosa è successo.
- Il segno accanto al nome vuol dire che l'ultimo controllo della posta non è riuscito: passaci sopra per leggere il motivo.

## <a id="posta-visualizzazione"></a>Come stanno le colonne

In **⋯ Altro** della pagina scegli una delle tre visualizzazioni. Il programma la ricorda, in questo browser.

| Visualizzazione | Come si presenta |
| --- | --- |
| **Cartelle, messaggi e messaggio in fila** | Tre colonne una accanto all'altra. È quella di partenza. |
| **Cartelle e messaggi, con il messaggio sotto** | Il messaggio aperto sta sotto l'elenco. |
| **Cartelle e messaggi, con il messaggio in scheda laterale** | Il messaggio si apre in una scheda a destra. L'elenco resta usabile: scegli un altro messaggio e la scheda mostra quello. |

- Le **maniglie** tra le colonne si trascinano per allargarle o stringerle; un doppio clic le riporta alla larghezza normale. Con il messaggio sotto, la maniglia orizzontale regola l'altezza dell'elenco.
- Il pulsante nell'intestazione dell'elenco nasconde la colonna delle cartelle; lo stesso pulsante la riapre.
- Sul telefono si vede una colonna alla volta. Il pulsante con la freccia in alto torna indietro: **Cartelle** dall'elenco, **Messaggi** dalla lettura.

## <a id="posta-elenco"></a>L'elenco dei messaggi

- Sopra l'elenco ci sono la **ricerca** e il **filtro**. La ricerca guarda tutti i messaggi della casella, non solo la cartella aperta. Il filtro mostra i non letti, quelli in evidenza, con allegati, solo PEC o assegnati a te.
- **In evidenza** è il segno dei messaggi importanti, la bandierina sulla riga: si mette e si toglie dal menu del messaggio. Non va confuso con i [preferiti](area-di-lavoro.md#preferiti) (la stella accanto all'oggetto, che mette il messaggio nel tuo menu).
- **Scegli più messaggi** (l'icona a sinistra della barra) mostra le spunte. La casella in testa sceglie tutti i messaggi dell'elenco. <kbd>Maiusc</kbd>+clic sceglie tutti quelli tra l'ultimo scelto e quello cliccato.
- Con dei messaggi scelti, **Altro** nella barra li segna come letti o non letti, li mette in evidenza o li toglie, li sposta in un'altra cartella, li mette nel cestino o, dal Cestino, li elimina definitivamente.
- Il **tasto destro** su un messaggio apre lo stesso menu: per quel messaggio, o per tutti quelli scelti se è uno di loro.
- Il **mittente** che è un cliente o un fornitore si riconosce dal suo chip: un clic apre la sua scheda sopra la pagina, senza cambiare pagina.

## <a id="posta-trascinare"></a>Spostare trascinando

Trascina un messaggio, o quelli scelti, su una cartella della stessa casella: la cartella si evidenzia e, quando lo lasci, i messaggi si spostano lì. Non si spostano messaggi da una casella all'altra. Serve il diritto di scrivere sulla casella.

## <a id="posta-lettura"></a>Leggere un messaggio

- Un clic sul messaggio lo apre (da tastiera <kbd>Invio</kbd>). La prima apertura lo segna come letto.
- **‹** e **›** in alto passano al messaggio precedente o successivo dell'elenco; da tastiera le frecce <kbd>↑</kbd> e <kbd>↓</kbd>.
- **Rispondi** è il solo pulsante blu. In **Altro** ci sono rispondi a tutti, inoltra, segna come letto o non letto, metti in evidenza, sposta in un'altra cartella, sposta nel cestino e scarica il messaggio (.eml).
- La **stella** ★ accanto all'oggetto mette il messaggio tra i tuoi [preferiti](area-di-lavoro.md#preferiti): dal menu o dalla Home lo riapri in una scheda sopra la pagina in cui sei. Se nel frattempo il messaggio è stato eliminato, la scheda lo dice e propone **Togli dai preferiti**.
- Nelle caselle condivise con te o aziendali il messaggio si **assegna**, come nelle [attività](attivita.md): **Assegna a un collega…** oppure **Assegna a me**; la × toglie l'assegnazione.
- Le **ricevute PEC** di un messaggio inviato stanno in una lista sola, una per riga (vedi [PEC e ricevute](#posta-pec)).
- Negli **allegati** il nome apre l'anteprima; accanto, il file si scarica o si salva in Documenti (vedi [Allegati e Documenti](#posta-allegati)).
- Lo **storico**, in fondo, dice chi ha letto, risposto, inoltrato, assegnato, spostato o eliminato il messaggio, e quando.
- Le **immagini** che arrivano da internet restano bloccate, perché farle arrivare dice al mittente che hai aperto il messaggio: **Mostra le immagini** le fa vedere per quel messaggio.
- Un messaggio con la scritta *Solo nell'archivio* non è più sul server della posta: lo trovi solo in BlackHole.

## <a id="posta-scrivere"></a>Scrivere

- **Scrivi** (tasto <kbd>N</kbd>) apre un messaggio nuovo in una scheda a lato. In **Da** scegli la casella da cui parte. Mentre scrivi i destinatari, il programma propone i contatti della Rubrica, i clienti e gli indirizzi già usati nella posta. **Cc** e **Ccn** si aggiungono con i loro pulsanti.
- **Allega dal PC** prende un file dal computer. **Allega da Documenti** apre una scheda a lato in cui cerchi il file per nome. Il messaggio ne manda una copia: il file resta dov'è.
- La **firma** della casella va in fondo al messaggio ed è tua: ognuno ha la sua, anche nelle caselle condivise. Si cambia dal **⋯** della casella, linguetta **Firma**; chi può scrivere ma non gestire la casella vede lì soltanto **La tua firma**. In scrittura una riga ne mostra solo il testo.
- Rispondendo o inoltrando, il messaggio originale sta in fondo, chiuso: **Messaggio originale** lo apre.
- Chiudere la scheda con qualcosa di scritto chiede conferma. **Invia** dice subito se il server ha accettato il messaggio.
- Se il messaggio non ha l'**oggetto**, o nel testo parli di un **allegato** («in allegato», «allego»…) ma non hai aggiunto nessun file, **Invia** chiede prima **Inviare lo stesso?**: **Torna al messaggio** (già scelto) ti riporta a scrivere, **Invia lo stesso** lo manda così.

## <a id="posta-scorciatoie"></a>Scorciatoie

Valgono quando non stai scrivendo in un campo (vedi anche le [scorciatoie generali](interfaccia.md#interfaccia-scorciatoie)).

| Tasti | Che cosa fanno |
| --- | --- |
| <kbd>N</kbd> | Un messaggio nuovo, come **Scrivi**. |
| <kbd>↑</kbd> <kbd>↓</kbd> | Il messaggio precedente o successivo dell'elenco, sia nell'elenco sia nella lettura. |
| <kbd>Invio</kbd> | Apre il messaggio scelto nell'elenco. |
| <kbd>Spazio</kbd> | Con **Scegli più messaggi** attivo, sceglie il messaggio o lo toglie dalla scelta. |
| <kbd>Canc</kbd> | Mette nel cestino il messaggio scelto, o quelli scelti; nel Cestino li elimina definitivamente, dopo la conferma. |
| <kbd>F9</kbd> | Controlla la posta adesso, come l'icona ↻ sopra l'elenco. |

## <a id="posta-casella"></a>La scheda della casella

Si apre dal **⋯** della casella, a sinistra, con **Impostazioni della casella…**. Le sue parti stanno in quattro linguette:

| Linguetta | Che cosa c'è |
| --- | --- |
| **Casella** | Indirizzo e password, il nome nell'elenco (per esempio *Posta di Mario*) e il nome del mittente (per esempio *Mario Rossi*), il tipo di ricezione (IMAP o POP3), se è una PEC, la copia nella posta inviata, ogni quanti minuti controllare la posta, i server di arrivo e di invio. **Prova la connessione** dice se la ricezione e l'invio rispondono, prima di salvare. |
| **Sul server** | Che cosa fare dei messaggi sul server, il cestino del server e la data dell'ultimo backup che contiene la posta. |
| **Condivisione** | Chi vede la casella e con quale diritto: può leggere, può scrivere, può gestire. |
| **Firma** | La firma che va in fondo ai messaggi che invii da questa casella. |

- **Aggiungi una casella** (in **⋯ Altro**, o nella pagina ancora vuota) apre la stessa scheda con la sola linguetta **Casella**. Scrivi l'indirizzo e la password: il programma propone i server dal dominio dell'indirizzo, e puoi cambiarli. Le altre linguette ci sono quando la casella è creata.
- **Attiva** è l'interruttore in fondo alla scheda: con la casella spenta il programma non controlla più la posta da sé.
- Il pulsante blu è **Salva** (per una casella nuova **Crea la casella**) e salva tutte le linguette insieme. Chiudere con modifiche non salvate chiede conferma.
- **Elimina la casella…**, in fondo, chiede se tenere l'archivio dei messaggi o cancellarlo.

## <a id="posta-ricezione"></a>IMAP o POP3

Ogni casella usa uno dei due modi per ricevere la posta. Si sceglie nella linguetta **Casella**, in **Tipo di ricezione**:

- **IMAP** (consigliato): la posta resta sul server e qui si vede la stessa cosa. Leggere, segnare, spostare o eliminare un messaggio si riflette sul server alla sincronizzazione successiva. Le cartelle sono quelle del server (Posta inviata, Bozze, Cestino, Spam, Archivio).
- **POP3**: i messaggi si scaricano nella Posta in arrivo di BlackHole. Le cartelle sono solo quelle locali (Posta in arrivo, Posta inviata, Cestino).

## <a id="posta-server"></a>Che cosa succede dei messaggi sul server

Nella linguetta **Sul server** della casella si sceglie che cosa fare dei messaggi già in archivio. Ogni scelta ha la sua spiegazione.

- **IMAP, messaggi**: *tienili tutti sul server*, oppure *svuota il server dei messaggi più vecchi di N giorni*; quelli più vecchi restano solo nell'archivio di BlackHole.
- **IMAP, cestino del server**: *lascia com'è*, *svuota a ogni aggiornamento*, o *svuota i messaggi più vecchi di N giorni*.
- **POP3**: *lasciali sul server*, *cancellali dopo averli scaricati*, *cancellali dopo N giorni*, oppure *cancellali dal server quando li cancelli qui*.

**Nulla si cancella dal server finché il messaggio non è nell'archivio di BlackHole e in un backup completo.** Nella stessa linguetta si vede la data dell'ultimo backup che contiene la posta: senza backup, dal server non si cancella niente.

## <a id="posta-pec"></a>PEC e ricevute

Una casella PEC si riconosce dal dominio (o si segna con **È una PEC**, nella linguetta **Casella**). Accanto al messaggio compare la pillola **PEC**. Un messaggio inviato con la PEC mostra lo stato (accettata, consegnata, consegnata in parte, mancata consegna) e, nella lettura, le ricevute in una lista sola, una per riga, con la data e il destinatario. Nell'elenco le ricevute non si mescolano con i messaggi: si vedono con **Mostra le ricevute PEC** nella barra dell'elenco. I messaggi PEC e le loro ricevute non si eliminano definitivamente: restano nel cestino.

## <a id="posta-condivisione"></a>Condivisione e diritti

Una casella si condivide con colleghi e gruppi, nella linguetta **Condivisione** della sua scheda, con un diritto per ciascuno:

- **Può leggere**: vede i messaggi, li segna come letti e li cerca.
- **Può scrivere**: in più risponde, invia, sposta ed elimina a nome della casella.
- **Può gestire**: in più cambia le impostazioni e le condivisioni.

Chi ha la casella condivisa può prendere un messaggio con **Assegna a me**, o assegnarlo a un collega: la lettura lo dice, l'elenco mostra a chi è assegnato e lo storico del messaggio riporta chi l'ha letto, risposto o spostato. Le caselle personali di un altro utente non si vedono, nemmeno dall'amministratore. Le caselle aziendali (per esempio l'indirizzo generale o la PEC) le crea e le gestisce chi ha il permesso **Gestire le caselle aziendali**: nella linguetta **Casella** c'è la voce **Casella aziendale**.

## <a id="posta-allegati"></a>Allegati e Documenti

Nella lettura il nome dell'allegato apre l'anteprima. Accanto, ⬇ scarica il file e **Salva in Documenti** lo mette nella cartella che scegli; per salvarlo serve il permesso di caricare documenti. Scrivendo, **Allega dal PC** prende un file dal computer e **Allega da Documenti** ne cerca uno nei Documenti: il messaggio ne manda una copia, il file resta dov'è.

## <a id="posta-eliminare"></a>Cestino ed eliminazione

- **Sposta nel cestino** mette il messaggio nella cartella **Cestino** della casella. Da lì lo rimetti dove vuoi con **Sposta in…** o trascinandolo.
- **Elimina definitivamente** c'è solo nel Cestino e chiede conferma. Il messaggio non passa dal [cestino del programma](cestino.md): sparisce e non si recupera. Dal server della posta si cancella solo quando un backup lo contiene.
- **Svuota il cestino…**, con il tasto destro sul Cestino, fa lo stesso con tutti i messaggi del cestino, dopo la conferma. Le PEC e le loro ricevute restano: non si eliminano mai definitivamente.
- **Elimina la casella…** chiede se tenere l'archivio dei messaggi. Se scegli di cancellarlo, nemmeno l'archivio passa dal cestino: i messaggi non si recuperano, neanche dai backup in cui ci sono ancora.

## <a id="posta-da-sapere"></a>Da sapere

- La **password per l'invio** salvata si cambia scrivendo quella nuova; **Rimuovi la password salvata**, sotto il campo, la toglie e l'invio usa la password della casella. Se il nome utente per l'invio è diverso da quello della ricezione, per toglierla svuota anche quel nome.
- In scrittura la **firma** si vede solo come testo semplice: com'è davvero si vede nella linguetta **Firma** e nel messaggio inviato.
- Il **colore** della casella non si cambia: l'avatar prende il colore dal nome.

---

[← Rubrica](rubrica.md) · [Indice](README.md) · [Password →](password.md)
