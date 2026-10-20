[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="progetti"></a>Progetti

**Commesse → Progetti** raccoglie le **lavorazioni** da organizzare: un cantiere, una commessa, uno sviluppo, una manutenzione, un lavoro interno. Ogni progetto ha una **pagina propria** con le [attività](attivita.md) collegate, i documenti e lo storico. La pagina compare a chi può **Vedere i progetti** (vedi [Permessi](#progetti-permessi)) e ha le schede **Progetti**, **Modelli** e, per chi ha il permesso riservato **Budget e consuntivo delle commesse**, **Economia** (vedi [Budget e consuntivo](#progetti-budget)). Ciò che un progetto installa presso il cliente diventa un [impianto](impianti.md), che resta anche quando il progetto si chiude.

## <a id="progetti-pagina"></a>L'elenco e la pagina del progetto

La scheda **Progetti** elenca i progetti che vedi, con il [tipo](#progetti-tipi) come etichetta colorata, stato, responsabile, avanzamento (attività completate sul totale e quelle in ritardo), scadenza e ore; i filtri mostrano gli aperti, uno stato, un tipo (o quelli senza tipo) o solo quelli in cui sei coinvolto. **Nuovo progetto**, in alto, crea un progetto vuoto oppure, se ci sono, un progetto da un [modello](#progetti-modelli).

Un clic su un progetto apre la sua **pagina**:

- in testa codice, nome, cliente, stato, responsabile, date e avanzamento (attività completate, in ritardo, prossima scadenza, ore registrate su quelle stimate), con i pulsanti **Stampa**, **Elimina**, **⋯** (nuova attività, cartella in Documenti, **Salva come modello**…) e **Modifica**, che apre la [scheda del progetto](#progetti-scheda) (**Scheda**, in consultazione, per chi non può modificarlo);
- la linguetta **Attività**: le [attività collegate](#progetti-attivita);
- la linguetta **Impianti**: gli [impianti](impianti.md#impianti-progetti) che il progetto realizza o modifica, per chi può vederli;
- la linguetta **Certificazioni**: le [certificazioni](certificazioni.md) collegate al progetto, per chi può vederle; **Nuova certificazione** parte da uno degli impianti del progetto;
- la linguetta **Preventivi**: i [preventivi](preventivi.md#preventivi-commessa) della commessa;
- la linguetta **Budget**, per chi ha il permesso riservato: il [budget e il consuntivo](#progetti-budget) della commessa;
- la linguetta **Documenti**: la [cartella del progetto](#progetti-documenti);
- la linguetta **Storico**: chi ha cambiato che cosa nel progetto (dati, responsabile, membri, riservatezza, cliente) e quali attività sono state create, completate, eliminate, collegate o scollegate.

L'indirizzo della pagina (`#/projects?project=…`) si può mandare a un collega: lo apre chi vede il progetto. La pagina si aggiorna da sola quando un collega cambia il progetto o le sue attività.

**Elimina**, per chi può modificare il progetto, chiede che cosa fare delle attività collegate:

- **Elimina il progetto e lascia le attività**: restano senza progetto, con le loro persone, ore, commenti e file, e nel loro storico resta scritto da quale progetto vengono. Chi le vedeva solo attraverso il progetto non le vede più: le vedono chi le ha create, assegnatari, revisore, chi le riceve in condivisione e chi elimina il progetto, con cui vengono condivise con **Può modificare** (così le ritrovi nella pagina Attività, in **Le mie**). È la scelta proposta per i progetti non riservati.
- **Elimina anche le attività**, con le sottoattività, le voci, i commenti e le ore, dopo un'altra conferma. È la scelta proposta per un **progetto riservato**: le sue attività, lasciate senza progetto, non sarebbero più riservate (le vedrebbe anche chi ha **Vedere tutte le attività**) e il loro storico non nomina il progetto.

La cartella in Documenti resta.

## <a id="progetti-scheda"></a>La scheda del progetto

**Nuovo progetto** e **Modifica** aprono la scheda:

- **Codice**: ne viene proposto uno con l'anno (`2026-001`, `2026-002`…), ma puoi scrivere quello che usi già, per esempio il numero di commessa. Deve essere unico.
- **Nome**, **Tipo** (dall'[elenco dei tipi](#progetti-tipi), con il suo colore; un progetto nuovo parte da «Progetto»), **Cliente** (il progetto compare nella [scheda del cliente](clienti.md#clienti-documenti)), **Responsabile** (di norma chi lo crea), **Stato** (Pianificato, In corso, In pausa, Completato, Annullato), **Inizio**, **Scadenza**, **Priorità**, **Ore stimate**, **Colore** (quello del codice nelle attività), **Etichette** e una **Descrizione** con testo formattato.
- **Persone**: i membri, utenti o gruppi, con il loro ruolo. Chi **Gestisce le attività** collega al progetto attività nuove o esistenti, le modifica, le assegna e le elimina; chi **Partecipa** vede il progetto e le sue attività e lavora su quelle che lo riguardano. Il **responsabile** modifica anche il progetto e approva le attività che non hanno un revisore.
- **Progetto riservato**: lo vedono solo il responsabile e i membri; per gli altri non esiste, nemmeno nella Home o nella scheda del cliente. Le sue attività restano tra le persone del progetto: assegnatari, revisore e colleghi della condivisione devono poterlo vedere, e chi ha **Vedere tutte le attività** non le vede se non è tra i membri. Rendendo riservato un progetto, o togliendo un membro, chi non lo vede più perde anche le sue attività e le relative notifiche. Nello storico delle attività un progetto riservato non si nomina (*Collegata a un progetto riservato*).
- **Cartella in Documenti**: vedi [Documenti del progetto](#progetti-documenti).

Se due persone modificano lo stesso progetto insieme, il secondo salvataggio non sovrascrive il primo: un messaggio chiede di riaprire la scheda per vedere la versione aggiornata.

## <a id="progetti-tipi"></a>Tipi dei progetti

Il **tipo** (Progetto, Commessa, Sviluppo, Manutenzione, Assistenza, Interno…) si sceglie da un elenco uguale per tutti, come le [categorie dei clienti](clienti.md#clienti-categorie): ogni tipo ha il suo colore, che l'elenco dei progetti e dei modelli mostra come etichetta accanto al nome. Chi ha il permesso **Gestire i tipi dei progetti** trova in cima alla pagina il pulsante **Tipi**: nel pannello dei [tipi e delle categorie](interfaccia.md#interfaccia-tipi) li aggiunge, li rinomina, ne sceglie icona e colore e li elimina, vedendo quanti progetti e modelli usano ciascuno. Eliminando un tipo, i suoi progetti restano senza tipo. Un progetto creato da un modello prende il tipo del modello.

## <a id="progetti-attivita"></a>Le attività del progetto

- La linguetta **Attività** della pagina del progetto elenca le attività collegate, comprese le sottoattività, con stato, scadenza e persone; un clic apre la scheda dell'attività. **Nuova attività** ne crea una già collegata al progetto; **Apri in Attività** mostra le stesse attività nella [pagina Attività](attivita.md#attivita-viste), con il kanban, il calendario e il Gantt.
- Un'attività già esistente si collega dalla sua scheda, scegliendo il progetto nel campo **Progetto**; con **Nessun progetto** si scollega. Le sottoattività seguono sempre la principale.
- Collegano attività al progetto, e le creano già collegate, quelli che ne **gestiscono le attività**: il responsabile, i membri con il ruolo *Gestisce le attività*, chi ha il permesso **Gestire le attività dei progetti** (se non è membro con il ruolo *Partecipa*) o **Gestire tutti i progetti**. Le stesse persone modificano ed eliminano tutte le attività del progetto. Per scollegare un'attività basta poterla modificare; per spostarla in un altro progetto bisogna anche gestire le attività di quello.
- Chi vede il progetto vede anche le sue attività; ci lavorano, come sempre, assegnatari, revisore e chi le riceve in condivisione (vedi [chi può fare che cosa](attivita.md#attivita-assegnare)).
- L'avanzamento del progetto conta tutte le attività collegate, sottoattività comprese; le ore del progetto sono quelle registrate sulle sue attività.

## <a id="progetti-documenti"></a>Documenti del progetto

- Alla creazione del progetto, con la casella **Crea la cartella del progetto in Documenti** spuntata, nasce la cartella **Documenti → Progetti → *codice nome***, collegata al cliente e, se il progetto è riservato, riservata alle stesse persone: i membri con il loro ruolo e il responsabile con la modifica. Si riallinea da sola quando cambiano riservatezza, cliente, responsabile o membri.
- La linguetta **Documenti** della pagina del progetto mostra il contenuto della cartella: un clic apre un file nel visualizzatore, **Apri in Documenti** porta alla cartella nella pagina [Documenti](documenti.md). Se la cartella manca, **Crea la cartella** la aggiunge (per chi può modificare il progetto). Per vedere i file serve il permesso **Visualizzare i documenti**.
- È lì che vanno i [file delle attività](attivita.md#attivita-file) collegate al progetto.
- Eliminando il progetto la cartella resta in Documenti, con i suoi file.

## <a id="progetti-modelli"></a>Modelli di progetto

- Un **modello** raccoglie le attività tipo di un lavoro che si ripete (un'installazione, un sito, una pratica): la scheda **Modelli** li elenca e un clic apre la pagina del modello, con le sue attività tipo, che si creano e si modificano come le altre. Le date sono **giorni dall'inizio del progetto** (*Inizio: giorno 0*, *Scadenza: giorno 5*). **Nuovo modello** ne crea uno vuoto.
- **Usa** (o **Nuovo progetto → da un modello**) chiede codice, nome, cliente, responsabile e data di inizio, e crea il progetto con tutte le attività: i giorni diventano date vere e ogni attività prende un numero nuovo. Puoi copiare i membri del modello e mantenere le persone assegnate (in un progetto riservato, solo quelle che lo vedono).
- **Salva come modello**, nel menu **⋯** della pagina di un progetto, crea un modello da un progetto riuscito: le date diventano giorni dall'inizio; commenti, ore e file non si copiano.
- Le attività dei modelli si vedono solo dal modello: non compaiono nella pagina Attività, nella ricerca né nella Home, non si condividono e non hanno ore né file.
- La scheda Modelli c'è per chi può creare progetti o gestirli tutti; i modelli li crea e li modifica chi può **Gestire tutti i progetti**.

Nella scheda Modelli, **Esporta tutti** e **Importa…** (e **Esporta il modello in un file** nel menu **⋯**) portano i modelli, con le attività tipo e i membri per nome, su un altro server: vedi [Modelli tra server](impostazioni.md#impostazioni-modelli).

## <a id="progetti-budget"></a>Budget e consuntivo

Per ogni commessa si confronta quanto si era **previsto** con quanto si è **speso** e **fatturato**, mentre il lavoro va avanti. Lo vede solo chi ha il permesso riservato **Budget e consuntivo delle commesse** (nella policy proposta Amministrazione): nella pagina della commessa la linguetta **Budget**, nella pagina Progetti la scheda **Economia** con tutte le commesse.

- **Il previsto**: ricavo, ore di manodopera e costi per voce (manodopera, materiale, prestazioni esterne, altre spese). Finché non lo scrivi vale la **proposta dai preventivi accettati** della commessa: il loro imponibile (con lo sconto) come ricavo, il costo delle righe per tipo (materiale, prestazioni, manodopera), le ore di manodopera e di posa; le ore di posa sono valorizzate al costo orario medio del personale. **Scrivi il budget** apre il pannello a destra con i numeri proposti, da correggere; **Riprendi la proposta** li rimette, **Togli il budget** torna alla proposta. Nel pannello anche la soglia dell'**avviso** (90 % se non la cambi) e le note.
- **Il fatto** si calcola da solo da quello che c'è già nel programma:
   - **manodopera**: le ore registrate sulle attività della commessa per il costo orario di ogni persona: quello della sua [scheda del personale](personale.md), altrimenti quello della manodopera del listino per la sua mansione, altrimenti il costo orario medio del personale (le ore senza nessun costo sono segnalate);
   - **materiale**: gli scarichi di magazzino per la commessa (anche quelli dei DDT) meno i rientri dal cantiere, al costo del movimento, più la merce ancora nel magazzino presso il cliente collegato alla commessa;
   - **fatture dei fornitori** collegate alla commessa (o abbinate ai suoi ordini), per voce secondo la voce del listino della riga (senza voce: altre spese); le note di credito in meno. Le righe arrivate in magazzino con l'ordine non contano qui: contano quando la merce si scarica sulla commessa, così non si contano due volte.
- **L'impegnato**: degli ordini ai fornitori della commessa inviati o confermati, quanto non è ancora arrivato in magazzino né fatturato; più (dalla 1.113.0) la merce arrivata in magazzino con gli ordini della commessa e non ancora scaricata su di lei, al prezzo dell'ordine (la tabella **In magazzino per la commessa**): è già comprata per la commessa, e quando si scarica o va con un DDT diventa fatto.
- **A finire**: per ogni voce il più alto tra il previsto e fatto + impegnato; il **margine a finire** è il ricavo previsto meno i costi a finire. Il **fatturato** sono le fatture emesse meno le note di credito della commessa (o dei suoi preventivi); i DDT ancora da fatturare sono indicati a parte.

In cima alla linguetta i numeri principali (ricavo e costi previsti, fatti e impegnati, margine previsto e a finire, fatturato), poi la tabella voce per voce con la barra dell'uso del previsto (piena per il fatto, più chiara per l'impegnato; gialla oltre la soglia dell'avviso, rossa oltre il previsto), i costi per mese e il dettaglio: ore per persona con il costo orario e da dove viene, registrazioni di magazzino, fatture dei fornitori, ordini aperti e vendite (un clic apre il documento). La commessa è **Nel budget**, **Vicino al budget** (fatti + impegnati oltre la soglia, oppure una voce vicina o oltre il suo previsto) o **Fuori budget** (oltre il previsto in tutto).

**L'avviso arriva da solo**: ogni 10 minuti il server guarda le commesse aperte (in programma, in corso o sospese) e, quando una diventa **Vicino al budget** o **Fuori budget**, manda una [notifica](notifiche.md) a chi ne vede budget e consuntivo (amministratori e chi ha il permesso riservato, se vede la commessa), con la percentuale e le voci oltre il previsto, senza importi. Arriva una volta sola per ogni passo: se il budget si alza e la commessa torna sotto, il successivo sforamento avvisa di nuovo. Il clic apre la linguetta Budget della commessa. Chi non la vuole la spegne nelle preferenze delle notifiche.

La scheda **Economia** della pagina Progetti elenca le commesse con ricavo e costi previsti, fatti + impegnati, uso del previsto, fatturato e margine a finire, con i totali sotto le colonne; i riquadri in cima e il filtro mostrano le aperte, quelle fuori budget, vicine al budget, senza budget o concluse. **Stampa** stampa l'elenco com'è. Scrivere o togliere un budget resta nello **Storico** della commessa (senza importi) e nel registro attività.

## <a id="progetti-importa"></a>Importare ed esportare

**Esporta** scarica i progetti in **Excel**, **CSV** o come **calendario** (un evento dall'inizio alla scadenza). **Importa** (a chi crea i progetti) li porta da un foglio: codice (vuoto: il prossimo libero), nome, tipo, cliente, responsabile (nome utente o nome e cognome), stato, priorità, date, ore previste, etichette e descrizione. Un cliente, un responsabile, uno stato che non si trovano finiscono nella descrizione, «Da controllare». Ogni progetto ha la sua cartella in Documenti. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="progetti-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere i progetti | Aprire la pagina Progetti e vedere i progetti non riservati (e quelli riservati di cui si è responsabili o membri), con le attività collegate; sulle attività si lavora secondo i propri diritti. |
| Gestire le attività dei progetti | Collegare, creare, modificare, assegnare ed eliminare le attività dei progetti che si vedono, tranne quelli in cui si è membri con il ruolo *Partecipa*. |
| Creare progetti | Creare progetti (anche da un modello): chi crea ne diventa responsabile, se non ne sceglie un altro. |
| Gestire tutti i progetti | Modificare ed eliminare qualsiasi progetto visibile, i suoi membri e le sue attività, e creare e modificare i modelli. |
| Gestire i tipi dei progetti | Aggiungere, rinominare, colorare ed eliminare i [tipi dei progetti](#progetti-tipi), uguali per tutti. |
| Budget e consuntivo delle commesse *(dati riservati)* | Vedere il [budget e il consuntivo](#progetti-budget) delle commesse che si vedono (con il costo delle ore di ogni persona, il materiale, gli acquisti e il fatturato) e scriverne il budget. |

Inoltre il **responsabile** di un progetto lo modifica e ne gestisce le attività, e i membri con il ruolo **Gestisce le attività** ne gestiscono le attività, anche senza i permessi qui sopra. Le ore stanno nel [registro ore delle attività](attivita.md#attivita-ore) (permesso **Vedere le ore di tutti**). Gli amministratori possono tutto.

---

[← Produttori](produttori.md) · [Indice](README.md) · [Impianti →](impianti.md)
