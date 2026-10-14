[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="archivio-rete"></a>Archivio di rete

Le cartelle dell'ufficio che stanno sul server o in rete (la cartella condivisa di lavoro, i vecchi archivi, i manuali) si aggiungono alla [ricerca](ricerca.md): la piattaforma ne legge **in sola lettura** i nomi di file e cartelle, le dimensioni e le date, e li tiene in un indice. I file restano dove sono: la piattaforma non li sposta, non li copia, non li modifica e non ne legge il contenuto.

## <a id="archivio-rete-cartelle"></a>Le cartelle

**Sistema → Archivio di rete**, riservata agli amministratori. **Nuova cartella** e, per ognuna:

- **Nome**: come compare nella ricerca e nelle linguette dell'archivio (*Archivio ufficio*, *Manuali*). **Attiva**: tolta la spunta, la cartella non si aggiorna e non si trova.
- **Percorso**, come lo vede il server: una cartella del server (*D:\\Archivio*) o della rete (*\\\\server\\condivisione\\cartella*). **Prova** controlla che si raggiunga e che se ne legga il contenuto, e dice quante cartelle e quanti file ci sono al primo livello; se il contenuto è negato o la cartella risulta vuota, lo dice con l'account con cui il server l'ha letta. Non si può scegliere la cartella di lavoro della piattaforma né una che la contiene.
- **Utente** e **Password**: per le cartelle di rete che il servizio della piattaforma non legge con il suo account (per esempio *DOMINIO\\utente*, anche il tuo). La password si salva cifrata e non si rivede: il campo vuoto la lascia com'è, **Rimuovi la password salvata** la toglie.
- **Chi la trova con la ricerca**: **Solo gli amministratori**, **Tutti gli utenti** oppure **I gruppi scelti** (i [gruppi](gruppi-policy.md) di Sistema). Gli amministratori la vedono sempre.

> [!NOTE]
> **Cartelle condivise «aperte a tutti».** Il servizio di Windows della piattaforma gira con un account di sistema, che in rete si presenta come il computer (o come anonimo), non come un utente. Una condivisione aperta a tutti gli utenti del PC o del dominio può non lasciarlo entrare, oppure mostrargli una cartella vuota: in quel caso **Prova** lo dice e basta scrivere un utente che la vede, anche il tuo. Le cartelle del server stesso (un disco come *D:*) di solito non ne hanno bisogno.

- **Cartelle da saltare**, una per riga: un nome (*Backup*) salta tutte le cartelle con quel nome, un percorso dalla cartella dell'archivio (*UFFICIO\\Vecchi*) solo quella. Si saltano sempre i file nascosti e di sistema, i file temporanei di Office (*~$…*), *Thumbs.db* e *desktop.ini*, e le cartelle del server stesso (i suoi dati, il programma, i backup) se capitano dentro il percorso indicizzato.

Il cestino 🗑, in basso nel pannello, toglie la cartella dall'archivio e il suo indice: i file non si toccano. Ogni modifica finisce nel [registro attività](registro.md).

## <a id="archivio-rete-aggiornamento"></a>L'aggiornamento

- **Aggiorna**, accanto a ogni cartella, o **Aggiorna tutto** rileggono tutte le cartelle e i file; mentre lavora la riga mostra quanti ne ha letti, con **Ferma**. Finito, mostra file, cartelle, spazio, quando si è aggiornata, quante cartelle ha saltato e l'eventuale errore (per esempio la rete che non risponde: l'indice di prima resta). I file si trovano quando l'aggiornamento è finito: il primo di una condivisione grande può richiedere parecchi minuti.
- **Se il servizio si chiude a metà** (un aggiornamento del programma, un riavvio, la corrente che manca), l'aggiornamento riparte da solo una decina di minuti dopo la ripartenza del servizio, quando il server ha finito di avviarsi; intanto resta l'indice di prima. Un errore o **Ferma** non fermano mai il resto della piattaforma.
- **Senza rubare il disco alla piattaforma**: gli aggiornamenti completi lavorano a priorità bassa, così le richieste di chi usa la piattaforma e il suo database passano sempre per prime, anche quando l'archivio sta sullo stesso disco del server. Se il server è molto impegnato e una scrittura deve aspettare troppo, la piattaforma chiede di riprovare tra qualche secondo invece di dare un errore.
- **Ogni notte**, all'ora scelta in **Aggiornamento di ogni notte** (02:30 se non la cambi), si rilegge tutto. Una condivisione con centinaia di migliaia di file richiede qualche minuto: meglio quando la rete è libera. Se a quell'ora il server era spento, l'aggiornamento parte quando si riaccende, una decina di minuti dopo l'avvio. Senza la spunta si aggiorna solo con i pulsanti.
- **Mentre si lavora**: dopo il primo aggiornamento la piattaforma si accorge da sola dei file creati, rinominati, spostati o cancellati e aggiorna l'indice in pochi secondi, senza aspettare la notte.

