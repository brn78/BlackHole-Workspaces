[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="posta"></a>Posta

**Il mio spazio → Posta** legge e invia la posta delle tue caselle, dentro BlackHole: i messaggi restano nell'archivio, si cercano in tutta la casella e vanno nei backup. Le caselle sono a sinistra, l'elenco dei messaggi al centro e il messaggio aperto a destra. Sul telefono si vede una colonna alla volta: il pulsante **Indietro** torna a quella di prima.

- **Scrivi** è il pulsante blu della pagina: apre un messaggio nuovo dalla casella scelta in **Da**. Nella lettura il pulsante blu è **Rispondi**; rispondere a tutti, inoltrare, spostare o eliminare stanno in **Altro**.
- **Aggiungi una casella** (in **Altro**, o nella pagina ancora vuota): scrivi l'indirizzo e la password. Il programma propone i server dal dominio dell'indirizzo; puoi cambiarli. **Prova la connessione** dice se la ricezione e l'invio rispondono, prima di salvare.
- **Impostazioni e condivisione** di una casella: il pulsante **⋯** accanto alla casella selezionata. Sono impostazioni, non servono nel lavoro di ogni giorno.
- **Cerca** nella casella: la ricerca guarda tutti i messaggi della casella, non solo la cartella aperta. **Scegli più messaggi** (l'icona a sinistra della barra) permette di segnarli come letti, metterli nel cestino, spostarli o eliminarli tutti insieme.
- **Il mittente** che è un cliente o un fornitore si riconosce dal suo chip: un clic apre la sua scheda sopra la pagina, senza cambiare pagina.

## <a id="posta-ricezione"></a>IMAP o POP3

Ogni casella usa uno dei due modi per ricevere la posta, e si sceglie quando la si aggiunge:

- **IMAP** (consigliato): la posta resta sul server e qui si vede la stessa cosa. Leggere, segnare, spostare o eliminare un messaggio si riflette sul server alla sincronizzazione successiva. Le cartelle sono quelle del server (Posta inviata, Bozze, Cestino, Spam, Archivio).
- **POP3**: i messaggi si scaricano nella Posta in arrivo di BlackHole. Le cartelle sono solo quelle locali (Posta in arrivo, Posta inviata, Cestino).

## <a id="posta-server"></a>Che cosa succede dei messaggi sul server

Accanto al server si sceglie che cosa fare dei messaggi già in archivio. Ogni scelta ha la sua spiegazione nella finestra.

- **IMAP, messaggi**: *tienili tutti sul server*, oppure *svuota il server dei messaggi più vecchi di N giorni*; quelli più vecchi restano solo nell'archivio di BlackHole.
- **IMAP, cestino del server**: *lascia com'è*, *svuota a ogni aggiornamento*, o *svuota i messaggi più vecchi di N giorni*.
- **POP3**: *lasciali sul server*, *cancellali dopo averli scaricati*, *cancellali dopo N giorni*, oppure *cancellali dal server quando li cancelli qui*.

**Nulla si cancella dal server finché il messaggio non è nell'archivio di BlackHole e in un backup completo.** Nella finestra della casella si vede la data dell'ultimo backup che contiene la posta: senza backup, dal server non si cancella niente. Eliminare un messaggio qui lo sposta nel cestino; dal cestino si elimina per sempre, e il server lo segue quando il backup lo contiene.

## <a id="posta-pec"></a>PEC e ricevute

Una casella PEC si riconosce dal dominio (o si segna con **È una PEC**). Accanto al messaggio compare la pillola **PEC**; un messaggio inviato con la PEC mostra lo stato (accettata, consegnata, consegna parziale, mancata consegna) e, nella lettura, la cronologia delle ricevute, una per riga, con la data e il destinatario. Le ricevute non si mescolano con i messaggi: si vedono con **Mostra le ricevute PEC** nella barra dell'elenco. I messaggi PEC e le loro ricevute non si eliminano per sempre: vanno nel cestino.

## <a id="posta-condivisione"></a>Condivisione e diritti

Una casella si condivide con colleghi e gruppi, dalla sua **Condivisione**, con un diritto per ciascuno:

- **Può leggere**: vede i messaggi, li segna come letti e li cerca.
- **Può scrivere**: in più risponde, invia, sposta ed elimina a nome della casella.
- **Può gestire**: in più cambia le impostazioni e le condivisioni.

Chi ha la casella condivisa può **La prendo io** su un messaggio, o assegnarlo a un collega: la lettura lo dice e la storia del messaggio riporta chi l'ha letto, risposto o spostato. Le caselle personali di un altro utente non si vedono, nemmeno dall'amministratore. Le caselle aziendali (per esempio l'indirizzo generale o la PEC) le crea e le gestisce chi ha il permesso **Gestire le caselle aziendali**.

## <a id="posta-allegati"></a>Allegati e Documenti

Gli allegati si scaricano dal messaggio, oppure si salvano in **Documenti** con **Salva in Documenti**, scegliendo la cartella. Scrivendo, **Allega dal PC** prende un file dal computer e **Allega da Documenti** ne cerca uno nei Documenti: il messaggio ne manda una copia, il file resta dov'è. Per salvare un allegato serve il permesso di caricare documenti. Le immagini esterne di un messaggio restano bloccate, perché farle arrivare dice al mittente che hai aperto il messaggio: **Mostra le immagini** le fa vedere per quel messaggio.

---

[← Rubrica](rubrica.md) · [Indice](README.md) · [Password →](password.md)
