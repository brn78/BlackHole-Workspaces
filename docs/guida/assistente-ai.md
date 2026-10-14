[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="assistente-ai"></a>Assistente AI

L'**assistente AI** è una chat con un modello linguistico che gira sul server dell'azienda: risponde alle domande, riordina gli appunti in attività, prepara bozze di rapportini di intervento e riassume testi lunghi. Si apre con il pulsante ✨ nella barra superiore, accanto alla radio, in un pannello a destra. Il pulsante c'è quando un amministratore ha preparato l'assistente (vedi [Impostazioni → Assistente AI](impostazioni.md#impostazioni-ai)) e il tuo account ha il permesso **Usare l'assistente AI** (gli amministratori lo hanno sempre); se compare o sparisce mentre lavori, un amministratore l'ha appena attivato o spento. Alle stesse condizioni l'assistente lavora anche dentro i moduli, con [Migliora testo](#assistente-moduli): corregge, chiarisce, accorcia o traduce le descrizioni, i commenti e le note mentre le scrivi; e legge le cartelle del PC in [Da una cartella del PC](impianti.md#impianti-cartella), per proporre clienti, impianti e schede tecniche. **Da un testo** compila la scheda nuova da un'email, un messaggio o un documento: clienti e fornitori, personale, mezzi e attrezzature, richieste di assistenza, preventivi e, dalla 1.123.0, [attività](attivita.md#attivita-da-testo), [trattative](trattative.md#trattative-da-testo), [pratiche](pratiche.md#pratiche-da-testo) e [scadenze dell'azienda](scadenze.md#scadenze-da-testo).

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

Nei campi dove si scrive di più c'è il pulsante ✨ **Migliora testo**: in fondo alla barra dell'editor della descrizione di [attività](attivita.md) e [progetti](progetti.md) e del testo degli [appunti](appunti.md); nell'angolo in alto a destra dei commenti delle attività, delle note dei [clienti](clienti.md), della descrizione dei [documenti](documenti.md) e dei testi dell'[assistenza](assistenza.md) (problema, lavoro svolto, soluzione). Compare alle stesse condizioni del pulsante della chat, e solo nei campi che puoi modificare.

1. Premi ✨ e scegli che cosa fare: **Correggi** (ortografia, grammatica e punteggiatura: il resto non cambia), **Rendi più chiaro**, **Accorcia**, **Tono professionale** (adatto a un cliente o a un collega), **Elenco puntato**, **Traduci in inglese** o **Traduci in italiano**.
2. Se prima hai **selezionato una parte** del testo, l'assistente lavora solo su quella (in cima al menu c'è scritto *Sulla parte selezionata*), altrimenti su tutto il testo. Si lavora su al massimo 4.000 caratteri per volta, circa una pagina: un testo più lungo si migliora una parte alla volta.
3. La **proposta** compare in una finestra man mano che l'assistente la scrive. Alla fine **Differenze** mostra le parole tolte barrate in rosso e quelle nuove in verde (per Correggi la finestra si apre già così); **Proposta** mostra il testo intero.
4. **Sostituisci** mette la proposta al posto del testo (o della parte selezionata); **Aggiungi sotto** la aggiunge sotto, comodo per avere il testo in due lingue; **Riprova** ne chiede un'altra; **Annulla** lascia tutto com'era. Dopo Sostituisci, <kbd>Ctrl</kbd>+<kbd>Z</kbd> riporta il testo di prima, e niente si salva finché non salvi la scheda.

- Un avviso giallo, **Controlla questi dati**, elenca numeri, date, orari, importi, codici, email e collegamenti che nella proposta sono stati tolti o cambiati: dovrebbero restare uguali, quindi controllali prima di applicare. Un altro avviso segnala una proposta molto più lunga del testo o con poco del testo di partenza: succede quando il modello, invece di elaborare il testo, risponde a una domanda o esegue una richiesta che ci trova scritta.
- Negli editor con la formattazione restano grassetto, corsivo, titoli, elenchi (anche le caselle da spuntare) e collegamenti; colori, evidenziato, sottolineato, barrato e allineamenti della parte riscritta si perdono, e la finestra lo ricorda.
- Migliora testo ha una **corsia sua**: non aspetta le risposte lunghe della chat. Su un server senza scheda video un paragrafo chiede da qualche secondo a mezzo minuto, secondo il server e la lunghezza; se un collega sta già usando Migliora testo, la tua richiesta aspetta il suo turno (*In coda*).

## <a id="importare-pdf"></a>Importare da un PDF

Tutte le importazioni guidate da un foglio (clienti, personale, mezzi e attrezzature, produttori, dispositivi del monitoraggio, listino, listini fornitori) accettano anche un **PDF**, per esempio il listino di un fornitore che non manda l'Excel. Il PDF si legge nel browser; poi si scelgono le pagine (**Dalla pagina**, **Alla pagina**: salta copertina, indice e condizioni di vendita) e come leggerle:

- **✨ Leggi con l'assistente** (con l'assistente AI attivo per le analisi): ogni pagina va all'assistente insieme ai dati di quell'importazione, che ne ricava una riga per articolo (o per persona, mezzo…) anche da un catalogo con foto e testi sparsi. Si vede l'avanzamento, con **Ferma**. I valori si copiano come sono scritti: una riga con valori che nella pagina non ci sono si scarta. Gli avvisi dell'assistente (per esempio «prezzi IVA esclusa») e le pagine non lette compaiono sopra la scelta delle colonne.
- **Leggi senza assistente**: le righe del testo con più pezzi diventano righe di una tabella, in colonne allineate per posizione. Va bene per un PDF fatto come una tabella; per un catalogo il risultato è grezzo.

Dopo, i passi sono quelli di un foglio Excel: le colonne (già scelte, perché hanno i nomi dei dati), l'anteprima, l'importazione. Il testo delle pagine scelte va all'assistente configurato nelle impostazioni (sul server o il servizio esterno). Un PDF fatto di immagini (una scansione) non ha testo da leggere: serve il file in Excel, in CSV o un PDF con il testo. Fino a 150 MB.

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
