[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="password"></a>Password

**Il mio spazio → Password** è il gestore di password della piattaforma: conserva le credenziali di accessi a siti e programmi, server e dispositivi, reti Wi-Fi, caselle di posta, database, chiavi API, licenze, con tutto ciò che serve per usarle (dove si usano, link, cliente, etichette, note). Password, note riservate, chiavi della verifica in due passaggi e campi riservati sono **cifrati sul server**. Una voce è **personale** finché non la condividi con colleghi, gruppi o tutti. Per usare il servizio serve il permesso **Usare la gestione password** (vedi [Permessi](#password-permessi)).

La pagina ha quattro viste, ciascuna con il suo numero: **Tutte**, **Preferite**, **Controllo** (le password da sistemare) e **Cestino**. In alto ci sono **Esporta CSV** (per chi ne ha il permesso), **Importa**, **Tipi** (per chi gestisce i tipi), **Generatore**, **Nuova cartella** e **Nuova password**. Le password si mettono in ordine nelle [cartelle](#password-cartelle).

## <a id="password-cartelle"></a>Le cartelle

Le cartelle mettono in ordine le password, come i gruppi del [monitoraggio](monitoraggio.md): un cliente, una sede, i fornitori. Sono un **albero unico per tutta l'azienda**, una dentro l'altra fino a otto livelli, ma **non cambiano chi vede una password**: una password personale resta personale anche dentro una cartella che vedono tutti, una condivisa resta condivisa con le stesse persone.

- **Chi vede una cartella**: chi l'ha creata e chi vede almeno una password al suo interno, anche in una sottocartella, con le cartelle che la contengono. Una cartella con dentro solo password che non vedi, per te non esiste (nemmeno per gli amministratori, che non vedono le password personali degli altri).
- **Nell'elenco** di **Tutte**, senza ricerca né filtri, in cima ci sono le cartelle della cartella aperta, con quante password e sottocartelle contengono, e sotto le sue password. Un clic su una cartella la apre; il **percorso** sopra l'elenco («Tutte le password › Clienti › Rossi») riporta indietro. Con la ricerca, un filtro o un'etichetta l'elenco mostra tutte le password della cartella aperta e di quelle dentro, con il percorso sotto il nome; per cercare dappertutto si torna a **Tutte le password**. La scheda di una password dice in che cartella sta (un clic la apre).
- **Creare**: **Nuova cartella** la crea dentro quella aperta (anche dentro la cartella di un altro, se la vedi); una **Nuova password** nasce nella cartella aperta. Nella scheda della password il campo **Cartella** la sposta.
- **Spostare**: si trascinano password e cartelle su una cartella dell'elenco o su un passo del percorso (anche **Tutte le password**, per toglierle dalle cartelle); con l'icona delle caselle in alto a destra se ne scelgono più insieme e **Sposta in…** chiede dove. Una password la sposta chi la può modificare: quelle condivise con te in sola lettura restano dove sono.
- **Rinominare, spostare ed eliminare una cartella** (dal menu ⋯ della riga o del percorso): chi l'ha creata, chi gestisce le password condivise e gli amministratori. Gli altri ci mettono dentro le proprie password e le proprie sottocartelle, ma non la toccano. Nello stesso posto non ci sono due cartelle con lo stesso nome tra quelle che vedi.
- **Eliminare una cartella non elimina mai le password**: quelle che contiene, anche quelle degli altri che non vedi e quelle nel cestino, e le sue sottocartelle passano nella cartella superiore (o in cima). La conferma dice quante delle tue password si spostano e, se dentro ce ne sono di altri, che restano dei loro proprietari, senza dire quante. Creazioni, modifiche, eliminazioni e spostamenti finiscono nel registro attività; ogni spostamento di una password anche nel suo storico.

## <a id="password-voci"></a>Le voci

Ogni voce ha un **tipo**, con il suo colore: si sceglie dall'elenco con il pallino e si filtra nella barra dell'elenco. I tipi di partenza scelgono anche l'icona e il nome dei campi:

| Tipo | Per esempio |
| --- | --- |
| Accesso web o programma | Il gestionale, un portale fornitori, un servizio online. |
| Server o dispositivo | Router, NAS, stampanti, telecamere, server. |
| Rete Wi-Fi | Il **nome della rete (SSID)** e la sua password. |
| Casella di posta | Una casella email o una PEC. |
| Database | Utente e password di un database, con server e porta in **Dove si usa**. |
| Chiave API o token | La chiave di un servizio, con l'account a cui appartiene. |
| Licenza software | L'intestatario e il **codice di licenza**. |
| Nota riservata | Codici di recupero, risposte di sicurezza, istruzioni riservate. |

### <a id="password-tipi"></a>Cambiare l'elenco dei tipi

Chi ha il permesso **Gestire i tipi delle password** apre con **Tipi** il pannello dei [tipi e delle categorie](interfaccia.md#interfaccia-tipi):

- **aggiungere** un tipo: **Aggiungi un tipo**, nome, icona e colore (per esempio *Videosorveglianza*, *Antintrusione*, *Controllo accessi*). Un tipo aggiunto ha l'icona della chiave e i campi **Utente** e **Password**;
- **rinominare** un tipo o cambiarne **icona e colore**, anche uno di partenza (che conserva i nomi dei campi): clic sulla riga, poi **Salva**;
- **eliminare** un tipo con 🗑: le password che lo avevano restano **senza tipo** e si ritrovano nel filtro con **Senza tipo**;
- dare al tipo un'**icona** con il pulsante con l'immagine accanto al pallino (un router per *Rete*, una telecamera per *Videosorveglianza*): compare accanto a ogni password di quel tipo. Vedi [Icone e colori](interfaccia.md#interfaccia-icone).

Accanto a ogni tipo c'è quante password lo usano. L'elenco è uguale per tutti; il nome di un tipo è unico.

Oltre al **Nome** (l'unico campo obbligatorio), la scheda contiene: **utente**, **email**, **password**, **verifica in due passaggi**, **dove si usa** (un server, un indirizzo IP, una sede), i **link web** (fino a 10, ciascuno con un'etichetta: senza `https://` viene aggiunto da solo), il **cliente**, la data **Da cambiare entro**, le **etichette**, i **campi aggiuntivi** (PIN, PUK, numero di serie…, ciascuno **riservato** o no), le **note riservate** e una **descrizione** non riservata.

## <a id="password-usare"></a>Usare una password

- **Dall'elenco**: a fine riga i pulsanti copia l'utente, copia la password e apre il sito; il menu **⋯** (o il **tasto destro**) ha anche apri, modifica, preferita, storico e cestino. Un clic sulla riga apre la scheda.
- **Dalla scheda**: accanto a ogni valore ⧉ lo copia; per password, note e campi riservati 👁 **Mostra** fa vedere il valore al posto dei puntini, che tornano da soli dopo un minuto (o con un altro clic).
- **Codice di verifica**: se la voce ha la verifica in due passaggi, **Mostra il codice** fa comparire il codice a 6 cifre, come in un'app di autenticazione, con la barra del tempo che resta; finché la scheda è aperta si rinnova da solo ogni 30 secondi.
- **Appunti**: copiando un segreto dalla piattaforma aperta in `https://` o dal server stesso (`localhost`), gli appunti del computer **si svuotano dopo 30 secondi**, se nel frattempo non hai copiato altro dalla pagina. Con un indirizzo `http://` della rete il browser non lo consente: incolla e poi copia qualcos'altro.
- **Preferite** ★: la stella nella scheda (o nel menu della riga) mette la voce tra le **Preferite**, solo per te.
- **Cercare**: la ricerca trova le voci che contengono tutte le parole scritte nel nome, nell'utente, nei link, nel cliente, nelle etichette, nella descrizione o nei campi non riservati (mai nei segreti); maiuscole e accenti non contano. Sotto le linguette, i **filtri rapidi** scelgono di chi sono le voci: **Tutte**, **Personali**, **Condivise da me**, **Condivise con me** e, per chi gestisce le password condivise, **Di altri (gestione)**. Nell'elenco i filtri scelgono il **tipo** e l'**etichetta**; un clic su un'etichetta nell'elenco mostra le voci che la hanno.

## <a id="password-storico"></a>Segreti, storico e password precedenti

I segreti non compaiono mai negli elenchi e arrivano al browser solo quando li chiedi, uno alla volta. Ogni volta che qualcuno **mostra o copia** un segreto, la scheda lo annota nel suo **Storico** e il [registro attività](registro.md) lo riporta nella categoria **Password**, con il nome della voce e del campo: **mai il valore**.

- La scheda **Storico** elenca chi ha creato, modificato, condiviso, mostrato o copiato, con data e ora, e non si può cancellare. La visione del codice di verifica vi compare al massimo una volta ogni dieci minuti per persona.
- **Password precedenti**: quando una password cambia, la precedente resta nella scheda Storico, cifrata, con la data fino a cui è stata in uso: si può mostrare o copiare (e anche questo resta annotato). Se ne tengono le ultime 20.

## <a id="password-modificare"></a>Creare e modificare

**Nuova password** apre il modulo; **Modifica** nella scheda di una voce lo apre con i suoi dati. Nel campo della password:

- 👁 mostra quello che scrivi; **Attuale** carica la password salvata, per correggerla; **Genera** apre il [generatore](#password-generatore) e la sua scelta finisce nel campo. Sotto compare subito la [robustezza](#password-robustezza).
- Lasciato vuoto, la password salvata resta com'è; **Togli la password salvata** la cancella (va comunque tra le precedenti).
- **Verifica in due passaggi**: incolla la **chiave segreta** che il sito mostra sotto il QR code (lettere e cifre; spesso alla voce «Non riesci a scansionare?») oppure l'indirizzo `otpauth://totp/…` del QR code. I codici a contatore (HOTP) non sono gestiti.
- **Campi riservati e note riservate** già salvati non tornano nel modulo: un campo riservato resta com'è finché non ne scrivi un valore nuovo (solo allora puoi anche togliergli la spunta **Riservato**); le note si modificano dopo **Carica per modificarle**.

**Duplica** (nel menu della riga e in fondo alla scheda) serve quando per lo stesso servizio c'è un'altra credenziale, per esempio una chiave API o un token accanto alla password di accesso: apre una **voce nuova** con tipo, nome seguito da «(copia)», utente, email, dove si usa, link, cliente, etichette, descrizione, campi aggiuntivi e, se la voce è tua, la condivisione. I **segreti non si copiano**: password, verifica in due passaggi, note riservate e valori dei campi riservati (di cui resta il nome) sono da scrivere. Cambia il tipo, il nome e il segreto, poi **Crea**.

Se tra le password che vedi ce n'è già una con lo **stesso utente** (o la stessa email) **sullo stesso sito** o nello stesso **Dove si usa**, mentre compili compare l'avviso **Possibile doppione** con il link alla voce, e creando la voce viene chiesta conferma: spesso conviene aggiornare quella che c'è. Lo stesso sito con un altro utente o un nome simile compaiono solo come informazione. I segreti non si confrontano mai. Vedi [Avviso dei possibili doppioni](interfaccia.md#interfaccia-doppioni).

Chiudendo il modulo con modifiche non salvate viene chiesta conferma (vedi [Modifiche non salvate](interfaccia.md#interfaccia-non-salvate)). Se un collega salva la stessa voce mentre la stai modificando, il tuo salvataggio viene fermato con un messaggio che dice chi l'ha cambiata: chiudi e riapri la scheda per vedere la versione aggiornata. Le schede aperte in consultazione e l'elenco si aggiornano da soli quando qualcuno cambia una voce che vedi.

## <a id="password-generatore"></a>Generatore di password

**Generatore** , in alto nella pagina o accanto al campo della password, crea una password nel tuo browser, con il generatore casuale crittografico: non viaggia sulla rete finché non la salvi. Tre modi:

| Modo | Come è fatta |
| --- | --- |
| **Casuale** | Da 8 a 64 caratteri, scegliendo maiuscole, minuscole, cifre e simboli (almeno uno per tipo scelto). **Senza caratteri che si confondono** evita O 0 o I l 1, utile per le password da dettare o ricopiare (per esempio quella del Wi-Fi). I simboli sono quelli accettati quasi ovunque: niente virgolette, barre rovesciate e spazi. |
| **Da leggere** | Da 3 a 8 parole inventate di tre sillabe, con l'iniziale maiuscola, un separatore e due cifre in fondo (*Vatemo-Rilugo-Pisane-42*): facili da leggere e da dettare. |
| **PIN** | Da 4 a 12 cifre, per i codici che accettano solo numeri. Un PIN corto non è una password robusta. |

Sotto la password compaiono la robustezza e i **bit di casualità**: ogni bit in più raddoppia i tentativi che servirebbero per indovinarla. ↻ ne genera un'altra, ⧉ la copia. Le scelte restano ricordate nel browser. Aperto dalla pagina, **Salva nuova password** apre una nuova password con quella generata; aperto dal modulo, **Usa questa password** la mette nel campo.

## <a id="password-robustezza"></a>Robustezza

Una barra a cinque tacche stima quanto è difficile indovinare la password: **Molto debole**, **Debole**, **Discreta**, **Robusta**, **Molto robusta**. Contano la lunghezza e i tipi di caratteri; valgono poco le ripetizioni e le sequenze (*aaa*, *123*, *abc*, *Ab1!Ab1!*), le password più comuni, le parole più usate (anche scritte con cifre al posto delle lettere, come *P4ssw0rd*) e gli anni (*2024*). È un'indicazione: una password generata è sempre la scelta migliore. Il server conserva solo il livello, che serve all'elenco e al controllo, senza dover decifrare le password.

## <a id="password-condividere"></a>Condividere

Nel modulo della voce, la scheda **Condivisione**:

- **Condivisa con tutti**: **No**, **Sì, in sola lettura** oppure **Sì, con la modifica**. La vedono tutti gli utenti che usano la gestione password.
- **Colleghi e gruppi**: scrivi qualche lettera e scegli dall'elenco i colleghi (con un account abilitato) o i [gruppi di utenti](gruppi-policy.md); per ciascuno **Può vedere** (la scelta iniziale) oppure **Può modificare**; la **×** lo toglie. Il collega deve avere il permesso **Usare la gestione password** per aprire la pagina e vederla.

La condivisione vale dal salvataggio. Condivide chi ha il permesso **Condividere le password**; chi non lo ha può solo togliere la condivisione delle sue voci o ridurla.

| Chi | Che cosa può fare |
| --- | --- |
| Il proprietario | Tutto: modificare, condividere, spostare nel cestino, ripristinare ed eliminare. |
| Un destinatario con **Può modificare** (o **con la modifica**, per tutti) | Modificare la voce, password compresa. Non la condivisione, e non può spostarla nel cestino. |
| Un destinatario con **Può vedere** | Consultarla, copiarne e mostrarne i segreti; la scheda lo ricorda con la dicitura **Sola lettura**. |
| Chi ha **Gestire tutte le password condivise** | Vedere, modificare, condividere, cestinare ed eliminare **tutte le password condivise**, anche quelle non condivise con lui: la scheda lo dice. Le password **personali** degli altri restano invisibili anche a lui. |

- **Gruppi**: una voce condivisa con un gruppo arriva a tutti i suoi membri, anche a chi entra in seguito; chi ne esce smette di vederla. Chi la riceve in più modi ha il permesso più ampio.
- Nell'elenco la colonna **Condivisione** dice *Personale*, *Con tutti*, *Con Mario Rossi*, *Con 3 destinatari* oppure, per quelle ricevute, *Da Anna Verdi*; fermando il mouse compaiono tutti i nomi.
- Una password si può condividere al massimo con **100** tra utenti e gruppi.

## <a id="password-controllo"></a>Controllo delle password

La vista **Controllo** raccoglie le voci da sistemare, tra tutte quelle che vedi (comprese quelle condivise con te). Il numero sulla linguetta conta le voci con almeno un problema; un clic su un riquadro porta alla sua sezione, un clic su una voce ne apre la scheda e **Cambia** la apre direttamente in modifica.

| Sezione | Che cosa contiene |
| --- | --- |
| **Trafugate** | Compaiono tra le password trafugate nei furti di dati (Have I Been Pwned, dalla 1.140.0), con quante volte: chi prova le password a tappeto le conosce. Il server le controlla in sottofondo, senza che le password escano (vedi [Password trafugate](impostazioni.md#impostazioni-password)); salvando una password trafugata compare subito un avviso. |
| **Non leggibili** | Segreti cifrati con chiavi che questo server non ha (vedi [Riservatezza e backup](#password-riservatezza)): vanno scritti di nuovo. |
| **Scadute** | Hanno passato la data **Da cambiare entro**. |
| **Deboli** | Robustezza **Molto debole** o **Debole**. |
| **Ripetute** | La stessa password usata in più voci, a gruppi: chi ne scopre una entra anche nelle altre. |
| **In scadenza** | Da cambiare entro i prossimi 30 giorni. |
| **Vecchie** | Non cambiate da più di un anno. |

Il confronto avviene sul server, in memoria: le password non escono e non viene salvato nulla. Per le trafugate il server chiede a Have I Been Pwned solo l'inizio dell'impronta di ogni password e salva solo l'esito.

## <a id="password-clienti"></a>Le password dei clienti

Collegando una voce a un **cliente** (campo **Cliente** del modulo), la ritrovi nella [scheda del cliente](clienti.md), sezione **Password** , insieme alle altre voci del cliente che puoi vedere. Da lì **Nuova password per questo cliente** ne crea una già collegata e **Apri nella pagina Password** mostra l'elenco filtrato per quel cliente (il filtro compare accanto agli altri, con la **×** per toglierlo). Chi non può vedere il cliente collegato legge *Cliente riservato*.

## <a id="password-importare"></a>Importare ed esportare

**Importa** ⬆ apre l'importazione guidata, nel pannello a destra. Scegli l'**etichetta** da dare a tutte le voci importate (all'inizio *Importate*; vuota per non darne) e il file, anche trascinandolo nel riquadro. Il file si legge nel computer; le voci importate sono tutte **personali**. Secondo il file:

- **CSV di un browser o di un gestore** (Chrome, Edge, Firefox: nelle impostazioni delle password, il comando per esportarle; Bitwarden, KeePass, LastPass, 1Password e simili): le colonne si riconoscono da sole (nome, indirizzo, utente, password, verifica in due passaggi, note, cartella o etichette). L'anteprima mostra il formato, quante righe verranno importate e le prime righe; le righe senza nome, indirizzo né utente si scartano, con il motivo.
- **Foglio Excel o CSV con altre colonne** (per esempio l'elenco degli apparati di un impianto): scegli che cosa c'è in ogni colonna (nome, indirizzo, utente, password, email, dove si usa, verifica in due passaggi, etichette, note). Le password non si vedono: al loro posto ci sono segnaposto come *[segreto 1]*. Con l'assistente AI attivo, **✨ Proponi con l'assistente** propone le colonne.
- **Documento** (testo, file INFO, Word, PDF): le password si trovano nelle righe come «password: …», «utente / password», «PIN: …» e negli elenchi degli apparati, con il nome dalla riga o dal titolo sopra. Con l'assistente AI attivo, **✨ Analizza con l'assistente** le cerca leggendo il documento: capisce meglio nomi, utenti, indirizzi e dove si usano. **All'assistente non arriva nessuna password**: ogni password, e ogni valore che ne ha l'aspetto, diventa un segnaposto prima di partire e torna al suo valore nel computer; *Che cosa ha letto l'assistente* mostra il testo che è partito.

Per fogli e documenti c'è poi il **controllo delle voci**: una riga per password, con nome, utente, indirizzo e dove si usa da correggere, la password nascosta (**Mostra le password** per vederle) e la riga del documento da cui viene. Togli la spunta a quelle da non importare (**Tutte**, **Nessuna**), poi **Importa**. Un indirizzo che non è un sito (un indirizzo IP) va in «Dove si usa».

Al massimo 5 MB e 5.000 righe per file. Un codice di verifica in due passaggi non riconosciuto non ferma la riga: la voce viene importata senza, e l'esito lo segnala.

**Esporta CSV** ⬇ (con il permesso **Esportare le password**) scarica in un file CSV **in chiaro** le password che vedi, escluse quelle nel cestino: tutte, oppure solo quelle mostrate dai filtri. Chiede la **password del tuo account**. Le colonne sono quelle che leggono browser e gestori: `name`, `url`, `username`, `password`, `totp`, `notes`, più `email`, `location`, `customer`, `tags` e `type`. L'esportazione resta nel registro attività e nello storico di ogni voce esportata.

> [!WARNING]
> Un file CSV di password è leggibile da chiunque lo apra: dopo un'importazione o un'esportazione **eliminalo** (e svuota il cestino del computer). Non inviarlo per email e non lasciarlo in cartelle condivise.

## <a id="password-cestino"></a>Cestino

**Sposta nel cestino** 🗑 è del **proprietario** (e, per le condivise, di chi le gestisce). Una voce condivisa nel cestino **sparisce anche ai destinatari**, per questo viene chiesta conferma. Dalla vista **Cestino**, **Ripristina** la rimette com'era, condivisione compresa; **Elimina definitivamente** la cancella con lo storico e le password precedenti. Dopo **30 giorni** nel cestino una voce si elimina da sola.

## <a id="password-permessi"></a>Permessi

| Permesso | Che cosa consente |
| --- | --- |
| Usare la gestione password | Aprire la pagina, creare voci personali, vedere quelle condivise con sé, importare. |
| Condividere le password | Condividere le proprie voci con colleghi, gruppi o tutti (comprende Usare). |
| Gestire tutte le password condivise | Vedere e gestire ogni voce condivisa, anche quelle non condivise con sé e quelle di utenti eliminati (comprende Condividere). |
| Gestire i tipi delle password | Aggiungere, rinominare, colorare ed eliminare i [tipi](#password-tipi), uguali per tutti (comprende Usare). |
| Esportare le password | Scaricare in CSV le password che si vedono, confermando la propria password (comprende Usare). |

## <a id="password-riservatezza"></a>Riservatezza e backup

> [!NOTE]
> Una password **personale** la vede solo chi l'ha creata: nessun altro. Nel database i segreti sono cifrati con le chiavi del server (le stesse che proteggono sessioni e password della posta); nel registro attività finiscono le operazioni, mai i valori. Le password sono comprese nei backup.

- **Backup cifrati**: portano con sé le chiavi, quindi le password restano leggibili anche ripristinando su un altro server. Un backup **non cifrato** ripristinato su un altro server lascia le voci al loro posto, ma i segreti non si leggono più: il [controllo](#password-controllo) li elenca tra i **Non leggibili** e vanno scritti di nuovo. Per questo, con la gestione password, conviene [cifrare i backup](backup.md#backup-impostazioni).
- **Eliminando un utente** le sue password personali vengono eliminate; quelle che aveva condiviso restano ai destinatari, senza proprietario, e le gestisce chi ha **Gestire tutte le password condivise**. **Disabilitando** l'utente restano tutte.
- **Eliminando un gruppo di utenti** finisce la condivisione fatta con quel gruppo.

## <a id="password-limiti"></a>Limiti

| Che cosa | Limite |
| --- | --- |
| Nome · utente · dove si usa | 200 · 200 · 300 caratteri |
| Password | 1.000 caratteri |
| Link | 10 per voce (indirizzo fino a 1.000 caratteri, etichetta fino a 60) |
| Etichette | 10 per voce, ciascuna fino a 40 caratteri |
| Campi aggiuntivi | 20 per voce (nome fino a 60 caratteri, valore fino a 2.000) |
| Note riservate · descrizione | 10.000 · 4.000 caratteri |
| Password precedenti | le ultime 20 per voce |
| Condivisione | 100 tra utenti e gruppi per voce |
| Voci | 20.000 per persona, compreso il cestino |
| Importazione | 5 MB e 5.000 righe per file |

---

[← Rubrica](rubrica.md) · [Indice](README.md) · [Clienti →](clienti.md)
