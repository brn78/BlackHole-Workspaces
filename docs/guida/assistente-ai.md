[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="assistente-ai"></a>Assistente AI

L'**assistente AI** è una chat con un modello linguistico che gira sul server dell'azienda: risponde alle domande, riordina gli appunti in attività, prepara bozze di rapportini di intervento e riassume testi lunghi. Si apre con il pulsante ✨ nella barra superiore, accanto alla radio, in un pannello a destra. Il pulsante c'è quando un amministratore ha preparato l'assistente (vedi [Impostazioni → Assistente AI](impostazioni.md#impostazioni-ai)) e il tuo account ha il permesso **Usare l'assistente AI** (gli amministratori lo hanno sempre); se compare o sparisce mentre lavori, un amministratore l'ha appena attivato o spento. Alle stesse condizioni l'assistente lavora anche dentro i moduli, con [Migliora testo](#assistente-moduli): corregge, chiarisce, accorcia o traduce le descrizioni, i commenti e le note mentre le scrivi; e legge le cartelle del PC in [Da una cartella del PC](impianti.md#impianti-cartella), per proporre clienti, impianti e schede tecniche. **Da un testo** compila la scheda nuova da un'email, un messaggio o un documento: clienti e fornitori, personale, mezzi e attrezzature, richieste di assistenza, preventivi e, dalla 1.123.0, [attività](attivita.md#attivita-da-testo), [progetti](trattative.md#trattative-da-testo), [pratiche](pratiche.md#pratiche-da-testo) e [scadenze dell'azienda](scadenze.md#scadenze-da-testo). Tutte queste funzioni, dalla 1.219.0, ci sono [anche senza assistente](#assistente-senza).

## <a id="assistente-attesa"></a>L'attesa: che cosa sta facendo l'assistente

Ogni volta che l'assistente prepara una proposta (una scheda **Da un testo**, un carico da un documento, la risposta di un fornitore, le colonne di un foglio, le pagine di un PDF, le password di un documento) si apre la stessa **finestra dell'attesa**:

- **che cosa succede adesso**: *In coda* (sta rispondendo a un'altra richiesta: tocca a te appena finisce), *Avvio del modello sul server* (la prima richiesta dopo una pausa), *Sta leggendo il testo*, *Sta scrivendo la proposta* con i caratteri o le righe scritte finora;
- **chi risponde**: il motore del server oppure il servizio esterno;
- **da quanto aspetti** e, dalla seconda volta, **quanto ci mette di solito** una richiesta di quel tipo: la barra avanza su quel tempo. La prima volta non si sa, e la barra scorre senza misura;
- **Ferma**: ferma la richiesta anche sul server, e si torna dov'eri senza aver perso niente.

Con il **motore del server** i tempi dipendono dal processore: su un server senza scheda grafica una scheda da un biglietto da visita richiede circa un minuto, le righe di un documento di una pagina tre o quattro. Per questo, dove c'è una tabella, la piattaforma la legge [senza assistente](#importare-pdf). Se l'assistente serve spesso su documenti lunghi, un amministratore può mandare le sole analisi a un servizio esterno, più veloce ([Impostazioni → Assistente AI](impostazioni.md#impostazioni-ai), «Chi risponde a che cosa»).

## <a id="assistente-senza"></a>Con l'assistente o senza: due modi

Dalla 1.219.0 ogni funzione che legge un testo o un documento si usa in **due modi**, e scegli tu ogni volta:

- **Senza assistente**: risponde subito. Il programma compila quello che riconosce dalla **forma** di ciò che è scritto (una partita IVA o un codice fiscale con il carattere di controllo giusto, un'email, una PEC, un telefono, un indirizzo con il CAP, una data dopo «scadenza», la riga con la forma giuridica, un elenco puntato) e, per i documenti con una **tabella**, le righe così come sono. Non interpreta: quello che non è scritto in modo riconoscibile resta vuoto e lo completi tu. Il testo non esce dal server.
- **Con l'assistente**, se è configurato: legge anche il resto (riassume, capisce una frase, separa le voci di un discorso), ma con il motore del server ci vogliono [minuti](#assistente-attesa); se è un servizio esterno, il testo esce dall'azienda.

Per questo i pulsanti **Da un testo**, **Da una richiesta**, **Da una scheda tecnica** e **Da un documento** ci sono sempre, anche senza assistente. Nella finestra di **Da un testo** i pulsanti sono due, **Senza assistente** e **Proponi con l'assistente** (senza assistente configurato ce n'è uno solo, **Compila i dati**). Nella lettura di un documento sono **Usa la tabella** e **Leggi con l'assistente**. La scheda che si apre dice sempre da dove vengono i dati: «letti dal testo, senza assistente» oppure «proposti dall'assistente». In tutti e due i casi niente si salva da solo e, dopo, il programma fa gli stessi controlli e le stesse ricerche: il cliente in anagrafica (partita IVA, email, telefono, nome), l'impianto, gli ordini aperti, le voci del listino.

Che cosa si riconosce **senza assistente**:

- **Clienti e fornitori**: ragione sociale e forma giuridica (la riga che finisce con S.r.l., S.p.A., S.n.c.…), partita IVA, codice fiscale, codice SDI, PEC, email, telefoni con «Ufficio», «Cellulare» e «Fax», indirizzi con il CAP (anche scritti come nelle visure), il sito, chi firma con il suo ruolo e le cariche di una visura.
- **Personale**: nome e cognome (con il codice fiscale si capisce anche l'ordine), codice fiscale, nascita e sesso, email, telefoni, indirizzo; mansione, reparto e data di assunzione se sono scritti con l'etichetta.
- **Mezzi e attrezzature**: targa, telaio e alimentazione di un libretto; marca, modello e matricola con l'etichetta, la data di acquisto dopo «fattura … del».
- **Richieste di assistenza, attività, progetti**: l'oggetto come titolo (o la prima frase, senza i saluti), il testo senza saluti e firma, le righe di un elenco come voci da spuntare, l'urgenza dalle parole («urgente», «pericolo», «con calma»), la data dopo «entro» (anche «entro venerdì»), l'impianto di cui si parla, chi scrive e chi cercare sul posto, il numero del ticket, l'importo scritto in euro.
- **Pratiche**: il tipo dalle parole del nome e dall'ente, il codice dell'ente, il titolare, le date con l'etichetta.
- **Scadenze**: la data dopo «scadenza» o «valido fino al», ogni quanto si rinnova, i giorni della disdetta, la categoria dalle parole (polizza, certificato, contratto…).
- **Preventivo da una richiesta**: le voci scritte una per riga con la quantità davanti («8 telecamere…», «circa 350 metri di cavo», «un monitor») o in una tabella, il cliente, l'oggetto, il riferimento, l'indirizzo dei lavori. Una riga con più cose resta una voce sola, e dalle frasi di un discorso le voci le ricava solo l'assistente.
- **Voce del listino da una scheda tecnica**: la prima riga come descrizione; marca, codice del produttore ed EAN con l'etichetta.
- **Carico di magazzino, arrivo merce, risposta a una richiesta d'offerta**: le righe della tabella del documento, con le colonne riconosciute dai nomi e da correggere; tipo, numero e data del documento e la partita IVA del fornitore dal testo.
- **Corsi, documenti e visite del personale**: tipo, numero, date, ore, giudizio di idoneità.

## <a id="assistente-chat"></a>Fare una domanda

- Scrivi nella casella in basso e premi <kbd>Invio</kbd> o **Invia**; <kbd>Maiusc</kbd>+<kbd>Invio</kbd> va a capo. Puoi incollare anche un testo lungo: con le impostazioni normali fino a circa 8.000 caratteri.
- La risposta compare **man mano che il modello la scrive**, con titoli, elenchi e grassetto. **Ferma** la interrompe: quello che è già arrivato resta.
- La prima domanda dopo una pausa chiede qualche secondo in più, perché il server carica il modello in memoria (*Avvio del modello sul server*). Le domande passano una alla volta: se un collega ne sta già facendo una, la tua aspetta il suo turno (*In coda*), e ognuno ne può avere una sola in corso.
- L'assistente tiene conto della **conversazione**: puoi chiedere di correggere, accorciare o continuare («più breve», «in forma di elenco», «continua»). Quando la conversazione diventa troppo lunga le domande più vecchie non sono più considerate e un avviso lo dice; per un argomento nuovo usa **Nuova conversazione** +.
- **Copia** ⧉, sotto ogni risposta, la mette negli appunti, pronta da incollare in un'[attività](attivita.md), in un [appunto](appunti.md) o in un'email; accanto ci sono il modello che ha risposto e il tempo impiegato.

## <a id="assistente-modalita"></a>Le modalità

**Modalità**, in basso, sceglie che cosa chiedere all'assistente; a conversazione vuota le stesse modalità sono proposte come scorciatoie. Vale dalla domanda successiva e la conversazione resta.

- **Domanda libera**: domande, testi da scrivere o correggere, idee.
- **Riordina in un'attività**: da appunti sparsi a un titolo, una descrizione e le **voci da spuntare**, da copiare in una nuova attività.
- **Rapportino di intervento**: dagli appunti del cantiere (lavori fatti, materiali, esito) a un rapportino con le sezioni Intervento, Lavori eseguiti, Materiali utilizzati, Esito e verifiche, Da fare. I dati che mancano restano «da completare».
- **Riassunto**: il punto principale, i punti chiave e, se ci sono, scadenze, importi, persone e decisioni.
- **Supporto tecnico**: indicazioni pratiche, per passi, su impianti elettrici, reti, videosorveglianza, antintrusione, controllo accessi, rivelazione incendi e automazione.
- **Come si fa (guida)**: domande sull'uso della piattaforma scritte come si parla («come registro una violazione dei dati?», «dove scrivo il budget di una commessa?»). Il server cerca nella guida le sezioni più vicine e le passa all'assistente, che risponde solo con quelle, con i nomi di menu e pulsanti come li scrive la guida e, in fondo, **Nella guida:** con i collegamenti alle sezioni (un clic le apre). Se la guida non risponde, lo dice. Dalla pagina della guida la apre **Chiedi all'assistente**, in alto.

## <a id="assistente-moduli"></a>Migliora testo nei moduli

Nei campi dove si scrive di più c'è il pulsante ✨ **Migliora testo**: in fondo alla barra dell'editor della descrizione di [attività](attivita.md) e [commesse](progetti.md), del testo degli [appunti](appunti.md), del leggimi degli [impianti](impianti.md) e (dalla 1.202.1) del messaggio che scrivi nella [Posta](posta.md), dove lavora solo sul tuo testo, non sulla firma né sul messaggio a cui rispondi; nell'angolo in alto a destra dei commenti delle attività, delle note dei [clienti](clienti.md), della descrizione dei [documenti](documenti.md) e dei testi dell'[assistenza](assistenza.md) (problema, lavoro svolto, soluzione). Compare alle stesse condizioni del pulsante della chat, e solo nei campi che puoi modificare.

1. Premi ✨ e scegli che cosa fare: **Correggi** (ortografia, grammatica e punteggiatura: il resto non cambia), **Rendi più chiaro**, **Accorcia**, **Tono professionale** (adatto a un cliente o a un collega), **Elenco puntato**, **Traduci in inglese** o **Traduci in italiano**.
2. Se prima hai **selezionato una parte** del testo, l'assistente lavora solo su quella (in cima al menu c'è scritto *Sulla parte selezionata*), altrimenti su tutto il testo. Si lavora su al massimo 4.000 caratteri per volta, circa una pagina: un testo più lungo si migliora una parte alla volta.
3. La **proposta** compare in una finestra man mano che l'assistente la scrive. Alla fine **Differenze** mostra le parole tolte barrate in rosso e quelle nuove in verde (per Correggi la finestra si apre già così); **Proposta** mostra il testo intero.
4. **Sostituisci** mette la proposta al posto del testo (o della parte selezionata); **Aggiungi sotto** la aggiunge sotto, comodo per avere il testo in due lingue; **Riprova** ne chiede un'altra; **Annulla** lascia tutto com'era. Dopo Sostituisci, <kbd>Ctrl</kbd>+<kbd>Z</kbd> riporta il testo di prima, e niente si salva finché non salvi la scheda.

- Un avviso giallo, **Controlla questi dati**, elenca numeri, date, orari, importi, codici, email e collegamenti che nella proposta sono stati tolti o cambiati: dovrebbero restare uguali, quindi controllali prima di applicare. Un altro avviso segnala una proposta molto più lunga del testo o con poco del testo di partenza: succede quando il modello, invece di elaborare il testo, risponde a una domanda o esegue una richiesta che ci trova scritta.
- Negli editor con la formattazione restano grassetto, corsivo, titoli, elenchi (anche le caselle da spuntare) e collegamenti; colori, evidenziato, sottolineato, barrato e allineamenti della parte riscritta si perdono, e la finestra lo ricorda.
- Migliora testo ha una **corsia sua**: non aspetta le risposte lunghe della chat. Su un server senza scheda video un paragrafo chiede da qualche secondo a mezzo minuto, secondo il server e la lunghezza; se un collega sta già usando Migliora testo, la tua richiesta aspetta il suo turno (*In coda*).

## <a id="importare-pdf"></a>Importare da un PDF, una scansione o una foto

Tutte le importazioni guidate da un foglio (clienti, personale, mezzi e attrezzature, produttori, dispositivi del monitoraggio, listino, listini fornitori, preventivi) e **Da un'offerta del fornitore** nei preventivi accettano anche un **PDF**, una **scansione** o una **foto** del documento: l'offerta di un fornitore, il listino di chi non manda l'Excel. Un PDF con il testo si legge nel browser, subito. Una scansione (un PDF fatto di immagini) o una foto la legge il server con il [riconoscimento del testo](documenti.md#documenti-ocr), che dà le parole con la loro posizione: righe e colonne si ricavano come da un PDF con il testo. La finestra dell'attesa dice a che pagina è e quanto manca; da una scansione conviene ricontrollare numeri e codici, perché qualche lettera può essere scambiata. Poi si scelgono le pagine (**Dalla pagina**, **Alla pagina**: salta copertina, indice e condizioni di vendita) e come leggerle:

- **Usa la tabella**: se nel documento c'è la tabella delle voci (la riga con i nomi delle colonne: «Codice», «Descrizione», «U.M.», «Q.tà», «Prezzo», «Sconto», «Importo»…) la finestra lo dice subito, con quante righe e quali colonne, ed è la scelta già pronta: **senza assistente**, immediata ed esatta. Le voci arrivano fino ai totali, una descrizione su più righe resta una voce sola, la tabella continua sulle pagine dopo anche se l'intestazione non è ripetuta, i totali parziali e i titoli delle posizioni di un'offerta si saltano.
- **✨ Leggi con l'assistente** (con l'assistente AI attivo per le analisi): ogni pagina va all'assistente insieme ai dati di quell'importazione, che ne ricava una riga per articolo (o per persona, mezzo…) anche da un catalogo con foto e testi sparsi. Serve quando la tabella non c'è o non è quella giusta. Con il motore del server ci vuole qualche minuto per pagina: la [finestra dell'attesa](#assistente-attesa) dice la pagina, le righe trovate e il tempo, e **Ferma** tiene quello che è stato letto fin lì. I valori si copiano come sono scritti: una riga con valori che nella pagina non ci sono si scarta. Gli avvisi dell'assistente (per esempio «prezzi IVA esclusa») e le pagine non lette compaiono sopra la scelta delle colonne.
- **Leggi senza assistente** (quando la tabella delle voci non c'è): le righe del testo con più pezzi diventano righe di una tabella, in colonne allineate per posizione. Va bene per un PDF fatto come una tabella; per un catalogo il risultato è grezzo.

Dopo, i passi sono quelli di un foglio Excel: le colonne (già scelte, se hanno i nomi dei dati), l'anteprima, l'importazione. All'assistente va solo il testo delle pagine che gli fai leggere (sul server o al servizio esterno configurato nelle impostazioni). Senza il riconoscimento del testo installato sul server (Impostazioni → Server) una scansione non si legge: serve il file in Excel, in CSV o un PDF con il testo. Fino a 150 MB.

> [!TIP]
> I fogli Excel che dichiarano migliaia di colonne o di righe vuote (formattazioni trascinate fino in fondo) si leggono solo dove ci sono i dati: nella scelta delle colonne compaiono solo quelle vere.

## <a id="assistente-riservatezza"></a>Riservatezza e limiti

- Con l'assistente **sul server** (la scelta consigliata) domande e testi non escono dal server dell'azienda: sotto il titolo della chat c'è scritto *sul server: i testi restano in azienda*. Se un amministratore ha scelto un server esterno, sotto il titolo compare il suo nome.
- Le conversazioni **non si salvano sul server** e non finiscono nel registro attività: restano solo in questa scheda del browser finché non la chiudi o non scegli **Nuova conversazione**. Lo stesso vale per i testi mandati a Migliora testo.
- L'assistente **non vede i dati della piattaforma** (clienti, attività, documenti): lavora solo sul testo che scrivi o incolli, o su quello del campo in cui usi Migliora testo. Le password e le note della [gestione password](password.md) non passano mai dall'assistente.
- Conosce però i [dati dell'azienda](impostazioni.md#impostazioni-azienda), per rispondere a tono e firmare le email: ragione sociale, di che cosa si occupa, sede principale, partita IVA, primo telefono, prima email, PEC e sito (non le coordinate bancarie né i referenti). E sa **con chi sta parlando**: il tuo nome, il ruolo aziendale, il reparto e l'email di lavoro del tuo profilo, così ti chiama per nome e firma a tuo nome le email che gli chiedi.

> [!WARNING]
> Le risposte possono contenere **errori**, anche scritti con sicurezza: controlla dati, misure, prezzi e norme prima di usarle, soprattutto nel supporto tecnico.

---

[← Notifiche](notifiche.md) · [Indice](README.md) · [Sistema →](sistema.md)