## <a id="archivio-rete-sfogliare"></a>Sfogliare e aprire i file

**Archivio → Archivio di rete** compare a chi vede almeno una cartella. In alto le linguette delle cartelle, il percorso in cui ti trovi (clic su un pezzo per tornarci) e la casella per filtrare la cartella; sotto l'elenco con nome, data di modifica e dimensione. Clic su una cartella per entrare, su un file per aprirlo nel [visualizzatore](documenti.md#documenti-visualizzatore): PDF, Word, Excel e CSV, immagini (anche TIFF), video e audio, testo, disegni DXF e DWF e modelli 3D, con **←** e **→** per passare agli altri file della cartella. I formati che il visualizzatore dell'archivio non apre (DWG, ZIP, programmi, vecchi formati di Office) aprono il pannello del file. Sui disegni, i PDF e le immagini dell'archivio si possono fare [annotazioni e misure](documenti.md#documenti-annotazioni): si salvano a parte, il file resta com'è.

Sopra l'elenco c'è lo **stato dell'indice** della cartella: quanti file e cartelle, quanto pesano e quando è stata aggiornata, oppure, mentre si aggiorna, quanti elementi ha già letto. Gli amministratori hanno anche:

- **Aggiorna** (la cartella che stai guardando) e **Aggiorna tutto** in alto: lanciano subito l'aggiornamento a mano, come da Sistema → Archivio di rete; mentre gira compare **Ferma**, e alla fine l'elenco si rilegge da solo.

In **Sistema → Archivio di rete**, in testa, il riquadro **Informazioni di sistema**, lo stesso delle [Impostazioni](impostazioni.md): versione, server, modalità (servizio di Windows o applicazione), cartella dati e schema del database; processore e memoria in quel momento (aggiornati ogni 3 secondi, con quanto usa la piattaforma e quanto gli altri programmi) e lo spazio sul disco dei dati. Serve a capire se il server è già impegnato prima di lanciare un aggiornamento pesante. Si chiude con un clic sul titolo, e resta chiuso la volta dopo.

Quando un file sparisce dalla cartella condivisa (eliminato, spostato o rinominato), al primo aggiornamento completo dell'archivio se ne vanno anche le sue annotazioni; se una parte della cartella non si è potuta leggere, si aspetta l'aggiornamento successivo.

Il tasto destro, o ⋯ sulla riga, dà le altre azioni: **Apri**, **Apri in una nuova scheda del browser** (PDF, immagini, testo), **Scarica**, **Percorso e dettagli** e **Copia il percorso**; su una cartella **Apri la cartella** e **Copia il percorso**. Il pannello del file (anche nel visualizzatore) ha:

- il **percorso completo**, con ⧉ per copiarlo e incollarlo in Esplora risorse da un PC dell'ufficio;
- **Apri** e **Scarica**;
- **Apri la cartella** per tornare all'elenco della cartella che lo contiene.

Nella [ricerca](ricerca.md) i file dell'archivio hanno la loro linguetta, **Archivio di rete**, con il percorso delle cartelle: si trovano anche scrivendo un pezzo del nome o il nome di una cartella che li contiene (*manuali centrale*), senza badare ad accenti e maiuscole. Un clic su un file trovato apre la sua cartella e il file nel visualizzatore.

> [!NOTE]
> Tutto in sola lettura: dall'archivio non si cancella, non si rinomina e non si carica niente (le annotazioni stanno nella piattaforma, non nella cartella). Chi non vede una cartella non ne trova i file, nemmeno nei conteggi, e non li apre neanche con un link. Ogni file aperto o scaricato finisce nel [registro attività](registro.md).

---

[← Archiviazione](archiviazione.md) · [Indice](README.md) · [Privacy →](privacy.md)
