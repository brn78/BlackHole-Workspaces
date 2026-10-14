[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="listino"></a>Listino

**Commerciale → Listino** raccoglie ciò che l'azienda vende, con il **prezzo di vendita** e l'IVA: **materiali** (con marca, codici e fornitore), **prestazioni** (sopralluogo, collaudo, diritto di chiamata, canoni…) e **manodopera** per qualifica. A chi ne ha il permesso mostra anche **costo**, **ricarico** e **margine**. Serve all'assistenza e ai preventivi. La pagina compare solo a chi ha i permessi del listino (vedi [Permessi](#listino-permessi)): nessuna policy li riceve da sola.

## <a id="listino-elenco"></a>L'elenco

Le linguette **A listino** e **Fuori listino** dicono quante voci ci sono; **Da controllare** compare quando ci sono voci da sistemare (vedi [Importare ed esportare](#listino-importare)). Sotto si sceglie il tipo (**Materiali**, **Prestazioni**, **Manodopera**). La ricerca trova codice, descrizione, produttore, codice del produttore, codici a barre (del pezzo e della confezione), fornitore, qualifica e categoria. Gli elenchi scelgono la **categoria**, comprese le sottocategorie, il **produttore** e il **fornitore**. Una voce con le immagini mostra la principale al posto dell'icona del tipo. **Leggi codice** apre la voce dal suo codice a barre (vedi [Codici a barre ed etichette](#listino-codici)); anche un lettore che scrive il codice nella ricerca e preme Invio apre la voce.

Ogni riga mostra:

- la voce, con un'icona per il tipo, il codice, la descrizione, la categoria e la marca;
- l'unità di misura;
- il **prezzo**, e per chi vede i costi anche **costo** e **ricarico**; passando sopra al ricarico si legge da dove viene e il margine;
- la **variazione**: una freccia rossa se il prezzo è salito, verde se è sceso, con la percentuale dall'ultimo cambio; passando sopra, il prezzo di prima e la data.

In alto ci sono:

- **Stampa**: il listino prezzi da dare al cliente, il listino con costi e ricarichi per uso interno, le **etichette con il codice a barre** delle voci in elenco, oppure lo scarico in **CSV** per Excel;
- **Esporta** e **Importa**: tutto il listino in Excel, CSV o JSON, e le voci da un file (vedi [Importare ed esportare](#listino-importare));
- **Categorie**;
- **Ricarico**: il ricarico predefinito e l'IVA proposta;
- **Nuova voce**.

Un clic apre la voce. Il tasto destro (o ⋯) offre:

- lo storico dei prezzi;
- il listino del fornitore da cui viene la voce;
- **Etichette** (per i materiali);
- **Duplica**;
- **Togli dal listino** (o **Rimetti a listino**);
- **Segna da controllare** (o **Segna come controllata**);
- **Elimina**.

## <a id="listino-voci"></a>La voce

Una voce nuova parte dal tipo: **Materiale**, **Prestazione** o **Manodopera**. I campi sono:

- il **codice**, unico: vuoto = il prossimo libero, cioè ART-00001 per i materiali, PRE-0001 per le prestazioni e MDO-01 per la manodopera;
- la **categoria**;
- la **descrizione**;
- l'**unità di misura** (pz, m, h, a corpo…);
- l'**IVA**;
- per materiali e prestazioni il **tempo di posa**: le ore per installarne un'unità (0,5 per una presa, 0,02 per un metro di cavo). Quando la voce entra in un [preventivo](preventivi.md#preventivi-righe) la riga lo prende da sola, si accende la colonna «Posa» e le ore entrano nelle ore stimate; nel preventivo si cambia riga per riga.

Per i materiali ci sono anche il **produttore** (vedi [Produttori](produttori.md)), il codice del produttore, il **fornitore** dell'anagrafica e il suo codice, e i [codici a barre](#listino-codici) del pezzo e della confezione. Scrivendo il nome di un produttore che ha la scheda la voce si collega a lui; un nome senza scheda resta scritto come marca, e il pulsante accanto apre la scheda del produttore o la crea.

In cima alla voce ci sono le sue [immagini](#listino-immagini).

La **descrizione estesa** è il testo da mettere nei preventivi sotto la descrizione; le **note interne** restano per voi. Spento l'interruttore **A listino** (in basso, nella fascia dei pulsanti), la voce passa tra quelle «Fuori listino» con il suo storico: è il modo giusto per una voce che non si vende più.

In basso ci sono **Elimina** e **Duplica**, che apre una voce nuova con gli stessi dati tranne i codici.

## <a id="listino-da-scheda"></a>Una voce da una scheda tecnica

Dalla 1.103.0, con l'assistente attivo, **Da una scheda tecnica** (in alto nella pagina del listino, per chi lo modifica) apre un pannello dove incollare la scheda del produttore o una pagina di catalogo, oppure leggerla da un PDF o da una scansione con **Da un file**. L'assistente propone la **descrizione** breve da preventivo, la **descrizione estesa** con i dati tecnici utili (alimentazione, portata, grado di protezione, dimensioni…), la **marca**, il **codice del produttore**, l'**EAN** e l'unità; la piattaforma cerca il **produttore** tra quelli in anagrafica e la **categoria** dal tipo di prodotto. Si apre la voce nuova già compilata: aggiungi costo, prezzo e immagini e salva.

## <a id="listino-immagini"></a>Le immagini

Una voce ha fino a **12 immagini** (il prodotto da più lati, la confezione, un dettaglio). La prima è la **principale**: è quella dell'elenco, delle righe dei preventivi e delle loro stampe. Si aggiungono in tre modi:

- **Dal PC**;
- **Incolla**: nel browser, clic destro su un'immagine › *Copia immagine*, poi **Incolla**. Dall'indirizzo sicuro (https) l'immagine arriva subito; dall'indirizzo della rete locale il browser non lascia leggere gli appunti e si apre la finestra **Premi Ctrl+V adesso**, dove si incolla l'immagine (o il suo indirizzo, se hai copiato quello) o la si trascina. Anche Ctrl+V in qualunque punto della scheda aggiunge l'immagine copiata;
- **Da un indirizzo web**: incolli l'indirizzo dell'immagine (clic destro › *Copia indirizzo immagine*) e la scarica il server. Per sicurezza raggiunge solo indirizzi pubblici di internet, mai la rete dell'ufficio.

Prima di salvarla la ritagli; resta tutta l'immagine, su fondo bianco. Sotto i pulsanti ci sono le **miniature**: un clic apre il visualizzatore («1 di 3», con le frecce o ← → per scorrere, la rotellina con Ctrl o i pulsanti per ingrandire); trascinandone una sopra un'altra si cambia l'ordine; ★ la rende principale, 🗑 la toglie. Le modifiche alle immagini valgono quando salvi la voce. Accanto ci sono **Cerca immagini** e **Cerca sul web**, che aprono la ricerca con produttore e codice, e **Scheda del produttore**, se il produttore ha l'indirizzo della scheda prodotto. Le immagini non si scaricano da internet da sole: le scegli tu.

## <a id="listino-codici"></a>Codici a barre ed etichette

Un materiale ha due codici a barre: quello del **pezzo** e quello della **confezione**, con i **pezzi nella confezione** (nell'unità di misura della voce: 10 pz, 100 m). Ogni codice:

- si **scrive**; sotto il campo compare subito il disegno del codice. Un EAN o UPC (8, 12, 13 o 14 cifre) con l'ultima cifra, quella di controllo, che non torna viene segnalato in rosso e non si salva: di solito è una cifra letta o scritta male;
- si **legge** con : con un **lettore USB o Bluetooth** (scrive il codice come una tastiera, seguito da Invio) oppure con la **fotocamera** del telefono. La fotocamera legge i codici in Chrome su Android (anche su macOS e ChromeOS) e solo dall'indirizzo sicuro della piattaforma (https); sul PC Windows si usa il lettore;
- si **genera** con **Genera**: un EAN-13 interno che inizia con **20** (GS1 riserva i prefissi da 20 a 29 all'uso interno: non finiscono mai su un prodotto in commercio), progressivo, diverso da tutti quelli già usati. Serve per i prodotti senza codice, per le confezioni fatte da voi o per le parti di magazzino.

**Etichette** (nella voce, dal menu della riga, dalle voci scelte o da Stampa per tutte quelle in elenco) prepara le etichette da stampare: il codice del pezzo, della confezione o entrambi, su fogli A4 da 24 etichette (70 × 37 mm) o da 65 (38 × 21 mm), oppure una per foglio da 62 × 29 mm per le stampanti di etichette; con le copie per ogni etichetta, il prezzo di vendita (della confezione intera, sull'etichetta della confezione) e il QR code con il codice della voce. Le voci senza codice a barre possono portare il codice della voce (in Code 128), che si legge con lo stesso lettore. L'anteprima mostra le prime etichette come verranno.

I codici a barre si usano poi nei [preventivi](preventivi.md#preventivi-righe): letto il codice della confezione, la riga prende già la quantità della confezione.

## <a id="listino-prezzi"></a>Costo e prezzo

**Il costo** è quanto costa a voi un'unità, IVA esclusa. Si ottiene in due modi:

- con il **prezzo di listino del fornitore** e lo **sconto**, il costo si calcola da solo. Lo sconto può essere in cascata: **50+10** vuol dire il 50 % e poi il 10 % sul resto, cioè il 55 % in tutto;
- senza prezzo di listino, il costo si scrive direttamente.

**Il prezzo di vendita** si ottiene in tre modi:

- **Ricarico della categoria**: il costo più il ricarico della categoria della voce. Se la categoria non ne ha uno, vale quello della categoria sopra; in cima vale il **ricarico predefinito**. Se il ricarico cambia, il prezzo si ricalcola da solo.
- **Ricarico della voce**: un ricarico solo per questa voce.
- **Prezzo scritto a mano**: il prezzo resta quello scritto, anche quando cambia il costo. È il modo tipico di prestazioni e manodopera.

Mentre scrivi, i riquadri sotto mostrano costo, prezzo, prezzo IVA inclusa, ricarico e margine; il margine diventa rosso se il prezzo è sotto il costo. Il **ricarico** si calcola sul costo, il **margine** sul prezzo. Per esempio, un costo di 10 € con il 30 % di ricarico dà un prezzo di 13 €: il margine è 3 € su 13, cioè il 23 %.

Gli importi sono esatti: niente arrotondamenti nascosti. Il prezzo calcolato si arrotonda al centesimo, a metà verso l'alto (12,345 diventa 12,35). Sotto 1 € il prezzo tiene fino a quattro decimali (per esempio 0,5937 € al metro di cavo), perché lì il centesimo pesa troppo.

La linguetta **Storico prezzi** mostra il **grafico** del prezzo nel tempo, e per chi vede i costi anche il costo (linea tratteggiata). Sotto c'è ogni cambio, con il motivo (scritto nella voce, ricarico della categoria, aumento di più voci, listino nuovo del fornitore), chi l'ha fatto, il costo e il prezzo.

## <a id="listino-categorie"></a>Categorie e ricarico predefinito

**Categorie** apre l'albero delle categorie merceologiche, per esempio Videosorveglianza › Telecamere, Cavi, Prestazioni. Ogni categoria può avere un suo **ricarico**; senza, prende quello della categoria sopra, e in cima il ricarico predefinito. Accanto a ogni categoria si legge quale ricarico vale e da dove viene.

Quando cambia un ricarico, o una categoria si sposta, i prezzi delle voci che lo seguono si ricalcolano e il cambio finisce nel loro storico. Eliminare una categoria non elimina le voci: le sue voci e le sue sottocategorie passano alla categoria sopra. In cima al riquadro c'è il **ricarico predefinito** con l'IVA proposta per le voci nuove; si cambia anche dal pulsante **Ricarico** della pagina.

## <a id="listino-iva"></a>Aliquote IVA

**Aliquote IVA**, nella pagina del listino (e **Gestisci le aliquote** sotto la scelta dell'IVA di una voce), elenca le aliquote che scelgono le voci del listino e le righe dei preventivi. Ognuna ha:

- la **percentuale**;
- per le aliquote allo 0%, la **natura**, cioè perché non c'è l'IVA: esente, non imponibile, fuori campo, inversione contabile… con i codici N1–N7 della fattura elettronica;
- la **descrizione**, che si legge nelle scelte e nel riepilogo IVA dei preventivi (per esempio «Ridotta: interventi di recupero edilizio su abitazioni»);
- la **nota da stampare**: di solito il riferimento di legge, che compare sotto il riepilogo IVA dei preventivi con quell'aliquota.

Si parte con le più comuni già pronte, da controllare e completare: 22% ordinaria, 10% per il recupero edilizio su abitazioni, 5%, 4%, esente art. 10, non imponibile per esportazione e per dichiarazione d'intento, inversione contabile per il subappalto edile e per l'installazione di impianti in edifici, esclusa art. 15. Una sola è la **proposta**: va sulle voci nuove e sulle righe nuove dei preventivi (si cambia anche da **Ricarico**). Le frecce cambiano l'ordine delle scelte. Un'aliquota mai usata si elimina; una usata si **archivia**: resta sulle voci e sulle righe che ce l'hanno e non si propone più.

> [!TIP]
> Le righe dei preventivi tengono descrizione e nota dell'aliquota com'erano quando sono state salvate: cambiare una descrizione non cambia i preventivi già fatti, finché non li si salva di nuovo. Una voce importata con la sola percentuale prende l'aliquota con quella percentuale (per lo 0%, la prima allo 0% dell'elenco): controllala.

## <a id="listino-manodopera"></a>Manodopera dal personale

Una voce di manodopera ha la **qualifica**, cioè la mansione delle schede del [personale](personale.md), per esempio Tecnico specializzato. Il riquadro **Dal personale** mostra quante persone in forza hanno quella mansione e la loro **tariffa media**. A chi ha anche il permesso dei [costi del personale](personale.md#personale-orario) mostra il **costo orario medio**. **Usa questi valori** mette il costo medio come costo e la tariffa media come prezzo scritto a mano.

## <a id="listino-insieme"></a>Più voci insieme

Con l'icona della barra dell'elenco compaiono le caselle: scegli le voci (Maiusc+clic per un intervallo) e usa **Prezzi e categoria…**. Le operazioni possibili sono:

- **Cambia il costo in percentuale**, per esempio +5 quando un fornitore aumenta. Con il prezzo di listino cambia quello e lo sconto resta. Il prezzo segue il ricarico; quello scritto a mano resta.
- **Cambia il prezzo in percentuale**: il prezzo diventa scritto a mano.
- **Ricarico della voce**: lo stesso ricarico per tutte.
- **Torna al ricarico della categoria**.
- **Sposta in un'altra categoria**.

Accanto c'è **Togli dal listino** (o **Rimetti a listino**) e **Da controllare**; nella linguetta **Da controllare**, **Segna come controllate**. Le voci collegate a un listino del fornitore non cambiano costo da qui: lo prendono dal listino e dagli sconti delle famiglie.

## <a id="listino-importare"></a>Importare ed esportare

**Esporta** scarica **tutto il listino**, anche le voci fuori listino:

- **Excel (.xlsx)** e **CSV**: una riga per voce, con le colonne che l'importazione riconosce da sola (codice, descrizione, categoria, marca, codici, fornitore, prezzi, IVA, a listino, da controllare, note). Si sistema in Excel e si reimporta.
- **JSON, da reimportare**: tutto, anche la descrizione estesa e le ore di posa, per portare il listino su un altro server.
- **Solo le voci mostrate, in CSV**: quelle dell'elenco con i filtri di adesso.

Prezzo di listino, sconto, costo e ricarico ci sono solo per chi vede i costi.

**Importa** (a chi gestisce il listino) apre l'importazione guidata, nel pannello a destra:

1. **Il file**: Excel (.xlsx, .xls, .ods), CSV oppure il JSON di **Esporta** o quello estratto dal vecchio gestionale (listino.json). Al massimo 150 MB.
2. **Le colonne** (Excel e CSV): per ogni colonna del file, il dato della voce; quelle con il nome giusto (Codice, Descrizione, Prezzo listino, Sconto, EAN…) sono già scelte. Servono almeno codice e descrizione. Un prezzo di vendita scritto nel file resta così, come prezzo fisso; senza, si calcola dal costo (o dal prezzo di listino con lo sconto) con il ricarico. **Metti nelle note le colonne da non importare** conserva anche il resto. Con l'[assistente AI](assistente-ai.md) attivo per le analisi, **✨ Proponi con l'assistente** guarda i nomi e i primi valori delle colonne (per esempio «ART», «PRZ» o «Colonna C») e mette nelle scelte la sua proposta, evidenziata: controllala prima di andare avanti.
3. **L'anteprima**: quante voci sono nuove, già nel listino (stesso codice), con il codice a barre di un'altra voce, con errori (codice o descrizione mancanti, codice doppio nel file) e da controllare. Le scelte: Sotto, le voci a pagine, per stato e con la ricerca; passando sopra all'icona si leggono errori e segnalazioni.
   - **Voci già nel listino**: **Lasciale come sono**, **Aggiorna i prezzi** (prezzo di listino, sconto, costo e prezzo; il cambio va nello storico dei prezzi) oppure **Aggiorna tutto** (anche descrizioni, marca, unità, codici a barre, fornitore, IVA, categoria e stato; le note del file si aggiungono una volta sola). Le voci collegate al listino di un fornitore tengono i prezzi del listino del fornitore.
   - **Maiuscole e minuscole** come nel resto della piattaforma, con qualche esempio.
   - **Sconti per marca**: per le voci con il prezzo di listino ma senza sconto, lo sconto da dare a tutta la marca (45 oppure 45+10); è già proposto quello che hanno quasi tutte le altre voci della marca.
   - Per il file del vecchio gestionale anche **Tieni i prezzi di vendita del vecchio gestionale** (quelli rimasti indietro dopo un aumento del listino, che l'estrazione ricalcola) e **Salta le voci senza nessun prezzo**.
4. **Importa**: prima di un'importazione grande si salva una copia del database (in recovery); le voci si scrivono a blocchi, così il listino resta consultabile. L'esito dice quante voci sono state create, aggiornate, già uguali, saltate e da controllare, con le righe non create.

Niente si perde: un dato del file che non va bene (codice a barre non valido, valore fuori misura, categoria che non c'è, fornitore che non è in anagrafica) finisce nelle **note** della voce, che resta segnata **Da controllare**. La categoria si riconosce dal nome, il fornitore dalla partita IVA, dal codice fiscale o dal codice. Una voce si toglie dalle «Da controllare» togliendo la spunta nella sua scheda, oppure insieme ad altre con **Segna come controllate**.

> [!TIP]
> Il listino del vecchio gestionale si porta così: sul PC con la cartella del vecchio gestionale si esegue esporta\_listino.py, che scrive listino.json (con i codici «SIGLA codice» come quelli dei listini METEL, così le stesse voci prese dopo da un listino del fornitore non si doppiano) e un riepilogo delle correzioni; poi **Importa** con quel file.

## <a id="listino-permessi"></a>Permessi

Costi e ricarichi sono dati riservati: la pagina e i suoi dati li vede solo chi ha uno di questi permessi nella sua policy, e gli amministratori.

| Permesso | Consente |
| --- | --- |
| Vedere il listino | Le voci con il prezzo di vendita e l'IVA, lo storico dei prezzi senza i costi, gli articoli dei listini dei fornitori con il prezzo al pubblico. Niente costi, sconti, ricarichi né margini. |
| Costi e ricarichi del listino | In più: costi, prezzi di listino e sconti dei fornitori, ricarichi e margini, la stampa con i costi. |
| Gestire il listino | Creare, modificare ed eliminare voci e categorie, cambiare ricarichi e prezzi anche di più voci insieme, importare i listini dei fornitori e scriverne gli sconti. |

---

[← Assistenza](assistenza.md) · [Indice](README.md) · [Listini fornitori →](listini-fornitori.md)
