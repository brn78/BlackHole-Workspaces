# Novità delle versioni

Il setup di ogni versione è nella pagina [Releases](https://github.com/brn78/BlackHole-Workspaces/releases).
Per aggiornare basta **Scarica e installa** in *Sistema → Impostazioni → Aggiornamento del programma* (dalla 1.136.0),
oppure caricare il setup nello stesso riquadro o eseguirlo sul server: dati, account e impostazioni restano.

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
