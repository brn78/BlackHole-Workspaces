[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="appunti"></a>Appunti

**La mia giornata → Appunti** è il blocco per appunti della piattaforma: note di testo, **elenchi di cose da fare** e **lavagne** su cui disegnare, ciascuno in un riquadro che puoi colorare, etichettare e fissare in alto. Un appunto è **personale** finché non lo condividi con colleghi o gruppi di utenti. Il servizio è disponibile a tutti gli utenti, senza permessi da assegnare.

La pagina ha tre viste, ciascuna con il numero dei suoi appunti: **Appunti** (quelli in uso), **Archivio** (quelli messi da parte) e **Cestino**. In alto ci sono i pulsanti **Stampa**, **Nuova lavagna**, **Nuovo elenco** e **Nuovo appunto**; sotto le linguette i filtri rapidi e la barra con la ricerca, come in tutte le pagine. Gli appunti sono in ordine di ultima modifica, i più recenti per primi; finché resti sulla pagina i riquadri non cambiano posto mentre li usi.

## <a id="appunti-scrivere"></a>Scrivere un appunto

**Nuovo appunto** apre la finestra dell'appunto, un pannello a destra che si allarga trascinandone la linguetta: scrivi il **titolo** (facoltativo; <kbd>Invio</kbd> porta al testo) e il **testo**, poi premi **Crea**. Serve almeno un titolo, un testo oppure una voce: un appunto del tutto vuoto non si salva.

- Per **riaprire** un appunto fai clic sul suo riquadro (o premi <kbd>Invio</kbd> o la barra spaziatrice quando è selezionato con la tastiera), modifica e premi **Salva**. In basso a sinistra la finestra dice chi lo ha modificato per ultimo e quando.
- Il riquadro mostra il titolo, le prime righe del testo, le etichette e da quanto tempo l'appunto non viene modificato: fermando il mouse sulla data compaiono giorno, ora e autore dell'ultima modifica.
- Chiudendo la finestra con modifiche non salvate viene chiesta conferma: vedi [Modifiche non salvate](interfaccia.md#interfaccia-non-salvate).

## <a id="appunti-formattare"></a>Testo formattato e caselle da spuntare

Sopra il testo c'è la barra dell'editor, la stessa dei [documenti Word](documenti.md#documenti-editor) in versione ridotta:

- **Stile del paragrafo**: **Normale** oppure **Titolo 1**, **2** e **3**;
- **grassetto** (<kbd>Ctrl</kbd>+<kbd>B</kbd>), *corsivo* (<kbd>Ctrl</kbd>+<kbd>I</kbd>), sottolineato (<kbd>Ctrl</kbd>+<kbd>U</kbd>) e barrato;
- **colore del testo** ed **evidenziato**, con le tinte della piattaforma (fermando il mouse su un quadratino compare il nome del colore; il primo, barrato, toglie il colore). I colori del testo si leggono sia con il tema chiaro sia con quello scuro; sul tema scuro il testo evidenziato diventa scuro, come un evidenziatore su carta;
- **casella da spuntare** : trasforma la riga in una casella; un clic sulla casella la spunta e la riga diventa barrata. Così in un appunto di testo puoi mettere qualche cosa da fare in mezzo alle note, senza farne un [elenco](#appunti-elenchi);
- **elenco puntato** ed **elenco numerato**;
- **collegamento** (<kbd>Ctrl</kbd>+<kbd>K</kbd>): seleziona il testo e scrivi l'indirizzo, che deve iniziare con `https://`, `http://`, `mailto:` o `tel:`. Nel riquadro il collegamento si apre in una nuova scheda del browser;
- **Togli la formattazione** riporta il testo selezionato a testo semplice;
- in fondo a destra, se puoi usare l'assistente AI, **Migliora testo** ✨: corregge, chiarisce, accorcia o traduce il testo (o la parte selezionata), con la proposta da accettare. La stessa barra c'è nella descrizione di attività e progetti; vedi [Migliora testo nei moduli](assistente-ai.md#assistente-moduli).

Il riquadro mostra il testo con la sua formattazione (titoli, grassetto, colori, caselle). Il testo incollato da altri programmi conserva solo questi formati: immagini e tabelle non entrano negli appunti (per quelle c'è un [documento Word](documenti.md#documenti-editor)). Gli indirizzi web scritti senza usare il pulsante **Collegamento** restano testo.

> [!NOTE]
> Un appunto condiviso è scritto da altri: prima di salvarlo il server tiene solo i formati elencati qui sopra, con colori e collegamenti controllati, e scarta tutto il resto. Nessun contenuto di un appunto può eseguire codice nella pagina di chi lo apre.

## <a id="appunti-elenchi"></a>Elenchi di cose da fare

**Nuovo elenco** crea un appunto fatto di **voci**, ciascuna con la sua casella da spuntare: la spesa, le cose da preparare per una riunione, i passaggi di una pratica.

- **Scrivere le voci**: <kbd>Invio</kbd> aggiunge la voce successiva; <kbd>Backspace</kbd> su una voce vuota la toglie; **Aggiungi voce** ne mette una in fondo; la **×** a fine riga la rimuove.
- **Riordinare**: trascina la maniglia all'inizio della riga, con il mouse o con il dito, oppure usa le frecce a fine riga.
- **Spuntare**: nella finestra le spunte si salvano con **Salva**, insieme al resto. Dal **riquadro**, senza aprire l'appunto, la spunta vale subito. Le voci completate sono barrate.
- Il riquadro mostra le prime **8 voci**, nello stesso ordine della finestra: una voce spuntata resta al suo posto. Delle altre dice quante sono (*+ 3 voci · + 5 completate*).
- **Testo** ed **Elenco**, i due pulsanti accanto al titolo, trasformano l'appunto da un tipo all'altro: ogni riga del testo diventa una voce e ogni voce una riga; le righe vuote si scartano. Passando a **Elenco** la formattazione del testo si perde (un messaggio lo ricorda), mentre le **caselle spuntate** del testo diventano voci completate. Se passi a **Testo** e poi torni a **Elenco**, le righe rimaste uguali riprendono la loro spunta, quelle nuove o cambiate sono voci da fare. Se il risultato supera i [limiti](#appunti-limiti) la trasformazione non avviene e un messaggio ne dice il motivo.

> [!TIP]
> **Elenco o caselle nel testo?** L'**elenco** è fatto per le cose da fare: le voci si spuntano anche dal riquadro, senza aprire l'appunto, si riordinano trascinandole e il riquadro conta quelle completate. Le **caselle nel testo** servono quando le cose da fare stanno in mezzo a note formattate: si spuntano nella finestra dell'appunto.

## <a id="appunti-lavagna"></a>Lavagna: disegnare a mano libera, linee e forme

**Nuova lavagna** apre un foglio a puntini su cui si disegna con il mouse, con la penna di un tablet o con il dito: uno schema dell'impianto, il percorso dei cavi, una piantina al volo. Accanto al titolo ci sono tre pulsanti, **Testo**, **Elenco** e **Lavagna**: anche un appunto già scritto può diventare una lavagna e viceversa.

- **Strumenti**: **penna** a mano libera, **linea**, **freccia**, **rettangolo** e **ellisse**. Con <kbd>Maiusc</kbd> premuto linee e frecce restano diritte o a 45°, il rettangolo diventa un quadrato e l'ellisse un cerchio.
- **Colori**: il primo è l'inchiostro, che segue il tema (scuro sul tema chiaro, chiaro su quello scuro), poi rosso, arancione, giallo, verde, blu e viola; apre tutti i colori della piattaforma. Tre **spessori**: sottile, medio e spesso. Strumento, colore e spessore restano per la volta successiva.
- **Gomma**: toglie i tratti che tocca, interi. **Annulla** (<kbd>Ctrl</kbd>+<kbd>Z</kbd>) e **Ripeti** (<kbd>Ctrl</kbd>+<kbd>Y</kbd>) valgono finché la finestra è aperta; 🗑 cancella tutto il disegno, dopo una conferma (anche questo si annulla).
- Il foglio ha sempre le stesse proporzioni e si adatta alla finestra: allargando il pannello, o aprendolo a tutto schermo con la sua linguetta, il disegno si ingrandisce senza perdere definizione.
- Il **riquadro** mostra la parte disegnata; la lavagna compare anche nella Home e si **stampa** a tutta pagina. La ricerca trova le lavagne dal titolo e dalle etichette.
- Passando da **Testo** o **Elenco** alla **Lavagna** (e viceversa) il contenuto non si trasforma: resta da parte finché la finestra è aperta, e tornando indietro lo ritrovi; salvando, si tiene solo quello del tipo scelto. Un messaggio lo ricorda.

## <a id="appunti-organizzare"></a>Colori, etichette, fissare e archiviare

Le azioni di un appunto compaiono in fondo al riquadro quando ci passi sopra con il mouse o lo raggiungi con la tastiera; sugli schermi a tocco sono sempre visibili. Le stesse azioni sono nel menu del pulsante **⋯** e del **tasto destro**.

- **Colore** : le diciotto tinte della piattaforma (più **Predefinito**), che colorano il riquadro in modo tenue per riconoscere gli appunti a colpo d'occhio. Si sceglie dal riquadro (un menu con il pallino di ogni colore) oppure dalla tendina **Colore** nel pannello dell'appunto.
- **Etichette** : parole libere (casa, lavoro, idee…) da scrivere nella finestra dell'appunto. <kbd>Invio</kbd> o la virgola aggiungono l'etichetta; mentre scrivi compaiono quelle che hai già usato.
- **Fissa in alto** 📌: l'appunto passa nel gruppo **Fissati**, in cima alla vista Appunti, sopra gli **Altri**. **Togli dai fissati** lo rimette con gli altri. Nella finestra dell'appunto lo stesso pulsante è in alto, accanto alla **×**, e vale al salvataggio.
- **Archivia** : sposta l'appunto nella vista **Archivio**, per toglierlo di mezzo senza eliminarlo. Da lì **Togli dall'archivio** lo riporta tra gli appunti. Un appunto archiviato non resta fissato.
- **Stampa** 🖨: dal menu **⋯** del riquadro stampa l'appunto, con la formattazione e le caselle; dal menu **⋯** della finestra stampa l'appunto così com'è, anche con le modifiche non ancora salvate. Il pulsante **Stampa** in alto stampa **tutti gli appunti mostrati**, uno dopo l'altro, con i filtri scritti in testa al foglio. Il formato è quello di tutte le [stampe della piattaforma](interfaccia.md#stampa).

> [!TIP]
> **Fissato e archiviato valgono solo per te**, anche su un appunto ricevuto: ognuno fissa e archivia per conto suo, e agli altri non cambia nulla. Colore, etichette e contenuto sono invece dell'appunto: chi li cambia li cambia per tutte le persone che lo vedono.

## <a id="appunti-cercare"></a>Cercare e filtrare

- **Cerca negli appunti** 🔍: trova, nella vista aperta, gli appunti che contengono tutte le parole scritte nel titolo, nel testo, nelle voci, nelle etichette o nel nome del proprietario. Maiuscole e accenti non contano.
- **Tutti** · **Miei** · **Condivisi con me**: tutti gli appunti, solo quelli scritti da te oppure solo quelli ricevuti dai colleghi.
- **Tutte le etichette**: l'elenco compare quando almeno un appunto della vista ha un'etichetta, e mostra solo gli appunti con quella scelta; accanto a ogni etichetta c'è il numero dei suoi appunti.

Accanto ai filtri c'è il conteggio: *12 appunti*, oppure *3 di 12* quando la ricerca o i filtri ne nascondono alcuni. Vista ed etichetta scelte restano nell'indirizzo della pagina: ricaricandola le ritrovi.

## <a id="appunti-condividere"></a>Condividere con colleghi e gruppi

La condivisione la gestisce **solo il proprietario**, cioè chi ha scritto l'appunto. Apri l'appunto, oppure scegli **Condividi** dal riquadro, e nella sezione **Condivisione**:

1. nel campo **Aggiungi un collega o un gruppo** scrivi qualche lettera e scegli dall'elenco: compaiono i colleghi con un account abilitato, con ruolo e reparto, e i [gruppi di utenti](gruppi-policy.md), con il numero dei loro membri;
2. per ciascun destinatario scegli **Può leggere** (la scelta iniziale) oppure **Può modificare**; la **×** lo toglie dalla condivisione;
3. premi **Salva**: la condivisione vale da quel momento e ai nuovi destinatari arriva un [avviso](#appunti-ricevuti).

| Chi | Che cosa può fare |
| --- | --- |
| Il proprietario | Tutto: modificare, condividere, spostare nel cestino, ripristinare ed eliminare. |
| Un destinatario con **Può modificare** | Cambiare titolo, testo, voci, spunte, colore ed etichette. Non la condivisione, e non può spostare l'appunto nel cestino. |
| Un destinatario con **Può leggere** | Leggere l'appunto, che si apre in sola lettura; nel riquadro lo ricorda l'icona 👁. |
| Ogni destinatario | Fissare e archiviare per sé, creare una copia personale e, se la condivisione è diretta, rimuovere l'appunto dai propri: vedi [Appunti ricevuti](#appunti-ricevuti). |

- **Gruppi**: un appunto condiviso con un gruppo arriva a tutti i suoi membri, anche a chi entra nel gruppo in seguito; chi esce dal gruppo smette di vederlo. Chi lo riceve sia direttamente sia tramite un gruppo ha il permesso più ampio tra i due.
- **Amministratori**: non fanno parte dei gruppi, quindi un appunto condiviso con un gruppo a loro non arriva. Per condividerlo con un amministratore aggiungilo **per nome**. (Chi diventa amministratore conserva gli appunti che riceveva dai suoi gruppi: diventano condivisioni dirette.)
- Chi vede un appunto vede anche **con chi è condiviso**: nel riquadro l'icona con il numero dei destinatari (fermando il mouse compaiono i nomi), nella finestra la riga *Condiviso da … con …*.
- Togliendo un destinatario e salvando, l'appunto sparisce dai suoi appunti, a meno che gli arrivi anche tramite un gruppo.
- Un appunto si può condividere al massimo con **100** tra utenti e gruppi.

## <a id="appunti-ricevuti"></a>Appunti ricevuti

Quando un collega condivide un appunto con te, o con un gruppo di cui fai parte, in **basso a destra** compare l'avviso **Ha condiviso un appunto con te**, con il suo nome e il titolo dell'appunto (le prime parole, se il titolo manca): un clic sull'avviso apre l'appunto.

- Se in quel momento non eri collegato, l'avviso compare al prossimo accesso. Con molte condivisioni in attesa ne vengono segnalate tre: le altre le trovi nella pagina.
- Aprendo la pagina **Appunti** tutte le condivisioni risultano viste e gli avvisi non tornano più. Se sei già sulla pagina l'avviso non compare: l'appunto si aggiunge da solo all'elenco.

Un appunto ricevuto si riconosce dal nome del proprietario in fondo al riquadro (*di Mario Bianchi*). Oltre a leggerlo, e a modificarlo se ne hai il permesso, puoi:

- **fissarlo** o **archiviarlo**, solo per te;
- **Crea una copia** : nasce un appunto **tuo** con lo stesso titolo, contenuto, colore ed etichette, non condiviso con nessuno. Da lì in poi copia e originale sono indipendenti;
- **Rimuovi dai miei appunti** , se l'appunto è stato condiviso direttamente con te: toglie la tua condivisione. L'appunto resta al proprietario, che per fartelo riavere dovrà condividerlo di nuovo.

> [!NOTE]
> **Appunti ricevuti tramite un gruppo.** Chi riceve un appunto perché fa parte di un gruppo non può toglierlo dai propri appunti: può **archiviarlo**. **Rimuovi dai miei appunti** toglie solo la condivisione diretta: se lo stesso appunto ti arriva anche tramite un gruppo continui a vederlo, e da quel momento puoi solo archiviarlo.

## <a id="appunti-conflitti"></a>Modifiche contemporanee

Gli appunti si aggiornano **dal vivo**: quando un collega modifica, spunta, condivide o cestina un appunto che vedi, la pagina si aggiorna da sola in pochi istanti, senza ricaricarla. Lo stesso vale tra le tue schede del browser e i tuoi dispositivi.

- Se hai l'appunto **aperto senza averlo toccato**, la finestra passa da sola alla versione aggiornata.
- Se invece **hai scritto qualcosa o stai scrivendo**, in cima alla finestra compare un messaggio, per esempio **L'appunto è stato modificato da … alle …** oppure **La condivisione dell'appunto è cambiata**. Quello che hai scritto resta dov'è e nulla viene sovrascritto di nascosto: né il tuo lavoro né quello del collega. Un messaggio simile compare quando premi **Salva** su un appunto che nel frattempo è cambiato.

Sotto il messaggio ci sono due pulsanti:

| Pulsante | Che cosa fa |
| --- | --- |
| **Ricarica l'appunto** | Mostra la versione aggiornata. Quello che avevi scritto in questa finestra va perso: prima viene chiesta conferma. |
| **Salva come copia** | Salva quello che hai scritto in un **nuovo appunto personale**, non condiviso; l'originale resta com'è, e puoi riportarvi le tue modifiche con calma. |

- Conta come modifica anche un **cambio della condivisione**: se un destinatario viene aggiunto o tolto, o si rimuove da solo, mentre l'appunto è rimasto aperto in un'altra finestra, quella finestra riceve il messaggio al salvataggio. Per lo stesso motivo, dopo un cambio della condivisione l'appunto risulta modificato in quel momento da chi l'ha cambiata.
- La **spunta di una voce** fatta dal riquadro è un'operazione a sé: va a buon fine anche se nel frattempo un collega ha cambiato altro nell'appunto.
- Se nel frattempo ti è stato tolto il permesso di modifica, oppure l'appunto non è più disponibile (il proprietario lo ha cestinato o ha tolto la condivisione), il messaggio lo dice: resta comunque **Salva come copia**, per non perdere il lavoro.

## <a id="appunti-cestino"></a>Cestino

**Sposta nel cestino** 🗑 è riservato al **proprietario**. L'appunto passa nella vista **Cestino** e, se era condiviso, **sparisce anche ai destinatari**: per un appunto condiviso viene quindi chiesta conferma.

- Nel cestino l'appunto si può aprire ma non modificare. **Ripristina** lo rimette dov'era, con la stessa condivisione: torna visibile anche ai destinatari.
- **Elimina definitivamente** lo cancella dopo una conferma: non si potrà più recuperare.
- **Svuota cestino** elimina definitivamente, dopo una conferma, tutti gli appunti del tuo cestino.
- Un appunto rimasto nel cestino per **30 giorni** viene eliminato da solo.

Il cestino è personale e contiene solo appunti tuoi. Chi ha ricevuto un appunto non può cestinarlo: lo archivia oppure lo [rimuove dai propri appunti](#appunti-ricevuti).

## <a id="appunti-riservatezza"></a>Riservatezza

> [!NOTE]
> Un appunto lo vedono **solo chi lo ha scritto e le persone con cui è condiviso**, direttamente o tramite un gruppo. Come per la chat, non esiste una consultazione degli appunti altrui, e degli appunti **nulla finisce nel registro attività**. Gli appunti sono compresi nei backup.

- **Eliminando un utente** vengono eliminati tutti i suoi appunti, **anche quelli che aveva condiviso**, che spariscono a chi li riceveva. Finiscono anche le condivisioni fatte dagli altri verso di lui; quegli appunti restano ai loro proprietari.
- **Disabilitando** un utente i suoi appunti restano, e chi li riceveva continua a vederli. Un account disabilitato non compare più tra i colleghi con cui condividere un appunto; le condivisioni già fatte verso di lui restano.
- **Eliminando un gruppo di utenti** finisce la condivisione fatta con quel gruppo: l'appunto resta al proprietario e agli altri destinatari.

> [!WARNING]
> Prima di **eliminare l'account** di un collega, chi ha bisogno degli appunti che lui aveva condiviso ne faccia una copia con **Crea una copia**: la copia appartiene a chi la crea e non viene eliminata. Per togliere soltanto l'accesso è preferibile **disabilitare** l'account.

## <a id="appunti-limiti"></a>Limiti

| Che cosa | Limite |
| --- | --- |
| Titolo | 200 caratteri |
| Testo | 20.000 caratteri (la formattazione non conta; un testo formattato occupa al massimo 512 KB) |
| Elenco | 200 voci, ciascuna fino a 500 caratteri |
| Lavagna | 3.000 tratti e 512 KB di disegno (un messaggio avvisa quando è piena) |
| Etichette | 10 per appunto, ciascuna fino a 40 caratteri |
| Condivisione | 100 tra utenti e gruppi per appunto |
| Appunti | 5.000 per persona, compresi quelli nel cestino |

Se titolo, testo o voci superano il limite, l'appunto non viene salvato e un messaggio dice quale limite è stato superato: quello che hai scritto o incollato resta nella finestra, da accorciare, e nulla viene tagliato di nascosto. Il campo delle etichette, invece, si ferma da solo a 40 caratteri e a 10 etichette.

---

[← Attività](attivita.md) · [Indice](README.md) · [Rubrica →](rubrica.md)
