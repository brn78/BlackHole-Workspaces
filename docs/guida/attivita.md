[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="attivita"></a>Attività

**La mia giornata → Attività** raccoglie le **cose da fare**: le tue, quelle da affidare ai colleghi e quelle da seguire insieme, con scadenze, priorità, persone assegnate, revisione, voci da spuntare, file e ore lavorate. È una funzione di base, come gli appunti: **tutti** creano attività, le ricevono e le condividono, senza permessi da assegnare. Un'attività sta in piedi da sola e, se serve, si collega a un [cliente](clienti.md) e a un [progetto](progetti.md).

La pagina ha due schede: **Attività**, con le viste elenco, kanban, calendario e Gantt, e **Ore**, il [registro delle ore](#attivita-ore). **Nuova attività**, in alto, c'è sempre. Ognuno vede le attività che lo riguardano (vedi [Chi vede un'attività](#attivita-condivisione)); quello che succede arriva nelle [notifiche](notifiche.md).

## <a id="attivita-scheda"></a>La scheda dell'attività

**Nuova attività** (in alto, nel kanban, nel calendario, nella Home, nella pagina di un progetto o nella scheda di un cliente) apre la scheda. Ogni attività ha un **numero** (`#12`) unico tra tutte le attività: non cambia e non viene riusato, nemmeno dopo un'eliminazione. I campi:

- **Titolo** e **Sottoattività di**: un'attività può essere il passo di un'altra più grande (un solo livello); le sottoattività compaiono nella scheda dell'attività principale, con l'avanzamento, e si aggiungono anche da lì scrivendo il titolo e premendo <kbd>Invio</kbd>.
- **Progetto**, facoltativo: **Nessun progetto** oppure uno dei progetti di cui [gestisci le attività](progetti.md#progetti-attivita). Collegata, l'attività porta il codice del progetto, compare nella sua pagina e la vede anche chi vede il progetto. Si scollega o si sposta in un altro progetto in ogni momento, cambiando il campo; le sottoattività stanno sempre nel progetto della principale e la seguono.
- **Cliente**, facoltativo: il cliente per cui si lavora; scegliendo un progetto che ha un cliente viene proposto il suo. L'attività compare nella [scheda Attività del cliente](clienti.md#clienti-documenti). Si scelgono solo i clienti che puoi vedere; un cliente collegato da altri che non puoi vedere compare come *Cliente riservato* e resta collegato.
- **Impianto**, facoltativo, per chi può vedere gli impianti: uno degli [impianti](impianti.md) del cliente scelto (prima quelli in servizio, poi i dismessi). L'attività diventa un suo [intervento](impianti.md#impianti-interventi) e compare nella pagina dell'impianto, anche dopo la chiusura del progetto; cambiando cliente, l'impianto di un altro cliente si toglie.
- **Stato**: **Da fare**, **In corso**, **In attesa** (ferma per qualcosa che non dipende da te), **In revisione**, **Completata**. **Priorità**: bassa, normale, alta, urgente (bandierina arancione o rossa).
- **Inizio** e **Scadenza**: un'attività scaduta e non completata è segnata in rosso ovunque; oggi e domani in evidenza. **Avviso alle**, facoltativo, è l'ora dei promemoria della scadenza (il giorno prima, il giorno stesso e se scade): arrivano a quell'ora nella campanella, per email e su Telegram, anche fuori dall'orario di lavoro. Vuoto: al mattino, come sempre, e su Telegram nell'orario di lavoro. Si copia nelle ricorrenze e nei modelli di progetto.
- **Assegnata a**, **Revisore** e **Ore stimate** (vedi i paragrafi che seguono), **Si ripete** (vedi [Attività ricorrenti](#attivita-ricorrenti)), **Etichette** e **Descrizione**, con grassetto, elenchi, caselle, colori e collegamenti come negli appunti.
- **Voci da spuntare**: i piccoli passi dell'attività. **Aggiungi voce** (o <kbd>Invio</kbd> in una voce) ne aggiunge un'altra; la **×** la toglie.
- **Condivisione**: i colleghi e i gruppi che ricevono l'attività, vedi [Chi vede un'attività e condivisione](#attivita-condivisione).

Le altre schede: **Commenti** (<kbd>Ctrl</kbd>+<kbd>Invio</kbd> invia; commenta chi lavora sull'attività e li ricevono assegnatari, revisore, chi l'ha creata e chi partecipa alla discussione), **Ore**, **File** e **Storico**, con chi ha cambiato che cosa: stato, date, persone, progetto, cliente, condivisione, file. Nel menu **⋯**: **Stampa**, **Apri il progetto** e **Apri il cliente** (se collegati), **Nuova sottoattività**, **Duplica**, **Elimina**. Eliminando un'attività spariscono anche le sue sottoattività, le voci, i commenti, le ore e la condivisione; i file collegati restano in Documenti.

**Duplica** (nel menu **⋯** della scheda e nel menu della riga, del kanban e del calendario) apre una **attività nuova** con gli stessi dati, da controllare prima di **Crea**: titolo con «(copia)», progetto, cliente, attività principale, date, priorità, ore stimate, persone, revisore, ricorrenza, etichette, descrizione, condivisione e voci da spuntare, tutte da fare. Lo stato riparte da **Da fare**; commenti, ore, file e sottoattività restano all'originale.

## <a id="attivita-da-testo"></a>Un'attività da un testo

Dalla 1.123.0, con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (in alto nella pagina Attività) apre un pannello dove incollare l'**email**, il **messaggio** o l'**appunto** con il lavoro da fare. L'assistente propone il **titolo**, la **descrizione** (senza saluti e firme), le singole cose da fare come **voci da spuntare**, la **priorità**, l'inizio e la **scadenza** («entro venerdì» diventa una data), le ore previste. Con **Da un file** il testo si legge anche da un PDF o da una scansione. **Proponi i dati** chiede all'assistente i dati e la piattaforma cerca il **cliente** tra quelli che vedi (partita IVA, email anche dei referenti, telefono, nome, poi un nome simile da controllare) e, con il cliente, il suo **impianto** dalle parole del testo. Si apre la scheda nuova **già compilata**, con in cima la nota dell'assistente: controlla, correggi e salva come sempre. Niente si salva da solo e il testo non si conserva.

## <a id="attivita-condivisione"></a>Chi vede un'attività e condivisione

Un'attività non è visibile a tutti. La vedono:

- chi l'ha **creata**;
- le persone **assegnate** e il **revisore**;
- chi la riceve in **condivisione**, direttamente o tramite un [gruppo di utenti](gruppi-policy.md) di cui fa parte;
- se è collegata a un progetto, chi **vede il progetto** (per un [progetto riservato](progetti.md#progetti-scheda), il responsabile e i membri);
- chi ha il permesso **Vedere tutte le attività** (o **Gestire tutte le attività**), tranne quelle collegate a un progetto riservato che non vede.

Una sottoattività la vede anche chi vede l'attività principale. Le attività di un [progetto riservato](progetti.md#progetti-scheda) restano comunque tra chi vede il progetto: se il progetto diventa riservato dopo, o toglie qualcuno dai membri, chi non lo vede più perde anche le sue attività (pure quelle che ha creato, che gli sono assegnate o che riceve in condivisione) e non ne riceve più le notifiche. Per tutti gli altri l'attività non esiste: non compare negli elenchi, nella ricerca, nella Home né nei conteggi.

**Condividere.** Nella sezione **Condivisione** della scheda, come per gli [appunti](appunti.md#appunti-condividere):

1. nel campo **Aggiungi un collega o un gruppo** scrivi qualche lettera e scegli dall'elenco un collega con l'account abilitato oppure un gruppo di utenti, con il numero dei suoi membri;
2. per ciascuno scegli **Può leggere** (la scelta iniziale) oppure **Può modificare**; la **×** lo toglie;
3. salva la scheda: ai nuovi destinatari arriva la notifica **Attività condivisa con te**.

- Chi riceve l'attività, anche con **Può leggere**, **ci lavora**: cambia lo stato, spunta le voci, commenta, collega i file e registra le ore. Con **Può modificare** cambia anche tutto il resto, condivisione compresa, e può eliminarla (vedi [chi può fare che cosa](#attivita-assegnare)).
- La condivisione la cambia chi può modificare l'attività. Non si condivide con sé stessi; al massimo **100** tra utenti e gruppi.
- Un gruppo porta l'attività a tutti i suoi membri, anche a chi entra in seguito; chi ne esce smette di vederla, a meno che la veda per un'altra via.
- Se l'attività è collegata a un **progetto riservato**, i colleghi della condivisione devono poter vedere il progetto e i gruppi devono esserne membri: altrimenti il salvataggio si ferma, con il nome di chi manca.
- Le attività dei [modelli di progetto](progetti.md#progetti-modelli) non si condividono.

## <a id="attivita-assegnare"></a>Assegnare e lavorare sulle attività

- In **Assegnata a** scegli una o più persone (fino a 20) tra i colleghi con l'account abilitato; **Assegna a me** aggiunge te. Chi viene assegnato riceve una notifica e trova l'attività in **Le mie** e nella Home.
- Il **Revisore** è chi controllerà il lavoro finito: vedi [Revisione](#attivita-revisione).
- Se l'attività è collegata a un **progetto riservato**, assegnatari e revisore si scelgono tra chi vede il progetto. Per collegare (o spostare) a un progetto riservato un'attività esistente anche chi l'ha creata deve vedere il progetto: altrimenti il salvataggio si ferma, con il suo nome.

| Chi | Che cosa può fare |
| --- | --- |
| Chi l'ha creata, chi la riceve con **Può modificare**, chi gestisce le attività del [progetto collegato](progetti.md#progetti-attivita), chi ha **Gestire tutte le attività** | **Modificarla**: titolo, date, progetto, cliente, persone, condivisione, sottoattività; eliminarla. In più tutto quello della riga sotto. |
| Assegnatari, revisore, chi la riceve in condivisione (anche con **Può leggere**) | **Lavorarci**: cambiare lo stato (si salva subito), spuntare le voci, commentare, caricare e collegare file, registrare le ore. Il resto della scheda è in consultazione. |
| Chi la vede per altre vie (il progetto collegato, **Vedere tutte le attività**) | Consultarla. |

Le sottoattività seguono la principale: chi può modificare l'attività principale, o lavorarci, può fare lo stesso sulle sue sottoattività, e per aggiungerne una bisogna poter modificare la principale. Gli amministratori possono tutto.

## <a id="attivita-viste"></a>Elenco, kanban, calendario e Gantt

Nella scheda **Attività** scegli quali vedere: **Le mie** (quelle che hai creato, assegnate a te, da rivedere da te o condivise con te), **Tutte** (tutte quelle che puoi vedere) oppure **Da rivedere** (quelle che puoi approvare, con il loro numero). Poi i filtri: il **progetto** (anche *Senza progetto*), il **cliente**, la **ricerca** (titolo, numero, etichetta, persona), lo **stato** (*Aperte*, cioè non completate, tutte, uno stato oppure *In ritardo*), la **priorità**, il **periodo** della scadenza e la persona assegnata (anche *Senza assegnatari*). A destra le quattro viste, ricordate nel browser:

| Vista | Che cosa mostra e come si usa |
| --- | --- |
| **Elenco** | Una riga per attività con numero, progetto, stato, priorità, persone e scadenza; un clic sull'intestazione ordina. Il **cerchio** a sinistra la completa, dopo una conferma (un clic per sbaglio non la fa sparire dalle aperte: le completate si ritrovano con il filtro **Tutti gli stati** o **Completata**), oppure la riapre. Dalla 1.124.3 la stessa conferma, con l'avviso di che cosa succede (la prossima occorrenza di una ricorrente, la revisione), c'è ovunque si completa con un clic: menu della riga, colonna «Completata» del kanban, stato nella scheda, spunta delle sottoattività; un clic sulla riga apre la scheda; il tasto destro o **⋯** danno le azioni: cambiare stato, approvare, registrare ore, nuova sottoattività, aprire il progetto, eliminare. |
| **Kanban** | Una colonna per stato. **Trascina** una scheda in un'altra colonna per cambiarne lo stato, o su e giù per decidere l'ordine; il **+** in testa alla colonna crea un'attività già in quello stato. La colonna *Completata* mostra le 30 più recenti (**Mostra le altre** per vederle tutte). Una scheda con la barra rossa è in ritardo; la barra verde è l'avanzamento delle voci e delle sottoattività. |
| **Calendario** | Le attività nel **giorno di scadenza**, per **Mese** o **Settimana**. Trascinale su un altro giorno per cambiarne la scadenza (l'inizio si sposta dello stesso numero di giorni); il **+** di un giorno crea un'attività che scade quel giorno; **+N altre** apre la settimana. Le attività senza scadenza non compaiono: il conto è sotto il calendario. Le **domeniche** hanno il numero in rosso, i **festivi** anche la casella rossa tenue con il nome della festa (dalla 1.97.0). |
| **Gantt** | Il cronoprogramma: una **barra** da inizio a scadenza per ogni attività, raggruppate per progetto (con la barra del progetto) e, in fondo, il gruppo *Senza progetto*; le sottoattività sotto la principale. Il **rombo** è un'attività con la sola scadenza; la parte colorata della barra è l'avanzamento; la linea rossa è oggi. **Trascina** una barra per spostarla, i suoi **bordi** per cambiare inizio o scadenza. Scala in **Giorni**, **Settimane** o **Mesi**; **Oggi** riporta alla data di oggi. Nella scala in giorni domeniche e festivi sono in rosso e i festivi hanno la colonna rossa tenue (il nome della festa passandoci sopra). |

Trascinare nel kanban richiede di poter lavorare sull'attività; nel calendario e nel Gantt, di poterla modificare. Sul telefono il kanban scorre di lato una colonna alla volta; per cambiare stato o date si usa la scheda. Dalla pagina di un progetto (**Apri in Attività**) e dalla scheda di un cliente (**Apri nella pagina Attività**) si arriva qui con il filtro del progetto o del cliente già scelto.

## <a id="attivita-revisione"></a>Revisione

- Il **revisore** è chi controlla il lavoro finito. Se c'è, chiunque altro porti l'attività a **Completata** la manda invece **In revisione**, e il revisore riceve la notifica «Da rivedere».
- Aprendo l'attività, il revisore trova in alto **Approva**, che la completa, e **Rimanda**, che chiede un commento su cosa rivedere e la riporta **In corso**: gli assegnatari e chi l'ha creata ricevono l'esito.
- Se c'è un revisore, approva solo lui. Un'attività **In revisione** senza revisore la approvano chi l'ha creata, il responsabile del progetto collegato e chi può modificarla. Senza revisore, portata a **Completata**, l'attività si completa direttamente.
- Le attività che aspettano te sono in **Da rivedere**, nella pagina e nella Home.

## <a id="attivita-ricorrenti"></a>Attività ricorrenti

In **Si ripete** scegli ogni giorno, settimana, mese o anno, ogni quanti (per esempio ogni 2 settimane) ed eventualmente **fino al**. Quando l'attività viene completata ne nasce la **successiva**, con un numero nuovo: stesso titolo, descrizione, progetto, cliente, persone e condivisione, voci da rifare, date spostate della ricorrenza, e gli assegnatari ricevono la notifica. Oltre la data *fino al* non ne nascono altre. Nell'elenco l'icona indica un'attività ricorrente. Si ripetono solo le attività principali, non le sottoattività.

## <a id="attivita-file"></a>File delle attività

- I file stanno in [Documenti](documenti.md), con revisioni, visualizzatore e permessi di sempre; l'attività ne tiene il collegamento.
- **Dove finiscono** i file caricati da un'attività: se è collegata a un progetto che ha la [cartella in Documenti](progetti.md#progetti-documenti), in quella cartella; altrimenti nella **cartella dell'attività**, **Documenti → Attività → *#12 titolo***, creata al primo caricamento. È riservata alle persone dell'attività (chi l'ha creata, assegnatari, revisore, colleghi e gruppi della condivisione), tutte con la modifica, ed è collegata al cliente dell'attività; si riallinea da sola quando cambiano persone, condivisione o cliente. Se l'attività è collegata a un progetto [riservato](progetti.md#progetti-permessi), la cartella la vedono solo le sue persone che vedono anche il progetto (e i gruppi membri del progetto); si riallinea anche quando il progetto diventa riservato o non lo è più, quando ne cambiano responsabile o membri e quando il progetto viene eliminato lasciando le attività.
- Nella scheda **File** dell'attività: **Carica file…** li carica e li collega (serve il permesso **Caricare documenti**), **Nuovo documento Word** apre l'[editor](documenti.md#documenti-editor) e salva il documento lì, **Collega un documento** cerca tra tutti i file che vedi in Documenti, in qualsiasi cartella e sottocartella. La **×** scollega il file dall'attività: il file resta in Documenti.
- Caricano, collegano e scollegano i file le persone che lavorano sull'attività. Un clic apre il file nel visualizzatore, per chi può **Visualizzare i documenti**. Un file messo nel cestino dei documenti resta nell'elenco barrato.

## <a id="attivita-ore"></a>Registro ore

- Le ore si registrano dalla scheda **Ore** di un'attività (giorno, durata, nota) oppure con **Registra ore** nella scheda **Ore** della pagina, cercando l'attività. La durata si scrive come viene: `1:30`, `2h`, `2h 15`, `45m` oppure `1,5` (ore). Non si registrano ore nel futuro.
- Registra ore chi lavora sull'attività, con o senza progetto: assegnatari, revisore, chi la riceve in condivisione e chi può modificarla. Ciascuno modifica ed elimina le proprie (un clic sulla riga le modifica); chi può modificare l'attività anche quelle degli altri.
- La scheda **Ore** mostra una **settimana** o un **mese** (frecce per spostarsi, **Oggi** per tornare), con il totale e la ripartizione per persona, per progetto (*Senza progetto* per le attività non collegate) e per cliente (quello dell'attività, altrimenti quello del suo progetto); si filtra per persona, progetto e cliente, si stampa e si scarica in **CSV** per Excel.
- Vedi le tue ore, quelle delle attività che puoi modificare (per esempio dei progetti di cui sei responsabile) e, con il permesso **Vedere le ore di tutti**, tutte le ore, tranne quelle dei progetti riservati che non vedi. Il totale di un'attività o di un progetto comprende sempre le ore di tutti.

## <a id="attivita-importa"></a>Importare ed esportare

**Esporta** scarica le attività mostrate, scelte o tutte in **Excel**, **CSV** o come **calendario** (un evento dall'inizio alla scadenza). **Importa** le porta da un foglio: titolo, progetto (codice o nome), cliente, impianto, stato, priorità, date, assegnatari (più nomi separati da virgola), ore previste, ora dell'avviso, voci da spuntare (separate da punto e virgola), etichette e descrizione. Il progetto si cerca tra quelli a cui puoi collegare attività; senza cliente vale quello del progetto. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="attivita-permessi"></a>Permessi

Per usare le attività non servono permessi: ognuno crea le sue, lavora su quelle che gli vengono assegnate o condivise e vede quelle dei progetti a cui ha accesso. Tre permessi delle [policy](gruppi-policy.md#policy-permessi) servono a chi coordina il lavoro degli altri:

| Permesso | Consente |
| --- | --- |
| Vedere tutte le attività | Vedere tutte le attività, anche quelle che non ci riguardano, tranne quelle collegate a un progetto riservato che non si vede. |
| Gestire tutte le attività | Modificare, riassegnare, condividere ed eliminare qualsiasi attività visibile (comprende Vedere tutte le attività). |
| Vedere le ore di tutti | Consultare il registro ore di tutte le persone, con i totali per persona, progetto e cliente. |

Sulle attività collegate a un progetto valgono anche i diritti del progetto: chi ne [gestisce le attività](progetti.md#progetti-attivita) (il responsabile, i membri con il ruolo *Gestisce le attività*, chi ha **Gestire le attività dei progetti**) le crea, le modifica e le elimina. Gli amministratori possono tutto.

## <a id="attivita-dal-vivo"></a>Lavorare insieme

La pagina, la Home, la scheda Attività dei clienti, la pagina dei progetti e la campanella si aggiornano da sole quando un collega cambia un'attività. Se due persone modificano la stessa attività insieme, il secondo salvataggio non sovrascrive il primo: compare «L'attività è stata modificata da … alle …: riaprila…»; riaprila e riporta le tue modifiche. Le operazioni rapide (stato, voci, commenti, ore, file) non entrano in conflitto: si applicano subito.

---

[← Home](home.md) · [Indice](README.md) · [Appunti →](appunti.md)
