[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="assistenza"></a>Assistenza

**Azienda → Assistenza** raccoglie le **richieste di assistenza dei clienti**: chi chiama (anche un cliente che non è ancora in anagrafica), dove, per quale impianto, chi cercare sul posto e il problema, con una **priorità** che dà la **scadenza** del primo intervento; poi gli **interventi**, anche pianificati come attività, finché il problema non è risolto. Il **laboratorio** segue allo stesso modo i pezzi che i clienti portano da riparare, dalla consegna al ritiro, con il cartellino da attaccare al pezzo e la ricevuta per il cliente. La pagina compare a chi può **Vedere l'assistenza**, con le stesse regole dei clienti: le richieste dei contatti privati le vede solo il proprietario (vedi [Permessi](#assistenza-permessi)).

## <a id="assistenza-pagina"></a>La pagina Assistenza

- **Da fare**: le richieste aperte di interventi sul posto o da remoto, prima quelle in ritardo e quelle che stanno per scadere.
- **Laboratorio**: i pezzi ricevuti, in lavorazione, in attesa o pronti da ritirare.
- **Chiuse**: le richieste risolte, i pezzi ritirati e le richieste annullate, con l'anno tra i filtri (a chi vede i prezzi anche l'imponibile del consuntivo e lo stato della fatturazione).
- **Da fatturare** (a chi vede i prezzi): le richieste chiuse con importi nel consuntivo che non sono ancora segnate «Fatturata» o «Non da fatturare», con imponibile e totale; **Scarica in CSV** le passa all'amministrazione. Vedi [Il consuntivo e la fatturazione](#assistenza-consuntivo).

