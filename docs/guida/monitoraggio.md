[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="monitoraggio"></a>Monitoraggio

**Strumenti → Monitoraggio**. Il server controlla a intervalli regolari i dispositivi, i servizi e i siti che scegli: un NVR o un router con il ping, la porta di un servizio, la pagina web di un datalogger, di Home Assistant o del sito aziendale. Sai subito chi non risponde, da quanto, quanto ci mette a rispondere quando funziona e quanto è stato disponibile nei giorni e nei mesi, e chi deve saperlo riceve l'avviso nel sito e per email.

## <a id="monitoraggio-elenco"></a>La pagina

- In alto i filtri rapidi con quanti sono: **Tutti**, **Non raggiungibili** (con il pallino rosso), **Raggiungibili**, **In pausa**, **Disattivati**; sotto la ricerca (nome, indirizzo, gruppo, cliente, impianto, note) e il tipo, e il percorso del [gruppo](#monitoraggio-gruppi) aperto.
- Ogni riga: lo **stato** con da quanto (*Giù da 12 min*, *Su da 3 g*) e il motivo dell'ultimo controllo fallito; il **controllo** con il cliente e l'impianto; l'**indirizzo**; la **risposta**, cioè l'ultimo tempo in millisecondi con il piccolo grafico degli ultimi controlli (i trattini rossi sono quelli falliti); la **disponibilità** delle ultime 24 ore e degli ultimi 30 giorni (verde, gialla sotto il 99,95%, rossa sotto il 99%); l'ultimo controllo.
- Quelli non raggiungibili vengono per primi; **Non raggiungibili** comprende anche gli irraggiungibili dietro un apparato giù di una [topologia](#monitoraggio-topologia). La pagina si aggiorna da sola quando uno stato cambia, e ogni 30 secondi per tempi e disponibilità.
- Un clic apre la scheda; il tasto destro (o ⋯) dà **Controlla adesso**, la **pausa**, **Sposta nel gruppo**, **Duplica** ed **Elimina**. **Stampa** stampa i controlli del gruppo aperto (e di quelli dentro) con i filtri scelti, con la colonna del gruppo.

## <a id="monitoraggio-gruppi"></a>Gruppi e reti

I controlli si mettono in ordine nei **gruppi**, come i file nelle cartelle dei Documenti: una sede, una rete, un cliente, uno dentro l'altro fino a sei livelli (*Sede centrale / Rete telecamere*).

- **Nuovo gruppo** lo crea dentro il gruppo aperto: **Nome**, il **Tipo** (**Semplice**, una cartella, oppure **Topologia**, una rete con i collegamenti: vedi [sotto](#monitoraggio-topologia)), l'**icona** (al posto della cartella: un edificio per una sede, la rete per una VLAN), **Dentro a**, le **Reti** (una per riga, nella forma *192.168.1.0/24*, oppure un indirizzo solo), la **VLAN** e le note. Con le reti il modulo offre di spostarci subito i controlli senza gruppo che hanno l'indirizzo lì dentro.
- In cima all'elenco ci sono i gruppi del gruppo aperto, con lo stato riassunto (*2 non raggiungibili*, *Tutti raggiungibili*, quanti in pausa o in attesa) e la disponibilità media; un clic entra, il percorso in alto riporta indietro. Accanto al percorso le reti e la VLAN del gruppo aperto e **Modifica il gruppo**.
- Per spostare si **trascina** un controllo (o un gruppo) su un gruppo dell'elenco o su un pezzo del percorso; con le caselle se ne scelgono molti e si trascinano insieme, oppure si usa **Sposta in…** nella barra che compare, con **Pausa**, **Riprendi** ed **Elimina**. Un avviso dice che cosa è stato spostato e dove.
- Un **controllo nuovo** nasce nel gruppo aperto; scrivendo l'indirizzo, se è nella rete di un gruppo va da solo in quello (la rete più stretta vince), finché non scegli il gruppo a mano. Nel modulo il campo **Gruppo** lo cambia in ogni momento.
- Il menu di un gruppo (tasto destro o ⋯) dà **Nuovo controllo qui**, **Nuovo gruppo dentro**, la pausa di tutti i suoi controlli (per i lavori in una sede) e **Riprendi tutti i controlli**, **Modifica**, **Sposta in…** ed **Elimina il gruppo**: i controlli e i gruppi che contiene passano al gruppo sopra, nessun controllo si elimina.
- Con un filtro di stato, un tipo o la ricerca l'elenco mostra tutti i controlli del gruppo aperto e di quelli dentro, con il gruppo di ognuno: da **Tutti i controlli**, **Non raggiungibili** mostra quelli giù di tutte le sedi.
- Il gruppo compare anche negli avvisi e nelle email (*192.168.1.20 · Sede centrale / Rete telecamere*) e nei risultati della ricerca, che trova i controlli anche dal nome del loro gruppo.

## <a id="monitoraggio-topologia"></a>Topologia: router, switch e access point ad albero

Un gruppo di tipo **Topologia** disegna la rete com'è collegata, da sinistra a destra: il router, poi gli switch (o un nodo senza controllo, per esempio uno switch non gestito), poi gli access point, le telecamere, i server.

- Si comincia dall'apparato in cima (di solito il router). Ogni altro dispositivo ha, nel modulo, la sezione **Collegamento nella topologia**: **Collegato a** (l'apparato a monte, nello stesso gruppo), la **porta sull'apparato a monte** (*#49*), la **porta di questo dispositivo** (*#26*, *LAG1*) e la **velocità del collegamento** (*1000FDX*, *10G*, *Wi-Fi*). Un dispositivo senza apparato a monte resta da solo, in cima.
- Aprendo il gruppo si vede l'**albero**: ogni dispositivo con la sua icona, sotto il pallino dello stato, il nome e l'indirizzo; le linee sono verdi se il dispositivo a valle risponde, rosse se è giù, grigie tratteggiate se è irraggiungibile perché non risponde un apparato a monte; sopra la linea le porte (*#49 ↔ #26*), sotto la velocità. Il pulsante tondo accanto a un apparato **chiude il ramo** e mostra quanti dispositivi ci sono dietro (verde se rispondono tutti, rosso se qualcuno è giù); di nuovo per riaprirlo. In basso la legenda e l'ingrandimento. **Elenco**, accanto al percorso, torna alla tabella; **Stampa** dall'albero stampa la topologia (solo i dispositivi, senza lo spazio vuoto attorno) su un foglio orizzontale.
- **Ingrandire e scorrere**: la **rotellina** del mouse (o il pizzico del touchpad) ingrandisce e rimpicciolisce attorno al puntatore, da 25% a 200%; i pulsanti in basso fanno lo stesso (*−*, *+*; la percentuale torna al 100%), **Adatta** fa entrare tutta la topologia nella vista. Per scorrere si **trascina il fondo** (o si usano le barre). L'ingrandimento resta per le volte successive.
- **Spostare i dispositivi** (con il permesso di gestire il monitoraggio): si trascina un dispositivo dove si vuole e il suo **ramo lo segue**, con le linee che si adeguano mentre si muove; con <kbd>Maiusc</kbd> premuto si sposta **solo lui** e il ramo resta dov'è. Le posizioni si salvano sul server e le vedono tutti. Chi non è mai stato spostato sta al suo posto nell'albero, accanto al suo apparato a monte, e lo segue. Attorno al disegno c'è spazio libero in cui spostarli; portandoli oltre, il disegno si allarga. Dal tasto destro **Rimetti al suo posto nell'albero** annulla lo spostamento di un dispositivo; **Riordina**, in basso (o dal menu del gruppo), rimette tutti al loro posto, dopo una conferma.
- Per **collegare** si trascina un dispositivo sopra l'apparato a cui è collegato: l'icona di arrivo si illumina e, lasciato lì, il collegamento cambia (il dispositivo torna dov'era). Dal tasto destro: **Nuovo dispositivo collegato qui** (il modulo parte già collegato) e **Stacca dall'apparato a monte**. Non si può collegare un dispositivo a sé stesso né a uno che gli sta dietro.
- Un **nodo senza controllo** (tipo di controllo nel modulo) serve solo a disegnare: uno switch non gestito, un gruppo di client, un armadio. Non si controlla, l'indirizzo è facoltativo e può essere un testo qualsiasi; nella catena si guarda oltre lui.
- Eliminando un apparato, quelli collegati a lui passano al suo apparato a monte; spostando un dispositivo in un altro gruppo, o tornando il gruppo **Semplice**, i collegamenti si tolgono (i controlli restano). Anche la posizione scelta a mano vale solo nel suo gruppo: in un altro gruppo il dispositivo riparte dal suo posto nell'albero.

## <a id="monitoraggio-importa"></a>Importare ed esportare con Excel

**Esporta** ⬇ scarica in **Excel** o in **CSV** i dispositivi (quelli del gruppo aperto) che vedi (filtri compresi) o tutti, con le colonne scelte tra quelle che l'importazione riconosce: il file si sistema in Excel e si reimporta così com'è. Con il gruppo e l'apparato a cui è collegato.

**Importa** ⬆ (a chi può creare le schede) apre l'importazione guidata da un foglio **Excel** (.xlsx, .xls, .ods) o **CSV**, una riga per dispositivo, nel pannello a destra:

1. **Il file**, anche trascinandolo nel riquadro (al massimo 20 MB e 5.000 righe). **Scarica il modello Excel** dà il foglio già pronto con la riga dei campi e le istruzioni: compilato e importato così com'è, salta la scelta delle colonne. Un file con più fogli mostra quali importare (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)).
2. **Che cosa c'è in ogni colonna**: quelle con il nome giusto sono già scelte, le altre si scelgono a mano oppure, con l'assistente AI attivo, con **✨ Proponi con l'assistente**. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda.
3. **L'anteprima**: ogni riga con il suo esito (**Nuova**, **Già presente**, **Con errori**), i filtri per esito e una casella per scegliere che cosa importare. Un dispositivo è già presente con lo stesso tipo di controllo, indirizzo e porta.
4. **Importa** crea le schede una dopo l'altra, come dal modulo, con l'avanzamento e **Ferma**; l'esito dice quante sono state importate e, riga per riga, quelle non importate con il motivo.

Niente si perde: un valore che non va (un gruppo che non c'è) non ferma la riga, finisce nelle **note** della scheda dopo «Da controllare:».

I dispositivi vanno nel gruppo aperto, oppure in quello scritto nella colonna «Gruppo». Il **tipo di controllo**, se il foglio non lo dice, si capisce dall'indirizzo: un indirizzo http o https è un sito, con la porta è una porta TCP, altrimenti il ping. «Collegato a» resta nelle note: i collegamenti della topologia si fanno poi dalla scheda o trascinando.

## <a id="monitoraggio-controlli"></a>Un controllo

**Nuovo controllo** (a chi può **Gestire il monitoraggio**), poi la linguetta **Impostazioni**:

- **Nome**: come compare nell'elenco e negli avvisi (*NVR negozio*, *Home Assistant Rossi*).
- **Icona e colore**: per riconoscere il dispositivo nell'elenco (una telecamera, un router, un server); senza, l'icona del tipo di controllo. Vedi [Icone e colori](interfaccia.md#interfaccia-icone).
- **Tipo di controllo**:
   - **Ping**: il dispositivo risponde in rete (telecamere, NVR, router, switch, datalogger);
   - **Porta TCP**: un servizio è in ascolto su quella porta (per esempio la porta di un NVR o di MQTT);
   - **Sito web**: l'indirizzo http o https risponde con un codice accettato (vuoto = da 200 a 399; per una pagina che chiede l'accesso, per esempio *200-399, 401*); facoltativi il **testo atteso** nella pagina, l'avviso quando il **certificato** https sta per scadere e **Accetta un certificato non valido** per i dispositivi in rete con il loro certificato fatto da sé.
   - **Nodo senza controllo**: solo per la [topologia](#monitoraggio-topologia), non si controlla.
- **Indirizzo**: come lo raggiunge il server: un indirizzo IP (*192.168.1.20*), un nome (*nvr.local*) oppure, per un sito, l'indirizzo completo (*https://www.esempio.it*, *http://192.168.1.20:8123*). Per un dispositivo di un cliente raggiunto da internet, il suo indirizzo pubblico o il nome DDNS. **Prova** fa subito un controllo, senza salvare: dice se risponde, in quanto tempo, l'indirizzo IP raggiunto (rete locale o internet) e, per https, fino a quando vale il certificato.
- **Già controllato?** Scrivendo l'indirizzo, sotto compare chi controlla già lo stesso dispositivo (stesso IP o nome), con il nome cliccabile e il gruppo: in giallo se è lo **stesso controllo** (stesso tipo, indirizzo e porta), e allora salvando si chiede conferma prima di farne un altro uguale; in azzurro se è un altro controllo dello stesso dispositivo (per esempio il ping e la pagina web dell'NVR), che va bene. Se lo [scanner della rete](rete-locale.md) conosce il dispositivo, vale anche quando lo stesso dispositivo è scritto in un altro modo: l'indirizzo IP in un controllo e il nome nell'altro (con scritto *stesso dispositivo*, il nome e il MAC).
- **Ogni quanto** (da 30 secondi a un'ora), **Attesa della risposta** e **Giù dopo**: quanti controlli falliti di fila prima di dirlo non raggiungibile. Quando un controllo fallisce, le conferme partono dopo pochi secondi, senza aspettare l'intervallo: con 3, un pacchetto perso o un riavvio veloce non fanno scattare niente.
- **Cliente** e **Impianto**, facoltativi (vedi sotto), gli **avvisi** e le **Note**; in basso, nella fascia dei pulsanti, **Attivo** (spento: il controllo resta con la sua storia ma non si fa più).

> [!NOTE]
> **Senza internet.** Se manca la connessione a internet del server (l'[avviso di internet assente](interfaccia.md)), i controlli degli indirizzi fuori dalla rete locale non contano: il dispositivo non va giù e non parte nessun avviso finché internet non torna. Quelli della rete locale continuano come sempre.

## <a id="monitoraggio-rallentato"></a>Perdita, jitter e «rallentato»

Dalla 1.142.0 un controllo ping può mandare **più ping** per controllo (3, 5 o 10, uno ogni 200 ms; i controlli nuovi ne mandano 3): fallisce solo se non ne torna nessuno, e misura la **perdita** e il **jitter**, che compaiono nell'elenco, nell'andamento (con il grafico dei ping persi) e nella prova. Con **Rallentato oltre** (millisecondi, per ogni tipo di controllo) e **Oppure se perde più del** (percentuale, per il ping) il controllo diventa **rallentato**, con il pallino giallo e il motivo, quando risponde ma oltre le soglie per due controlli di fila; torna normale al primo controllo sotto le soglie. Rallentato non manda avvisi: è un segnale da guardare. Dalla scheda, **Diagnostica** apre gli [Strumenti di rete](strumenti-rete.md) con il traceroute verso il dispositivo.

## <a id="monitoraggio-andamento"></a>Andamento e interruzioni

La scheda si apre su **Andamento**: in alto lo stato, da quanto, l'ultimo controllo e il motivo dell'ultimo errore, con **Controlla adesso** e **Pausa**. Si sceglie il periodo (**24 ore**, **7 giorni**, **30 giorni**, **1 anno**):

- i numeri: la **disponibilità** e il tempo in cui è stato giù, la **risposta media** con la più veloce e la più lenta, le **interruzioni** con la loro durata media, i **controlli** fatti e quelli falliti;
- le **barre della disponibilità** per ora, giorno o mese (passa con il mouse per il valore e quanto è stato giù);
- il grafico dei **tempi di risposta**: la linea è la media, la fascia va dal più veloce al più lento, i segni rossi in basso sono i controlli falliti;
- per i siti https, fino a quando vale il certificato.

La linguetta **Interruzioni** elenca quelle del periodo: inizio, fine (o *in corso*), durata e motivo. Un'interruzione va dal primo controllo fallito al primo riuscito; il tempo in **pausa** non conta come interruzione. Si conservano ogni controllo per 8 giorni e i riassunti per ora per oltre un anno.

**Pausa** (per 1 ora, 4 ore, fino a domani alle 8, una settimana): durante lavori o manutenzioni il controllo non si fa e non parte nessun avviso; alla fine riprende da solo, oppure con **Riprendi**.

## <a id="monitoraggio-avvisi"></a>Avvisi

- **A chi**: gli utenti e i gruppi scelti nella sezione **Avvisi** del controllo e, con **Il reperibile di turno**, chi è [reperibile](reperibilita.md#reperibilita-avvisi) quando parte l'avviso (fuori orario, se scelto nella reperibilità, solo lui). Ricevono gli avvisi solo gli utenti che possono vedere il monitoraggio.
- **Quando**: quando non risponde (dopo i controlli falliti scelti), quando risponde di nuovo (con quanto è durata l'interruzione) e, per i siti https, una volta al giorno quando il certificato sta per scadere. **Se resta giù**: una volta sola, oppure di nuovo ogni ora, 4 ore, 12 ore o ogni giorno.
- **Un solo avviso nella topologia**: se non risponde un apparato a monte (il router), l'avviso arriva solo per lui, con quanti dispositivi ci sono dietro (*3 dispositivi collegati a valle*); quelli dietro diventano **Irraggiungibili** (pallino ad anello rosso), senza avvisi né interruzioni loro. Prima di dire giù un dispositivo, il server ricontrolla subito il suo apparato a monte, se non l'aveva appena fatto. Quando l'apparato torna su, quelli dietro si ricontrollano subito e tornano su con lui, in silenzio. Senza apparato a monte ogni dispositivo avvisa per conto suo, come sempre.
- **Dove**: nel sito, nella [campanella](notifiche.md), e, ognuno con la sua spunta (dalla 1.96.0), **Per email** e **Su Telegram** (a chi ha collegato la sua chat), appena succede (non dopo i soliti due minuti delle notifiche). Su Telegram arrivano subito anche fuori dall'orario di chi li riceve, se nel suo profilo ha lasciato **Gli avvisi del monitoraggio arrivano subito** (vedi [Quando disturbarmi](notifiche.md#notifiche-quando)). Ognuno può spegnerli nelle [preferenze delle notifiche](notifiche.md#notifiche-preferenze).
- Nella [Home](home.md), a chi vede il monitoraggio, il riquadro **Monitoraggio** mostra i dispositivi non raggiungibili e da quanto, oppure *Tutti raggiungibili*.

## <a id="monitoraggio-clienti"></a>Clienti, impianti e richieste di assistenza

Un controllo si collega, se serve, a un **cliente** e a uno dei suoi **impianti** (per esempio il datalogger del fotovoltaico o l'Home Assistant di casa Rossi). Allora compare anche nella linguetta **Monitoraggio** della [pagina dell'impianto](impianti.md) e della [scheda del cliente](clienti.md), con lo stato e la disponibilità degli ultimi 30 giorni; da lì **Nuovo controllo** parte con cliente e impianto già scelti.

Con il cliente, **Richiesta di assistenza** sceglie dopo quanto tempo di interruzione (da 15 minuti a un giorno) aprire da sola una [richiesta di assistenza](assistenza.md) per il cliente e l'impianto, con priorità alta, a nome di chi ha creato il controllo: una sola per interruzione. La richiesta compare nella scheda del controllo.

## <a id="monitoraggio-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere il monitoraggio | La pagina, le schede con l'andamento e le interruzioni, la linguetta di impianti e clienti, il riquadro della Home e i risultati nella ricerca; **Controlla adesso**; ricevere gli avvisi quando si è tra i destinatari. |
| Gestire il monitoraggio | Creare, modificare, mettere in pausa ed eliminare i controlli, scegliere a chi vanno gli avvisi e quando aprire una richiesta di assistenza; creare, modificare, spostare ed eliminare i gruppi. Chi vede soltanto sfoglia i gruppi. |

Gli stessi permessi valgono per la [Rete locale](rete-locale.md).

---

[← Condivisioni](condivisioni.md) · [Indice](README.md) · [Voce da testo →](voce-da-testo.md)
