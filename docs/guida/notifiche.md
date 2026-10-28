[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="notifiche"></a>Notifiche

Le **notifiche** ti avvisano di ciò che ti riguarda nelle [attività](attivita.md) e nelle [commesse](progetti.md): non serve tenere aperta la pagina Attività per sapere che qualcuno ti ha assegnato un lavoro, te lo ha condiviso, ha commentato o aspetta la tua approvazione. Arrivano qui anche i promemoria delle [scadenze](scadenze.md) a chi le gestisce. Agli amministratori arriva qui anche l'avviso di una [nuova versione](server.md#server-nuove-versioni) della piattaforma.

## <a id="notifiche-campanella"></a>La campanella

- La campanella 🔔 nella barra superiore mostra in rosso quante notifiche hai **da leggere**. Un clic apre l'elenco, dalle più recenti; quelle da leggere hanno lo sfondo colorato e un pallino.
- Un clic su una notifica la segna come letta e apre l'attività (o la pagina della commessa) a cui si riferisce.
- Mentre carichi o scarichi documenti, in cima al pannello c'è la sezione **Trasferimenti**, con l'avanzamento di ciascun file; attorno alla campanella un anello mostra la percentuale complessiva. Lì ci sono anche i PDF che il server sta rendendo ricercabili, con le pagine lette. Vedi [Caricare e scaricare](documenti.md#documenti-caricare) e [Riconoscimento del testo](documenti.md#documenti-ocr).
- In alto nell'elenco: **Segna tutte come lette**, 🗑 **Elimina le notifiche già lette** e ⚙ le [preferenze](#notifiche-preferenze). Le notifiche lette si eliminano comunque da sole dopo 90 giorni.
- Mentre usi la piattaforma, una notifica nuova compare anche come **avviso in basso a destra**, una volta sola: un clic sull'avviso apre l'attività o la commessa. Aprendo la piattaforma, compaiono come avviso al massimo le tre più recenti tra quelle arrivate mentre non c'eri; le altre sono nella campanella.
- In basso a destra restano in vista al più **tre avvisi** (notifiche, messaggi della chat, scadenze, la password da cambiare): gli altri si raccolgono nella riga **Altri N avvisi**, che con un clic li mostra tutti. Sul telefono gli avvisi sono più bassi e il testo sta in una riga.

## <a id="notifiche-tipi"></a>Che cosa arriva

| Notifica | Chi la riceve |
| --- | --- |
| Nuova attività per te | Chi viene assegnato a un'attività (non chi si assegna da sé). |
| Attività condivisa con te | I colleghi aggiunti alla [condivisione](attivita.md#attivita-condivisione) di un'attività, direttamente o tramite un loro gruppo (non gli assegnatari, che la vedono già). |
| Commento | Assegnatari, revisore, chi ha creato l'attività e chi l'ha già commentata, se la vede ancora. |
| Cambio di stato | Assegnatari e chi ha creato l'attività, quando un altro ne cambia lo stato. |
| Da rivedere | Il revisore quando l'attività passa «In revisione»; se non c'è, il responsabile della commessa collegata oppure, senza commessa, chi ha creato l'attività. |
| Approvata o rimandata | Gli assegnatari e chi ha creato l'attività, con il commento del revisore se l'ha rimandata. |
| Promemoria delle scadenze | Gli assegnatari (se non ce ne sono, il responsabile della commessa collegata oppure, senza commessa, chi ha creato l'attività): il giorno prima della scadenza, il giorno stesso e, una volta, quando l'attività è scaduta. Arrivano dalle 7 del mattino, oppure all'ora di **Avviso alle** se l'attività ce l'ha, anche per le attività senza commessa; non per quelle delle commesse completate o annullate. |
| Nuova occorrenza | Gli assegnatari di un'[attività ricorrente](attivita.md#attivita-ricorrenti) quando ne nasce la successiva. |
| Commessa | Chi viene aggiunto ai membri di una commessa o ne diventa responsabile: il clic apre la [pagina della commessa](progetti.md#progetti-pagina). |
| Scadenze in arrivo e passate | Chi gestisce il personale (per documenti e visite, chi ha anche il permesso dei dati delicati), chi gestisce mezzi e attrezzature, chi gestisce le manutenzioni e chi gestisce le scadenze dell'azienda: quando una scadenza entra nel preavviso e quando passa senza rinnovo, una volta sola. Il clic apre la scheda della persona, del bene, la manutenzione o la scadenza. Vedi [I promemoria](scadenze.md#scadenze-promemoria). |
| Scadenze dei beni in consegna | Chi ha in consegna un mezzo o un'attrezzatura (con la sua scheda del personale collegata all'utente): le stesse notifiche per le scadenze di quel bene. Il clic apre la scheda del bene, oppure la Home per chi non vede mezzi e attrezzature. Vedi [Le consegne](mezzi.md#mezzi-consegne). |
| Richiesta di assistenza assegnata | Il tecnico a cui viene assegnata una [richiesta di assistenza](assistenza.md) (se non se l'è assegnata da solo): il clic apre la richiesta. Le notifiche dell'assistenza le vede nelle preferenze solo chi vede l'assistenza. |
| Richiesta di assistenza in scadenza | Il tecnico assegnato (o, senza tecnico, chi l'ha aperta): quando la richiesta entra nell'ultima parte del suo tempo e quando la scadenza passa senza intervento, una volta sola. Vedi [Priorità e scadenze](assistenza.md#assistenza-priorita). |
| Monitoraggio | Gli utenti e i gruppi scelti in un [controllo](monitoraggio.md#monitoraggio-avvisi), se vedono il monitoraggio: quando un dispositivo non risponde (anche ripetuto, se scelto), quando risponde di nuovo e quando un certificato https sta per scadere. Le email e i messaggi su Telegram di questi avvisi partono subito. Il clic apre il controllo. |
| Rete locale | Chi gestisce il monitoraggio, se scelto nelle [impostazioni dello scanner](rete-locale.md#rete-locale-impostazioni): i dispositivi nuovi trovati da una scansione e i controlli del monitoraggio rimasti su un indirizzo che il dispositivo non ha più. |
| Turno di reperibilità | Chi riceve un [turno di reperibilità](reperibilita.md#reperibilita-turni) (anche a rotazione o come sostituto) o se lo vede cambiare, passare a un collega o togliere da un altro; il promemoria il giorno prima del turno. Il clic apre il turno. |
| Richiesta di assistenza mentre sei reperibile | Chi è reperibile quando si apre una richiesta di assistenza, se vede l'assistenza: sempre o solo fuori orario, come scelto nelle [impostazioni della reperibilità](reperibilita.md#reperibilita-impostazioni). |
| File ricevuto con un link | Chi ha creato un [link che accetta file](condivisioni.md#condivisioni-caricamenti), per ogni file che arriva: il clic lo apre in Documenti. La notifica la vede nelle preferenze solo chi può condividere. |
| Indicatore oltre la soglia | Gli utenti e i gruppi scelti in un [indicatore](indicatori.md#indicatori-obiettivi), se possono vedere il gruppo (azienda, reparto, persona): una volta per periodo e gruppo, quando l'ultimo periodo finito supera la soglia di allarme. Il clic apre il dettaglio dell'indicatore. |
| Mancano i dati di una misura | Chi deve inserire una [misura](indicatori.md#indicatori-misure), i giorni scelti dopo la fine del periodo, se i valori non ci sono tutti. Il clic apre i dati della misura. |
| Budget della commessa | Chi vede [budget e consuntivo](progetti.md#progetti-budget) di una commessa aperta, quando diventa vicina al budget o lo supera: una volta per passo, con la percentuale e le voci oltre il previsto (senza importi). Il clic apre la linguetta Budget. Nelle preferenze solo per chi ha il permesso. |
| Nuova versione | Gli amministratori, una volta per versione, quando su GitHub è pubblicata una versione più recente di quella installata (se l'avviso è attivo in Impostazioni). Vedi [Avviso delle nuove versioni](server.md#server-nuove-versioni). |

Non ricevi notifiche delle cose che fai tu, e le notifiche di un'attività arrivano solo a chi può [vederla](attivita.md#attivita-condivisione).

## <a id="notifiche-accesso"></a>Avviso di accesso

Dalla 1.143.0, quando qualcuno entra con il tuo account ricevi subito un'**email** o un messaggio su **Telegram**: chi, quando, da quale indirizzo e con quale browser. Se non sei stato tu te ne accorgi: cambia subito la password, chiudi le altre sessioni da [Profilo e sicurezza](profilo.md) e avvisa un amministratore. Lo scegli in **Profilo e sicurezza → Notifiche → Avviso di accesso**:

- **Quando entro da un browser o un dispositivo nuovo** (di serie, consigliato): l'avviso arriva solo la prima volta che il tuo account entra da un browser; dallo stesso browser, le volte dopo, no. Un browser diverso, un'altra persona che usa il tuo PC con il suo account, una finestra in incognito o i cookie cancellati contano come nuovi.
- **A ogni accesso**: sempre, anche dal solito browser.
- **Mai**.
- **Per email** e **Su Telegram**: dove riceverlo. Servono la posta configurata e l'email dell'account, o la chat di Telegram collegata.

L'avviso parte **a qualsiasi ora**, anche fuori dal tuo [orario](#notifiche-quando), e **non passa dalla campanella**: chi entrasse al posto tuo non lo vede e non può fermarlo leggendo la notifica. Con la [verifica in due passaggi](profilo.md) arriva dopo il codice, quando l'accesso è completo; un accesso non riuscito non manda nulla. In **Impostazioni → Posta e Telegram → Anteprima delle email** si vede com'è fatta l'email.

## <a id="notifiche-email"></a>Per email

Se la [posta in uscita](impostazioni.md) è configurata e il tuo account ha un indirizzo email, le notifiche che restano **da leggere per qualche minuto** arrivano anche per email, riunite in un solo messaggio con il collegamento a ciascuna attività o commessa. Se le leggi subito nella piattaforma l'email non parte. Il collegamento usa l'indirizzo pubblico indicato in Impostazioni. Gli avvisi del monitoraggio partono subito, se il controllo lo prevede.

Tutto si sceglie nel riquadro **Notifiche per email** del [profilo](profilo.md):

- **Lo stato del servizio**: **Attiva** (con l'indirizzo da cui partono le email e l'ultimo invio riuscito), **Problema** (l'ultimo invio non è riuscito: agli amministratori anche il motivo) oppure **Non configurata**. Sotto, il tuo indirizzo email.
- **Ricevi le notifiche per email** le accende o le spegne tutte; **Quali per email** sceglie i tipi, per esempio solo le scadenze e l'assistenza. In grigio i tipi spenti nel riquadro **Notifiche**: per email arriva solo ciò che arriva nella campanella.
- **Mandami un'email di prova** ne manda una al tuo indirizzo (al più una ogni 30 secondi): se non arriva, guarda nello spam, poi avvisa un amministratore.

## <a id="notifiche-telegram"></a>Su Telegram

Se è configurato il [bot di Telegram](impostazioni.md#impostazioni-telegram) dell'azienda, le notifiche arrivano anche sul telefono, nella chat con il bot. Per collegare la tua chat:

1. In [Profilo e sicurezza](profilo.md), scheda **Notifiche**, riquadro **Su Telegram**, scegli **Collega Telegram**.
2. Inquadra il **codice QR** con la fotocamera del telefono su cui usi Telegram, oppure **Apri Telegram** da un computer con Telegram (o copia il link): si apre la chat con il bot.
3. Premi **Avvia**: il bot chiede il **PIN**.
4. Scrivi nella chat il **PIN di 6 cifre** che vedi nella finestra della piattaforma, accanto al codice QR: il bot risponde «Collegato a BlackHole Workspaces come…» e la finestra si chiude da sola. Il codice vale 10 minuti e una volta sola; scaduto, **Nuovo codice** ne crea un altro.

**Perché il PIN** (dalla 1.108.0): il codice QR e il link portano solo alla chat con il bot; il PIN si vede soltanto nella tua finestra della piattaforma, dopo l'accesso con la tua password, e non è nel link. Chi riesce ad avere il link o a fotografare il QR (una foto dello schermo, un link inoltrato per sbaglio) senza il PIN non collega niente, e un'altra persona che sta scrivendo al bot nello stesso momento non può prendere il tuo posto: il bot collega solo la chat che ha aperto il tuo link **e** ha scritto il tuo PIN. In più:

- mentre aspetta il PIN la finestra dice **da quale chat** lo aspetta (nome e @nome di Telegram): se non è la tua, non scrivere niente e chiudi;
- il link vale per **una chat sola**: se lo apre anche un'altra chat, il collegamento si annulla per sicurezza;
- tre PIN sbagliati annullano il collegamento; con **Nuovo codice** ricominci;
- ogni collegamento finisce nel [registro attività](registro.md), con la chat che l'ha fatto.

- **Che cosa arriva**: i tipi scelti in **Quali su Telegram**, tra quelli che arrivano nella campanella (gli altri sono in grigio): per esempio su Telegram solo il monitoraggio e l'assistenza, per email le scadenze. Gli avvisi del [monitoraggio](monitoraggio.md#monitoraggio-avvisi) partono subito (se il controllo ha **Anche per email e Telegram, subito**); le altre notifiche se restano da leggere per due minuti, come le email: se le leggi prima nella piattaforma il messaggio non parte. Fino a tre notifiche insieme arrivano una per messaggio, di più in un messaggio solo con l'elenco.
- **Il messaggio**: il titolo in grassetto, il testo e **Apri**, che porta all'attività, al controllo o alla pagina della piattaforma (con l'indirizzo della piattaforma indicato in Impostazioni; dal telefono si apre se la piattaforma è raggiungibile da lì, per esempio con la VPN).
- Nel riquadro **Notifiche su Telegram**: lo stato del bot (**Attivo**, con l'ultimo contatto con Telegram, oppure **Problema**: agli amministratori anche il motivo), la chat collegata, **Ricevi le notifiche su Telegram** che sospende i messaggi senza scollegare la chat (si salva con **Salva le notifiche** in fondo) e **Mandami un messaggio di prova**. **Scollega** la scollega e la chat riceve un ultimo messaggio che lo dice. Nella chat, **/stop** la scollega e **/start** dice a quale account è collegata.
- **Quando arrivano**: quando vuoi tu, come lo scegli in [Quando disturbarmi](#notifiche-quando); di serie come l'azienda, cioè solo nell'orario di lavoro, al mattino con un ritardo (di serie mezz'ora, il tempo di sistemarsi) e la sera con un anticipo (di serie mezz'ora); nei festivi niente. Le notifiche nate fuori orario aspettano e partono all'apertura della fascia successiva, in un messaggio solo se sono più di tre. Partono comunque subito i promemoria delle attività con **Avviso alle** (all'ora scelta) e quelli per chi è reperibile; gli avvisi del monitoraggio subito, se non hai scelto altrimenti.
- **Il tuo compleanno**: quel giorno, verso le 10, anche se è festa, il bot ti manda gli auguri, solo su Telegram (la data di nascita è quella della tua scheda utente).
- **Senza internet** sul server (o con la posta che non risponde) i messaggi e le email aspettano e partono al ritorno, fino a una settimana; poi restano solo nella campanella. Anche a server spento la coda resta e riparte all'accensione. Se blocchi il bot o cancelli la chat, la piattaforma la scollega da sola.
- Solo chat private: in un gruppo il bot non si collega. I messaggi contengono titoli di attività e nomi di clienti: collega solo il tuo account personale di Telegram.

## <a id="notifiche-quando"></a>Quando disturbarmi

In [Profilo e sicurezza](profilo.md), scheda **Notifiche**, il riquadro **Quando disturbarmi** (dalla 1.96.0) dice quando possono arrivarti le notifiche su Telegram e, se vuoi, per email. La campanella non ha orari.

- **Come l'azienda** (di serie): la regola scelta da un amministratore nelle [impostazioni di Telegram](impostazioni.md#impostazioni-telegram), scritta accanto in parole.
- **A qualsiasi ora**.
- **Nell'orario di lavoro dell'azienda, con i miei minuti**: l'orario di [Reperibilità → Impostazioni](reperibilita.md#reperibilita-impostazioni) (festivi esclusi, pause escluse), con il tuo **Ritardo al mattino** e il tuo **Anticipo la sera** (da 0 a 240 minuti).
- **Nei miei orari**: le tue fasce, giorno per giorno, anche per i festivi (si parte dall'orario di lavoro dell'azienda; «Non disturbare» per un giorno senza notifiche).
- **Vale anche per le email**: senza la spunta le email arrivano come sempre; con la spunta aspettano il tuo orario.
- **Gli avvisi del monitoraggio arrivano subito, anche fuori orario** (di serie sì): se un controllo li manda su Telegram a te, ti arrivano subito; senza la spunta aspettano anche loro il tuo orario.
- **Auguri di compleanno su Telegram** (se l'azienda li ha accesi): verso le 10 del tuo compleanno.

Sotto si legge in parole quando ti arrivano adesso. Le notifiche nate fuori orario aspettano e arrivano tutte all'inizio della fascia successiva. Arrivano sempre all'ora giusta i promemoria delle attività con **Avviso alle** e le richieste di assistenza quando sei reperibile.

## <a id="notifiche-preferenze"></a>Preferenze

In [Profilo e sicurezza](profilo.md), scheda **Notifiche** (la apre anche l'icona ⚙ della campanella), ci sono i riquadri **Nella piattaforma** (che cosa arriva nella campanella: togli la spunta ai tipi che non vuoi), [Per email](#notifiche-email) e [Su Telegram](#notifiche-telegram) (se averle anche lì, e quali) e [Quando disturbarmi](#notifiche-quando). I tipi sono divisi per area (attività e commesse, scadenze, assistenza e reperibilità, monitoraggio, commerciale, piattaforma) con un nome corto: la descrizione intera compare passandoci sopra con il mouse. Un tipo spento nella campanella non arriva nemmeno per email o su Telegram. Dalla 1.124.0 si salva tutto insieme con **Salva le notifiche**, in fondo e sempre in vista (dice *Modifiche da salvare* quando c'è qualcosa di nuovo). Le preferenze sono dell'account: valgono su ogni computer.

---

[← Chat e presenze](chat.md) · [Indice](README.md) · [Assistente AI →](assistente-ai.md)
