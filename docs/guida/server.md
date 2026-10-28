[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="server"></a>Server e installazione

## <a id="server-installazione"></a>Installazione

Il programma di installazione (`BlackHoleWorkspaces-<versione>-Setup.exe`) si esegue sul PC o server che ospiterà la piattaforma, con diritti di amministratore. Alla prima installazione chiede la **cartella dei dati** (vedi sotto). Poi chiede la **porta TCP** (predefinita 5180) e, sempre alla prima installazione, l'**account amministratore** (facoltativo, vedi [Configurazione iniziale](accesso.md#accesso-primo-avvio); sotto la conferma della password la pagina dice subito se le due password coincidono). Installa poi il **servizio di Windows** «BlackHole Workspaces», che parte da solo a ogni avvio del sistema (con **avvio ritardato**, quando il server è meno impegnato) anche senza utenti collegati e si riavvia in caso di errore. Con il servizio installa l'[icona di stato](#server-icona-stato), apre la porta nel Firewall di Windows per le reti Private e di Dominio (a richiesta anche per le Pubbliche) e crea i collegamenti nel menu Start.

**La cartella dei dati** contiene database, impostazioni, documenti, chiavi di cifratura e backup automatici. Il setup propone `C:\ProgramData\BlackHoleWorkspaces`; su un server conviene una cartella su un disco dati locale, per esempio `D:\BlackHole Workspaces\Dati`.

- Non si può scegliere una cartella di rete né un'unità di rete: con il database in rete i dati rischiano di rovinarsi.
- Non si può scegliere la radice di un disco, la cartella dei programmi né quella del programma.
- Se la cartella contiene già i dati della piattaforma (per esempio dopo una reinstallazione), il programma usa quelli.
- Se contiene altri file, il setup chiede la conferma: la piattaforma ci crea le sue cartelle accanto, senza toccarli.

La scelta finisce nelle impostazioni dell'installazione (`appsettings.Local.json`). Negli aggiornamenti la pagina non compare: i dati restano dove sono, e si spostano da [Sistema › Archiviazione](archiviazione.md#archiviazione-cambio), che copia e verifica ogni file. Nell'installazione non presidiata la cartella si indica con `/DATADIR="D:\BlackHole Workspaces\Dati"`.

In alternativa, il pacchetto compresso (cartella con `BlackHoleWorkspaces.exe`) si avvia con un doppio clic e tiene i dati nella sottocartella `data`; gli script `Install-Service.ps1` e `Uninstall-Service.ps1` installano e rimuovono a mano il servizio, la regola del firewall e l'icona di stato.

## <a id="server-windows-server"></a>Windows Server

Sono supportati Windows Server 2016, 2019, 2022 e 2025, anche **Server Core**, oltre a Windows 10 e 11. Tutto il necessario è incluso nel setup.

- **Amministratore**: crealo nella pagina **Account amministratore** del setup e accedi da un PC della rete: sul server spesso manca un browser adatto (Internet Explorer non è supportato, Server Core non ha browser).
- **Rete Pubblica**: su un server non in dominio Windows classifica spesso la rete come Pubblica. Seleziona nel setup anche le **reti Pubbliche** oppure classifica la rete come Privata.
- **Server Desktop remoto**: usa sempre il servizio; senza, ogni utente collegato avvierebbe una propria copia del programma sulla stessa porta.

## <a id="server-icona-stato"></a>Icona di stato sul server

Con il servizio, il setup installa un'icona nell'area di notifica, accanto all'orologio, per chiunque accede al server, anche in Desktop remoto. Ogni 5 secondi controlla il servizio e la piattaforma; il pallino ne indica lo stato:

- **Verde**: in funzione, la piattaforma risponde. Passando con il mouse compare anche la versione.
- **Giallo**: avvio, arresto o aggiornamento in corso; primi minuti dopo l'avvio di Windows (avvio ritardato); [spostamento della cartella di lavoro](archiviazione.md#archiviazione-cambio) in corso.
- **Rosso**: servizio fermo, oppure avviato ma la piattaforma non risponde. Se dura più di un minuto e mezzo compare un avviso di Windows, e un altro quando torna in funzione.
- **Grigio**: servizio non installato.

Doppio clic: apre la piattaforma. Clic destro: **Apri BlackHole Workspaces**, **Apri la cartella di lavoro** e **Apri la cartella dei backup** (le apre in Esplora risorse la pagina [Archiviazione](archiviazione.md#archiviazione-apri), nel browser del server e dopo l'accesso se serve: solo per gli amministratori), **Avvia il servizio** o **Riavvia il servizio** (Windows chiede la conferma da amministratore), **Aggiorna il programma…**, **Servizi di Windows**, **Chiudi l'icona**: il servizio continua a funzionare e l'icona ricompare al prossimo accesso a Windows, o subito dal menu Start. Dopo un aggiornamento l'icona passa da sola alla nuova versione. Su Server Core, senza area di notifica, non viene installata.

**Aggiorna il programma…** apre, nel browser del server, il riquadro **Aggiornamento del programma** della piattaforma (dopo l'accesso, se serve): dal server l'aggiornamento è sempre consentito. Quando su GitHub esce una [nuova versione](#server-nuove-versioni), la voce diventa **Aggiorna alla versione …** in grassetto, il numero compare in cima al menu e passando con il mouse, e un avviso di Windows lo segnala una volta sola per versione (un clic sull'avviso apre lo stesso riquadro).

## <a id="server-icona"></a>Avvio con doppio clic

Avviato con doppio clic (senza servizio), il programma non apre finestre: compare un'**icona nell'area di notifica**. Clic destro per il menu: **Apri BlackHole Workspaces**, **Mostra la finestra dei messaggi**, **Apri la cartella di lavoro**, **Apri la cartella dei backup**, **Esci e arresta il server**. Un secondo avvio non crea una seconda copia ma apre la piattaforma nel browser.

> [!WARNING]
> Avviato così il programma dipende dall'utente collegato: chiudendo la sessione di Windows si ferma. Per un server sempre attivo usa il **servizio di Windows** installato dal setup.

## <a id="server-rete"></a>Accesso dagli altri PC

Dagli altri PC la piattaforma risponde su `http://<nome-del-server>:5180` (o l'IP del server). Se non si raggiunge: verifica che la rete del server sia classificata **Privata** o di Dominio, che la porta sia quella scelta e che il servizio sia in esecuzione (icona di stato verde).

Per l'avviso **Internet assente** il server prova ogni minuto (ogni 20 secondi mentre manca) gli indirizzi di controllo usati anche da Windows e da Android (*www.msftconnecttest.com* e *connectivitycheck.gstatic.com*): rispondono con un testo o un codice noto, così un router che risponde al loro posto non inganna. I cambi finiscono nel registro del servizio (Visualizzatore eventi di Windows).

## <a id="server-aggiornamento"></a>Aggiornare

**Con un clic** (dalla 1.136.0): quando esce una nuova versione, in **Impostazioni → Aggiornamento del programma** c'è **Scarica e installa**. Confermi con la tua password, lasciando selezionato **Crea prima un backup completo**, e il server fa tutto da solo, con una barra che mostra a che punto è:

1. **scarica** il setup dalla pagina ufficiale del programma su GitHub (solo da lì);
2. **controlla** che sia proprio il file pubblicato (dimensione e impronta **SHA-256** indicata da GitHub), che sia il setup di BlackHole Workspaces e che sia della versione annunciata: se qualcosa non torna non installa niente e dice il motivo;
3. crea il **backup** completo dei dati;
4. **installa**: il servizio resta fermo per circa un minuto e la pagina si ricarica da sola con la nuova versione.

Prima di confermare, la finestra mostra **chi è collegato**: puoi avvisarlo o invitarlo a non operare e aspettare che confermi (vedi [Chi è collegato durante l'aggiornamento](#server-collegati)).

Valgono le stesse regole del caricamento a mano (amministratori, rete locale, servizio installato dal setup, un aggiornamento alla volta); nel [registro attività](registro.md) restano lo scaricamento, l'aggiornamento avviato «con SHA-256 verificato» oppure il motivo per cui non è riuscito. Se il server non raggiunge GitHub (niente Internet, firewall), scarica il setup dal tuo PC e caricalo come descritto qui sotto.

**Caricando il setup**: **Impostazioni → Aggiornamento del programma**, scegli il nuovo setup (`BlackHoleWorkspaces-<versione>-Setup.exe`) o trascinalo nel riquadro. Il file viene **controllato subito**, prima di chiedere la password e di caricarlo sul server:

- se non è un programma di installazione, se è il setup di un altro programma o un altro file di BlackHole Workspaces, viene rifiutato all'istante con un messaggio che dice che cosa è stato scelto;
- se è di una **versione precedente** a quella installata viene rifiutato, indicando le due versioni: dalla piattaforma non si torna indietro;
- se è quello giusto, la finestra di conferma mostra **Setup di BlackHole Workspaces** con la sua versione e dice se è un **aggiornamento** dalla versione installata oppure una **reinstallazione** della stessa versione.

Lascia selezionato **Crea prima un backup completo** e conferma con la tua password. Il server ripete gli stessi controlli sul file ricevuto (è lui a decidere, anche quando il browser non riesce a leggere le informazioni del file), crea il backup e installa. Il servizio resta fermo per circa un minuto, poi la pagina si ricarica da sola con la nuova versione. Dati, account e impostazioni restano. Per sicurezza, dato che il setup gira con i privilegi di sistema:

- solo gli **amministratori**, con la conferma della password;
- solo da un PC della **rete locale** del server (o dalla VPN), aprendo la piattaforma con l'indirizzo interno: non attraverso un proxy. Se hai aperto la piattaforma in un altro modo, il riquadro mostra l'indirizzo interno come collegamento e il pulsante **Apri la piattaforma locale**, che apre in una nuova scheda la piattaforma locale direttamente su questo riquadro (dopo l'accesso, se serve);
- solo con il **servizio di Windows installato dal setup**;
- solo il **setup originale** (dalla 1.164.2): il server confronta l'impronta SHA-256 del file con quella della stessa versione pubblicata su GitHub. Se è diversa non installa niente. Se non la può confrontare (il server non raggiunge Internet, la versione non è pubblicata) la finestra chiede il **codice letto sul server**: è scritto nel file `update-code.txt` della cartella dei dati (di solito `C:\ProgramData\BlackHoleWorkspaces`), che aprono solo gli amministratori di Windows. Il codice vale una volta: dopo l'aggiornamento il file si cancella.

**Sul server**: esegui il nuovo setup sopra l'installazione esistente: ferma il servizio, sostituisce i file e lo riavvia. Il pacchetto compresso si aggiorna invece con `Update.ps1`. Anche in questi casi, al riavvio il riquadro mostra come **Ultimo aggiornamento** le due versioni e la data, con **direttamente sul server** al posto del nome di chi l'ha avviato: vale sempre l'aggiornamento più recente, fatto dalla piattaforma o sul server.

A ogni aggiornamento il database viene adeguato da solo, dopo averne fatto una copia in `recovery`; l'esito dell'ultimo aggiornamento resta in Impostazioni e nel registro attività, il log del setup nella cartella `recovery`. Le pagine rimaste aperte nei browser avvisano di ricaricare.

## <a id="server-collegati"></a>Chi è collegato durante l'aggiornamento

Dalla 1.138.0, prima di aggiornare l'amministratore vede **chi sta lavorando** e lo avvisa; chi lavora riceve l'avviso e, mentre il setup aggiorna, nessuno entra.

- **L'elenco**: in **Impostazioni → Server → Aggiornamento del programma**, in fondo, e nelle due finestre che avviano il setup (**Scarica e installa** e il setup caricato dal PC). Per ognuno: nome, mansione, se è attivo adesso o assente da qualche minuto, quante pagine ha aperte e, con un avviso in corso, se lo ha **confermato** (in alto «2 di 3 hanno confermato»). Si aggiorna da solo.
- **Avvisa**: un messaggio (proposto, da cambiare a piacere) a tutti quelli che hanno la piattaforma aperta. Compare in una **fascia** sotto la barra in alto, con chi lo manda e quando, e si conferma con **Ho capito**.
- **Invita a non operare**: come l'avviso, ma più deciso; si apre anche una **finestra** (con il richiamo alle modifiche non salvate della pagina) che si chiude con **Ho salvato, aspetto**. Così, prima di avviare il setup, sai chi ha salvato.
- Un avviso nuovo prende il posto di quello di prima. **Togli l'avviso** (nell'elenco o nella fascia di chi l'ha mandato) lo toglie a tutti: chi lavora legge «puoi riprendere a lavorare». Arriva anche a chi si collega dopo.
- **Quando il setup parte** (in tutti e due i modi), l'avviso dell'aggiornamento arriva **da solo** a tutti: «la piattaforma si sta aggiornando alla versione…: non operare». Al ritorno del server la fascia dice che è stata installata la versione nuova, con **Ricarica**. Anche quando il servizio si ferma per altri motivi (un setup avviato direttamente sul server, un riavvio) le pagine aperte lo dicono.
- **Durante l'aggiornamento non si entra**: la pagina di accesso mostra «Aggiornamento in corso» e si riapre da sola appena il server è di nuovo online; il server rifiuta comunque gli accessi (prima di guardare la password). Lo stesso per i [link di condivisione](condivisioni.md) e per il preventivo online: chi li apre aspetta e la pagina si ricarica da sola; caricamenti, accettazioni e messaggi non partono. Se il setup non parte, o il server non si ferma entro 10 minuti, l'accesso si riapre da solo.
- Con un avviso o un invito in corso, chi è sulla pagina di accesso, su un link di condivisione o sul preventivo online vede una fascia con una frase generica (il testo dell'amministratore lo legge solo chi è entrato); con l'invito a non operare si può comunque entrare.
- Il registro attività annota avvisi, inviti e avvisi tolti, con il testo e quanti erano collegati.

## <a id="server-nuove-versioni"></a>Avviso delle nuove versioni

Una volta al giorno il server chiede a GitHub qual è l'ultima versione pubblicata di BlackHole Workspaces e la confronta con quella installata. Quando ne esce una nuova, gli **amministratori**:

- ricevono una [notifica](notifiche.md) nella campanella 🔔, una volta per versione (e, come le altre, per email se resta da leggere); un clic porta al riquadro dell'aggiornamento. Se esce un'altra versione prima che tu la legga, la nuova notifica prende il posto della precedente; dopo l'installazione quelle rimaste da leggere risultano lette;
- vedono un **pallino** su **Sistema** e sulla voce **Impostazioni**, che porta direttamente al riquadro dell'aggiornamento, finché la versione nuova non viene installata;
- trovano in **Impostazioni → Aggiornamento del programma** la versione con la data di pubblicazione, le **novità** e i pulsanti **Scarica e installa** (il server scarica, controlla e installa da solo, vedi [Aggiornare](#server-aggiornamento)), **Scarica il setup** e **Pagina della versione**, che aprono GitHub in un'altra scheda.

Nulla si installa senza che un amministratore lo chieda: con **Scarica e installa**, oppure scaricando il setup sul tuo PC e caricandolo nello stesso riquadro. Sotto i pulsanti trovi l'impronta **SHA-256** del file pubblicato, che **Scarica e installa** controlla da solo e che si può confrontare con quella di un file scaricato a mano (in PowerShell: `Get-FileHash BlackHoleWorkspaces-<versione>-Setup.exe`).

Il riquadro mostra anche quando è stato fatto l'ultimo controllo; **Controlla ora** lo ripete subito. Finché su GitHub non è pubblicata nessuna versione, il riquadro lo dice e non compare alcun avviso. Gli utenti che non sono amministratori non vedono nulla. La prima segnalazione di ogni versione finisce nel [registro attività](registro.md) (categoria **Sistema**, «Nuova versione disponibile»).

> [!NOTE]
> **Riservatezza**: la richiesta va a `api.github.com` e non contiene alcun dato dell'organizzazione (né nome, né utenti, né versione installata). Per spegnere il controllo automatico togli la spunta **Avvisa quando esce una nuova versione** nel riquadro e premi **Salva** in fondo: il server non interroga più GitHub, niente notifiche né pallino; **Controlla ora** resta disponibile. Se il server non raggiunge Internet il controllo non riesce e il riquadro ne indica il motivo, senza altre conseguenze: il server riprova dopo qualche ora.

## <a id="server-licenza"></a>Licenza d'uso e responsabilità

BlackHole Workspaces è **gratuito per tutti**, anche per le aziende e per uso commerciale, senza limiti di utenti, di installazioni, di commesse o di documenti e senza scadenza; non servono registrazione né chiavi di attivazione. Il setup mostra la licenza da accettare prima di installare e la copia nella cartella del programma (`LICENZA.txt`, accanto a `THIRD-PARTY-NOTICES.md` con le licenze dei componenti di terze parti). In breve:

- è un software **proprietario**, non open source: il codice sorgente non è pubblico. Dalla 1.141.2 l'avviso di licenza, in italiano e in inglese, è anche dentro il programma: nelle informazioni del file, in `AVVISO-LICENZA.txt` e in testa ai file dell'interfaccia, così lo legge anche chi lo decompila o chiede a un assistente AI di farlo;
- si può installare ovunque e distribuire il setup originale, gratis e senza modifiche; non si può vendere il programma né modificarlo (il proprio lavoro di installazione e assistenza si può far pagare);
- il programma è fornito **così com'è**, senza garanzie: importi, fatture elettroniche, contabilità, scadenze e documenti vanno controllati prima di usarli, e il programma non sostituisce il commercialista o gli altri consulenti;
- i dati restano sul server dell'azienda, che ne è titolare (GDPR) e ne cura i [backup](backup.md); i servizi esterni collegati (assistente AI in cloud, Telegram, PEC…) si usano alle loro condizioni.

## <a id="server-disinstallazione"></a>Disinstallare

Da Impostazioni di Windows → App: rimuove servizio, icona di stato, regola del firewall e programma, e chiede se eliminare anche i dati (la risposta predefinita è no).

## <a id="server-reset-password"></a>Recupero dell'accesso amministratore

Sul server, da un prompt dei comandi **come amministratore** nella cartella di installazione:

`BlackHoleWorkspaces.exe --reset-password <utente> <nuova password>`

Reimposta la password, riabilita l'account e disattiva la sua verifica in due passaggi; se l'utente non esiste lo crea come amministratore. Funziona anche con il servizio in esecuzione.

---

[← Profilo e sicurezza](profilo.md) · [Indice](README.md) · [Buone pratiche di sicurezza →](sicurezza.md)
