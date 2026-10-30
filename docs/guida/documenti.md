[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="documenti"></a>Documenti

**Archivio → Documenti** è l'archivio dei file dell'azienda: progetti, disegni, manuali, programmi e setup, certificazioni, offerte, foto. I file stanno in **cartelle**, conservano tutte le **revisioni** precedenti, si collegano a un **cliente** e si ritrovano con **categorie**, **etichette**, **produttore** e **modello**. Il [visualizzatore](#documenti-visualizzatore) apre nella pagina PDF, Word, Excel, immagini, disegni CAD e modelli 3D; l'[editor](#documenti-editor) crea documenti Word e file di testo senza uscire dalla piattaforma. La pagina compare a chi ha almeno il permesso **Visualizzare i documenti** (vedi [Permessi e cartelle riservate](#documenti-permessi)).

Sopra l'elenco ci sono il **percorso** della cartella aperta (un clic su un nome risale, fino a **Documenti**), la scelta tra **Elenco** e **Schede** con le anteprime di immagini, PDF e disegni, e i filtri. Ogni file ha un'icona con la sigla del suo tipo (PDF, DOCX, XLSX, DWG, EXE…) in un colore che lo distingue a colpo d'occhio.

## <a id="documenti-cartelle"></a>Cartelle, file e azioni

- **Nuovo** → **Cartella…** crea una cartella nella cartella aperta, con un colore a scelta; **Documento Word…** e **File di testo…** aprono l'[editor](#documenti-editor).
- Un **clic** su una cartella la apre; su un file lo apre nel visualizzatore (anche <kbd>Invio</kbd> sul file selezionato). Un file che il visualizzatore non mostra apre la sua [scheda](#documenti-scheda). La scheda, la modifica e le altre azioni sono nel menu **⋯** e nel **tasto destro**.
- Le **azioni** di un elemento sono nel menu **⋯** a fine riga e del **tasto destro**: **Apri**, **Scheda**, **Modifica nell'editor** (documenti Word e file di testo), **Revisioni**, **Scarica**, **Condividi con un link…** (per chi può [condividere](condivisioni.md)), **Rinomina** (<kbd>F2</kbd>), **Sposta in…**, **Copia in…**, **Sposta nel cestino** (<kbd>Canc</kbd>). Per gli archivi ZIP anche **Estrai**; per i PDF e le immagini, se il riconoscimento del testo è installato, **Rendi ricercabile** ed **Estrai il testo** (vedi [Riconoscimento del testo](#documenti-ocr)).
- **Selezione multipla**: <kbd>Ctrl</kbd>+clic e <kbd>Maiusc</kbd>+clic, oppure le caselle a inizio riga, che compaiono con l'icona **Scegli più elementi** accanto ai pulsanti della vista (premuta di nuovo, le caselle spariscono e la scelta si toglie). Sopra l'elenco compare la barra con **Scarica ZIP**, **Sposta**, **Copia**, **Comprimi** (crea un archivio ZIP nella cartella) e **Cestino**.
- **Trascinare** file e cartelle su una cartella dell'elenco o del percorso li sposta lì (per una cartella lontana usa **Sposta**, che fa scegliere la destinazione).
- **Copia** duplica i file con la loro revisione corrente (il contenuto non occupa altro spazio sul disco) e le cartelle con il loro contenuto e la stessa riservatezza. Se il nome c'è già, la copia si chiama «nome - copia».
- Nella stessa cartella due elementi non possono avere lo stesso nome (maiuscole e minuscole non contano).
- Le cartelle **Commesse** e **Attività**, nella radice, le crea la piattaforma per i [documenti delle commesse](progetti.md#progetti-documenti) e per i [file delle attività](attivita.md#attivita-file) senza commessa: le loro sottocartelle seguono la riservatezza della commessa o dell'attività e si riallineano da sole.

## <a id="documenti-caricare"></a>Caricare e scaricare

**Carica** → **File…** oppure **Cartella intera…**, oppure **trascina** file e cartelle dal computer sulla pagina: le cartelle arrivano con tutte le sottocartelle. Prima di inviare si apre una finestra con l'elenco dei file e i dati da dare a quelli nuovi (categoria, cliente, produttore, prodotto, etichette, nota della revisione), tutti facoltativi, e la casella [Elimina dal PC dopo il caricamento](#documenti-originali).

- Se nella cartella c'è già un file con lo stesso nome, prima di inviare viene chiesto che cosa fare: caricarlo come **nuova revisione** di quello esistente (se puoi modificarlo), salvarlo **con un nome libero**, per esempio «offerta (2).pdf», oppure **saltarlo**.
- L'avanzamento di caricamenti e scaricamenti, con la velocità e il tempo che manca, è nella sezione **Trasferimenti** del pannello della [campanella](notifiche.md#notifiche-campanella) 🔔, che si apre da solo quando ne parte uno; chiuso il pannello, un **anello** attorno alla campanella mostra la percentuale finché c'è qualcosa in corso. Un trasferimento in corso si annulla con la **×**, uno non riuscito si riprova; **Togli i finiti** pulisce l'elenco. Puoi continuare a lavorare, anche in altre pagine.
- Un file può essere grande fino a **8 GB**. Prima di ricevere un file il server controlla che sul disco della cartella di lavoro resti spazio libero.
- Dei **programmi** (.exe, .dll) e dei **pacchetti di installazione** (.msi) il server legge dal file la **versione**, a ogni caricamento e a ogni nuova revisione, e compila **produttore** e **modello** (il nome del prodotto) se non li hai scritti tu.
- **Scarica** salva il file; più elementi selezionati, o una cartella, si scaricano in un unico **archivio ZIP** con le cartelle al loro posto.
- Un archivio **ZIP** caricato si può **estrarre** in una nuova cartella accanto, con lo stesso nome dell'archivio. Per sicurezza i nomi interni vengono ripuliti (nessun file finisce fuori dalla cartella) e l'estrazione si ferma oltre 20.000 voci o 8 GB di contenuto.

## <a id="documenti-originali"></a>Eliminare gli originali dal PC

Nella finestra di caricamento (e in [Da una cartella del PC](impianti.md#impianti-cartella)) la casella **Elimina dal PC dopo il caricamento** sposta i file invece di copiarli: finito il caricamento, i file caricati si tolgono dal PC, insieme alle cartelle rimaste vuote.

- Al clic su **Carica** (o **Importa**) il browser chiede il permesso di modificare i file della cartella; per dei file sciolti fa scegliere la cartella che li contiene (la finestra si apre già lì).
- Si eliminano solo i file **caricati davvero** e rimasti uguali (stessa dimensione e data di modifica): quelli non riusciti, saltati perché già presenti o cambiati nel frattempo restano sul PC, e una cartella che contiene ancora qualcosa non si tocca. Alla fine un avviso dice quanti file e cartelle sono stati tolti.
- La cancellazione **non passa dal cestino di Windows**: i file restano in Documenti, con le loro revisioni e il [cestino](#documenti-cestino) di Documenti.
- Funziona con **Chrome** o **Edge** quando BlackHole si apre da un **indirizzo sicuro** (https, per esempio quello per l'accesso da fuori). Da un indirizzo della rete locale come *http://192.168.1.10:5180* il browser non lo permette a nessun sito, e la casella è spenta con il motivo. Per l'ufficio il browser può trattare come sicuro l'indirizzo della rete locale (vale solo per quell'indirizzo):
   - in Chrome apri *chrome://flags/#unsafely-treat-insecure-origin-as-secure* (in Edge *edge://flags/#unsafely-treat-insecure-origin-as-secure*), scrivi l'indirizzo di BlackHole (per esempio *http://192.168.1.10:5180*), scegli **Enabled** e riavvia il browser;
   - su più PC lo stesso si fa con il criterio *OverrideSecurityRestrictionsOnInsecureOrigin* di Chrome o di Edge, per chi gestisce i criteri di Windows.

## <a id="documenti-scheda"></a>La scheda: categoria, cliente, produttore e prodotto, etichette

La **scheda** (la voce **Scheda** del menu ⋯ o del tasto destro, o il pulsante del visualizzatore) apre il pannello di un elemento, diviso in **Scheda**, **Revisioni**, **Accesso** (solo per le cartelle) e **Dettagli**:

- **Nome**: l'estensione resta quella del file, perché il tipo non cambia rinominando.
- **Categoria**: Progettazione, Software, Manuale, Scheda tecnica, Certificazione, Contratto, Offerta, Foto e video, Altro. Chi ha il permesso **Gestire le categorie dei documenti** le aggiunge, le rinomina, ne sceglie icona e colore e le elimina con **Altro** › **Categorie dei documenti** della pagina, nel pannello dei [tipi e delle categorie](interfaccia.md#interfaccia-tipi); eliminando una categoria i file restano, senza categoria.
- **Cliente**: collega il file o la cartella a un cliente. Il nome del cliente compare nell'elenco e il file si ritrova nella scheda **Documenti** del cliente, vedi [Documenti e stampa del cliente](clienti.md#clienti-documenti).
- **Produttore** e **Prodotto**: a che cosa si riferisce il file, per esempio produttore *Microsoft* e prodotto *Office Pro*, oppure *Siemens* e *S7-1200* per un manuale o una scheda tecnica. Mentre scrivi compaiono i valori già usati. Per programmi e pacchetti di installazione, se li lasci vuoti, si leggono dal file.
- **Versione**: c'è solo per programmi e pacchetti di installazione e non si scrive a mano, perché la legge il server dal file della revisione corrente; nell'elenco compare accanto al produttore (*v. 1.3.1*). Le versioni scritte a mano prima della 1.4 su altri tipi di file sono state spostate nella **Descrizione**.
- **Etichette**: parole libere (fino a 20). Un clic su un'etichetta nell'elenco mostra tutti i file che la hanno.
- **Descrizione** e, per le cartelle, il **colore**.
- **Dettagli**: tipo, dimensione, percorso, chi ha creato e modificato e quando, e per i programmi le informazioni di versione e la **firma digitale** (chi ha firmato il setup, oppure *Non firmato*). **Stampa scheda** stampa questi dati.

Se due persone modificano la stessa scheda, chi salva per secondo riceve un messaggio e nulla viene sovrascritto di nascosto: riapri la scheda per vedere la versione aggiornata.

## <a id="documenti-cercare"></a>Cercare e filtrare

- La casella **Cerca** trova i file per nome, descrizione, produttore, prodotto, versione, cliente ed etichette e, dalla 1.81.0, anche per le parole scritte **dentro i file** (vedi [Il testo dei file](#documenti-testo)); **In tutte le cartelle** oppure **Solo in questa cartella** sceglie dove cercare. Nei risultati c'è la cartella in cui si trova ogni file e, per quelli trovati dal testo, il pezzo di testo intorno alle parole.
- Gli elenchi **Categoria** e **Tipo** (PDF, documenti Office, immagini, CAD e 3D, video e audio, archivi, programmi, testo e codice) restringono l'elenco; i filtri attivi compaiono sopra l'elenco, ciascuno con la sua **×**.
- Un clic sull'intestazione di una colonna ordina per nome, categoria, dimensione o data.

## <a id="documenti-testo"></a>Il testo dei file

La ricerca (quella in alto e quella dei Documenti) trova anche le parole scritte **dentro i file**: PDF con il loro testo, documenti Word e OpenDocument, fogli Excel, presentazioni PowerPoint, file di testo, CSV, HTML, XML, RTF ed email salvate (.eml). Basta l'inizio delle parole e non contano maiuscole e accenti (*rele* trova *Relè*); devono esserci tutte. Nei risultati compare **Nel testo:** con il pezzo intorno alle parole trovate.

- Il server legge i file da solo, piano, qualche minuto dopo l'avvio e poi ogni due minuti: un file appena caricato si trova nel testo poco dopo. Ogni contenuto si legge una volta, anche se lo stesso file è in più cartelle.
- Contano solo le versioni correnti fuori dal cestino: una revisione nuova sostituisce il testo vecchio, un file nel cestino non si trova più (ripristinato, si ritrova).
- Le regole sono quelle di sempre: i file delle cartelle riservate li trova solo chi le vede.
- Le scansioni (PDF senza testo, foto) non hanno testo da leggere: prima [Rendi ricercabile](#documenti-ocr) con l'OCR.
- Gli amministratori, con **Leggi il testo dei file** in alto nella pagina, vedono quanti file sono stati letti, quanti sono in coda, senza testo o non letti (protetti, rovinati o oltre 60 MB) e possono **Rifare l'indice** da capo. Il testo sta in un indice a parte, fuori dalle copie di sicurezza: se si perde si rifà da solo.

## <a id="documenti-revisioni"></a>Revisioni

Ogni file conserva la sua **cronologia**. Una nuova revisione nasce caricando un file con lo stesso nome (e scegliendo **nuova revisione**), con **Carica nuova revisione** nella scheda **Revisioni** oppure salvando dall'[editor](#documenti-editor). La nuova revisione deve essere dello stesso tipo: un PDF resta un PDF.

- Con **Carica nuova revisione** l'avanzamento compare sotto il pulsante e nella [campanella](notifiche.md#notifiche-campanella): puoi chiudere la scheda, il caricamento continua e alla fine un avviso conferma che la revisione è stata caricata. Se chiudi o ricarichi la pagina mentre è in corso, il browser chiede conferma, perché il caricamento si interromperebbe.
- Nella scheda **Revisioni** ognuna ha numero, data, autore, dimensione e nota; la corrente è segnata. Ogni revisione si **apre** nel visualizzatore e si **scarica**.
- **Ripristina** rende di nuovo attuale una revisione precedente **come nuova revisione**: la cronologia resta intera e si può sempre tornare indietro.
- **Elimina** toglie una revisione precedente (mai la corrente): serve il permesso **Eliminare qualsiasi documento**.
- Un contenuto identico non viene salvato due volte sul disco: copie e revisioni uguali occupano lo spazio di una sola.

## <a id="documenti-visualizzatore"></a>Il visualizzatore

Il visualizzatore si apre sopra la pagina. In alto: nome, tipo e dimensione del file, i comandi del formato (zoom, pagine, fogli, livelli…), le frecce per passare agli altri file della cartella (anche con le frecce della tastiera), **Scheda** , **Annota** (vedi [Annotazioni e misure](#documenti-annotazioni)), **Scarica** ⬇, **Stampa un'area** , **Stampa** 🖨 e **Chiudi** (<kbd>Esc</kbd>). **Stampa** compare solo per i formati che si stampano: non per video, audio, archivi e programmi.

| Formato | Come si vede |
| --- | --- |
| **PDF** | Pagine nitide a ogni zoom, con il testo selezionabile e copiabile; adatta alla finestra, tutto schermo, vai a pagina. |
| **Word** (.docx) | Impaginato com'è, con titoli, tabelle, immagini; **Modifica** lo apre nell'editor. |
| **Excel** (.xlsx, .xls, .ods) e **CSV** | Tabella con i **fogli** in basso; dei fogli molto lunghi si vedono le prime righe. Un .xlsx ha **Modifica**, che lo apre nel [foglio di calcolo](#documenti-foglio). |
| **Altri documenti Office** (.doc, .ppt, .pptx, .odt, .rtf, Visio…) | Convertiti in PDF da [LibreOffice](#documenti-libreoffice), se è installato sul server; altrimenti si scaricano. Anche Word ed Excel hanno il pulsante **Impaginato**, che li mostra esattamente come in stampa. |
| **Immagini** (JPG, PNG, GIF, WebP, SVG…) e **TIFF** a più pagine | Zoom con la rotellina, sul punto indicato dal mouse (nei TIFF a più pagine la rotellina scorre le pagine e zooma con <kbd>Ctrl</kbd>), spostamento trascinando l'immagine, adatta alla finestra, rotazione. |
| **Disegni DXF** | Il disegno vettoriale con zoom e spostamento, sfondo chiaro o scuro e i **livelli** da accendere e spegnere. |
| **Disegni DWF** (.dwf, .dwfx) | Il disegno vettoriale, letto direttamente nel browser senza programmi sul server: zoom con la rotellina sul punto indicato, spostamento trascinando, **Adatta alla finestra**, sfondo chiaro o scuro, i **fogli** in basso quando il file ne ha più d'uno. Dei DWFx si vede per ora la miniatura del foglio. |
| **Disegni DWG** | Come i DXF, con livelli, zoom e stampa: il server converte il disegno in DXF la prima volta che lo apri (vedi [Disegni DWG sul server](#documenti-dwg)). Se sul server non c'è un convertitore, si vede l'**anteprima** che AutoCAD salva dentro il file, con la versione del formato. |
| **Modelli 3D** (STL, OBJ, 3MF, glTF) | Il modello da ruotare, spostare e ingrandire con il mouse o con le dita, in vista piena o **fil di ferro**, con le dimensioni d'ingombro. STEP e IGES non si vedono: si scaricano. |
| **Video** e **audio** | Partono da soli all'apertura, in una finestra della loro misura (più piccola per l'audio, adatta al video), anche spostandosi avanti e indietro. L'audio mostra delle barre che si muovono con il suono, dai bassi agli acuti, con l'altezza che si adatta al volume del brano, e scendono quando è in pausa. |
| **Testo e codice** (TXT, MD, JSON, XML, HTML, script…) | Testo con i numeri di riga e, a scelta, l'**A capo** automatico; **Modifica** lo apre nell'editor. Le pagine HTML si vedono come testo, mai come pagine. |
| **Archivi ZIP** | L'elenco del contenuto, con dimensioni e date, ed **Estrai in una cartella**. |
| **Programmi e setup** (.exe, .dll, .msi) | Prodotto, versione, produttore, copyright e **firma digitale**. Un programma non si avvia mai dalla piattaforma: va scaricato sul PC dove installarlo. |

**Stampa** stampa il file com'è: le pagine del PDF, il documento, il foglio, il disegno, l'immagine. Elenchi e schede si stampano invece nel [formato unico della piattaforma](interfaccia.md#stampa).

**Stampa un'area** stampa solo un pezzo: trascina un rettangolo sopra il contenuto (<kbd>Esc</kbd> annulla) e si stampa quella parte, ingrandita sul foglio. Funziona su immagini (anche ruotate), TIFF, PDF (la pagina si rifà ad alta definizione) e disegni DXF, DWG e DWF.

## <a id="documenti-annotazioni"></a>Annotazioni e misure

Su PDF (anche i documenti Office convertiti), immagini, TIFF e disegni DXF, DWG e DWF si può scrivere e misurare sopra il file: **Annota** in alto apre la barra degli strumenti a sinistra. Il file **non cambia**: le annotazioni si salvano a parte e si disegnano sopra, anche nella **Stampa** e nella **Stampa un'area**. Il pulsante dice quante ce ne sono, per esempio *Annota (3)*.

| Strumento | Come si usa |
| --- | --- |
| **Seleziona** (<kbd>V</kbd>) | Clic su un'annotazione per sceglierla, trascinala per spostarla, trascina i quadratini per cambiarne i punti; doppio clic su un testo o un commento per correggerlo; <kbd>Canc</kbd> la elimina. Trascinando il foglio vuoto ci si sposta. |
| **Penna** (<kbd>P</kbd>) e **Evidenziatore** (<kbd>H</kbd>) | A mano libera, trascinando. |
| **Linea** (<kbd>L</kbd>), **Freccia** (<kbd>F</kbd>), **Rettangolo** (<kbd>R</kbd>), **Ellisse** (<kbd>E</kbd>), **Nuvola di revisione** (<kbd>N</kbd>) | Trascina da un punto all'altro, oppure clic sul primo punto e clic sul secondo. Con <kbd>Maiusc</kbd> linee a 45°, quadrati e cerchi. |
| **Testo** (<kbd>T</kbd>) | Clic dove scrivere, <kbd>Invio</kbd> salva. Il testo cresce e cala con lo zoom, come il disegno. |
| **Commento** (<kbd>C</kbd>) | Un segnaposto numerato con un messaggio per i colleghi (<kbd>Maiusc</kbd>+<kbd>Invio</kbd> va a capo): sceglilo per leggerlo, con chi l'ha scritto e quando. |
| **Distanza** (<kbd>D</kbd>) | Clic sui due punti: la misura compare sulla quota. |
| **Lunghezza** (<kbd>M</kbd>) | Clic sui punti di un percorso (una canalina, un cavo); doppio clic o <kbd>Invio</kbd> per finire, <kbd>Backspace</kbd> toglie l'ultimo punto. |
| **Area** (<kbd>A</kbd>) | Clic sui vertici; doppio clic o <kbd>Invio</kbd> chiude la figura. Compaiono l'area e il perimetro. |
| **Area con un clic** (<kbd>K</kbd>) | Nei disegni DXF, DWG, DWF e nei PDF vettoriali (le planimetrie esportate dai CAD): un clic dentro un locale e il programma trova da solo il contorno chiuso intorno, con l'area e il perimetro (per i metri quadri di un pavimento o i metri di parete di un preventivo). Gli arredi dentro non si tolgono; le linee dei livelli spenti non contano. Se il locale non è chiuso (una porta aperta, un muro che non arriva) lo dice: allora si misura con i clic sui vertici. |
| **Quota** (<kbd>Q</kbd>) | Come le quote dei CAD: clic sui due punti da quotare, poi dove mettere la linea di quota; con <kbd>Maiusc</kbd> nell'ultimo clic la quota è orizzontale o verticale. Linee di richiamo, punte e misura; le punte (freccia, trattino obliquo, punto) si scelgono nel pallino dei colori. |

Nei disegni DXF, DWG e DWF le misure **si agganciano** ai punti del disegno vicini al mouse, come in AutoCAD (dalla 1.126.0): il simbolo arancione con il nome dice a che cosa ci si aggancia — quadrato **Estremo**, triangolo **Punto medio**, cerchio **Centro** (anche passando sulla curva), rombo **Quadrante**, croce **Intersezione**, angolo retto **Perpendicolare** (dal primo punto della misura), **Inserimento** di testi e blocchi, **Nodo** e **Vicino** (un punto qualsiasi della linea, spento all'inizio). <kbd>Alt</kbd> mentre clicchi non aggancia; <kbd>F3</kbd> accende e spegne gli agganci e il pulsante nella barra sceglie quali. Dalla 1.128.0 ci si aggancia anche alle linee dei **PDF vettoriali** (le planimetrie che arrivano esportate dai CAD), lette alla prima misura su quella pagina; i PDF scansionati non hanno linee.

## <a id="documenti-cad-fedelta"></a>Disegni fedeli: tratteggi, testi e accenti

Dalla 1.127.0 i DXF (e i DWG convertiti) si vedono come in AutoCAD anche nei dettagli:

- **Tipi di linea**: tratteggi, assi a tratto e punto, linee nascoste, puntinate… dalla tabella del disegno, con la scala generale (LTSCALE) e quella dell'oggetto, anche dentro i blocchi. Quando i trattini sarebbero troppo fitti per vedersi la linea resta continua.
- **Testi con il carattere a tratto**, da disegno tecnico, come i caratteri SHX di AutoCAD (con le lettere accentate); quello che il carattere non ha si scrive con il carattere normale. Il pulsante in alto passa dal carattere a tratto a quello normale e viceversa (la scelta resta).
- **Accenti dei disegni vecchi**: i DXF fino ad AutoCAD 2006 scrivono i testi nella code page del disegno (di solito Windows 1252), non in UTF-8: il visualizzatore la riconosce, così «Città» non diventa «Citt�».

## <a id="documenti-cad-pdf"></a>Esportare il disegno in PDF vettoriale

Dalla 1.129.0 i disegni DXF, DWG e DWF si esportano in un **PDF vettoriale**, come il «Pubblica» di AutoCAD: le linee restano linee, si ingrandiscono senza perdere qualità e si stampano nitide anche su un A0. Pulsante nella barra in alto, oppure il comando **PDF**. Si sceglie:

- **Formato** (da A4 ad A0) e **orientamento**; **tutto il disegno** o **la vista di adesso** (quello che si vede sullo schermo, per esportare un dettaglio);
- **Scala**: **Adatta al foglio** (il disegno più grande che ci sta) oppure **In scala** 1:50, 1:100… quando il disegno dice in che unità è (nei DWF solo «adatta»); se al rapporto scelto non ci sta, esce la parte centrale e lo avvisa;
- **Colori**: **Bianco e nero** (per l'impresa e il cantiere: tutto nero, anche le linee gialle), **Scala di grigi** o **A colori**; lo **spessore delle linee** in millimetri;
- **Con le annotazioni e le misure** fatte sul file (aree, quote, note), sopra il disegno: le aree colorate sono trasparenti e non coprono quello che c'è sotto;
- **Livelli**: nel PDF ogni livello del disegno si accende e si spegne dal pannello dei livelli di Acrobat (i livelli spenti nel visualizzatore non si esportano);
- il **nome del file, la scala e la data** in basso a destra.

Le scelte restano per la volta dopo. Il PDF si scarica sul PC; per metterlo tra i documenti si carica come gli altri file.

## <a id="documenti-cad"></a>Strumenti da disegnatore e riga di comando

Nei disegni DXF, DWG e DWF il visualizzatore lavora come un programma CAD (dalla 1.126.0; le idee vengono da AutoCAD e da CADCraft, il codice è nostro). Il disegno non cambia mai: misure e note restano annotazioni.

- **Orto** (<kbd>F8</kbd>, pulsante +): linee e misure solo orizzontali o verticali. **Polare** (<kbd>F10</kbd>, pulsante ): passando vicino agli angoli multipli del passo (15° di base; clic sul pulsante per 5, 10, 30, 45 o 90°) la linea si blocca su quell'angolo, con la linea tratteggiata di puntamento. Si usano anche su PDF e immagini. Un aggancio vince su orto e polare; con <kbd>Maiusc</kbd> restano i 45°.
- **La lunghezza a tastiera**: dopo il primo punto di una linea, freccia o misura, scrivi un numero (per esempio *1200*, oppure *3,5&lt;30* con l'angolo in gradi) e <kbd>Invio</kbd>: il punto va a quella distanza verso il mouse, nell'unità della scala (millimetri, metri…).
- **Proprietà** (<kbd>I</kbd>, o il comando **PROPRIETA**): passando sul disegno si evidenzia l'oggetto sotto il mouse; un clic mostra tipo, **livello**, lunghezza o perimetro, area, raggio e diametro, angolo, coordinate, il blocco e il testo. Da lì **Isola il livello**, **Spegni il livello** e **Tutti**.
- **Livelli**: il pannello (pulsante in alto) accende e spegne i livelli; **solo** accanto a un livello mostra soltanto quello, **Tutti** li riaccende. Anche nei DWF, quando il disegno porta i livelli. Gli agganci e la scelta degli oggetti valgono per quello che si vede.

La **riga di comando** sta in basso (<kbd>Ctrl</kbd>+<kbd>9</kbd> la mostra o la nasconde): basta scrivere sul disegno, le lettere vanno lì, con i suggerimenti mentre scrivi. <kbd>Invio</kbd> o <kbd>Spazio</kbd> esegue, <kbd>Invio</kbd> a vuoto ripete l'ultimo comando, <kbd>↑</kbd> e <kbd>↓</kbd> la cronologia, <kbd>Esc</kbd> annulla. A destra lo stato di **Agganci**, **Orto** e **Polare** (clic per cambiarlo, tasto destro per le scelte). Valgono anche i nomi di AutoCAD.

| Comando | Anche | Che cosa fa |
| --- | --- | --- |
| **DISTANZA**, **LUNGHEZZA**, **AREA** | DI, D · LEN, M · AA, A | Le misure |
| **CONTORNO**, **QUOTA** | BOUNDARY, BO, K · DIMALIGNED, DAL, Q | Area di un locale con un clic, quota con le frecce |
| **LINEA**, **FRECCIA**, **RETTANGOLO**, **ELLISSE**, **NUVOLA**, **TESTO**, **COMMENTO** | L, F, REC, EL, REVCLOUD, T, C | Le annotazioni |
| **PROPRIETA** | LIST, LI | Le proprietà dell'oggetto su cui fai clic |
| **ID** |   | Le coordinate del punto su cui fai clic (con gli agganci) |
| **ZOOM E**, **ZOOM 2**, **ZOOM 0,5** | Z, ZE | Tutto il disegno, più vicino, più lontano |
| **LIVELLI** | LAYER, LA | Apre il pannello dei livelli |
| **ISOLA** [nome] | LAYISO | Solo il livello scritto (bastano le prime lettere) o quello dell'oggetto su cui fai clic |
| **SPEGNI** [nome] | LAYOFF | Spegne il livello scritto o quello dell'oggetto scelto |
| **TUTTI** | LAYON | Riaccende tutti i livelli |
| **AGGANCI**, **ORTO**, **POLARE** [passo] | OSNAP, ORTHO, POLAR | Gli agganci da usare; orto e polare (ON/OFF, o POLARE 30 per il passo) |
| **SCALA**, **ANNULLA**, **RIPETI**, **STAMPA**, **ELENCO** | U, REDO, PLOT | Scala delle misure, annulla e ripeti, stampa, elenco delle annotazioni |
| **PDF** | ESPORTA, EXPORTPDF, PUBLISH | Esporta il disegno in PDF vettoriale (formato, scala, bianco e nero, livelli) |
| **?** | AIUTO | L'elenco dei comandi |

Con la riga di comando le lettere degli strumenti si scrivono lì (<kbd>L</kbd> e <kbd>Invio</kbd> per la linea); nascondendola tornano le scorciatoie di una lettera.

Il pallino colorato sceglie **colore**, **spessore** e **grandezza del testo** (valgono anche per l'annotazione scelta); **Annulla** (<kbd>Ctrl</kbd>+<kbd>Z</kbd>) e **Ripeti** (<kbd>Ctrl</kbd>+<kbd>Y</kbd>) valgono per tutto ciò che hai fatto con il file aperto. Per muoverti mentre disegni: rotellina per lo zoom, tasto centrale del mouse oppure <kbd>Spazio</kbd> e trascinamento per spostarti. <kbd>Esc</kbd> annulla ciò che stai disegnando, poi torna a **Seleziona**, poi chiude la barra.

**La scala** dice quanto vale nella realtà un'unità del file:

- nei **DXF e DWG** si usano le unità del disegno (per esempio i millimetri), se il disegno le dichiara; altrimenti scegli tu che cosa vale un'unità;
- nei **PDF** scegli il rapporto con cui è stampato il disegno (1:50, 1:100…); senza, le misure sono quelle sulla carta;
- su **immagini e DWF**, e ovunque la scala non sia sicura, usa **Da una misura nota…**: traccia una quota che conosci (una porta, un muro quotato) e scrivi quanto è lunga.

In **Mostra le misure in** scegli millimetri, centimetri, metri, pollici o piedi. La scala vale per tutta la pagina e per tutti; ogni pagina di un PDF può avere la sua.

**Elenco** mostra tutte le annotazioni con chi le ha fatte e quando: un clic porta il disegno su quella scelta, 🗑 la elimina, 👁 nasconde o rimostra tutte le annotazioni (anche in stampa).

- Le annotazioni le vede chi vede il file. Ognuno cambia ed elimina le proprie; chi può modificare il documento (nell'archivio di rete gli amministratori) anche quelle degli altri, e l'eliminazione resta nel [registro attività](registro.md).
- Sui **documenti** le annotazioni appartengono alla revisione: una revisione nuova parte pulita e nell'elenco **Copia qui** riporta quelle della revisione precedente. Se il documento viene eliminato definitivamente, se ne vanno anche le sue annotazioni.
- Sui file dell'[archivio di rete](archivio-rete.md) le annotazioni restano legate al percorso del file e il file nella cartella condivisa non viene toccato.
- Sui file aperti [dal PC senza salvarli](#documenti-dal-pc) si annota e si stampa, ma le annotazioni restano solo finché il visualizzatore è aperto.

## <a id="documenti-dal-pc"></a>Aprire un file del PC senza salvarlo

Per vedere un file al volo, senza metterlo nei Documenti: **Carica** → **Solo da vedere, senza salvarlo…** (chi non può caricare file ha il pulsante **Apri dal PC** 👁). Si possono scegliere più file insieme: si aprono nel visualizzatore con le frecce per passare dall'uno all'altro, e in alto c'è scritto *Dal PC · non salvato*.

- PDF, Word, Excel, immagini, video, audio, testo, disegni DXF e DWF e modelli 3D si aprono nel browser: il file non lascia il PC.
- I formati che hanno bisogno del server (vecchi formati di Office da convertire con LibreOffice, DWG, ZIP, programmi) passano dalla sua cartella temporanea: li vede solo chi li ha aperti e si cancellano, con le conversioni, quando si chiude il visualizzatore (o dopo due ore senza uso, o al riavvio del server).
- I tipi di file che non si aprono lo dicono in un avviso con il loro nome.

## <a id="documenti-editor"></a>Creare e modificare documenti: l'editor

**Nuovo** → **Documento Word…** chiede il nome e apre l'editor a tutta pagina, su un foglio A4 (per un foglio di calcolo vedi [qui sotto](#documenti-foglio)). Salvando nasce un vero file **.docx**, che si apre anche con Word e LibreOffice. La barra dell'editor ha:

- **Annulla** e **Ripeti** (<kbd>Ctrl</kbd>+<kbd>Z</kbd>, <kbd>Ctrl</kbd>+<kbd>Y</kbd>);
- **carattere**, **dimensione** e **stile del paragrafo** (Normale, Titolo 1, 2, 3);
- grassetto, corsivo, sottolineato, barrato, **colore** ed **evidenziato**, apice e pedice;
- elenchi numerati, puntati e **caselle da spuntare**, rientri, allineamento;
- citazione, codice, **collegamento** (<kbd>Ctrl</kbd>+<kbd>K</kbd>) e **immagine** dal computer (ridotta se molto grande);
- **tabelle**: inserisci una tabella 3 × 3, aggiungi o togli righe e colonne, elimina la tabella;
- **Togli la formattazione**.

In alto ci sono anche **Cerca e sostituisci** 🔍 (<kbd>Ctrl</kbd>+<kbd>F</kbd>; la casella **Maiuscole** distingue maiuscole e minuscole, **Sostituisci tutto** cambia ogni occorrenza), **Stampa** (<kbd>Ctrl</kbd>+<kbd>P</kbd>) e **Salva** (<kbd>Ctrl</kbd>+<kbd>S</kbd>); in basso il conteggio di parole e caratteri. Chiudendo con modifiche non salvate viene chiesta conferma.

- Il primo salvataggio crea il file nella cartella; i successivi ne creano una **nuova revisione**, così le versioni precedenti restano nella cronologia.
- **Modifica** su un documento Word esistente lo apre nell'editor. I documenti con un'impaginazione complessa (caselle di testo, colonne, intestazioni) vengono **semplificati**: un messaggio in alto a destra lo dice, e l'originale resta comunque nelle revisioni precedenti.
- **Nuovo** → **File di testo…** e **Modifica** su un file di testo o di codice (.txt, .md, .csv, .json, script… fino a 5 MB) aprono l'editor di testo semplice, con i numeri di riga e l'a capo automatico che si può togliere. Il file si salva in UTF-8.
- **Testo da immagine o PDF** , in alto, accanto a Cerca: scegli dal computer una scansione o una foto (PDF, JPG, PNG, TIFF, BMP, GIF) e il server ne riconosce il testo, che entra dove c'è il cursore (al posto del testo selezionato, se ce n'è); un testo di più righe va su righe sue. C'è quando il [riconoscimento del testo](#documenti-ocr) è installato. Rileggi il testo inserito: il riconoscimento può sbagliare qualche lettera.

Lo stesso editor, in versione ridotta, scrive il [testo degli appunti](appunti.md#appunti-formattare).

## <a id="documenti-foglio"></a>Il foglio di calcolo

**Nuovo** → **Foglio di calcolo…** chiede il nome e apre una griglia come quella di Excel; **Modifica** su un file **.xlsx** (fino a 15 MB) apre quello esistente. Salvando nasce un vero file Excel, che si apre anche con Excel e LibreOffice; come per i documenti, i salvataggi successivi sono **nuove revisioni**.

- **Scrivere**: clic su una cella e si scrive; <kbd>Invio</kbd> conferma e scende, <kbd>Tab</kbd> va a destra, <kbd>Esc</kbd> annulla, doppio clic o <kbd>F2</kbd> modifica il contenuto. In alto la **barra della formula** mostra e modifica la cella scelta, e la casella dell'indirizzo porta a una cella o a un intervallo (*B3*, *A1:C10*).
- **Valori**: i numeri all'italiana (*1.234,56*), le **percentuali** (*22%*), gli importi in **euro** (*€ 60*), le **date** (*15/10/2026*) e *VERO*/*FALSO* si riconoscono da soli. I codici con lo zero davanti (*00123*) restano testo; un apostrofo all'inizio scrive tutto come testo.
- **Formule**: si scrivono come in Excel in italiano, con <kbd>=</kbd> davanti: *=SOMMA(A1:A10)*, *=B2\*C2*, *=A1\*1,22*, *=SE(D7&gt;500;"sì";"no")*, anche tra fogli (*='Listino 2026'!B4*). Si calcolano subito: SOMMA, MEDIA, MIN, MAX, CONTA.NUMERI, CONTA.VALORI, CONTA.VUOTE, ARROTONDA (anche PER.ECC e PER.DIF), INT, ASS, RESTO, POTENZA, RADQ, PRODOTTO, SE, E, O, NON, SE.ERRORE, CONCATENA, LUNGHEZZA, MAIUSC, MINUSC, ANNULLA.SPAZI, SINISTRA, DESTRA, STRINGA.ESTRAI, OGGI, ADESSO, DATA, ANNO, MESE, GIORNO, SOMMA.SE, CONTA.SE, MEDIA.SE, CERCA.VERT. Le altre funzioni restano nella formula e le calcola Excel quando apre il file (qui mostrano *#NOME?*). Mentre scrivi una formula, un clic su una cella ne inserisce l'indirizzo (<kbd>Maiusc</kbd>+clic lo allarga a un intervallo). Una formula scritta male lo dice e resta da correggere.
- **Scegliere**: trascinando, con <kbd>Maiusc</kbd> e le frecce o con un clic sulle lettere delle colonne e sui numeri delle righe; in basso a destra la somma e la media dei numeri scelti.
- **Copia**, **Taglia** e **Incolla** (<kbd>Ctrl</kbd>+<kbd>C</kbd>, <kbd>X</kbd>, <kbd>V</kbd>) anche da e verso Excel; incollando celle copiate qui le formule spostano i riferimenti (quelli con <kbd>$</kbd> restano). **Riempi in basso** (<kbd>Ctrl</kbd>+<kbd>D</kbd>) copia la prima riga scelta in quelle sotto.
- Con il **tasto destro**: inserisci righe sopra o sotto, colonne a sinistra o a destra, elimina righe e colonne, cancella il contenuto. Le formule seguono: *=SOMMA(D2:D4)* diventa *=SOMMA(D2:D5)* se inserisci una riga in mezzo; un riferimento a una cella eliminata diventa *#RIF!*.
- **Colonne**: la larghezza si cambia trascinando il bordo destro della lettera.
- **Fogli**: le schede in basso; + ne aggiunge uno, doppio clic lo rinomina (le formule che lo usano prendono il nome nuovo), il tasto destro lo elimina.
- **Annulla** e **Ripeti** (<kbd>Ctrl</kbd>+<kbd>Z</kbd>, <kbd>Ctrl</kbd>+<kbd>Y</kbd>), **Cerca e sostituisci** 🔍 (<kbd>Ctrl</kbd>+<kbd>F</kbd>; si sostituisce nelle celle senza formula), **Stampa** del foglio scelto e **Salva** (<kbd>Ctrl</kbd>+<kbd>S</kbd>).

> [!NOTE]
> Si salvano valori, formule con il loro risultato, formati dei numeri (date, percentuali, euro), larghezze delle colonne e celle unite. Colori, bordi e caratteri di un file Excel esistente qui non si modificano e salvando non si conservano: il messaggio in alto a destra lo dice, e il file originale resta nella revisione precedente. Il file salvato chiede a Excel di ricalcolare tutte le formule all'apertura.

## <a id="documenti-cestino"></a>Cestino

**Sposta nel cestino** toglie file e cartelle dall'archivio senza eliminarli: la linguetta **Cestino** 🗑 della pagina, accanto a **Documenti**, con il numero degli elementi che contiene, li mostra con chi li ha cestinati e quando.

- **Ripristina** rimette l'elemento nella cartella dov'era (se nel frattempo un altro ha preso il suo nome, viene rinominato); una cartella torna con tutto il suo contenuto.
- **Elimina definitivamente** e **Svuota cestino** cancellano per sempre, dopo una conferma: serve il permesso **Eliminare qualsiasi documento**.
- Dopo **30 giorni** nel cestino gli elementi si eliminano da soli. Il contenuto di un file sparisce dal disco quando nessuna revisione lo usa più, insieme alle sue conversioni (il PDF fatto da LibreOffice, il DXF di un DWG). Con il file se ne vanno anche le revisioni, le [annotazioni](#documenti-annotazioni), i collegamenti ad attività, impianti, manutenzioni e assistenza e i link di condivisione.

## <a id="documenti-permessi"></a>Permessi e cartelle riservate

Ciò che ciascuno può fare con i documenti dipende dai permessi delle sue [policy](gruppi-policy.md#policy-permessi). Gli amministratori possono tutto.

| Permesso | Consente |
| --- | --- |
| Visualizzare i documenti | Sfogliare cartelle e file, aprirli nel visualizzatore, scaricarli e stamparli (escluse le cartelle riservate ad altri e quelle che chiedono un permesso che non si ha: per esempio la cartella **Listini** di ogni produttore, che la vede solo chi ha *Costi e ricarichi del listino*, perché i listini dei fornitori portano i prezzi di acquisto). |
| Caricare documenti | Caricare file e creare cartelle e documenti, anche estraendo un archivio ZIP o comprimendo una selezione. |
| Modificare i documenti caricati da sé | Rinominare, spostare, descrivere e caricare nuove revisioni dei file e delle cartelle creati da te. |
| Modificare tutti i documenti | Lo stesso, su qualsiasi file o cartella. |
| Eliminare i documenti caricati da sé | Spostare nel cestino (e ripristinare) i file e le cartelle creati da te. |
| Eliminare qualsiasi documento | Spostare nel cestino qualsiasi elemento, eliminare le revisioni precedenti e svuotare il cestino. |
| Gestire le categorie dei documenti | Aggiungere, rinominare, colorare ed eliminare le categorie. |
| Riservare le cartelle | Rendere una cartella visibile solo a utenti e gruppi scelti, anche in sola lettura. |
| Condividere con link esterni | Far vedere file, cartelle e la documentazione degli impianti a chi non ha un account, con un link (vedi [Condivisioni](condivisioni.md)). |
| Gestire tutti i link esterni | Vedere, modificare e disattivare i link creati da chiunque. |

**Cartelle riservate.** Nella scheda **Accesso** di una cartella, chi ha il permesso **Riservare le cartelle** attiva **Cartella riservata** e aggiunge gli utenti e i gruppi che possono vederla, ciascuno con **Lettura e modifica** oppure **Sola lettura**; poi **Salva l'accesso**.

- La riservatezza vale per la cartella e per **tutto ciò che contiene**, sottocartelle comprese. Una sottocartella riservata a sua volta restringe ancora: la vede solo chi è ammesso in entrambe.
- Per gli altri la cartella **non esiste**: non compare in elenchi, ricerche, conteggi, scelta della cartella e nella scheda dei clienti. Nell'elenco le cartelle riservate hanno il lucchetto .
- Con **Sola lettura** si vede e si scarica, ma non si carica, non si modifica e non si cestina nulla, anche avendo i permessi delle policy.
- Chi riserva una cartella senza essere amministratore deve restare tra gli ammessi, con la modifica: così non può chiudersi fuori da solo.
- Per spostare o cestinare una cartella intera bisogna poter modificare tutto ciò che contiene.

## <a id="documenti-libreoffice"></a>LibreOffice sul server

Il browser sa leggere PDF, Word .docx, Excel, immagini e disegni; i formati più vecchi o meno diffusi (.doc, .ppt, .pptx, .odt, .rtf, Visio…) li legge **LibreOffice**, il programma gratuito di The Document Foundation, se è installato sul server: li converte in PDF, che il visualizzatore mostra e stampa. La conversione si fa una volta sola per ogni revisione e viene ricordata.

Un amministratore installa LibreOffice da **Sistema → Impostazioni → Server → LibreOffice**, che mostra se è installato, la versione e il percorso:

- **Installa LibreOffice** (o **Aggiorna all'ultima versione**) cerca sul sito di The Document Foundation il setup ufficiale più recente disponibile per Windows (le versioni appena annunciate, il cui setup non è ancora pubblicato, si saltano). Se è la versione già installata te lo dice subito, senza chiedere la password e senza scaricare nulla; altrimenti la conferma mostra la versione nuova e quella installata;
- **Carica il setup (.msi)** usa un setup scaricato da te, utile se il server non esce su Internet. Il setup della versione già installata, o di una precedente, viene rifiutato.

In entrambi i casi, dopo la conferma con la tua password, il server **verifica la firma digitale** del setup (deve essere di The Document Foundation) e lo installa in silenzio, senza cambiare i programmi con cui il PC apre i file di Office. Ci vogliono alcuni minuti: il riquadro mostra l'avanzamento e l'esito. Un tentativo non riuscito per una versione che sul server c'è comunque compare come **Non necessaria**, senza messaggio di errore. Come per l'[aggiornamento](server.md#server-aggiornamento), si fa solo dalla rete locale e con la piattaforma installata come servizio di Windows.

**Rimuovi LibreOffice**, con le stesse regole (rete locale, conferma della password), lo disinstalla dal server in silenzio, in qualche minuto, insieme alla sua guida se c'è. Attenzione: LibreOffice è un normale programma di Windows, e sul server potrebbe usarlo anche qualcun altro o un altro programma; la conferma lo ricorda, perché rimuovendolo non c'è più per nessuno. I documenti già convertiti restano visibili; i nuovi .doc, .ppt, .odt… si possono solo scaricare finché non lo reinstalli. Il pulsante c'è quando LibreOffice è stato installato con il suo setup (dalla piattaforma o a mano); il riquadro mostra poi l'esito dell'**ultima rimozione**.

## <a id="documenti-dwg"></a>Disegni DWG sul server

Il DWG di AutoCAD è un formato chiuso: il browser non lo sa leggere. Per aprirlo nel visualizzatore come un DXF, con livelli, zoom e stampa, il server lo **converte in DXF** la prima volta che lo apri e ricorda il risultato, una volta per ogni revisione: le aperture successive sono immediate. Per convertire serve un programma sul server:

- **ODA File Converter**, gratuito, della Open Design Alliance: è il più fedele e legge tutte le versioni di AutoCAD. Si installa da **Sistema → Impostazioni → Server → Disegni DWG** con **Installa ODA File Converter** (poi **Aggiorna ODA File Converter**): come per LibreOffice il server cerca l'ultima versione sul sito della Open Design Alliance, che si scarica senza registrazione, e se è quella già installata te lo dice subito. Altrimenti, dopo la conferma con la tua password, scarica il setup ufficiale, ne **verifica la firma digitale** (deve essere della Open Design Alliance) e lo installa in silenzio al posto della versione precedente: ci vuole circa un minuto. **Carica il setup di ODA (.msi)** usa un setup scaricato da te, se il server non esce su Internet (la stessa versione o una precedente vengono rifiutate). Serve la piattaforma installata come servizio di Windows; installato a mano sul server va bene lo stesso: la piattaforma lo trova da sola nei Programmi e lo usa per primo. Si usa alle condizioni della Open Design Alliance (*ODA Community User Agreement*): per le sue funzioni, come la conversione dei disegni, senza rivenderlo né distribuirlo.
- **GNU LibreDWG**, software libero: si installa dallo stesso riquadro con **Installa LibreDWG** (oppure **Carica il pacchetto di LibreDWG**, se il server non esce su Internet). Dopo la conferma con la tua password il server scarica il pacchetto ufficiale per Windows, ne controlla l'**impronta** (deve essere quella del pacchetto firmato dal manutentore) e lo mette nella cartella di lavoro: bastano pochi secondi. Legge i disegni fino al formato 2018, che è anche quello delle versioni attuali di AutoCAD; in quelli più complessi qualche oggetto può mancare.

Se ci sono entrambi si usa ODA File Converter e, se non riesce, LibreDWG. Senza convertitore, o se la conversione non riesce, il visualizzatore mostra l'anteprima salvata nel disegno e il motivo. Il riquadro **Disegni DWG** di Impostazioni mostra quale convertitore è in uso, il suo percorso e l'esito dell'ultima installazione (dell'uno o dell'altro). Il pulsante **Rimuovi** (con tutti e due i convertitori **Rimuovi…**, che chiede quale) toglie, con la conferma della password, LibreDWG, che sta nella cartella di lavoro della piattaforma, oppure ODA File Converter: questo, come LibreOffice, è un programma di Windows che sul server potrebbe usare anche qualcun altro o un altro programma, e la conferma lo ricorda. Tolto ODA, i disegni si convertono con LibreDWG, se c'è. Come per LibreOffice, installazione e rimozione si fanno solo dalla rete locale.

## <a id="documenti-chiedi"></a>Chiedi al documento

Dalla 1.104.0, con l'[assistente](assistente-ai.md) attivo, il menu di un file ha **Chiedi all'assistente**: un pannello dove l'assistente **riassume** il documento o risponde alle domande su quello che c'è scritto, con le domande pronte **Riassumi**, **Date e scadenze**, **Importi** e **Che cosa chiede**, oppure una tua. Si leggono i PDF con il testo, Word, Excel, PowerPoint, i testi e le email; una **scansione** va prima resa ricercabile (**Rendi ricercabile** dallo stesso menu). Un documento molto lungo si legge fino a dove sta nel contesto dell'assistente, e la risposta lo dice. Il testo va all'assistente configurato (se è un servizio esterno, esce dall'azienda) e la conversazione non si salva.

## <a id="documenti-ocr"></a>Riconoscimento del testo (OCR)

Di una scansione o di una foto il computer vede solo un'immagine: non si cerca, non si copia, non si incolla. Il **riconoscimento del testo** la legge sul server, con il programma libero **Tesseract**, e ne ricava il testo, in italiano e in inglese. Le pagine girate di lato o capovolte si raddrizzano da sole e le foto del telefono si leggono nel verso in cui sono state scattate. I file non escono dal server.

- **Rendi ricercabile** (menu ⋯ o tasto destro su un PDF o un'immagine) crea un **PDF ricercabile**, come quelli degli scanner più recenti: le pagine restano le stesse immagini e sopra c'è il testo invisibile, che si cerca, si seleziona e si copia nel visualizzatore e in qualsiasi lettore di PDF. Per un **PDF** il risultato è una **nuova revisione** dello stesso file (l'originale resta nelle revisioni); le pagine che hanno già il testo si lasciano com'erano e, se lo hanno tutte, non cambia niente. Per un'**immagine** (anche un TIFF a più pagine) nasce un **PDF nuovo** nella stessa cartella, con lo stesso nome, la stessa categoria, lo stesso cliente e le stesse etichette; se il nome c'è già, prende un nome libero, per esempio «foto (2).pdf».
- Il lavoro continua in sottofondo: l'avanzamento, pagina per pagina, è nella sezione **Trasferimenti** della [campanella](notifiche.md#notifiche-campanella) 🔔, dove la **×** lo annulla (alla fine della pagina in corso). Alla fine un avviso dice com'è andata e l'elenco si aggiorna.
- **Estrai il testo** legge il file mostrando l'avanzamento (si può annullare) e apre l'[editor](#documenti-editor) con un documento Word nuovo che contiene il testo, già diviso in paragrafi, chiamato come il file con «- testo»: correggilo se serve e **Salva**, e il documento va nella cartella del file. Se chiudi senza salvare non resta niente. Dei PDF che hanno già il testo si prende quello, senza riconoscimento.
- Nell'editor, **Testo da immagine o PDF** fa lo stesso con un file del tuo computer e inserisce il testo dove c'è il cursore.
- Il server legge un file alla volta, circa un secondo per pagina, con priorità bassa, così il resto della piattaforma resta veloce: se ce ne sono altri prima, il tuo aspetta in coda e la finestra dice a che posto è. Ognuno può avere tre lavori in corso o in coda; un file può avere fino a 500 pagine e 256 MB.
- Per un buon risultato: scansioni a 300 dpi, foto con buona luce, il foglio intero e a fuoco. Il riconoscimento può sbagliare qualche lettera, soprattutto in tabelle, timbri e scritte a mano, che di solito non legge: rileggi i dati importanti, come importi e codici.
- Chi può farlo: **Estrai il testo** chi può vedere il documento; **Rendi ricercabile** chi può caricarne nuove revisioni (per un PDF) o caricare file nella sua cartella (per un'immagine). Nel registro attività restano i PDF resi ricercabili e quelli creati; il testo letto non si salva da nessuna parte, se non nel documento che salvi tu.

Un amministratore lo installa da **Sistema → Impostazioni → Server → Riconoscimento del testo (OCR)**: **Installa il riconoscimento del testo** scarica da GitHub i dati delle lingue italiana e inglese e del raddrizzamento delle pagine (circa 35 MB, sempre la stessa versione, controllata con l'impronta SHA-256) nella cartella `tools\tessdata` della cartella di lavoro. Non serve la password: sono dati, non programmi da installare in Windows, e il motore è già nella piattaforma. Il riquadro mostra l'avanzamento (si può annullare), lo stato, i lavori in corso e in coda; **Rimuovi** cancella i dati, e le voci del riconoscimento spariscono finché non lo reinstalli. Se il riquadro dice che il motore non parte, sul server manca il componente di Windows *Microsoft Visual C++ 2015-2022 Redistributable (x64)*: si scarica dal sito di Microsoft e si installa sul server.

## <a id="documenti-dal-vivo"></a>Lavorare insieme

La pagina si aggiorna da sola quando un collega carica, sposta, rinomina o cestina qualcosa. Nel registro attività restano caricamenti, eliminazioni, spostamenti, revisioni e cambi di accesso, con il nome dell'elemento.

---

[← Scadenze](scadenze.md) · [Indice](README.md) · [Condivisioni →](condivisioni.md)
