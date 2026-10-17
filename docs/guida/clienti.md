[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="clienti"></a>Clienti

**Anagrafiche → Clienti** raccoglie persone fisiche e aziende: i clienti e i potenziali clienti. La pagina gemella **Anagrafiche → Fornitori** mostra le schede dei fornitori: è la stessa anagrafica, e un'azienda che è insieme cliente e fornitore ha una scheda sola (vedi [Ruoli: clienti, potenziali clienti e fornitori](#clienti-ruoli)). L'elenco si cerca per nome, codice, gruppo, partita IVA, codice fiscale, città, email o telefono e si filtra per ruolo, tipo, gruppo, [categoria](#clienti-categorie) e stato; sotto le linguette **Clienti** (o **Fornitori**), **Gruppi** e **Cestino**, i **filtri rapidi** scelgono la visibilità: **Tutti**, **Condivisi** e **Miei privati**. **Esporta CSV** e **Importa** scambiano le schede con Excel e con altri programmi: vedi [Esportare i clienti in un file CSV](#clienti-esporta) e [Importare i clienti da un file CSV o JSON](#clienti-importa).

## <a id="clienti-ruoli"></a>Ruoli: clienti, potenziali clienti e fornitori

Ogni scheda ha uno o più **ruoli**, scelti in cima alla scheda con i pulsanti **Cliente** , **Potenziale** e **Fornitore** :

- **Cliente** e **Potenziale cliente** si escludono: quando un potenziale cliente compra, un clic su **Cliente** lo trasforma, senza rifare la scheda. Dalla 1.125.0 lo fa anche da solo quando **accetta un preventivo** (anche con il link) o riceve una **fattura** o un DDT: diventa cliente e il codice automatico *P00003* prende il prossimo *C* (un codice scritto a mano resta); lo dice un avviso e lo storico del documento.
- **Fornitore** sta da solo oppure insieme a uno dei due: chi ti vende e ti compra è **Cliente** e **Fornitore**, con una sola scheda, gli stessi recapiti e le stesse coordinate bancarie.
- Serve almeno un ruolo: togliere l'ultimo non si può.
- La pagina **Clienti** mostra clienti e potenziali; il filtro del ruolo sceglie **Solo clienti**, **Solo potenziali** oppure **Anche fornitori**. La pagina **Fornitori** mostra le schede con il ruolo Fornitore (**Anche clienti** o **Solo fornitori**). Accanto al nome un'etichetta dice i ruoli che la pagina non dice già: Potenziale o Fornitore tra i clienti, Cliente tra i fornitori.
- **Nuovo cliente** e **Nuovo fornitore** creano la scheda già con quel ruolo.
- Il **codice** assegnato da solo dice il ruolo di partenza: `C00001` per i clienti, `F00001` per i soli fornitori, `P00001` per i potenziali clienti. Se poi i ruoli cambiano, il codice resta.
- Ricerca generale, documenti, attività, progetti e password trovano e collegano anche i fornitori: nei suggerimenti accanto al nome compare *Fornitore* o *Potenziale cliente*.
- Le due pagine usano gli stessi [permessi dei clienti](#clienti-permessi).

## <a id="clienti-anagrafica"></a>Anagrafica

Scegli **Azienda** (ragione sociale, forma giuridica) oppure **Persona fisica** (nome, cognome, titolo, genere, data e luogo di nascita). Poi:

- **Maiuscole e minuscole**: ragione sociale, forma giuridica, nome e cognome prendono da soli la forma giusta quando esci dal campo (`ROSSI E FIGLI SNC` diventa *Rossi e Figli S.n.c.*, `de luca` *De Luca*); ciò che scrivi con maiuscole e minuscole volute (*ACME Impianti*) resta com'è. Vedi [Maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato).
- **Genere**: se è attivo il [genere dai nomi](impostazioni.md#impostazioni-genere), uscendo dal campo Nome con il genere ancora da indicare la piattaforma lo propone (sotto compare *Dedotto dal nome…*). Il pulsante ✨ **Genere dal nome**, accanto alla tendina, lo applica quando vuoi, anche al posto di un genere già scelto; se il nome è incerto (per esempio *Andrea*) lo dice e lascia la scelta a te. Il genere si cambia sempre a mano, e serve anche a **Calcola** del codice fiscale.
- **Gruppo**: vedi [Gruppi di clienti](#clienti-gruppi).
- **Codice**: lasciato vuoto viene assegnato da solo secondo il ruolo (C00001, F00001, P00001…); altrimenti scrivine uno tuo, unico.
- **Categoria**: si sceglie dall'elenco (Partner, Rivenditore, Installatore…), ognuna con il suo colore; vedi [Categorie dei clienti](#clienti-categorie). Le **etichette** invece sono parole libere per ritrovare la scheda (VIP, Edilizia…). Se è un cliente, un potenziale cliente o un fornitore lo dicono i [ruoli](#clienti-ruoli).
- **Immagine o logo**: **Dal PC**, **Incolla** (anche Ctrl+V in qualunque punto della scheda) o **Da un indirizzo web** (vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini)); il ritaglio ti fa spostare, ingrandire e ruotare l'immagine e scegliere lo sfondo prima di salvarla. In alternativa **Icona e colore** (vedi [Icone e colori](interfaccia.md#interfaccia-icone)): compare nell'elenco e nella scheda quando non c'è un'immagine.
- Sotto la **data di nascita** di una persona compare il suo **segno zodiacale** (anche nella stampa della scheda): solo un'informazione in più. Lo stesso nelle schede del personale e degli utenti.
- **Attivo**, nella fascia dei pulsanti in basso: una scheda non attiva resta in archivio e si nasconde con il filtro **Attivi**.

Se esiste già un cliente con lo stesso codice fiscale, la stessa partita IVA o lo stesso nome compare l'avviso **Possibile doppione**.

**Duplica** (nel menu della riga e in fondo alla scheda, per chi può creare schede o ha la rubrica personale) apre una **scheda nuova** con gli stessi dati, comoda per un'altra sede o un'altra società dello stesso gruppo: ruoli, anagrafica, categoria, gruppo, etichette, contatti, indirizzi (con le coordinate), coordinate bancarie, referenti e note. Non si copia ciò che identifica la scheda: **codice** (se ne assegna uno nuovo), **codice fiscale**, **partita IVA**, **codice SDI**, **PEC** e immagine. Al nome si aggiunge «(copia)»: cambialo, completa i dati fiscali e premi **Crea**. La copia di un tuo contatto privato resta privata.

## <a id="clienti-da-testo"></a>Una scheda nuova da un testo

Con l'[assistente AI](assistente-ai.md) attivo, **Da un testo** (in alto nelle pagine Clienti e Fornitori, per chi può creare schede) apre un pannello dove incollare una **firma email**, un **biglietto da visita** trascritto, un'email, l'intestazione di una fattura o una visura. **Proponi i dati** chiede all'assistente ragione sociale e forma (o nome e cognome di un privato), partita IVA, codice fiscale, codice SDI, PEC, sito, email, telefoni, indirizzi e referenti, e apre la **scheda nuova già compilata**: controllala, correggila e salvala come sempre. L'assistente usa solo ciò che c'è nel testo; i dati in un formato sbagliato (una partita IVA che non ha 11 cifre, un'email senza chiocciola) li toglie e lo scrive in cima alla scheda. La **provincia** di un indirizzo italiano, se nel testo manca o è scritta per intero, si prende dall'elenco dei comuni (con il CAP tra paesi omonimi). Niente si salva da solo e il testo non si conserva; se l'assistente usa un servizio esterno, il testo esce dall'azienda (lo dice l'informativa). Lo stesso pulsante c'è anche nel [Personale](personale.md#personale-da-testo) e in [Mezzi e Attrezzature](mezzi.md#mezzi-da-testo).

Dalla 1.102.0 il testo può arrivare anche **da un file**: il riquadro **Da un file** sopra il campo (ci si trascina il file o un clic lo sceglie; il file si può lasciare anche sul campo, o incollare con <kbd>Ctrl</kbd>+<kbd>V</kbd> una scansione copiata) legge un **PDF** o una **scansione**, anche una foto fatta con il telefono: la visura camerale, il libretto di circolazione, il biglietto da visita, un attestato. I PDF con il testo si leggono subito, le scansioni con il [riconoscimento del testo](documenti.md#documenti-ocr) del server. Il testo finisce nel campo: controllalo (e togli quello che non serve) prima di **Proponi i dati**.

## <a id="clienti-fiscali"></a>Dati fiscali e codice fiscale

Codice fiscale, partita IVA (con il paese), codice destinatario SDI e PEC vengono controllati mentre scrivi: per codice fiscale e partita IVA italiana si verifica anche il carattere di controllo.

- **Calcola** (persone fisiche) ricava il codice fiscale da nome, cognome, data di nascita, genere e **luogo di nascita**. Il luogo va scelto dall'elenco: comune italiano con la provincia, per esempio `Ragusa (RG)`, comune soppresso o rinominato, oppure stato estero.
- Al contrario, da un codice fiscale già scritto **Compila i dati mancanti** ricava data di nascita, genere e luogo.
- Se il codice non corrisponde a nome, cognome, data, genere o luogo dell'anagrafica compare un avviso.

> [!WARNING]
> Il codice calcolato va sempre confrontato con la tessera sanitaria: quando due persone avrebbero lo stesso codice (**omocodia**) l'Agenzia delle Entrate ne assegna uno diverso, che la piattaforma riconosce come valido ma non può calcolare.

## <a id="clienti-contatti"></a>Contatti, indirizzi e coordinate bancarie

- **Contatti**: più email e telefoni, ciascuno con un'etichetta (Lavoro, Amministrazione, Cellulare…), il **sito web** e i **referenti**, cioè le persone da contattare presso il cliente. Email e telefoni si controllano da soli: vedi [Campi che si controllano e si compilano da soli](interfaccia.md#interfaccia-campi). Il pulsante **Apri il sito**, accanto al sito web, lo apre in una nuova scheda del browser: è attivo quando l'indirizzo scritto è valido e, se manca `https://`, lo aggiunge da solo.
- **Indirizzi**: sede legale, sede operativa, residenza… con via, CAP, città, provincia e paese. L'etichetta è anche il **nome della sede** in cui stanno gli [impianti](impianti.md#impianti-sedi) del cliente: scrivi quello che usi (*Casa al mare*, *PV 01*, *Magazzino*); gli impianti restano legati alla loro sede anche se poi ne cambi il nome o l'indirizzo. Nel campo **Coordinate** scrivi latitudine e longitudine (`45.4642, 9.19`) oppure incolla un link di Google Maps; il pulsante accanto apre **Google Maps**: sul punto esatto se ci sono le coordinate, altrimenti cercando l'indirizzo scritto (lì le copi, calcoli un percorso, guardi Street View).
- **Mappa degli indirizzi** : in cima alla scheda **Indirizzi**, gli indirizzi con le coordinate compaiono su una mappa, ognuno con un segnaposto numerato come la sua riga (1 il primo dell'elenco, 2 il secondo…), e la vista li comprende tutti. Un clic sul segnaposto mostra etichetta e indirizzo e porta alla sua riga; la rotellina del mouse ingrandisce dopo un clic sulla mappa, così scorrendo la scheda non la sposti per sbaglio. Si aggiorna mentre scrivi o cerchi le coordinate; se nessun indirizzo le ha ancora, al posto della mappa c'è un promemoria. Le mappe sono quelle di **OpenStreetMap**: il browser ne scarica solo i riquadri della zona mostrata (OpenStreetMap vede quindi la zona, non i dati della scheda).
- **Cercare un indirizzo**: se un amministratore ha attivato la [ricerca degli indirizzi](impostazioni.md#impostazioni-indirizzi), nel campo della via c'è una lente 🔍. Si apre un riquadro in cui scrivere via e città, un luogo o un CAP, oppure incollare le coordinate o un link di Google Maps; scegli il risultato giusto (con il mouse, oppure con le frecce e <kbd>Invio</kbd>) e via, CAP, città, provincia, paese e coordinate si compilano da soli. Un risultato senza via (una città, un CAP) lascia la via già scritta. Incollando le **coordinate** in una riga ancora vuota, la ricerca parte da sola e propone gli indirizzi più vicini, dal più vicino.
- **Coordinate bancarie**: l'IBAN viene controllato e scritto a gruppi di quattro caratteri; per i conti italiani compaiono ABI e CAB. Poi BIC/SWIFT, banca e intestatario.

Di ogni tipo (email, telefoni, indirizzi, coordinate bancarie, referenti) si possono avere fino a **200 voci**: tante quante ne servono a chi ha molte sedi, come una catena di negozi o un amministratore di condomìni, ognuna con il suo telefono e il suo referente.

Via, città, provincia e paese, nome e ruolo dei referenti, le etichette di recapiti e indirizzi, la banca e l'intestatario prendono anch'essi da soli maiuscole e minuscole (`via roma 12/a` diventa *Via Roma 12/A*, una città scritta `RAGUSA` diventa *Ragusa*): vedi [Maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato).

## <a id="clienti-gruppi"></a>Gruppi di clienti

Il gruppo è un'**etichetta**: nel campo **Gruppo** dell'anagrafica scrivi un nome nuovo oppure scegline uno esistente dall'elenco che compare. Esempio: «Rossi Auto Ragusa» e «Rossi Auto Modica» nel gruppo «Gruppo Rossi». Ogni scheda sta in **un solo gruppo**.

- Per mettere **molte schede** in un gruppo in una volta scegline più d'una nell'elenco e premi **Metti nel gruppo…**: vedi [Scegliere più schede insieme](#clienti-selezione).
- Per vedere tutti i clienti di un gruppo fai clic sul **nome del gruppo** in una riga dell'elenco, oppure usa il filtro dei gruppi o la linguetta **Gruppi**.
- Dalla scheda **Gruppi** (tasto destro o ⋯) un gruppo si **rinomina**, gli si aggiunge una descrizione o si **elimina**: i clienti restano, senza gruppo.
- Un gruppo senza descrizione che nessun cliente usa più **sparisce da solo**.

## <a id="clienti-categorie"></a>Categorie dei clienti

La **categoria** classifica la scheda (Partner, Rivenditore, Installatore, Professionista, Ente pubblico, Ex cliente…): si sceglie dall'elenco nel campo **Categoria** dell'anagrafica, e ognuna ha il suo **colore**, come le [categorie dei documenti](documenti.md#documenti-scheda). Nell'elenco delle schede compare accanto al nome come etichetta colorata, e il filtro **Tutte le categorie** mostra le schede di una categoria o quelle **Senza categoria**.

- Chi ha il permesso **Gestire le categorie dei clienti** vede in cima alla pagina il pulsante **Categorie**: aggiunge, rinomina, sceglie icona e colore ed elimina le categorie, uguali per tutti, nel pannello dei [tipi e delle categorie](interfaccia.md#interfaccia-tipi). Sotto ognuna c'è quante schede la usano (tra quelle che vedi).
- Eliminando una categoria, le schede che l'avevano restano **senza categoria**; rinominandola, il nuovo nome vale subito per tutte.
- **Importare**: la colonna `Categoria` del file usa la categoria con quel nome (maiuscole e minuscole non contano); un nome che nell'elenco non c'è viene aggiunto, con il colore predefinito, da cambiare poi con **Categorie**. **Esportare** scrive il nome della categoria.
- Le categorie scritte nelle schede prima che ci fosse l'elenco ci sono già, ognuna con un colore (la stessa parola scritta in modi diversi, per esempio «partner» e «Partner», è una categoria sola).

## <a id="clienti-selezione"></a>Scegliere più schede insieme

Premi l'icona **Scegli più righe**, la prima a sinistra nella barra della ricerca: ogni riga dell'elenco mostra una **casella** a sinistra (premendo di nuovo l'icona le caselle spariscono e la scelta si toglie). Spunta le schede su cui lavorare:

- un clic sulla casella sceglie o toglie una scheda; con <kbd>Maiusc</kbd> premuto sceglie tutte quelle tra l'ultima casella cliccata e questa;
- la casella nell'intestazione sceglie **tutte le schede dell'elenco filtrato** (anche quelle più in basso, non ancora mostrate): prima cerca o filtra, per esempio per città, poi scegli tutte.

Sopra l'elenco compare la barra con il numero delle schede scelte e le azioni:

- **Metti nel gruppo…** : scrivi il nome del gruppo o sceglilo tra quelli esistenti. Le schede che erano in un altro gruppo passano a questo.
- **Togli dal gruppo**: le schede restano senza gruppo.
- **Ruoli**: aggiunge o toglie un [ruolo](#clienti-ruoli) a tutte. Aggiungendo **Potenziale** si toglie **Cliente**, e viceversa; una scheda che resterebbe senza ruoli resta com'era.
- **Sposta nel cestino**: dopo una conferma; il messaggio che segue ha **Annulla** per riportarle indietro subito.
- **Deseleziona** toglie la scelta.

Al termine un messaggio dice quante schede sono cambiate. Le schede che non puoi modificare (o eliminare) restano com'erano, e il messaggio ne elenca qualcuna con il motivo. Le azioni compaiono a chi può modificare o eliminare almeno qualche scheda: il controllo vero si fa scheda per scheda, con gli stessi [permessi](#clienti-permessi) della modifica una alla volta.

## <a id="clienti-cestino"></a>Cestino

**Sposta nel cestino**, dal menu della riga (tasto destro o ⋯), dalla scheda o dalla barra delle schede scelte, non elimina subito: la scheda va nel **Cestino**, la linguetta accanto a **Gruppi** con il numero di quelle che contiene. Il messaggio che compare ha **Annulla**, per un ripensamento immediato.

- Nel cestino una scheda **non compare altrove**: non negli elenchi, nella ricerca, nei suggerimenti di documenti e attività o nei conteggi dei gruppi. Si apre in sola lettura.
- **Ripristina** la rimette com'era, con gruppo, ruoli, recapiti e collegamenti. Serve lo stesso permesso che serve per spostarla nel cestino.
- Dopo **30 giorni** nel cestino la scheda viene eliminata da sola, con la sua immagine; l'elenco del cestino dice il giorno.
- **Elimina definitivamente** (sulle schede scelte) e **Svuota cestino** cancellano per sempre, dopo una conferma: servono il permesso **Svuotare il cestino dei clienti** e quello di vedere la scheda; i propri contatti privati li elimina sempre il proprietario. Con la scheda se ne vanno anche i suoi [impianti](impianti.md) e le loro [certificazioni](certificazioni.md); le cartelle in Documenti restano.
- Il **codice** di una scheda nel cestino resta suo: un'importazione con lo stesso codice si ferma e chiede di ripristinarla, oppure di lasciare vuoto il codice per crearne una nuova.

## <a id="clienti-privati"></a>Contatti privati

Nella sezione **Visibilità** un cliente può essere **condiviso** (lo vede chi ha accesso ai clienti) oppure **privato**: un contatto personale che vede solo il proprietario. Per gli altri utenti non esiste: non compare in elenchi, ricerche, suggerimenti e conteggi dei gruppi.

## <a id="clienti-esporta"></a>Esportare i clienti in un file CSV

**Esporta CSV** ⬇ scarica un file apribile con Excel con **tutte le schede della pagina che puoi vedere**: dalla pagina Clienti `clienti-<data>.csv`, con clienti e potenziali clienti; dalla pagina Fornitori `fornitori-<data>.csv`. La ricerca e i filtri dell'elenco non contano, le schede nel cestino non ci sono. Il pulsante compare a chi ha il permesso **Esportare i clienti**. Ogni riga è una scheda, con le colonne:

`Codice` · `Tipo` · `Ruoli` · `Nome` · `Ragione sociale` · `Forma giuridica` · `Titolo` · `Cognome` · `Nome proprio` · `Genere` · `Data di nascita` · `Luogo di nascita` · `Codice fiscale` · `Partita IVA` · `Codice SDI` · `PEC` · `Email` · `Telefono` · `Sito web` · `Indirizzo` · `CAP` · `Città` · `Provincia` · `Nazione` · `Categoria` · `Gruppo` · `Etichette` · `Note` · `Stato` · `Visibilità` · `Aggiornato il`

- Sono le colonne riconosciute dall'importazione: il file esportato **si reimporta così com'è**, su questa o su un'altra installazione.
- Di ogni cliente il file riporta la **prima email**, il **primo telefono** e il **primo indirizzo**. Gli altri recapiti, i referenti, le coordinate bancarie e le immagini non ci sono: per una copia completa dei dati serve un [backup](backup.md).
- I valori che iniziano con `=`, `+`, `-` o `@` (per esempio i telefoni `+39…`) sono preceduti da un apostrofo, perché Excel non li scambi per formule: l'importazione lo toglie da sola.

## <a id="clienti-importa"></a>Importare i clienti da un file CSV, Excel o JSON

**Importa** ⬆ aggiunge all'archivio i clienti elencati in un file: quelli esportati da un'altra installazione, quelli di un altro programma, un elenco preparato con Excel (file **CSV** o direttamente il foglio **.xlsx**, **.xls**, **.ods**) oppure l'intero archivio di un vecchio gestionale, con più indirizzi, recapiti, referenti e banche per cliente (file **JSON**). L'importazione **aggiunge soltanto**: non modifica e non sostituisce mai un cliente già presente e, ripetuta sullo stesso file, non crea doppioni.

1. **Scegli il file** o trascinalo nella finestra. Se puoi creare sia clienti condivisi sia contatti privati, indica prima in **Importa come** se saranno **Clienti condivisi** oppure **Miei contatti privati**. In **Ruolo** scegli **Cliente**, **Potenziale** o **Fornitore**: è il ruolo delle righe che non lo dicono da sole con la colonna `Ruoli` (dalla pagina Fornitori parte già da **Fornitore**).
2. Da un **foglio Excel**, o da un CSV con colonne dai nomi diversi da quelli del modello: scegli **che cosa c'è in ogni colonna** (quelle con il nome giusto sono già scelte; con l'assistente AI attivo, **✨ Proponi con l'assistente** le propone guardando i nomi e i primi valori). Serve il nome: *Ragione sociale*, oppure *Cognome* e *Nome proprio*, oppure *Nome intero*. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda. Le partite IVA e i CAP che Excel ha trasformato in numeri riprendono gli zeri davanti. Anche dall'anteprima di un CSV con colonne ignorate si arriva qui con **Scegli le colonne**.
3. Controlla l'**anteprima**: ogni riga del file ha il suo esito e una casella per decidere se importarla.
4. Premi **Importa N clienti**: al termine un riepilogo dice quanti clienti sono stati **creati**, quanti **saltati** e, riga per riga, perché.

### Il formato del file CSV

- Un file `.csv` o `.txt` di al massimo **20 MB** e **10.000 righe** di dati: un elenco più lungo va diviso in più file.
- La **prima riga è l'intestazione** con i nomi delle colonne, ed è obbligatoria. Le colonne possono stare in qualsiasi ordine; nei nomi non contano maiuscole, accenti, spazi e punteggiatura (`C.F.`, `citta`, `E-mail` vanno bene). Serve almeno una colonna da cui ricavare il nome: `Ragione sociale` per le aziende, `Cognome` e `Nome` per le persone.
- **Separatore**: punto e virgola, virgola o tabulazione. **Codifica**: UTF-8, UTF-16 oppure Windows-1252, cioè quella del CSV salvato da Excel. Si riconoscono da soli e l'anteprima dice che cosa è stato trovato.
- **Scarica il modello** dà il file `modello-clienti.csv` con la sola riga di intestazione e tutte le colonne importabili: compilalo con Excel, una riga per cliente, e salvalo in formato CSV.

### Le colonne riconosciute

| Colonne | Contenuto |
| --- | --- |
| `Codice` | Il codice cliente. Lasciato vuoto viene assegnato il prossimo libero. Accettati anche *Codice cliente* e *Cod*. |
| `Tipo` | **Azienda** (anche Società, Ditta, Ente) oppure **Persona fisica** (anche Persona, Privato). Senza questa colonna, o con la cella vuota, è un'azienda la riga che ha la ragione sociale e una persona quella che ha cognome o nome. |
| `Ruoli` | Uno o più tra **Cliente**, **Potenziale cliente** (anche Potenziale, Prospect, Lead) e **Fornitore**, separati da virgola, punto e virgola, barra o «e»: *Cliente, Fornitore*. Cliente vince su Potenziale. Una parola non riconosciuta è segnalata accanto alla riga e non conta. Cella vuota o colonna assente: il ruolo scelto nella finestra. Accettati anche *Ruolo* e *Roles*. |
| `Ragione sociale`, `Forma giuridica` | Per le aziende. Accettati anche *Denominazione*, *Azienda*, *Società*. |
| `Cognome`, `Nome proprio`, `Titolo`, `Genere`, `Data di nascita`, `Luogo di nascita` | Per le persone. Genere: M, F o X. Data: `gg/mm/aaaa` (anche con trattini o punti) oppure `aaaa-mm-gg`. Accettati anche *Sesso*, *Nato il*, *Nato a*. |
| `Nome` | Nel file esportato dalla piattaforma è il nome mostrato in elenco, usato solo se mancano le altre colonne del nome. Nei file di altri programmi che hanno `Cognome` ma non `Nome proprio` è il nome di battesimo. |
| `Codice fiscale`, `Partita IVA`, `Codice SDI`, `PEC` | Controllati come nella scheda del cliente. Una partita IVA estera va scritta con la sigla del paese davanti (`DE123456789`, `ATU12345678`): vale una delle sigle proposte nella scheda del cliente; senza sigla vale Italia. Accettati anche *CF*, *P.IVA*, *SDI*, *Codice destinatario*. |
| `Email`, `Telefono`, `Cellulare`, `Sito web` | I recapiti del cliente. Accettati anche *E-mail*, *Mail*, *Tel*, *Cell*, *Sito*. |
| `Indirizzo`, `CAP`, `Città`, `Provincia`, `Nazione`, `Latitudine`, `Longitudine` | Il primo indirizzo del cliente, con le eventuali coordinate. Per salvarlo serve almeno la via, il CAP o la città: provincia e nazione da sole non vengono importate, e una nota accanto alla riga lo dice. Accettati anche *Via*, *Comune*, *Località*, *Prov*, *Paese*. |
| `Categoria`, `Gruppo`, `Etichette`, `Note` | Le etichette si separano con la virgola o con il punto e virgola. Un gruppo che non esiste viene creato; la categoria è quella dell'[elenco](#clienti-categorie) con lo stesso nome, oppure viene aggiunta all'elenco con il colore predefinito; gruppo, categoria e forma giuridica prendono la grafia già in uso (*S.r.l.* e non *S.R.L.*). |
| `Referente`, `IBAN`, `BIC`, `Banca` | Un referente (il solo nome) e un conto bancario. |
| `Stato` | **Attivo** oppure **Non attivo** (anche Sì e No, Vero e Falso, 1 e 0). Vuoto vale attivo. |
| `Visibilità`, `Aggiornato il`, `Creato il`, `Proprietario` | Riconosciute ma non usate: la visibilità si sceglie nella finestra, non nel file. |

Le colonne con altri nomi vengono **ignorate**, e l'anteprima le elenca. Nomi, ragioni sociali e forme giuridiche, indirizzi, città, referenti e banche dei clienti importati prendono le stesse [maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato) della scheda: un file scritto tutto in maiuscolo non riempie l'archivio di nomi in maiuscolo (restano maiuscole le sigle).

### Il formato del file JSON

Serve per portare qui l'archivio di un altro gestionale con tutto quello che una riga di CSV non contiene: più indirizzi, recapiti, referenti e coordinate bancarie per cliente. Il file (`.json`, al massimo **20 MB** e **10.000 clienti**) è un elenco di clienti, oppure un oggetto con l'elenco in `customers`; ogni cliente ha i campi della scheda, con i nomi usati dalla piattaforma:

```
{ "customers": [
  { "code": "C00012", "kind": "company", "companyName": "ROSSI IMPIANTI SRL", "roles": ["customer", "supplier"],
    "vatNumber": "01234567897", "sdiCode": "M5UXCR1", "pec": "rossi@pec.it",
    "emails": ["info@rossi.it", { "label": "Amministrazione", "value": "amm@rossi.it" }],
    "phones": [["Ufficio", "0932 123456"], "333 1234567"],
    "addresses": [
      { "label": "Sede legale", "street": "Via Roma 1", "postalCode": "97100", "city": "Ragusa", "province": "RG" },
      { "name": "NEGOZIO CENTRO", "street": "Corso Italia 5", "city": "Ragusa",
        "contact": "Giuseppe Verdi", "phone": "0932 333333" } ],
    "people": [{ "name": "Anna Rossi", "role": "Amministrazione", "phone": "0932 555555" }],
    "bankAccounts": [{ "iban": "IT60X0542811101000000123456", "bankName": "Banca Prova" }],
    "tags": ["VIP"], "notes": "Testo libero", "active": true },
  { "kind": "person", "lastName": "BIANCHI", "firstName": "LUCIA", "fiscalCode": "BNCLCU85M41H163Q" }
] }
```

- **Campi semplici**: `code`, `kind` (company o person; anche Azienda o Persona fisica), `roles` (customer, prospect, supplier, oppure le parole della colonna `Ruoli`, in un elenco o in un testo), `companyName`, `legalForm`, `title`, `lastName`, `firstName`, `gender`, `birthDate`, `birthPlace`, `fiscalCode`, `vatNumber` (con `vatCountry` per una partita IVA estera), `sdiCode`, `pec`, `website`, `category`, `group`, `tags`, `notes`, `active`. Valgono anche i nomi delle colonne del CSV (`"Ragione sociale"`, `"Città"`…), e le maiuscole non contano.
- **Email e telefoni**: come testo, come coppia `[etichetta, valore]` o come `{ "label", "value" }`. Un **referente** con più telefoni o email (`phones`, `emails`) tiene il primo; gli altri vanno tra i recapiti del cliente, con il suo nome come etichetta.
- **Sedi**: `label` dice che sede è (Sede legale, Magazzino…); `name` è il nome di una destinazione (un condominio, un negozio della catena) e ne diventa l'etichetta, scritto come una ragione sociale e accorciato a 40 caratteri, con il nome intero nelle note. Il referente della sede (`contact`) diventa un referente del cliente con la sede come ruolo; telefono ed email di una sede senza referente vanno tra i recapiti del cliente, con la sede come etichetta.
- **Coordinate bancarie** senza IBAN (solo `abi` e `cab`, come per le ricevute bancarie) finiscono nelle note, da controllare.
- Nell'anteprima la colonna **Riga** di un file JSON è la posizione del cliente nell'elenco: 1, 2, 3…

### Dati non validi: nelle note, da controllare

Nei vecchi archivi i campi sono scritti come capitava: due email nello stesso campo, un nome al posto del telefono, una partita IVA sbagliata. Il cliente si importa lo stesso e **nessun dato del file si perde**:

- due o più email nello stesso campo diventano più email (un commento tra parentesi fa da etichetta); più numeri separati da `;` o `-` diventano più telefoni; le virgole tra le cifre di un numero si tolgono;
- ciò che resta non valido (codice fiscale, partita IVA, codice SDI, PEC, sito, telefoni ed email, una banca senza IBAN, coordinate incomplete, le voci oltre le 200 per tipo) va **in fondo alle note del cliente**, sotto «Dati del file da controllare», e il cliente prende l'etichetta Da controllare: scrivila nella ricerca dei clienti per ritrovarli tutti, e toglila quando hai sistemato;
- una «persona» che è in realtà un ente o una società (codice fiscale numerico di 11 cifre, oppure *condominio*, *associazione*, *S.r.l.*… nel nome) viene importata come **azienda**;
- ogni correzione è scritta accanto alla riga nell'anteprima; il riepilogo finale conta i clienti con dati da controllare e le persone importate come aziende.

Prima di importare **100 clienti o più** la piattaforma salva da sola una copia del database nella cartella `recovery` dei dati (restano le ultime 3), e il riepilogo ne dice il nome. Per tornare indietro si rimette quella copia al posto di `database\blackhole.db`, a servizio fermo; più comodo ancora, prima di un'importazione grande esegui un [backup manuale](backup.md#backup-elenco), che si ripristina dalla pagina Backup.

### L'anteprima e gli esiti

L'anteprima non scrive nulla in archivio. In alto dice come è stato letto il file (codifica, separatore, colonne riconosciute, oppure *File JSON*) e conta le righe per esito: un clic su un conteggio mostra solo quelle righe. La tabella mostra 500 righe alla volta; **Mostra altre 500** prosegue. Ogni riga ha uno di questi esiti, con il motivo accanto:

| Esito | Significato | Si importa? |
| --- | --- | --- |
| **Nuovo** | Dati validi e nessun cliente che gli somigli. | Sì: la riga è già selezionata. |
| **Possibile doppione** | Stesso codice fiscale, stessa partita IVA o stesso nome (senza contare la forma giuridica) di un cliente che puoi vedere, oppure di una riga precedente dello stesso file. Accanto c'è a chi somiglia: «uguale a C00012 Rossi S.r.l. (stessa partita IVA)», «uguale alla riga 7 del file (stesso nome)». | Solo se lo scegli: la riga non è selezionata. Selezionandola nasce un cliente nuovo, accanto a quello a cui somiglia. |
| **Già presente** | La colonna `Codice` è quella di un cliente che puoi vedere. | Mai: il cliente in archivio resta com'è. |
| **Errore** | Manca il nome, tipo non riconosciuto, valore troppo lungo, numero rovinato da Excel, codice cliente non valido, ripetuto nel file o non disponibile… Gli altri dati non validi (un codice fiscale o una partita IVA errati, un telefono scritto male) non fermano la riga: vanno nelle note, da controllare. | Mai: correggi la riga nel file e ripeti l'importazione. |

- **Seleziona tutti i nuovi** e **Deseleziona tutto** agiscono su tutte le righe; **Importa anche i possibili doppioni** li seleziona o li toglie tutti insieme. Se tra le righe scelte ci sono possibili doppioni, prima di importare viene chiesta una conferma.
- **Scegli un altro file** torna al primo passo. Chiudendo la finestra dopo aver cambiato la selezione viene chiesta conferma.
- Le righe scelte vengono importate **tutte insieme**: se qualcosa va storto a metà non resta un'importazione parziale, non viene creato nessun cliente.
- Al momento di importare gli esiti vengono ricalcolati: se nel frattempo un collega ha creato lo stesso cliente la riga viene **saltata**, e il riepilogo lo dice. Se il file è stato modificato dopo l'anteprima, l'anteprima va ripetuta.

### File passati da Excel

Excel tratta i codici come numeri e ne toglie gli zeri iniziali. L'importazione li rimette, scrivendolo ogni volta accanto alla riga:

- **partita IVA italiana** e **codice fiscale** numerico rimasti con 8, 9 o 10 cifre: riportati a 11 cifre (poi vale il normale controllo);
- **CAP** italiano di 3 o 4 cifre: riportato a 5 (`187` diventa `00187`);
- **codice SDI** di sole cifre più corto di 7: riportato a 7;
- **telefono** rimasto senza lo zero iniziale del prefisso: lo zero viene rimesso quando rende valido il numero.

> [!WARNING]
> Un numero lungo che Excel ha trasformato in **notazione scientifica** (`1,23E+10`) ha perso le sue cifre e non si può riparare: la riga risulta in errore. Nel foglio formatta la colonna come **Testo** prima di scrivere o incollare i valori, poi salva di nuovo il CSV. Anche un valore più lungo di quanto il campo consente è un errore: non viene mai accorciato di nascosto.

### Permessi e visibilità

- Il pulsante **Importa** compare a chi ha il permesso **Importare clienti**.
- **Clienti condivisi**: serve anche il permesso **Creare clienti**. Chi importa ne risulta l'autore, come se li avesse creati a mano.
- **Miei contatti privati**: serve anche la **Rubrica personale**. Il proprietario dei contatti importati è chi importa.
- I doppioni si cercano solo tra i clienti **che puoi vedere**: dei [contatti privati](#clienti-privati) degli altri non trapela nulla. Se un codice scritto nel file è già usato da un cliente che non vedi, la riga dice soltanto che il codice non è disponibile: lascia vuota la colonna `Codice` e verrà assegnato da solo.
- Nel [registro attività](registro.md) resta una sola voce per importazione, con il nome del file e i conteggi: mai nomi, codici fiscali o recapiti dei clienti.

## <a id="clienti-documenti"></a>Documenti, attività, progetti, impianti, password e stampa del cliente

Quando le sezioni della scheda non stanno tutte nella larghezza del pannello, quelle non scelte mostrano solo l'icona: fermando il mouse compare il nome (oppure allarga il pannello trascinandone la linguetta).

- La scheda **Attività** del cliente elenca le attività collegate al cliente, sia direttamente (campo **Cliente** nella [scheda dell'attività](attivita.md#attivita-scheda)) sia attraverso il loro progetto, con stato, scadenza e persone: un clic apre l'attività, **Nuova attività per questo cliente** (o **Nuova attività**, quando non ce n'è ancora nessuna) ne crea una già collegata, **Apri nella pagina Attività** le mostra nella pagina, filtrate per quel cliente. C'è per tutti e mostra solo le attività che puoi [vedere](attivita.md#attivita-condivisione).
- La scheda **Progetti** del cliente elenca i progetti e le commesse collegati (campo **Cliente** nella [scheda del progetto](progetti.md#progetti-scheda)), con stato e avanzamento: un clic apre la pagina del progetto. Compare a chi può **Vedere i progetti**, e mostra solo i progetti che puoi vedere.
- La scheda **Impianti** del cliente elenca i suoi [impianti](impianti.md) divisi per **sede** (gli indirizzi della scheda, ciascuno con il suo nome: *Casa al mare*, *PV 01*…), con tipo e data di installazione: un clic apre la pagina dell'impianto, **Nuovo impianto per questo cliente** ne crea uno già presso il cliente. Compare a chi può **Vedere gli impianti**.
- La scheda **Assistenza** del cliente elenca le sue [richieste di assistenza](assistenza.md) e i pezzi in laboratorio, le aperte prima, con **Nuova richiesta** già compilata con il cliente. Compare a chi può **Vedere l'assistenza**.
- La scheda **Documenti** del cliente elenca i file e le cartelle a cui è collegato (campo **Cliente** nella [scheda di un documento](documenti.md#documenti-scheda)): un clic apre il file nel visualizzatore, **Apri nella pagina Documenti** (c'è anche quando l'elenco è vuoto: da lì si carica un file e lo si collega al cliente) li mostra tutti nella pagina, filtrati per quel cliente. Vedi solo i documenti che puoi vedere: le [cartelle riservate](documenti.md#documenti-permessi) ad altri non compaiono. La scheda c'è per chi ha il permesso **Visualizzare i documenti**. In cima, a chi può condividere, i [link condivisi](condivisioni.md) collegati al cliente, con il loro stato.
- La scheda **Password** del cliente elenca le voci della [gestione password](password.md#password-clienti) collegate al cliente che puoi vedere, con la robustezza: un clic apre la scheda della password, **Nuova password per questo cliente** ne crea una già collegata. La scheda c'è per chi ha il permesso **Usare la gestione password**.
- La scheda **Privacy** dice se l'informativa è stata fornita, la manda per email o la stampa da firmare, registra il consenso alle comunicazioni commerciali ed esporta i dati del cliente (vedi [Informativa e consenso dei clienti](privacy.md#privacy-clienti)).
- **Stampa** 🖨, in fondo alla scheda, stampa il cliente; **Stampa** sopra l'elenco stampa i clienti mostrati, con i filtri applicati. Il formato è quello di tutte le [stampe della piattaforma](interfaccia.md#stampa).

## <a id="clienti-personale"></a>Anche nel personale

Una persona fisica tra i clienti può lavorare anche nell'azienda. A chi può **Vedere il personale**, in fondo alla sezione **Anagrafica** della scheda, il riquadro **Personale** mostra la sua [scheda del personale](personale.md) collegata, con **Apri la scheda**. Se nel personale c'è una persona con lo stesso codice fiscale, la propone (**Collega**); altrimenti, a chi può gestire il personale, **Crea la scheda nel personale** apre una scheda nuova con anagrafica, codice fiscale, email, telefoni, indirizzi e foto del cliente, già collegata: restano da scrivere mansione, contratto e assunzione. I dati si copiano solo in quel momento: dopo, ognuna si cambia per conto suo (vedi [Anche cliente](personale.md#personale-cliente)).

## <a id="clienti-valutazione"></a>Valutazione del cliente

Dalla 1.130.0 la linguetta **Valutazione** della scheda dice in un colpo d'occhio che cliente è: un **giudizio da 0 a 100** con una frase che lo riassume (per esempio «Cliente da 6 anni che ci fa lavorare parecchio: paga con qualche ritardo e ci lascia un buon margine»), **che cosa conviene fare** e i quattro aspetti, ognuno con il suo punteggio e i fatti che lo spiegano. Il programma la calcola ogni volta dai dati che ha già: non c'è niente da compilare.

| Aspetto | Da che cosa |
| --- | --- |
| **Come paga** | Le rate delle fatture scadute negli ultimi 24 mesi: in quanti giorni paga dopo la scadenza (in media, pesata sull'importo) e quanta parte paga in tempo (con 5 giorni di tolleranza). Contano anche le rate scadute e non ancora pagate, con il ritardo fino a oggi. Con scaduti oltre i 90 giorni il punteggio resta basso; se è [bloccato](vendite.md#vendite-crediti) va al minimo. |
| **Quanto è fedele** | Da quanti anni lavora con noi (il primo lavoro: una fattura, un DDT, una commessa, una richiesta di assistenza o un preventivo accettato), in quanti degli ultimi anni, quanto tempo fa l'ultimo lavoro e quanti preventivi accetta (ultimi 3 anni). |
| **Quanto ci fa lavorare** | Il fatturato degli ultimi 12 mesi e le ore di lavoro (attività e interventi) a confronto con gli altri clienti: con quanta parte del fatturato, in che posizione, rispetto ai 12 mesi prima; e quante commesse, richieste di assistenza e preventivi. |
| **Quanto ci fa guadagnare** | Il margine degli ultimi 24 mesi: il [consuntivo](progetti.md#progetti-budget) delle commesse completate e la previsione di quelle in corso, le vendite senza commessa di articoli del listino con il costo (o dal consuntivo dell'assistenza), meno il lavoro dell'assistenza non addebitato (righe gratuite, richieste «non da fatturare»). Le vendite senza un costo noto non contano e la valutazione lo dice. |

Il giudizio è la media pesata degli aspetti che si possono calcolare (come paga 30, fedeltà 20, lavoro 25, guadagno 25; ne servono almeno due): da 80 **ottimo cliente**, da 65 **buon cliente**, da 45 **nella media**, da 30 **da seguire**, sotto **attenzione** (sempre, se è bloccato per i pagamenti). I consigli vengono dai numeri: chiedere un acconto a chi paga in ritardo, rivedere i prezzi a chi lavora tanto ma rende poco, sentire chi non lavora con noi da più di un anno, tenere stretto chi è ottimo.

- Nell'elenco dei clienti la colonna **Valutazione** mostra punteggio e giudizio (clic sull'intestazione per ordinare: i migliori in alto, o quelli da seguire); nel menu della riga, **Valutazione** apre la linguetta. Il filtro **Tutti i giudizi**, accanto a quello dello stato, mostra soltanto gli ottimi, i buoni, quelli nella media, da seguire, con l'attenzione, **da seguire o attenzione** insieme (per la telefonata o il sollecito), oppure quelli **senza giudizio**; vale anche per la stampa dell'elenco (dalla 1.130.1).
- Nei [preventivi](preventivi.md) (dalla 1.131.0): nel **Nuovo preventivo** (e nella copia per un altro cliente), sotto il cliente scelto, l'avviso con il giudizio, la frase e il primo consiglio, insieme a quello dei pagamenti; nella scheda del preventivo, accanto al cliente, la pillola **Valutazione** (passa sopra per la frase e il consiglio).
- È un [dato riservato](gruppi-policy.md#policy-riservati) (permesso **Valutazione dei clienti**, nella policy proposta Amministrazione) e non compare mai in quello che vede il cliente: condivisioni, link del preventivo, stampe.
- Vale per i clienti, non per i potenziali clienti né per i fornitori. Un cliente nuovo, senza lavori, non ha ancora niente da valutare.

## <a id="clienti-permessi"></a>Permessi

Ciò che ciascuno può fare sui clienti condivisi dipende dai permessi delle sue [policy](gruppi-policy.md#policy-permessi). Gli amministratori possono tutto. Gli stessi permessi valgono per i potenziali clienti e per i fornitori, nelle pagine Clienti e Fornitori.

| Permesso | Consente |
| --- | --- |
| Visualizzare i clienti | Vedere l'elenco, le schede e i gruppi dei clienti condivisi. |
| Creare clienti | Aggiungere nuovi clienti condivisi. Da solo non permette di modificarli dopo averli creati (né di aggiungere l'immagine): per questo serve uno dei due permessi di modifica. |
| Modificare i clienti creati da sé | Modificare soltanto i clienti che hai creato tu. |
| Modificare tutti i clienti | Modificare qualsiasi cliente condiviso. |
| Eliminare i clienti creati da sé | Spostare nel [cestino](#clienti-cestino) (e ripristinare) soltanto i clienti che hai creato tu. |
| Eliminare qualsiasi cliente | Spostare nel cestino (e ripristinare) qualsiasi cliente condiviso. |
| Svuotare il cestino dei clienti | Eliminare definitivamente le schede nel cestino che puoi vedere, una alla volta o con **Svuota cestino**. Senza questo permesso le schede eliminate restano nel cestino e spariscono da sole dopo 30 giorni. |
| Gestire i gruppi di clienti | Rinominare, descrivere ed eliminare i gruppi di clienti. (Un gruppo nuovo nasce comunque scrivendone il nome nella scheda di un cliente che puoi modificare.) |
| Gestire le categorie dei clienti | Aggiungere, rinominare, colorare ed eliminare le [categorie](#clienti-categorie) con il pulsante **Categorie**. Sceglierne una nella scheda lo può fare chiunque modifichi la scheda. |
| Esportare i clienti | Scaricare in CSV i clienti che puoi vedere. |
| Importare clienti | Aggiungere clienti da un file CSV o JSON: condivisi se puoi crearli, privati se hai la rubrica personale. |
| Rubrica personale | Creare contatti privati, visibili solo a te. |
| Dati amministrativi dei clienti | Vedere e cambiare le **coordinate bancarie** (IBAN, BIC, banca) e il **codice destinatario SDI** di clienti e fornitori, anche nella stampa, nell'esportazione e nell'importazione. Senza, la scheda non ha la linguetta Coordinate né il campo SDI, e salvandola questi dati restano com'erano; nei propri contatti privati (la rubrica personale) si vedono e si scrivono comunque. Sono [dati riservati](gruppi-policy.md#policy-riservati). |
| Valutazione dei clienti | Vedere la [valutazione](#clienti-valutazione) di ogni cliente (come paga, fedeltà, lavoro e margine, con il giudizio e i consigli), nella scheda e nell'elenco. È un dato riservato. |

- **«Creati da sé»** significa creati con il tuo account, a mano o con un'importazione. Se l'account di chi ha creato un cliente viene eliminato, quel cliente non è più «di nessuno»: lo modifica o lo elimina solo chi ha il permesso su tutti.
- Nell'elenco e nella scheda compaiono solo i comandi che puoi usare: se un cliente non è tuo e non hai il permesso su tutti, la scheda si apre **in consultazione** e **Sposta nel cestino** non c'è.
- **Rendere privato** un cliente condiviso richiede di poterlo modificare ed eliminare e di avere la rubrica personale; **rendere condiviso** un proprio contatto privato richiede il permesso di creare clienti.
- Sui [contatti privati](#clienti-privati) questi permessi non contano: li gestisce solo il proprietario.

---

[← Password](password.md) · [Indice](README.md) · [Produttori →](produttori.md)
