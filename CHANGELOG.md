# Novità delle versioni

Il setup di ogni versione è nella pagina [Releases](https://github.com/brn78/BlackHole-Workspaces/releases).
Per aggiornare basta **Scarica e installa** in *Sistema → Impostazioni → Aggiornamento del programma* (dalla 1.136.0),
oppure caricare il setup nello stesso riquadro o eseguirlo sul server: dati, account e impostazioni restano.

## 1.150.2 · 20 ottobre 2026

- **Fattura dal preventivo con la merce già consegnata**: se parte del materiale è uscito con dei DDT non ancora fatturati,
  la finestra «Fattura dal preventivo» li elenca (già spuntati quelli della stessa commessa o dello stesso preventivo).
  La fattura delle righe o del saldo li richiama e diventa differita, con il riferimento ai DDT nella fattura
  elettronica, e i DDT escono da «Da fatturare». Prima restavano da fatturare e si rischiava di fatturarli due volte.

## 1.150.1 · 20 ottobre 2026

**Più robusta nei casi peggiori** (prove di spegnimenti a metà, disco pieno, backup rovinati, file ostili):
- **Ripristino interrotto**: se la corrente salta o il server si ferma mentre si applica un ripristino, al riavvio riprende
  da dove era arrivato. Prima, in un momento preciso, il server poteva ripartire vuoto (i dati restavano nella cartella
  di recupero, ma sembravano spariti).
- **Backup interrotti**: il file a metà lasciato da un backup interrotto (grande quanto un backup) si toglie da solo al
  backup successivo, dopo qualche ora.
- **Disco pieno**: un messaggio chiaro, «il disco del server è pieno… i dati salvati finora sono al sicuro», invece
  dell'errore tecnico; liberato lo spazio si riprende senza riavviare.
- **Storico delle vendite**: un'importazione interrotta a metà non lascia più una bozza in giro; ripetendola, le fatture
  già entrate si riconoscono e si aggiungono le altre.

**Correzioni trovate usando la piattaforma come un ufficio vero:**
- Uscendo da un preventivo inviato, accettato o rifiutato compariva «Modifiche non salvate» anche senza aver toccato
  niente.
- «Aggiungi dal listino» nei preventivi: descrizione e codice di nuovo su due righe e il pulsante «Aggiungi» sempre in
  vista (prima la tabella usciva dalla finestra).
- Ordini, richieste d'offerta, DDT e fatture: con la scheda stretta il menu «Altro» non ripete più la stessa azione due
  volte («Invia» e «Invia…», «Emetti» ed «Emetti»).
- Fattura dal preventivo: la percentuale dell'acconto compare solo scegliendo «Acconto».
- Scheda del cliente: l'avviso sulle coordinate degli indirizzi non compare più quando gli indirizzi non ci sono.
- Matricole: «1 pezzo», non «1 pezzi».

## 1.150.0 · 20 ottobre 2026

**Importare ed esportare, terza parte: i documenti con le righe.** Un foglio con una riga per ogni riga del documento e
i dati del documento ripetuti (oppure scritti solo nella prima): le righe con lo stesso numero fanno un documento.
- **Preventivi**: esportati e importati con capitoli, voci, note e subtotali; lo stato scritto nel file (inviato,
  accettato, rifiutato, annullato) si segna con la data del preventivo.
- **Acquisti**: ordini ai fornitori e richieste d'offerta. Si importano in bozza, e le righe con il codice di una voce
  del listino si collegano alla voce, così all'arrivo la merce entra in magazzino.
- **Vendite**: fatture, note di credito e DDT si esportano con le righe.

**Lo storico delle fatture**: le fatture e le note di credito già emesse con un altro programma entrano con il loro
numero e la loro data, dai file delle fatture elettroniche (XML, P7M e ZIP, come quelli del cassetto fiscale o
dell'intermediario) oppure da un foglio. Non si rimandano allo SDI e non toccano il magazzino; i clienti che mancano si
aggiungono con i dati della fattura; si possono segnare già incassate; la numerazione dell'anno prosegue dopo l'ultima
fattura importata.

Nella release anche i dati dimostrativi aggiornati alla 1.150.0.

## 1.149.1 · 20 ottobre 2026

- **Setup, scelta delle opzioni**: «Apri la porta nel Firewall di Windows» ora si spunta anche da sola; prima si
  accendeva solo spuntando «anche per le reti Pubbliche». Allo stesso modo, togliere «Icona di stato» non spegne più
  «Installa come servizio di Windows».

## 1.149.0 · 20 ottobre 2026

**Importare ed esportare, seconda parte: il lavoro di tutti i giorni.** Le stesse finestre «Importa» ed «Esporta» della
1.148.0 (tutti i fogli del file, modello Excel da compilare, import diretto, scelta delle colonne) arrivano in:
- **Impianti**: cliente, nome, tipo, sede, stato, data di installazione e Leggimi.
- **Manutenzioni**: il piano, con ogni quanto (in mesi o «semestrale», «annuale»…), prossima scadenza, controlli e
  contratto.
- **Progetti** e **attività**: codice, cliente, responsabile o assegnatari, stato, priorità, date, ore, voci da
  spuntare.
- **Scadenze dell'azienda**: certificazioni, polizze, contributi, con ogni quanto si ripetono e il preavviso.
- **Reperibilità**: i turni, con giorno e ora di inizio e fine.
- **Trattative**: un cliente che non è in anagrafica diventa il potenziale cliente, con telefono ed email.
- **Giacenze del magazzino**: le quantità di un foglio entrano come giacenza iniziale (un carico solo) oppure in un
  inventario da controllare e chiudere; l'export ha una colonna per ogni magazzino e furgone.

**Calendario (.ics)**: scadenze, manutenzioni, progetti, attività, turni di reperibilità e prossimi passi delle
trattative si esportano anche come calendario, da aprire in Outlook, Google Calendar o sul telefono.

**Collegamenti nelle importazioni**: il cliente, l'impianto, il progetto o la persona di una riga si riconoscono dal
codice, dalla partita IVA, dal codice fiscale o dal nome (anche senza la forma societaria). Quello che non si trova non
ferma la riga: finisce nelle note, «Da controllare».

Nella release anche i dati dimostrativi aggiornati alla 1.149.0.

## 1.148.0 · 20 ottobre 2026

**Importare ed esportare, uguale dappertutto** (prima parte: anagrafiche e listini). Le finestre «Importa» ed
«Esporta» di clienti e fornitori, rubrica, listino, listini dei fornitori, produttori, personale, mezzi e attrezzature e
monitoraggio funzionano ora allo stesso modo, e quello che esce si reimporta così com'è.
- **Qualsiasi foglio**: Excel, CSV o testo, letto come una tabella di database (la prima riga ha i nomi dei campi,
  sotto una scheda per riga). Le colonne con un nome noto si abbinano da sole, le altre si scelgono o le propone
  l'assistente AI.
- **Tutti i fogli del file**: un Excel con Foglio1, Foglio2, Foglio3… li mostra tutti, con le righe e le colonne
  riconosciute; si spuntano quelli da importare, anche più d'uno insieme. Nell'anteprima ogni riga dice da quale foglio
  e da quale riga viene.
- **Modello Excel da compilare** in ogni importazione: la riga dei campi già scritta e un foglio di istruzioni con i
  valori possibili e un esempio. Un foglio fatto con il modello, o esportato dalla piattaforma, salta la scelta delle
  colonne e va dritto all'anteprima.
- **La prima riga contiene già dei dati**: per i fogli senza la riga dei nomi (il programma se ne accorge da solo).
- **Esporta** apre una finestra unica: il formato, che cosa esportare (le schede scelte, quelle mostrate con i filtri
  o tutte) e le colonne. Le scelte restano per la volta dopo.
- **Clienti e fornitori**: export in Excel e in **vCard** per il telefono, Outlook e Google Contatti (anche i referenti,
  ognuno come contatto); la colonna «P.IVA/C.F.» dei gestionali si divide da sola tra partita IVA e codice fiscale; un
  CSV con colonne dai nomi sconosciuti passa sempre dalla scelta delle colonne, così non si perde niente.
- **Rubrica**: si importa anche da un foglio Excel o CSV qualunque e si esporta anche in Excel e CSV.
- **Listino e listini dei fornitori in METEL**: il listino al pubblico con la sigla dell'azienda, per un cliente o un
  altro gestionale, e i listini dei fornitori come li dà il produttore (con le famiglie di sconto).
- Guida utente: nuovo paragrafo *Importare ed esportare* (capitolo L'interfaccia) e i capitoli delle pagine aggiornati.

Nella release anche i dati dimostrativi aggiornati alla 1.148.0.

## 1.147.0 · 19 ottobre 2026

**Indicatori** (Azienda → Indicatori). L'andamento dell'azienda, dei reparti e, se si vuole, delle singole persone,
mese per mese: pezzi prodotti, rilavorazioni, ore, interventi chiusi nei tempi, preventivi accettati, fatturato,
crediti scaduti, persone in forza o qualunque altro numero si voglia seguire.
- **Misure**: quelle che il programma conta da solo (progetti, ore, assistenza, manutenzioni, preventivi, vendite,
  crediti, contabilità, personale) e quelle che si inseriscono a mano, anche importandole da Excel o CSV, con chi deve
  inserirle e il promemoria.
- **Indicatori**: si costruiscono dalle misure (per esempio rilavorazioni ÷ pezzi × 100), per mese, trimestre o anno,
  con obiettivo e soglia d'allarme. Il cruscotto li mostra con il grafico, il confronto con l'anno prima e il colore
  dello stato; la tabella li mette a confronto periodo per periodo. Quando un indicatore passa la soglia arriva un
  avviso a chi si è scelto.
- **Reparti e responsabili**: ogni responsabile vede il proprio reparto e le sue persone, senza bisogno di permessi.
- **Persone** (facoltativo): indicatori personali, valutazioni con voci a scelta, note dei colloqui e riepilogo da
  stampare e firmare, anche nella nuova linguetta *Indicatori* della scheda del personale. Si può lasciare che ognuno
  veda i propri.
- **Premi di fine anno** (facoltativo): fondo fisso o percentuale dell'utile, tre parti (azienda, reparto, persona) con
  i loro pesi, fasce, calcolo in proporzione per chi è entrato o uscito durante l'anno e forme del premio a scelta per
  persona. Tutti i nomi (del piano, delle parti, delle fasce, delle forme come «Welfare») si cambiano liberamente.
- **Modelli pronti** per produzione, squadre sul campo e ufficio, e configurazione da esportare e importare.
- **Periodi chiusi**: un mese chiuso conserva valori e obiettivi di allora, anche se poi si cambiano le formule.
- Nuovo gruppo di permessi *Indicatori*; il modulo è una sezione che si può spegnere in *Impostazioni → Sezioni*.

**La guida segue le sezioni**: i capitoli delle sezioni spente non compaiono più nella guida, nella sua ricerca e nelle
risposte dell'assistente AI.

**Dati dimostrativi nella release**: insieme al setup c'è `BlackHoleWorkspaces-demo-1.147.0.bhbak`, un backup con
un'azienda inventata e tutti i moduli pieni (Indicatori e Rubrica compresi) per provare la piattaforma su un PC di
prova; istruzioni nel README e in `BlackHoleWorkspaces-demo-LEGGIMI.txt`. Da ora ogni versione ha il suo.

## 1.146.1 · 19 ottobre 2026

- **Possibili doppioni anche nelle Password**: creando una voce, se tra quelle che vedi c'è già lo stesso utente (o la
  stessa email) sullo stesso sito o nello stesso «Dove si usa», compare l'avviso con il link alla voce e prima di
  salvare viene chiesta conferma. Lo stesso sito con un altro utente, o un nome simile, compaiono solo come
  informazione. Le password non si confrontano mai.
- **Guida utente**: nuovo paragrafo *Avviso dei possibili doppioni* (capitolo L'interfaccia), con la tabella di che
  cosa si controlla in ogni scheda; l'avviso ha la sua icona di aiuto con il rimando alla guida.

## 1.146.0 · 19 ottobre 2026

**Avviso dei possibili doppioni.** Mentre si compila una scheda, il programma controlla se c'è già: scrivendo
«Rossi srl» compare subito che in archivio c'è «Rossi S.r.l.», con il link per aprirla.
- **Possibile doppione** (avviso arancione): stesso nome, anche scritto con maiuscole, punteggiatura o forma societaria
  diverse, oppure stesso codice che identifica la scheda (partita IVA, codice fiscale, targa, matricola, codice
  dell'articolo, codice a barre, email…). Creando la scheda, il programma chiede conferma prima di salvarla.
- **Schede simili** (avviso azzurro): nomi che si somigliano, per esempio «Rossi Impianti» e «Rossi». È solo
  un'informazione.
- **Dove**: clienti e fornitori, rubrica, listino, produttori, mezzi e attrezzature, personale, impianti (dello stesso
  cliente), progetti e utenti.

## 1.145.1 · 19 ottobre 2026

Altre correzioni di sicurezza, dal terzo giro del controllo del codice. Si consiglia di aggiornare.
- **Programmi e pacchetti nei documenti e nei link**: la verifica della firma usa solo i certificati già presenti sul
  server, senza scaricarne altri da indirizzi scritti nel file; la scheda di un programma si ricorda e non si rifà a
  ogni apertura.
- **Anteprime con LibreOffice**: i collegamenti contenuti nei documenti (immagini, sezioni o oggetti presi da indirizzi
  web, cartelle di rete o file del server) non si aprono più e le macro restano disattivate. Se una conversione non
  riesce, il messaggio non mostra più dettagli del server.
- **Posta in uscita**: come per la PEC, cambiando server, porta, sicurezza o nome utente va scritta di nuovo la
  password.

## 1.145.0 · 19 ottobre 2026

Altre correzioni di sicurezza, dal secondo giro del controllo del codice. Si consiglia di aggiornare.
- **Contatti privati e progetti riservati**: non si possono più usare scegliendoli per numero in vendite, acquisti,
  gestione crediti, magazzino e monitoraggio da chi non li vede. Le bozze già fatte si modificano come prima; nel
  monitoraggio il cliente di un controllo si mostra come *Contatto riservato* a chi non lo vede.
- **Sintesi vocale**: gli audio di un cliente eliminato per sempre restano visibili solo agli amministratori.
- **Attività dei progetti riservati**: chi esce da un gruppo (o perde il permesso di vedere i progetti) non vede più
  la cartella delle attività del progetto.
- **Archivio di rete**: i file si aprono solo se sono davvero dentro la cartella dell'archivio, senza seguire
  collegamenti. Corretta la ricerca con parole di una o due lettere, che non trovava nulla.
- **PEC dello SDI**: cambiando server o nome utente della casella va scritta di nuovo la password.
- **Link di condivisione e anteprime**: limiti sugli archivi ZIP scaricati da un link (numero di file, dimensione e
  download insieme: la pagina spiega il motivo) e sui caricamenti in corso; le conversioni di disegni DWG e documenti
  Office che non riescono non si ripetono di continuo; la lettura del testo dei documenti e l'anteprima degli archivi
  ZIP hanno limiti di tempo e di dimensione.
- **Vendite e fatture dei fornitori**: i permessi si controllano prima di leggere i file caricati.

## 1.144.0 · 18 ottobre 2026

Correzioni di sicurezza, da un controllo del codice. Si consiglia di aggiornare.
- **Configurazione iniziale con un codice**: per creare il primo amministratore dal browser serve il codice del file
  `setup-code.txt` nella cartella dei dati, leggibile solo dagli amministratori del server. Aprendo la piattaforma
  dall'installazione o dall'icona del server il codice è già scritto. Le installazioni esistenti non cambiano.
- **Link di condivisione**: non mostrano più le cartelle con un permesso speciale (come i *Listini* dei produttori),
  che si condividono solo con un link fatto apposta su di loro. Il link di un impianto con i documenti lo crea solo chi
  vede la cartella dell'impianto. I file caricati con un link rispettano i limiti anche quando il programma che li manda
  non ne dichiara la dimensione.
- **Anteprima dei fogli di calcolo**: il testo formattato di un file si mostra come testo.
- **Dati riservati dei clienti**: IBAN, codice SDI e banche non si trovano più con la ricerca generale e nei
  suggerimenti da chi non li vede nella scheda. La ricerca nei documenti non usa più i nomi dei clienti che non si
  vedono.
- **PEC dello SDI**: si leggono solo i messaggi certificati dal gestore con lo SDI come mittente. Se usi l'invio con
  la PEC, dopo l'aggiornamento controlla che le ricevute continuino ad arrivare: i messaggi scartati restano non letti
  nella casella.
- **Preventivi**: l'indirizzo del link online lo vede solo chi compila i preventivi; riportando un preventivo in bozza
  il link si spegne e al nuovo invio se ne crea uno nuovo.
- **Recupero della password**: il limite di 3 email all'ora per account ora funziona.
- **Aggiornamento e motori dal browser**: più controlli che la richiesta arrivi davvero dalla rete locale.
- **Immagini da un indirizzo web**: rifiutati anche gli indirizzi IPv6 della rete interna.

## 1.143.7 · 18 ottobre 2026

- Il **«?»** accanto ai nomi dei campi non si illumina più passando con il mouse su tutta la riga: risponde solo
  sull'icona.
- **Crediti**: con più clienti scelti, il tasto destro su uno di loro propone *Manda N lettere* per tutti.

## 1.143.6 · 18 ottobre 2026

- **Filtri uguali in tutti gli elenchi**: accanto alla ricerca l'icona dell'imbuto apre al centro dello schermo la
  finestra con tutti i filtri; sull'icona il numero di quelli attivi, e sotto la barra le loro etichette con la × per
  toglierli (o *Togli tutti*). La barra resta su una riga. *Filtri…* anche nel menu di una riga.
- **Ordinamento delle schede** con un'icona e il suo menu (colonna e verso), anche sul telefono.
- **Più righe scelte**: il tasto destro (o ⋯) su una di esse mostra le azioni della scelta e vale per tutte; prima, per
  esempio in Documenti, eliminava solo quella cliccata.
- **Documenti** come gli altri elenchi: *Scegli più righe* a sinistra, *Elenco | Griglia* a destra.

## 1.143.5 · 18 ottobre 2026

- **Tipi e categorie senza chiudere la scheda**: nella scelta del tipo o della categoria (impianti, progetti, clienti,
  documenti, password) ci sono *Nuovo tipo…* / *Nuova categoria…*, che la crea e la sceglie, e *Gestisci l'elenco…*;
  anche con **F2** sulla scelta.
- **Rubrica a più righe**: con *Scegli più righe* si aggiungono o tolgono dai preferiti, si esportano e si spostano nel
  cestino tanti contatti insieme; nel cestino si ripristinano o si eliminano.
- **Impianti**: la cartella in Documenti si chiama come il tipo (*Antintrusione*), il nome dell'impianto resta una
  descrizione; la linguetta Documenti mostra il percorso vero della cartella. Il modello di partenza dell'antintrusione
  non crea più la cartella *Tecnoalarm*.
- **Cliente dalla Rubrica**: la scheda nasce normale, non più privata (la cartella in Documenti non è riservata).
- **Primi passi** in basso a sinistra, accanto al menu: una linguetta che sale col mouse sopra, e il riquadro che sale
  dal bordo.
- **Elenco/Schede** segnato già all'apertura degli elenchi; in Attività resta solo il selettore della pagina.
- Il **«?»** di un campo si apre solo sull'icona, non su tutta la riga; riga della Privacy del cliente allineata.

## 1.143.4 · 18 ottobre 2026

- **Pannello dell'assistente in ordine**: la modalità e *Nuova conversazione* sono sopra, il campo per scrivere è largo
  con *Invia* accanto e l'indicazione sotto, sul computer e sul telefono. Lo stesso in *Chiedi al documento*.

## 1.143.3 · 18 ottobre 2026

- **Rete locale a più righe**: con *Scegli più righe* si segnano tanti dispositivi insieme come conosciuti, ignorati o
  da eliminare. I conosciuti hanno la spunta verde accanto al nome, i nuovi la pastiglia *Nuovo*, e c'è il filtro
  *Conosciuti*.
- **Campi con la loro icona**: ogni campo che fa qualcosa (sito, indirizzo IP o nome di rete, MAC, coordinate, codice
  fiscale, partita IVA, importi, etichette…) ha la sua icona a destra e si distingue dai campi liberi; la spunta del
  controllo sta accanto all'icona, non sopra.
- **Etichette**: icona, aiuto che spiega come si aggiungono e si tolgono, un solo bordo quando il campo è attivo.
- **Calendario sul telefono**: *Copia l'indirizzo* lo ricopia quando serve; gli indirizzi creati prima vanno rifatti
  una volta.
- **Pagina di accesso rivista**: titolo fermo con gli errori, pulsanti alti quanto i campi, marchio uguale a tutte le
  larghezze.

## 1.143.2 · 18 ottobre 2026

- **Menu del telefono che restano aperti**: il menu che sale dal basso non sparisce più quando lo si tocca o trascina;
  se le voci sono tante scorrono dentro il menu, e si chiude con un tocco fuori o trascinandolo in giù (basta un gesto
  veloce). La pagina sotto resta ferma.
- **Scorrimento che non passa alla pagina**: arrivati in fondo al menu laterale, a un pannello, a una finestra o a un
  menu, la pagina principale non scorre più insieme.
- **Barra in alto del telefono più leggera**: restano menu, ricerca, notifiche, chat e profilo; assistente AI, radio e
  tema sono nel menu del profilo (la radio resta in barra mentre suona).

## 1.143.1 · 18 ottobre 2026

- **Testi incollati senza sorprese**: i caratteri che non si vedono e arrivano copiando da PDF, Word, pagine web o email
  (spazi di larghezza zero, segni di controllo, spazi «non separabili») si tolgono da soli al salvataggio, così ricerca
  e controlli trovano il testo anche incollato. Tabulazioni e a capo restano; password e note riservate restano come
  sono.
- **Testi lunghi su più righe** (una tabella copiata da Excel, un testo incollato dalla tastiera del telefono) entrano
  subito nelle descrizioni e nelle note: prima, con qualche centinaio di righe, la pagina poteva restare ferma per minuti.
- **Troppi dati**: un testo incollato enorme ferma il salvataggio con un messaggio che dice quanto pesa e cosa fare
  (accorciarlo o allegarlo come file), invece di «Server non raggiungibile» e della barra «Senza rete».
- **Fattura elettronica**: le virgolette tipografiche diventano quelle semplici (prima diventavano «?»), le lettere con
  segni che non ci sono in italiano tornano alla lettera di base (Dvořák → Dvorák), emoji e simboli si tolgono.
- Messaggi in italiano, con il nome del campo, quando un dato non si riesce a leggere.

## 1.143.0 · 17 ottobre 2026

- **Rubrica**, una pagina nuova in *La mia giornata*: i contatti che non sono clienti né fornitori (parenti, amici,
  tecnici di fiducia, numeri utili), personali oppure condivisi con colleghi, gruppi o tutti, con preferiti, cestino,
  foto o icona. Si importano dal telefono (vCard di iPhone e Android, CSV di Google Contatti e di Outlook) con
  l'anteprima, i doppioni riconosciuti e le foto, e si esportano in vCard.
- **Dalla rubrica ai clienti**: scrivendo un nome nei campi Cliente e Fornitore (preventivi, trattative, assistenza,
  attività, progetti, documenti, vendite, acquisti, pratiche) compaiono anche i contatti della rubrica; sceglierne uno
  apre la scheda cliente già compilata, che resta collegata al contatto.
- **Avviso di accesso**: un'email o un messaggio Telegram quando qualcuno entra con il tuo account, a ogni accesso o
  solo da un browser nuovo (*Profilo → Notifiche*).
- Indirizzi degli utenti e del personale con le coordinate e la mappa; **Genera** su ogni campo di una password nuova.
- **Elenchi tutti uguali**: *Scegli più righe* in alto a sinistra, il conteggio («3 di 7 contatti») in basso a sinistra,
  le indicazioni in basso a destra, e il menu della riga (tasto destro o ⋯) in ogni elenco; contatori sempre con il
  numero, anche 0, su fondo colorato.
- Interfaccia rifinita: notifiche sotto la barra in alto con il colore del tipo, altezze uniformi, barre con molti
  filtri su due righe; movimento rivisto, con dissolvenze anche quando il sistema chiede di ridurre le animazioni,
  pulsanti che rispondono alla pressione e menu che nascono dal pulsante che li apre.

## 1.142.0 · 17 ottobre 2026

- **Strumenti di rete**, una pagina nuova in *Strumenti*: diagnostica fatta dal server (ping in serie con perdita e
  jitter, traceroute con i nomi dei router, DNS con tutti i record e il server che scegli, WHOIS con RDAP, porte aperte
  con quello che dicono i servizi), il traffico delle schede di rete del server con l'andamento degli ultimi minuti e le
  **prove della connessione** (latenza, jitter e perdita verso il gateway e internet, DNS, download e upload), a mano o
  da sole ogni tante ore, con la storia e una nota che dice per che cosa basta la connessione.
- **Rete locale più ricca**, con le idee di WhoIs Pro: sistema operativo probabile dal TTL, indirizzi IPv6, porte UDP
  (DNS, orario NTP, SNMP con la descrizione del dispositivo, UPnP), che cosa dicono i servizi sulle porte aperte
  (programma e versione, certificato) e la storia delle porte aperte e chiuse, con l'avviso facoltativo delle porte
  nuove. L'elenco dei produttori si aggiorna da solo dall'IEEE alla prima scansione, se non ne è mai stato caricato uno.
- **Monitoraggio**: i ping mandano più pacchetti per controllo e misurano perdita e jitter (anche nell'andamento, con il
  grafico dei ping persi); un controllo diventa **rallentato** (pallino giallo) quando risponde oltre una soglia di tempo
  o di perdita; *Diagnostica* nella scheda apre il traceroute verso il dispositivo.
- **Tutti gli elenchi anche a schede**: con *Elenco | Schede* nella barra ogni voce si vede per intero in una scheda
  larga, con *Ordina per*; la scelta resta per ogni elenco.
- Barre di avanzamento nuove, piene e con un riflesso che scorre; negli elenchi lunghi frecce, Pag su/giù, Home e Fine
  fanno scorrere l'elenco.

## 1.141.2 · 16 ottobre 2026

- L'avviso di licenza è anche dentro il programma, in italiano e in inglese: nelle informazioni del file, in
  `AVVISO-LICENZA.txt` accanto all'eseguibile e in testa ai file dell'interfaccia. Ricorda che BlackHole Workspaces è
  gratuito ma non open source, anche a chi lo decompila o chiede a un assistente AI di estrarne o ricostruirne il codice.

## 1.141.1 · 16 ottobre 2026

- Scanner della rete locale: le marche dei produttori si cercano a parole intere. Prima alcuni produttori venivano
  scambiati per altri con un nome simile (per esempio Aztek per ZTE, quindi un apparato di rete, o Minimax per la
  centrale d'allarme Inim) e il tipo proposto era sbagliato.

## 1.141.0 · 16 ottobre 2026

- **Produttori più precisi nello scanner della rete locale**: per ogni dispositivo si usa il blocco di indirizzi MAC più
  preciso tra i tre registri dell'IEEE (MA-L, MA-M e MA-S), come in WhoIs Pro. Telecamere, domotica e apparati
  industriali mostrano il produttore vero invece di «IEEE Registration Authority».
- L'elenco dei produttori (oltre 58.000 blocchi) è **incluso nel programma**: il produttore si vede subito, anche senza
  internet. *Scarica l'elenco dall'IEEE* scarica i tre registri aggiornati; si possono anche caricare oui.csv, mam.csv,
  oui36.csv o il file manuf di Wireshark.
- Il tipo proposto riconosce anche le macchine virtuali, i telefoni dal nome e altri moduli di domotica.

## 1.140.0 · 16 ottobre 2026

- **Regole delle password**: in *Impostazioni → Sicurezza* l'amministratore sceglie la lunghezza minima (da 8 caratteri,
  12 consigliati con la piattaforma raggiungibile da internet) e la complessità (base, media con maiuscole, minuscole e
  numeri, alta anche con un simbolo). Valgono per tutte le password nuove; la pagina di accesso e i campi le dicono.
- **Password trafugate**: come fa Home Assistant, la piattaforma controlla con *Have I Been Pwned* se una password compare
  nei furti di dati, senza farla uscire dal server (parte solo l'inizio della sua impronta). Una password nuova
  trafugata viene rifiutata; chi entra con una password trafugata o che non rispetta più le regole riceve un avviso, o
  deve cambiarla subito se l'amministratore lo sceglie. Nell'elenco degli utenti le etichette *Password trafugata* e
  *Password debole*.
- Controllate anche le voci della **gestione password** (sezione *Trafugate* nella vista Controllo e avviso quando se ne
  salva una) e le **password dei servizi**: posta, PEC, NAS e password dei backup, archivio di rete.
- Senza internet, o se il servizio non risponde, non si blocca nulla.
- Le notifiche in alto a destra: la barra del tempo che resta si svuota verso destra, il lato da cui la notifica esce.

## 1.139.0 · 15 ottobre 2026

- **Sfoglia** per le cartelle del server: in *Backup*, *Archiviazione* e *Archivio di rete* la cartella si sceglie
  dall'elenco dei dischi del server e delle cartelle condivise dei NAS, come le vede il server, e se serve se ne crea una
  nuova.
- **Backup su un NAS**: se il NAS non lascia scrivere il servizio della piattaforma, si salvano utente e password della
  cartella di rete (cifrata); **Prova** dice se il server scrive nella cartella, con quale utente, e quanto spazio c'è. Il
  server entra nel NAS prima di ogni backup, anche quelli automatici della notte.
- Quando una cartella non si raggiunge o non si può scrivere, il messaggio dice con quale account ha provato il server e
  cosa fare.
- La cartella di lavoro, che contiene il database, non si sposta più in una cartella di rete: se la rete si interrompe il
  database si può rovinare. Sul NAS vanno i backup.

## 1.138.1 · 15 ottobre 2026

- Pagina **Sistema**: il campo di ricerca resta in vista sotto il titolo mentre si scorrono i riquadri, con il bordo
  intero.

## 1.138.0 · 15 ottobre 2026

- **Chi è collegato durante l'aggiornamento**: in *Impostazioni → Aggiornamento del programma* e nelle finestre che
  avviano il setup l'amministratore vede chi ha la piattaforma aperta (attivo o assente, quante pagine) e gli manda un
  **avviso** o l'**invito a non operare**; vede chi ha confermato e toglie l'avviso quando vuole.
- Chi lavora riceve l'avviso in una fascia in alto («Ho capito»); l'invito a non operare apre anche una finestra
  («Ho salvato, aspetto»). Tolto l'avviso, la piattaforma dice che si può riprendere.
- Quando il setup parte, l'avviso dell'aggiornamento arriva **da solo** a tutti; al ritorno del server la fascia offre di
  ricaricare la pagina con la versione nuova.
- **Durante l'aggiornamento non si entra**: la pagina di accesso mostra l'attesa e si riapre da sola appena il server è
  di nuovo online. Lo stesso per i **link di condivisione** e il **preventivo online**. Se il setup non parte, l'accesso
  si riapre da solo.

## 1.137.0 · 15 ottobre 2026

- **Sezioni del menu**: in *Impostazioni → Sezioni* l'amministratore spegne per tutta l'azienda le pagine che non usa
  (per esempio magazzino, vendite e contabilità per chi lavora solo con personale, assistenza e mezzi). Spariscono dal
  menu, dalla Home, dalla ricerca, dalle scadenze, dalle schede e dai pulsanti delle altre pagine e dalle notifiche, e i
  loro automatismi si fermano. I dati restano: riaccesa la sezione, torna tutto com'era.
- Le sezioni che servono ad altre si spengono e si riaccendono insieme (per esempio Impianti con Manutenzioni e
  Pratiche); chi ha la piattaforma aperta vede il menu cambiare da solo.

## 1.136.0 · 14 ottobre 2026 · prima versione pubblica

BlackHole Workspaces diventa **gratis per tutti**: il setup si scarica da questa pagina, senza limiti di utenti,
commesse o documenti e senza scadenza.

- **Scarica e installa**: quando esce una nuova versione, un amministratore la installa con un clic da *Sistema →
  Impostazioni → Aggiornamento del programma*. Il server scarica il setup da questa pagina, controlla che sia proprio
  quello pubblicato (impronta SHA-256), fa il backup completo dei dati e lo installa; la pagina si ricarica da sola.
- **Avviso delle nuove versioni** da questa pagina: una volta al giorno il server chiede a GitHub l'ultima versione e
  gli amministratori ricevono una notifica con le novità.
- **Licenza d'uso gratuita e responsabilità**: il setup la mostra da accettare e la copia nella cartella del programma
  (`LICENZA.txt`), accanto alle licenze dei componenti di terze parti.

Le novità delle ultime versioni, già comprese:

- **Pagina di accesso** rivista (marchio anche sul telefono e nelle finestre strette) e **bordo dei campi** attivi più
  netto in tutta la piattaforma; un campo sbagliato resta rosso mentre lo si corregge (1.135.1).
- **Pagina Sistema**: un riquadro per ogni pagina di gestione, con che cosa fa e le sue funzioni, e la ricerca (1.135.0).
- **Voce da testo**: l'audio creato si salva nei documenti del cliente o dell'impianto, oppure si scarica (1.134.0).
- **Fascia dei pannelli** con una regola sola in tutta la piattaforma: Annulla e il pulsante blu a destra, Altro a
  sinistra (1.133.0).
- **Voce da testo** in *Strumenti*: file audio da un testo con enfasi e pause, per centralini, annunci EVAC, video e
  social; motori OpenAI, Gemini, Piper sul server e voci di Windows; WAV, G.711, MP3 e M4A (1.132.0).
- **Valutazione del cliente** (come paga, quanto è fedele, quanto lavoro porta e quanto si guadagna), con il filtro
  nell'elenco clienti e il giudizio nei preventivi (1.130.0–1.131.0).
- **Disegni** nel visualizzatore come in un CAD: agganci, orto e polare, livelli, misure da preventivo e stampa in PDF
  vettoriale (1.126.0–1.129.0).
