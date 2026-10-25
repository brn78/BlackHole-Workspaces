[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="trattative"></a>Progetti

**Progettazione → Progetti** segue il **lavoro da prendere presso un cliente**, dal primo contatto all'accettazione, prima e durante i preventivi: chi ha chiesto, che lavoro, quanto vale, a che punto è, quanto è probabile prenderlo, quando si pensa che il cliente decida e **che cosa fare dopo**. Quando il cliente accetta, il progetto diventa una [commessa](progetti.md), il lavoro partito, e resta collegato a lei (vedi [Accettato: la commessa](#trattative-commessa)). Così nessuna richiesta si perde tra una telefonata e l'altra e si vede in anticipo quanto lavoro sta per arrivare. La pagina compare a chi vede i [preventivi](preventivi.md), con gli stessi permessi: chi li compila crea e cambia i progetti, chi li gestisce può anche eliminarli. Quelli dei contatti privati li vede solo il proprietario.

## <a id="trattative-fasi"></a>Kanban e fasi

- Nella linguetta **In corso** ogni progetto è una scheda nella colonna della sua fase: **Primo contatto**, **Sopralluogo**, **Preventivo** (in preparazione o inviato), **Trattativa** (si discute il prezzo o i tempi). Si **trascina** da una colonna all'altra; trascinandolo, sotto compaiono **Accettato** e **Rifiutato**. In testa a ogni colonna il valore e il valore pesato.
- Ogni fase propone la sua **probabilità** (10, 30, 50, 70%): cambiando fase la probabilità la segue, a meno che tu non l'abbia cambiata a mano.
- La scheda ha il **prossimo passo** (rosso quando il giorno è arrivato) e, con il bordo rosso, quelli con la chiusura prevista già passata. **Elenco** mostra gli stessi progetti in una tabella con i totali.
- In alto: il valore in corso, il **pesato** (valore × probabilità), quanto si pensa di chiudere entro il mese, quanti hanno il prossimo passo da fare (un clic li filtra) e quanti accettati sono ancora **Senza commessa**. I filtri **Miei** e **Da fare** e il commerciale valgono anche per la previsione.

## <a id="trattative-scheda"></a>La scheda del progetto

- **Il lavoro** in poche parole (è anche il nome proposto per la commessa) e il **cliente**. Se non è ancora in anagrafica, **Non è ancora in anagrafica** chiede solo nome, telefono ed email; **Crea la scheda del cliente** lo mette tra i potenziali clienti e lo collega. Un preventivo per il progetto lo collega comunque.
- **Valore stimato** (l'imponibile che si pensa di fatturare), **probabilità**, **chiusura prevista**, **commerciale** (di base chi lo crea), **provenienza** (passaparola, sito, fiera…) e **tipo di lavoro**, con i suggerimenti di quelli già scritti.
- In cima, per un progetto in corso: **Cliente sentito**, **Rifiutato** e **Accettato**; per uno chiuso, **Riapri**. Sotto, le [commesse](#trattative-commessa) nate dal progetto, i [preventivi](#trattative-preventivi) e lo **storico**: fasi, contatti, preventivi, chiusura.

## <a id="trattative-da-testo"></a>Un progetto da un testo

Dalla 1.123.0, con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (in alto nella pagina Progetti) apre un pannello dove incollare la **richiesta del cliente**: un'email, un messaggio, il modulo del sito o gli appunti di una telefonata. L'assistente propone il **lavoro**, chi lo chiede, il **tipo di lavoro**, la provenienza, il **valore** se c'è un budget, la fase (sopralluogo se lo chiede, altrimenti primo contatto o preventivo), il **prossimo passo** e le note con la richiesta riassunta. Con **Da un file** il testo si legge anche da un PDF o da una scansione. **Proponi i dati** chiede all'assistente i dati e la piattaforma cerca il **cliente** tra quelli che vedi (partita IVA, email anche dei referenti, telefono, nome, poi un nome simile da controllare) e, con il cliente, il suo **impianto** dalle parole del testo. Si apre la scheda nuova **già compilata**, con in cima la nota dell'assistente: controlla, correggi e salva come sempre. Niente si salva da solo e il testo non si conserva. Se chi chiede non è in anagrafica, la scheda è già su *Non è ancora in anagrafica* con nome, telefono ed email.

## <a id="trattative-prossimo-passo"></a>Prossimo passo e cliente sentito

Il **prossimo passo** dice che cosa fare e quando («fissare il sopralluogo», «mandare il preventivo rivisto»). Va nelle [Scadenze](scadenze.md) (area «Preventivi e progetti») e nel [calendario del telefono](profilo.md#profilo-calendario) di chi lo abbona; il giorno prima e il giorno stesso arriva il promemoria al commerciale (senza commerciale, a chi gestisce i preventivi). **Cliente sentito** scrive nello storico come vi siete sentiti e che cosa vi siete detti e fissa il passo successivo.

## <a id="trattative-preventivi"></a>I preventivi del progetto

- **Nuovo preventivo** nella scheda prepara il preventivo per quel cliente, con l'oggetto del progetto. Un progetto nelle prime fasi passa a **Preventivo**.
- Quando il preventivo è **inviato**, il valore del progetto diventa il suo imponibile; quando è **accettato**, il progetto risulta **accettato** da solo e si propone subito la commessa (vedi [Dopo l'accettazione: commessa o progetto](preventivi.md#preventivi-commessa)). Un rifiuto resta nello storico: si può fare una revisione (resta collegata) oppure segnare il progetto rifiutato.
- **Collega** aggancia un preventivo già fatto per lo stesso cliente; l'icona accanto lo toglie. Il preventivo mostra in testata il suo progetto, e la scheda del cliente, nella linguetta Preventivi, sopra i preventivi, i suoi **Progetti in corso**.

## <a id="trattative-chiusura"></a>Accettati e rifiutati

**Accettato** lo porta al 100%, **Rifiutato** allo 0% con il **motivo** (prezzo, concorrente, rinviato, nessuna risposta…): servono a capire dove si perde. Tutti e due chiedono il giorno. Le linguette **Accettati** e **Rifiutati** li elencano con il giorno e l'esito; **Riapri** li rimette nel kanban (le commesse già aperte restano). Eliminato, un progetto va nel [cestino](cestino.md) con il suo storico; i preventivi e le commesse restano, senza il collegamento.

## <a id="trattative-commessa"></a>Accettato: la commessa

Quando il cliente dice sì, il lavoro parte: il progetto diventa una [commessa](progetti.md), che resta collegata a lui da tutte e due le parti.

- **Accettato** (il pulsante in cima alla scheda, la barra in fondo al kanban mentre trascini la scheda, oppure il menu **⋯**) chiede il giorno. Se il progetto ha il cliente in anagrafica e chi lo segna può creare commesse, propone anche la casella **Poi apri la commessa**, già spuntata: confermando, si apre subito la finestra della commessa.
- **Apri la commessa** crea una **commessa nuova**: nome (di base il titolo del progetto), tipo, responsabile (di base il commerciale del progetto), inizio, fine prevista e la casella della [cartella in Documenti](progetti.md#progetti-documenti). Oppure, con **Commessa esistente**, collega una commessa già aperta dello stesso cliente.
- Un progetto ancora in corso, aprendo la commessa, risulta accettato oggi; uno rifiutato va prima riaperto. Senza il cliente in anagrafica la commessa non si apre: prima si sceglie il cliente, o si crea la sua scheda.
- Nella scheda del progetto la parte **Commesse** mostra le commesse nate da lui, con il loro stato: **Aperta dal progetto** (l'icona la scollega, la commessa resta) oppure **Da un preventivo del progetto** (si scollega dal preventivo). Un progetto accettato senza commessa mostra l'avviso con **Apri la commessa**.
- Nella pagina Progetti il filtro **Senza commessa** e il riquadro in cima **Senza commessa** mostrano gli accettati la cui commessa non è ancora aperta; la linguetta **Accettati** ha la colonna **Commessa**.
- La commessa mostra in testa **Dal progetto**, con il collegamento al progetto, e nel suo menu **⋯** ha **Il progetto della commessa**.

## <a id="trattative-importa"></a>Importare ed esportare

**Esporta** scarica i progetti in **Excel**, **CSV** o come **calendario** (i prossimi passi e le chiusure previste di quelli in corso). **Importa** (a chi li gestisce) li porta da un foglio: lavoro, cliente, telefono ed email, fase, probabilità, valore, chiusura prevista, commerciale, provenienza, tipo di lavoro, prossimo passo con la sua data, note. Un cliente che non è in anagrafica diventa un **potenziale cliente** del progetto, con il telefono e l'email del foglio. Si importano in corso: accettati e rifiutati si chiudono dalla scheda. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="trattative-previsione"></a>Previsione

- **Per mese di chiusura**: i progetti in corso nei prossimi sei mesi (più quelli in ritardo, quelli più avanti e quelli senza data), con il valore e il **pesato**, cioè quanto ci si può ragionevolmente aspettare.
- **Per fase**, **Accettati e rifiutati** negli ultimi 12 mesi (tasso di accettazione per numero e per valore, giorni medi per chiudere), **Perché si rifiutano** e **Da dove arrivano** (provenienze con in corso, accettati, rifiutati e il valore accettato).
- Nella Home, a chi gestisce i preventivi, il riquadro **Progetti** mostra il pesato di quelli in corso.

---

[← Incassi e pagamenti](incassi-pagamenti.md) · [Indice](README.md) · [Preventivi →](preventivi.md)