Sotto le linguette, **Tutte**, **Assegnate a me** o **Senza tecnico**; nella barra, la ricerca (numero, [ticket del cliente](#assistenza-apertura), cliente, sede, impianto, problema, pezzo, matricola, chi ha chiamato, anche dalle cifre del telefono), la priorità, il tecnico e il tipo d'impianto. La colonna **Scadenza** dice entro quando fare il primo intervento, con quanto manca: in arancione nell'ultima parte del tempo, in rosso (con la riga segnata) quando è passata; fatto il primo intervento la scadenza non conta più. Il numero accanto alla linguetta diventa rosso se c'è una richiesta in ritardo. Un clic apre la [scheda della richiesta](#assistenza-scheda); il tasto destro (o ⋯) registra un intervento, pianifica, modifica e stampa. **Stampa** stampa l'elenco come lo stai guardando. L'elenco si aggiorna da solo e le scadenze scorrono minuto per minuto. Le stesse richieste stanno nella linguetta **Assistenza** della pagina di ogni impianto e della scheda di ogni cliente, con **Nuova richiesta** già compilata con il cliente (e l'impianto).

## <a id="assistenza-apertura"></a>Aprire una richiesta

**Nuova richiesta** (oppure **Ricevi un pezzo** per il [laboratorio](#assistenza-laboratorio)) apre il modulo, pensato per compilarlo mentre il cliente è al telefono:

- **Cliente**: scrivi il nome, il codice o il **numero di telefono** di chi chiama (bastano le ultime cifre): si trovano anche i numeri dei referenti della scheda, e chi ha chiamato si compila da solo. Se il cliente non c'è, **Cliente nuovo** chiede il minimo (azienda o condominio, oppure persona; telefono, email, indirizzo, con il comune scelto dall'elenco): con la richiesta nasce la sua scheda con l'etichetta **Da completare**, anche se chi risponde al telefono non ha i permessi dei clienti.
- **Chi ha chiamato**, con il telefono (si propongono i referenti del cliente).
- **Ticket del cliente**: il numero della richiesta nel sistema di assistenza (help desk) del cliente, se ce lo manda. La ricerca lo trova, compare nella scheda, nelle stampe, nell'attività pianificata e nell'email al cliente.
- **Dove**: l'**impianto** del cliente, che porta con sé sede e tipo (e fa comparire la richiesta nella pagina dell'impianto); se il cliente non sa dire quale, una delle sue **sedi** (o un altro indirizzo) con il **tipo d'impianto**. Un cliente con un **solo impianto** lo trova già scelto (dalla 1.125.0), da cambiare se la richiesta è per altro.
- **Chi cercare sul posto**, con il suo telefono e le indicazioni: per esempio, se chiama l'amministratore del condominio, la signora che apre e mostra il guasto (*citofono interno 4, le chiavi dal portiere*).
- **Il problema**, con [Migliora testo](assistente-ai.md#assistente-moduli) se l'assistente AI è attivo.
- La [priorità](#assistenza-priorita), con la scadenza che ne viene; il **tecnico** che la segue (tra le persone che vedono l'assistenza: riceve una notifica); le **note interne**, che non si stampano.

I nomi prendono da soli le maiuscole giuste e i telefoni il loro formato (*+39 333 123 4567*). **Apri la richiesta** le dà il numero successivo dell'anno, **AT 2026-012** per gli interventi e **LAB 2026-004** per il laboratorio, e apre la sua scheda. Chi l'ha aperta la modifica (anche il cliente, l'impianto e la priorità); chi gestisce l'assistenza modifica tutte le richieste.

## <a id="assistenza-da-testo"></a>Una richiesta da un'email o da un messaggio

Dalla 1.102.0, con l'[assistente](assistente-ai.md) attivo, **Da un testo** (in alto nella pagina Assistenza) apre un pannello dove incollare l'**email** o il **messaggio** del cliente, oppure il ticket del suo help desk; con **Da un file** il testo si legge anche da un PDF o da una scansione. **Proponi i dati** chiede all'assistente il cliente, chi ha scritto o chiamato, chi cercare sul posto e le indicazioni, l'indirizzo, l'impianto, il problema (riscritto chiaro, senza saluti e firme), la priorità (dal tono della richiesta: tutto fermo, urgente, senza fretta), il ticket del cliente e, per il laboratorio, il pezzo e la matricola. Poi la piattaforma cerca il **cliente** tra quelli che vedi: per partita IVA, email (anche dei referenti), telefono (anche di chi chiama) o nome; con il cliente trovato cerca il suo **impianto** dalle parole dell'impianto e dell'indirizzo. Si apre il modulo della **richiesta nuova già compilato**, con in cima come è stato trovato il cliente: se non c'è in anagrafica il modulo è già su «Cliente nuovo» con nome, telefono ed email. Controlla, correggi e apri la richiesta come sempre: niente si apre da solo e il testo non si conserva.

## <a id="assistenza-priorita"></a>Priorità e scadenze

La priorità dice entro quando fare il **primo intervento** (in laboratorio: entro quando la riparazione deve essere pronta), a partire dall'apertura:

| Priorità | Tempo proposto |
| --- | --- |
| Critica | 4 ore |
| Alta | 1 giorno lavorativo |
| Normale | 3 giorni lavorativi |
| Bassa | 10 giorni lavorativi |

Le **ore** contano di calendario, anche di notte e nei festivi; i **giorni lavorativi** saltano sabati, domeniche e festivi (le festività nazionali, Pasquetta e il santo patrono indicato nelle impostazioni) e arrivano alla stessa ora. La scadenza calcolata compare nel modulo e si può **scrivere a mano**; cambiando la priorità di una richiesta già aperta si ricalcola dall'apertura. Una richiesta è **in scadenza** nell'ultimo quarto del suo tempo (o nell'ultima ora) e **in ritardo** quando la scadenza passa senza intervento; registrato il primo intervento, resta scritto se è arrivato **in tempo** o **in ritardo**. Il tecnico assegnato (o, senza tecnico, chi ha aperto la richiesta) riceve una [notifica](notifiche.md) quando la richiesta entra in scadenza e una quando passa, una volta sola. I tempi delle priorità si cambiano con **Impostazioni** nella pagina Assistenza, per chi gestisce l'assistenza: valgono per le richieste nuove.

## <a id="assistenza-scheda"></a>La scheda della richiesta

In alto lo **stato** (*Da fare*, *Pianificata*, *In lavorazione*, *In attesa*, *Pronta da ritirare*, *Chiusa*, *Ritirata*, *Annullata*), la priorità, la scadenza e i pulsanti della prossima cosa da fare; sotto, i dati (cliente, dove, impianto, ticket del cliente, chi ha chiamato e chi cercare sul posto, con i telefoni da chiamare con un clic), il problema, gli interventi con il tempo impiegato, la soluzione, i **file** e lo **storico**. I file (foto del guasto, rapporto firmato, preventivi) vanno in Documenti, nella cartella **… → impianto → Assistenza → AT 2026-012** (senza impianto, in quella del cliente), e si aprono dalla richiesta anche senza i permessi dei documenti; togliere un file dalla richiesta lo lascia in Documenti. **Stampa** apre l'anteprima del **rapporto di assistenza** da far firmare, con il [modello di stampa](modelli-stampa.md) dell'assistenza: il cliente, l'impianto, il riferimento del cliente, il problema, la tabella degli interventi, la soluzione e, in fondo all'ultimo foglio, le firme del tecnico e del cliente; il **consuntivo con i prezzi** ha il riporto tra i fogli. Il cartellino e la ricevuta del laboratorio restano nelle loro misure. Da ⋯ si aprono la scheda del cliente, la pagina dell'impianto e l'attività pianificata; chi gestisce l'assistenza **annulla** una richiesta (con il motivo) o la **elimina**, se è sbagliata o doppia.

## <a id="assistenza-interventi"></a>Interventi, attese e chiusura

- **Registra un intervento**: il giorno (non nel futuro) e l'**ora d'inizio** (con il giorno dicono se il primo intervento è arrivato in tempo), **come** (sul posto, da remoto, al telefono, in laboratorio), **chi ha lavorato** con le sue ore (le persone del Personale; senza persone nel Personale, i tecnici scritti e le ore), **diritto di chiamata** e **reperibilità**, il **materiale e le spese** e il **lavoro svolto**: persone, materiale e spese finiscono nel [consuntivo](#assistenza-consuntivo). L'esito **Da proseguire** lascia aperta la richiesta; **Risolto** la chiude con la soluzione (vuota: il lavoro svolto). **Salva e stampa il rapporto** lo stampa subito. Chi ha scritto un intervento lo corregge; chi gestisce l'assistenza corregge ed elimina quelli di tutti.
- **Pianifica**: il giorno, chi lo fa e una nota creano un'[attività](attivita.md) collegata al cliente e all'impianto, con l'etichetta *Assistenza* e nel testo il problema, il posto, chi cercare e il ticket del cliente. Nella scheda dell'attività un riquadro ricorda la richiesta, con **Registra l'intervento**: registrandolo l'attività si completa.
- **In attesa** con il motivo (pezzi ordinati, risposta del cliente, preventivo da approvare…); riprende con **Riprendi** o registrando un intervento.
- **Chiudi** chiede come è stato risolto; **Riapri** rimette aperta una richiesta chiusa.

## <a id="assistenza-consuntivo"></a>Il consuntivo e la fatturazione

Ogni richiesta ha il suo **consuntivo**, nella scheda sotto gli interventi: tutto ciò che va in fattura, un intervento per volta.

- **Manodopera**: nasce da **Chi ha lavorato** nel modulo dell'intervento, una riga per persona con le sue ore (un'ora in due = due righe da un'ora). In un intervento nuovo c'è già il tecnico a cui è assegnata la richiesta (altrimenti chi lo scrive); **Aggiungi una persona** parte da *Scegli una persona…*. Il prezzo è quello della [manodopera del listino](listino.md#listino-manodopera) con la mansione della persona (altrimenti la sua tariffa oraria di vendita nel Personale), il costo il suo costo orario. Persone e ore si cambiano correggendo l'intervento: il prezzo già deciso resta.
- **Diritto di chiamata** e **reperibilità** (fuori orario o nei festivi): si spuntano nell'intervento. Gli importi vengono dalle voci del listino scelte nelle **Impostazioni** dell'assistenza; la reperibilità può avere anche una **maggiorazione in percentuale** sulla manodopera di quell'intervento, ricalcolata da sola. In un intervento nuovo **In reperibilità** si spunta da sola di domenica, nei festivi e fuori dall'orario di lavoro (quello della pagina [Reperibilità](reperibilita.md)), con il perché sotto; cambiando giorno e ora si ricontrolla, finché non la si tocca a mano (dalla 1.125.0).
- **Materiale**: dal listino (anche leggendo il codice a barre, quello della confezione con la sua quantità) o scritto; **spese**: trasferta, parcheggio, materiale di consumo. Si aggiungono dall'intervento oppure dalla scheda (**Materiale**, **Spesa**) per le voci della richiesta. Il materiale del listino si scarica dal magazzino (o dal proprio furgone) con **Scarica dal magazzino**: vedi [Il materiale dell'assistenza](magazzino.md#magazzino-assistenza).
- **Noleggi** (dalla 1.98.0): un mezzo o un'attrezzatura presa a noleggio per l'intervento, per esempio un **cestello**, una **gru**, una piattaforma aerea. Nel modulo dell'intervento, in **Materiale, spese e noleggi**, il pulsante **Noleggio** aggiunge una riga: che cosa (con i suggerimenti), per quanto (di serie in *giorni*; anche ore, settimane…), **da chi** (il noleggiatore, con i suggerimenti dei fornitori in anagrafica) e il **costo** per unità che chiede il noleggiatore. Il noleggio va nel consuntivo dell'intervento con quel costo, e il **prezzo al cliente** è il costo più il **Ricarico sui noleggi** delle impostazioni dell'assistenza (vuoto o 0: al costo). Se poi cambia il costo, il prezzo lo segue, finché qualcuno non lo cambia a mano. Si aggiunge anche dalla scheda (**Noleggio**, per le voci della richiesta). Il costo dei noleggi lo vede anche chi registra gli interventi (lo scrive lui); il noleggiatore non va nelle stampe per il cliente.

Con la si corregge una riga: quantità e descrizione di materiale, spese e noleggi (dei noleggi anche noleggiatore e costo), e (per chi vede i prezzi) prezzo, sconto anche in cascata, IVA e **non addebitata** (resta nel consuntivo a zero: in garanzia, compresa, omaggio). Una riga senza prezzo è **da prezzare** e non conta nel totale finché non lo ha. Sotto, i conti: imponibile, IVA per aliquota e totale; a chi vede i costi anche **costo e margine**.

**Fatturazione…** (chi gestisce l'assistenza) segna la richiesta **Da fatturare**, **Fatturata** con numero e data della fattura, oppure **Non da fatturare** con il motivo (in garanzia, nel contratto di manutenzione, omaggio), con le note per l'amministrazione. Senza una scelta, una richiesta chiusa con importi risulta da fatturare da sola e compare nella linguetta **Da fatturare**. Una richiesta fatturata non cambia più il consuntivo (va tolto prima «Fatturata»).

Il **rapporto** stampa manodopera, materiale e spese senza prezzi, da far firmare; **Stampa → Consuntivo con i prezzi** stampa le righe con importi, imponibile, IVA e totale. Chi registra gli interventi (i tecnici) segna persone, ore, materiale e spese ma non vede prezzi e totali: li vede chi gestisce l'assistenza o il listino; i costi chi vede anche quelli del listino e del personale. Lo stesso vale per il laboratorio.

## <a id="assistenza-laboratorio"></a>Il laboratorio

1. **Ricevi un pezzo**: il cliente, **che cosa ha consegnato** (per esempio *Motore del cancello*), la **matricola**, gli **accessori** arrivati con il pezzo e il **difetto** segnalato; la priorità dice entro quando deve essere pronto. **Apri e stampa la ricevuta** stampa su un foglio A4 due copie, per il cliente e per il laboratorio, con le condizioni (il testo si cambia nelle impostazioni dell'assistenza) e le firme.
2. Dalla scheda, **Stampa → Cartellino**: un'etichetta di 85,6 × 54 mm da attaccare al pezzo, con il numero, il cliente, il pezzo, il difetto e un QR code che apre la richiesta nella piattaforma.
3. Le **lavorazioni** si registrano come gli interventi. **Pronta da ritirare** (oppure una lavorazione con esito *Riparato*) chiede che cosa è stato fatto.
4. **Avvisa il cliente**: chiamalo (i suoi numeri sono a un clic) oppure mandagli l'email «riparazione pronta», se la posta è configurata e il cliente ha un indirizzo. Resta scritto quando e da chi è stato avvisato.
5. **Consegnata al cliente**, con il nome di chi l'ha ritirata, chiude la richiesta: *Ritirata*. Il rapporto di riparazione si può stampare per la firma al ritiro.

## <a id="assistenza-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere l'assistenza | La pagina Assistenza e le linguette dell'impianto e del cliente: richieste, interventi, file e stampe. |
| Aprire le richieste e registrare gli interventi | Aprire le richieste al telefono o al banco del laboratorio (anche creando al volo la scheda del cliente nuovo), pianificare e registrare gli interventi, cambiare lo stato, aggiungere file; correggere le proprie richieste e i propri interventi. |
| Gestire l'assistenza | Correggere ed eliminare richieste e interventi di tutti, annullare le richieste, impostare i tempi delle priorità, il testo della ricevuta, diritto di chiamata e reperibilità; vedere prezzi e totali del consuntivo e segnare la fatturazione. |

Prezzi e totali del consuntivo li vede anche chi gestisce il listino; costi e margine chi, oltre ai prezzi, vede i costi del listino e del personale.

Le richieste si assegnano solo a chi vede l'assistenza. Per aprire la pagina dell'impianto o la scheda del cliente servono i loro permessi; le cartelle delle richieste le crea la piattaforma.

---

[← Pratiche](pratiche.md) · [Indice](README.md) · [Listino →](listino.md)
