[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="problemi"></a>Risoluzione dei problemi

<details>
<summary><b>Non ricordo la password</b></summary>

Usa [Password dimenticata](accesso.md#accesso-recupero); se la posta non è configurata chiedi a un amministratore. Se è l'unico amministratore a non poter entrare, vedi [Recupero dell'accesso amministratore](server.md#server-reset-password).

</details>

<details>
<summary><b>Ho perso il telefono con l'app dei codici</b></summary>

Usa un codice di recupero. Se non li hai, un amministratore può **reimpostare** la tua verifica in due passaggi dalla scheda dell'utente, sezione Sicurezza.

</details>

<details>
<summary><b>«Accesso sospeso» dopo troppi tentativi</b></summary>

Attendi i minuti indicati: il blocco si toglie da solo. Se succede senza che tu abbia sbagliato, qualcuno sta provando la tua password da un altro browser: entra dal browser che usi di solito, che non risente del blocco, e cambia la password se il [registro attività](registro.md) mostra tentativi che non sono tuoi.

</details>

<details>
<summary><b>Il codice fiscale calcolato è diverso da quello del documento</b></summary>

Controlla nome, cognome, data, genere e soprattutto il luogo di nascita (il comune giusto tra quelli con lo stesso nome). Se i dati sono corretti si tratta di **omocodia**: scrivi il codice del documento, che risulterà comunque valido.

</details>

<details>
<summary><b>Chiama un cliente ma non lo trovo nella ricerca della richiesta di assistenza</b></summary>

Prova con le ultime cifre del numero da cui chiama (si cercano anche i numeri dei referenti) o con il codice cliente. Se è un contatto privato di un collega non compare. Se non c'è, **Cliente nuovo** lo crea al volo: la sua scheda resta con l'etichetta *Da completare* finché qualcuno non aggiunge i dati che mancano. Vedi [Aprire una richiesta](assistenza.md#assistenza-apertura).

</details>

<details>
<summary><b>Il cliente ci ha mandato il numero del suo ticket: dove lo scrivo?</b></summary>

Nel campo **Ticket del cliente** della richiesta di assistenza (anche dopo, con **Modifica**): la ricerca la ritrova da quel numero e compare nel rapporto, nella ricevuta e nell'email al cliente.

</details>

<details>
<summary><b>Un numero di telefono viene segnalato come non valido</b></summary>

I numeri italiani iniziano con 0 (fissi) o 3 (cellulari, 9 o 10 cifre). Per un numero estero inizia con `+` e il prefisso del paese.

</details>

<details>
<summary><b>Il nome di un'azienda (o di una persona, di una via) è stato cambiato dopo che l'ho scritto</b></summary>

Sono le [maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato): correggono le parole scritte tutte in minuscolo, tutte in maiuscolo o con le maiuscole a caso. Se il risultato non è quello giusto, scrivi il nome come lo vuoi, con le maiuscole e le minuscole al loro posto (*ACME Impianti*, *McDonald*): ciò che è scritto così viene rispettato. Di un nome d'azienda scritto tutto in maiuscolo restano maiuscole solo le sigle: per tenere maiuscola una parola più lunga scrivi il resto del nome con le minuscole (*ITALTEL Group* resta così, *ITALTEL GROUP* diventa *Italtel Group*).

</details>

<details>
<summary><b>Un campo ha il bordo rosso e non riesco a salvare</b></summary>

Il valore non ha la forma giusta per quel campo: sotto il campo c'è che cosa non va (per esempio *al dominio manca l'estensione* per un'email, *non è un indirizzo IP*). Correggilo, oppure svuota il campo se il dato non c'è ancora: un campo vuoto non è mai sbagliato. Vedi [Controllo dei campi](interfaccia.md).

</details>

<details>
<summary><b>Compare «Internet assente» ma internet sul mio PC funziona</b></summary>

L'avviso riguarda il **server**: è lui che usa internet per meteo, mappe, indirizzi, email e aggiornamenti. Controlla la rete del server (cavo, router, firewall che blocca le uscite); l'avviso sparisce da solo appena il server raggiunge di nuovo internet. Vedi [Accesso dagli altri PC](server.md#server-rete).

</details>

<details>
<summary><b>Dove sono finite le caselle per scegliere più clienti?</b></summary>

Compaiono con l'icona **Scegli più righe**, la prima a sinistra nella barra della ricerca: vedi [Scegliere più schede insieme](clienti.md#clienti-selezione).

</details>

<details>
<summary><b>La casella «Elimina dal PC dopo il caricamento» è spenta</b></summary>

Il browser lascia eliminare i file del PC solo con Chrome o Edge e da un indirizzo sicuro (https). Apri BlackHole dall'indirizzo https, oppure fai trattare come sicuro l'indirizzo della rete locale: vedi [Eliminare gli originali dal PC](documenti.md#documenti-originali).

</details>

<details>
<summary><b>Da una cartella: l'assistente non ha compilato la scheda tecnica</b></summary>

Succede se il tipo dell'impianto non propone un [modello di scheda](impianti.md#impianti-modelli), se i dati non sono scritti nei documenti (o sono in una scansione senza testo) o se i documenti non sono entrati nella misura del modello (la revisione lo dice: conviene un contesto più grande in Impostazioni → Assistente AI). I dati trovati sono comunque nell'elenco **Dati trovati nei documenti**, in fondo, da copiare. Vedi [Da una cartella del PC](impianti.md#impianti-cartella).

</details>

<details>
<summary><b>Dove scrivo la password del registratore o del router?</b></summary>

Nella scheda tecnica, se il modello ha un campo **Password**: resta nascosta, cifrata e fuori da stampe e link condivisi, e la vede chi vede l'impianto. Se deve vederla solo qualcuno, usa la linguetta **Password** dell'impianto. Vedi [La scheda tecnica](impianti.md#impianti-scheda-tecnica).

</details>

<details>
<summary><b>Un valore di una scheda tecnica o di una certificazione ha cambiato le maiuscole</b></summary>

Il campo prende le maiuscole dalla sua etichetta (Marca, Modello, Numero di serie…): vedi [Maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato). Se per quel campo non va bene, chi gestisce i modelli sceglie **Come si scrive** (o un altro formato) in **Maiuscole**, nella linguetta dei campi del modello. Password, PIN e utenti non vengono mai toccati.

</details>

<details>
<summary><b>In un campo non compaiono i suggerimenti</b></summary>

L'elenco si apre quando scrivi, clicchi nel campo o premi <kbd>↓</kbd>, e propone solo i valori già scritti nello stesso campo che puoi vedere: in un archivio appena iniziato, o per chi non vede quella pagina, può essere vuoto. Vedi [Suggerimenti mentre scrivi](interfaccia.md#interfaccia-suggerimenti).

</details>

<details>
<summary><b>Nell'anteprima dell'importazione molte righe sono «Già presente» o «Possibile doppione»</b></summary>

È normale se il file è già stato importato o viene da un'esportazione della piattaforma: **Già presente** vuol dire che il codice della riga è quello di un cliente in archivio, che resta com'è. Un **Possibile doppione** ha lo stesso codice fiscale, la stessa partita IVA o lo stesso nome di un altro cliente: di norma va lasciato fuori; selezionalo solo se è davvero un cliente diverso. Per aggiornare un cliente esistente apri la sua scheda: l'[importazione](clienti.md#clienti-importa) non modifica mai i clienti già presenti.

</details>

<details>
<summary><b>L'importazione segnala «valore rovinato da Excel», oppure partite IVA e CAP hanno perso gli zeri iniziali</b></summary>

Gli zeri iniziali tolti da Excel vengono rimessi da soli, con una nota accanto alla riga. Un numero finito in notazione scientifica (`1,23E+10`) invece non si recupera: nel foglio formatta la colonna come **Testo**, riscrivi o incolla di nuovo i valori e salva ancora il file in formato CSV.

</details>

<details>
<summary><b>Dopo l'importazione molti clienti hanno l'etichetta «Da controllare»</b></summary>

Nel file c'erano dati non validi: un nome nel campo del telefono, una partita IVA sbagliata, una banca senza IBAN… Invece di perderli, l'importazione li ha messi in fondo alle note del cliente, sotto «Dati del file da controllare». Scrivi *Da controllare* nella ricerca dei clienti, sistema i dati nella scheda e togli l'etichetta: vedi [Dati non validi: nelle note, da controllare](clienti.md#clienti-importa).

</details>

<details>
<summary><b>Come porto qui i clienti del vecchio gestionale, con tutte le sedi e i referenti?</b></summary>

Con un file **JSON**: un elenco di clienti, ognuno con più indirizzi, recapiti, referenti e banche. Lo si prepara con un piccolo programma che legge l'archivio del vecchio gestionale (chiedi a chi gestisce il server) e si importa da **Clienti → Importa** come un CSV: vedi [Il formato del file JSON](clienti.md#clienti-importa).

</details>

<details>
<summary><b>Una password risulta «Non leggibile», oppure mostrarla dà un errore sulle chiavi di cifratura</b></summary>

I segreti sono cifrati con chiavi di un altro server: succede dopo il ripristino di un backup **non cifrato** creato altrove. Le voci restano, ma password, note e campi riservati vanno scritti di nuovo (il [controllo](password.md#password-controllo) le elenca). Con i backup cifrati non succede.

</details>

<details>
<summary><b>Gli appunti non si svuotano dopo aver copiato una password</b></summary>

Il browser consente di svuotarli solo alle pagine aperte in `https://` o sul server stesso (`localhost`): da un indirizzo `http://` della rete, dopo aver incollato la password copia qualcos'altro. Gli appunti non si svuotano nemmeno se nel frattempo hai copiato altro dalla pagina.

</details>

<details>
<summary><b>«Apri cartella» mostra il percorso invece di aprire la cartella</b></summary>

La cartella è sul server e la finestra si può aprire solo lì: vedi [Aprire la cartella sul server](archiviazione.md#archiviazione-apri). Da un altro computer usa **Copia percorso**.

</details>

<details>
<summary><b>Non ricevo i messaggi della chat</b></summary>

Controlla il numero sul pulsante della chat: gli avvisi compaiono solo quando la conversazione non è già aperta. Con la pagina in secondo piano il controllo avviene ogni mezzo minuto, quindi il numero nel titolo della scheda può comparire con questo ritardo; tornando sulla pagina i messaggi arrivano subito.

</details>

<details>
<summary><b>Un collega non vede l'appunto che ho condiviso</b></summary>

Controlla, nell'ordine: che dopo averlo aggiunto alla **Condivisione** tu abbia premuto **Salva** (nel riquadro deve esserci l'icona con il numero dei destinatari); che l'appunto non sia nel tuo **Cestino**, perché un appunto cestinato sparisce anche ai destinatari; che il collega non lo abbia **archiviato** (lo trova nella vista Archivio) e non abbia attivi la ricerca, il filtro **Miei** o un filtro per etichetta. Se lo ha tolto con **Rimuovi dai miei appunti**, condividilo di nuovo. Se hai condiviso con un **gruppo**, il collega deve farne parte: lo verifica un amministratore in **Sistema → Gruppi**. Vedi [Condividere con colleghi e gruppi](appunti.md#appunti-condividere).

</details>

<details>
<summary><b>Ho eliminato un appunto per errore</b></summary>

Apri la vista **Cestino** della pagina Appunti e scegli **Ripristina**: l'appunto torna dov'era, anche per le persone con cui era condiviso. Hai **30 giorni** di tempo. Dopo **Elimina definitivamente**, dopo **Svuota cestino** o trascorsi i 30 giorni l'appunto non si può più recuperare. Se invece era un appunto di un collega che hai tolto con **Rimuovi dai miei appunti**, chiedigli di condividerlo di nuovo. Vedi [Cestino](appunti.md#appunti-cestino).

</details>

<details>
<summary><b>Salvando un appunto compare «L'appunto è stato modificato da…»</b></summary>

Qualcun altro lo ha cambiato mentre lo avevi aperto, oppure è cambiata la sua condivisione. Quello che hai scritto è ancora nella finestra: scegli **Salva come copia** per conservarlo in un nuovo appunto, oppure **Ricarica l'appunto** per vedere la versione aggiornata. Vedi [Modifiche contemporanee](appunti.md#appunti-conflitti).

</details>

<details>
<summary><b>Su un cliente non trovo «Salva» o «Elimina»</b></summary>

Dipende dai [permessi](clienti.md#clienti-permessi): con «Modificare (o Eliminare) i clienti creati da sé» puoi farlo solo sui clienti che hai creato tu; gli altri si aprono in consultazione. Per agire su tutti servono i permessi «Modificare tutti i clienti» ed «Eliminare qualsiasi cliente»: chiedi a un amministratore.

</details>

<details>
<summary><b>Non riesco a togliere il ruolo di amministratore a un utente</b></summary>

È voluto: un amministratore non può essere declassato. Se non deve più amministrare la piattaforma, disabilita l'account (resta tutto dov'è) oppure eliminalo. Vedi [Ruoli](utenti.md#utenti-ruoli).

</details>

<details>
<summary><b>Un amministratore non compare tra i membri di un gruppo</b></summary>

Gli amministratori non fanno parte dei gruppi: hanno già tutti i permessi e le policy non si applicano a loro. Per condividere un appunto con un amministratore aggiungilo per nome.

</details>

<details>
<summary><b>Nel menu non trovo una pagina</b></summary>

Le pagine di gestione della piattaforma (utenti, gruppi, policy, registro, archiviazione, backup, impostazioni) sono nel menu del pulsante **Sistema** , in fondo al menu laterale: un clic lo apre (con il menu ridotto alle icone, un clic sullo scudo). Se di un'area (Anagrafiche, Commesse, Archivio) vedi solo il titolo (o, nel menu ridotto, solo la freccia), è chiusa: un clic la riapre. Una pagina che non puoi usare non compare: chiedi a un amministratore. Vedi [Il menu laterale](interfaccia.md#interfaccia-menu).

</details>

<details>
<summary><b>Il tema o il carattere che ho scelto non ci sono su un altro computer</b></summary>

Sono preferenze del browser, non dell'account: vanno scelte su ogni computer e in ogni browser che usi. Vedi [Aspetto: tema e carattere](profilo.md#profilo-aspetto).

</details>

<details>
<summary><b>La pagina avvisa che è stata installata una nuova versione</b></summary>

Ricarica la pagina (<kbd>F5</kbd>) per usare la versione nuova.

</details>

<details>
<summary><b>L'aggiornamento dalla piattaforma non è disponibile</b></summary>

Serve il servizio di Windows installato dal setup e bisogna collegarsi dalla rete locale con l'indirizzo interno del server. Il riquadro spiega il motivo esatto; il pulsante **Apri la piattaforma locale** apre l'indirizzo interno per te, se il tuo PC è nella rete locale o nella VPN.

</details>

<details>
<summary><b>Il setup scelto per l'aggiornamento viene rifiutato subito</b></summary>

Il file viene controllato appena lo scegli: deve essere il setup di BlackHole Workspaces (`BlackHoleWorkspaces-<versione>-Setup.exe`) di una versione uguale o successiva a quella installata. Il messaggio dice che cosa è stato scelto al suo posto.

</details>

<details>
<summary><b>L'aggiornamento non va a buon fine</b></summary>

In Impostazioni compare l'esito con il percorso del log del setup. I dati non vengono toccati dal setup e, se lo hai lasciato selezionato, c'è il backup **Pre-aggiornamento**.

</details>

<details>
<summary><b>Il controllo delle nuove versioni non riesce</b></summary>

In **Impostazioni → Aggiornamento del programma** il riquadro giallo indica il motivo. «Il server non raggiunge GitHub» o «non ha risposto»: il server non esce su Internet, oppure un firewall o un proxy blocca `api.github.com` (HTTPS, porta 443); il servizio gira con l'account di sistema, che usa il proxy di sistema di Windows e non quello del tuo utente. «Troppe richieste»: dalla stessa connessione a Internet sono partite molte richieste a GitHub, riprova dopo un'ora. Se il server deve restare senza Internet, togli la spunta all'avviso. Vedi [Avviso delle nuove versioni](server.md#server-nuove-versioni).

</details>

<details>
<summary><b>Dopo un riavvio del server la piattaforma non risponde</b></summary>

Il servizio parte con avvio ritardato: attendi un paio di minuti (icona di stato gialla). Se resta rossa, apri **Servizi di Windows** dal menu dell'icona e avvia «BlackHole Workspaces».

</details>

<details>
<summary><b>Dagli altri PC la piattaforma non si apre</b></summary>

Vedi [Accesso dagli altri PC](server.md#server-rete).

</details>

<details>
<summary><b>Un documento .doc, .ppt o .odt non si vede nel visualizzatore</b></summary>

Quei formati li legge LibreOffice sul server: un amministratore lo installa da Impostazioni, vedi [LibreOffice sul server](documenti.md#documenti-libreoffice). Intanto il file si può scaricare.

</details>

<details>
<summary><b>Di un disegno DWG vedo solo un'immagine</b></summary>

Sul server non c'è un convertitore dei DWG, oppure la conversione di quel disegno non è riuscita: sotto l'anteprima c'è il motivo. Un amministratore attiva il convertitore da Impostazioni → Disegni DWG (vedi [Disegni DWG sul server](documenti.md#documenti-dwg)). Se un disegno particolare non si converte con LibreDWG, installa ODA File Converter dallo stesso riquadro, oppure carica anche la versione **DXF** (in AutoCAD: *Salva con nome → DXF*).

</details>

<details>
<summary><b>Nel menu di un PDF o di un'immagine non c'è «Rendi ricercabile» o «Estrai il testo»</b></summary>

Il riconoscimento del testo non è installato sul server: lo installa un amministratore da Impostazioni → Server (vedi [Riconoscimento del testo](documenti.md#documenti-ocr)). Se c'è «Estrai il testo» ma non «Rendi ricercabile», non puoi caricare nuove revisioni di quel PDF o file in quella cartella.

</details>

<details>
<summary><b>Il testo riconosciuto ha molti errori</b></summary>

Di solito l'immagine è piccola, sfocata, storta o con poca luce. Scansiona il foglio a 300 dpi oppure rifai la foto con il foglio intero, dritto e ben illuminato. Scritte a mano, timbri e tabelle fitte si leggono male anche così.

</details>

<details>
<summary><b>Il caricamento di un file si ferma con «Spazio su disco insufficiente sul server»</b></summary>

Sul disco della cartella di lavoro deve restare libero almeno mezzo gigabyte anche dopo il file. Libera spazio, elimina dal [cestino dei documenti](documenti.md#documenti-cestino) ciò che non serve o [sposta la cartella di lavoro](archiviazione.md#archiviazione-cambio) su un disco più grande.

</details>

<details>
<summary><b>Non vedo un progetto che un collega vede</b></summary>

È un [progetto riservato](progetti.md#progetti-scheda): chiedi al responsabile di aggiungerti tra i membri, nella scheda del progetto. Se non vedi del tutto la pagina Progetti, ti manca il permesso **Vedere i progetti**.

</details>

<details>
<summary><b>Non vedo un'attività che un collega vede</b></summary>

Un'attività la vedono solo chi la riguarda e chi vede il suo progetto: chiedi a chi l'ha creata di assegnartela o di [condividerla](attivita.md#attivita-condivisione) con te. Controlla anche i filtri della pagina: con **Le mie** compaiono solo quelle che ti riguardano direttamente.

</details>

<details>
<summary><b>Non riesco ad assegnare (o condividere) un'attività a un collega</b></summary>

Il collega deve avere l'account abilitato. Se l'attività è collegata a un progetto riservato deve anche poter vedere il progetto, cioè esserne membro (anche tramite un gruppo): il messaggio dice chi manca. Lo stesso vale per il revisore e per i gruppi della condivisione.

</details>

<details>
<summary><b>Non posso collegare un'attività a un progetto</b></summary>

Nel campo **Progetto** compaiono solo i progetti di cui gestisci le attività: chiedi al responsabile di aggiungerti tra i membri con il ruolo *Gestisce le attività*. Vedi [Le attività del progetto](progetti.md#progetti-attivita).

</details>

<details>
<summary><b>Ho completato un'attività ma è finita «In revisione»</b></summary>

L'attività ha un revisore: è lui a completarla approvandola. Vedi [Revisione](attivita.md#attivita-revisione).

</details>

<details>
<summary><b>Nell'attività non posso cambiare il titolo o le date</b></summary>

Ci lavori ma non la puoi modificare: puoi cambiarne lo stato, spuntare le voci, registrare le ore e commentarla. Il resto lo cambiano chi l'ha creata, chi la riceve con la modifica e chi gestisce le attività del progetto collegato. Vedi [Assegnare e lavorare](attivita.md#attivita-assegnare).

</details>

<details>
<summary><b>Ho eliminato un progetto: dove sono finite le sue attività?</b></summary>

Se hai scelto **Elimina il progetto e lascia le attività**, sono ancora nella pagina Attività, *Senza progetto*, con le loro persone, ore e commenti: a te sono state condivise con la modifica (le trovi in **Le mie**) e nel loro storico c'è scritto da quale progetto vengono. Chi le vedeva solo attraverso il progetto non le vede più: condividile di nuovo se serve. Se hai scelto di eliminarle (la scelta proposta per un progetto riservato) non si recuperano, se non da un [backup](backup.md).

</details>

<details>
<summary><b>Non ricevo le notifiche per email</b></summary>

Servono la posta in uscita configurata, un indirizzo email sul tuo account e l'opzione attiva nelle [preferenze](notifiche.md#notifiche-preferenze). L'email parte solo per le notifiche rimaste da leggere per qualche minuto: se le leggi subito nella piattaforma non arriva.

</details>

<details>
<summary><b>Non ricevo le notifiche su Telegram</b></summary>

In [Profilo e sicurezza](profilo.md) la chat deve risultare **Collegato**, con **Anche su Telegram** spuntato. Come le email, le notifiche partono solo se restano da leggere per due minuti (gli avvisi del monitoraggio subito). Se il bot non risponde a **/start**, in Impostazioni → Posta e Telegram il riquadro Telegram dice il problema: il caso più comune è lo stesso bot usato anche da un altro programma. Vedi [Telegram](impostazioni.md#impostazioni-telegram).

</details>

<details>
<summary><b>Non vedo una cartella che un collega vede</b></summary>

Probabilmente è una [cartella riservata](documenti.md#documenti-permessi): chiedi a chi la gestisce, o a un amministratore, di aggiungerti nella sua scheda **Accesso**.

</details>

<details>
<summary><b>Non vedo il pulsante dell'assistente AI</b></summary>

Compare quando l'assistente è pronto (motore e modello installati, oppure il server esterno indicato) e il tuo account ha il permesso **Usare l'assistente AI**: chiedi a un amministratore. Lui trova il motivo nella scheda [Assistente AI](impostazioni.md#impostazioni-ai) delle Impostazioni.

</details>

<details>
<summary><b>Nei moduli non vedo il pulsante Migliora testo</b></summary>

Il pulsante ✨ c'è alle stesse condizioni di quello della chat, nei campi che puoi modificare: in una scheda che stai solo consultando non compare. Vedi [Migliora testo nei moduli](assistente-ai.md#assistente-moduli).

</details>

<details>
<summary><b>La proposta di Migliora testo ha cambiato un dato</b></summary>

Succede, soprattutto con i modelli più piccoli: per questo la finestra elenca in giallo numeri, date, codici, email e collegamenti tolti o cambiati. Correggili prima di applicare, oppure scegli **Riprova**; se hai già sostituito il testo, <kbd>Ctrl</kbd>+<kbd>Z</kbd> lo riporta com'era.

</details>

<details>
<summary><b>L'assistente risponde lentamente</b></summary>

Il modello gira con il processore del server: una risposta lunga può chiedere un minuto, la prima dopo una pausa qualche secondo in più per caricarlo, e le domande passano una alla volta. Un amministratore può scegliere un modello più leggero (Qwen3 1.7B), tenerlo in memoria più a lungo o usare un server della rete con una scheda video.

</details>

<details>
<summary><b>Il motore dell'assistente non parte</b></summary>

Nella scheda [Assistente AI](impostazioni.md#impostazioni-ai) il riquadro **Motore** mostra l'errore e **Ultimi messaggi del motore**. Il caso più comune è la memoria: scegli un modello più piccolo o un contesto più corto, oppure aumenta la memoria del server.

</details>

---

[← Buone pratiche di sicurezza](sicurezza.md) · [Indice](README.md) · [Fonti e riconoscimenti →](crediti.md)
