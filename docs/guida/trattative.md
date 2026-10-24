[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="trattative"></a>Trattative

**Progettazione → Trattative** (dalla 1.117.0) segue i **lavori da prendere** prima e durante i preventivi: chi ha chiesto, che lavoro, quanto vale, a che punto è, quanto è probabile prenderlo, quando si pensa di chiudere e **che cosa fare dopo**. Così nessuna richiesta si perde tra una telefonata e l'altra e si vede in anticipo quanto lavoro sta per arrivare. La pagina compare a chi vede i [preventivi](preventivi.md), con gli stessi permessi: chi li compila crea e cambia le trattative, chi li gestisce può anche eliminarle. Quelle dei contatti privati le vede solo il proprietario.

## <a id="trattative-fasi"></a>Kanban e fasi

- Nella linguetta **In corso** ogni trattativa è una scheda nella colonna della sua fase: **Primo contatto**, **Sopralluogo**, **Preventivo** (in preparazione o inviato), **Trattativa** (si discute il prezzo o i tempi). Si **trascina** da una colonna all'altra; trascinandola, sotto compaiono **Vinta** e **Persa**. In testa a ogni colonna il valore e il valore pesato.
- Ogni fase propone la sua **probabilità** (10, 30, 50, 70%): cambiando fase la probabilità la segue, a meno che tu non l'abbia cambiata a mano.
- La scheda ha il **prossimo passo** (rosso quando il giorno è arrivato) e, con il bordo rosso, quelle con la chiusura prevista già passata. **Elenco** mostra le stesse trattative in una tabella con i totali.
- In alto: il valore in corso, il **pesato** (valore × probabilità), quanto si pensa di chiudere entro il mese e quante hanno il prossimo passo da fare (un clic le filtra). I filtri **Mie** e **Da fare** e il commerciale valgono anche per la previsione.

## <a id="trattative-scheda"></a>La scheda della trattativa

- **Il lavoro** in poche parole e il **cliente**. Se non è ancora in anagrafica, **Non è ancora in anagrafica** chiede solo nome, telefono ed email; **Crea la scheda del cliente** lo mette tra i potenziali clienti e lo collega. Un preventivo per la trattativa lo collega comunque.
- **Valore stimato** (l'imponibile che si pensa di fatturare), **probabilità**, **chiusura prevista**, **commerciale** (di base chi la crea), **provenienza** (passaparola, sito, fiera…) e **tipo di lavoro**, con i suggerimenti di quelli già scritti.
- In cima, per una trattativa in corso: **Cliente sentito**, **Persa** e **Vinta**; per una chiusa, **Riapri**. Sotto, lo **storico**: fasi, contatti, preventivi, chiusura.

## <a id="trattative-da-testo"></a>Una trattativa da un testo

Dalla 1.123.0, con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (in alto nella pagina Trattative) apre un pannello dove incollare la **richiesta del cliente**: un'email, un messaggio, il modulo del sito o gli appunti di una telefonata. L'assistente propone il **lavoro**, chi lo chiede, il **tipo di lavoro**, la provenienza, il **valore** se c'è un budget, la fase (sopralluogo se lo chiede, altrimenti primo contatto o preventivo), il **prossimo passo** e le note con la richiesta riassunta. Con **Da un file** il testo si legge anche da un PDF o da una scansione. **Proponi i dati** chiede all'assistente i dati e la piattaforma cerca il **cliente** tra quelli che vedi (partita IVA, email anche dei referenti, telefono, nome, poi un nome simile da controllare) e, con il cliente, il suo **impianto** dalle parole del testo. Si apre la scheda nuova **già compilata**, con in cima la nota dell'assistente: controlla, correggi e salva come sempre. Niente si salva da solo e il testo non si conserva. Se chi chiede non è in anagrafica, la scheda è già su *Non è ancora in anagrafica* con nome, telefono ed email.

## <a id="trattative-prossimo-passo"></a>Prossimo passo e cliente sentito

Il **prossimo passo** dice che cosa fare e quando («fissare il sopralluogo», «mandare il preventivo rivisto»). Va nelle [Scadenze](scadenze.md) (area «Preventivi e trattative») e nel [calendario del telefono](profilo.md#profilo-calendario) di chi lo abbona; il giorno prima e il giorno stesso arriva il promemoria al commerciale (senza commerciale, a chi gestisce i preventivi). **Cliente sentito** scrive nello storico come vi siete sentiti e che cosa vi siete detti e fissa il passo successivo.

## <a id="trattative-preventivi"></a>I preventivi della trattativa

- **Nuovo preventivo** nella scheda prepara il preventivo per quel cliente, con l'oggetto della trattativa. Una trattativa nelle prime fasi passa a **Preventivo**.
- Quando il preventivo è **inviato**, il valore della trattativa diventa il suo imponibile; quando è **accettato**, la trattativa si chiude **vinta** da sola. Un rifiuto resta nello storico: si può fare una revisione (resta collegata) oppure chiudere la trattativa persa.
- **Collega** aggancia un preventivo già fatto per lo stesso cliente; l'icona accanto lo toglie. Il preventivo mostra in testata la sua trattativa, e la scheda del cliente, nella linguetta Preventivi, le sue trattative in corso.

## <a id="trattative-chiusura"></a>Vinte e perse

**Vinta** la porta al 100%, **Persa** allo 0% con il **motivo** (prezzo, concorrente, rinviato, nessuna risposta…): servono a capire dove si perde. Le linguette **Vinte** e **Perse** le elencano con il giorno e l'esito; **Riapri** le rimette nel kanban. Eliminata, una trattativa va nel [cestino](cestino.md) con il suo storico; i preventivi restano.

## <a id="trattative-importa"></a>Importare ed esportare

**Esporta** scarica le trattative in **Excel**, **CSV** o come **calendario** (i prossimi passi e le chiusure previste di quelle in corso). **Importa** (a chi le gestisce) le porta da un foglio: lavoro, cliente, telefono ed email, fase, probabilità, valore, chiusura prevista, commerciale, provenienza, tipo di lavoro, prossimo passo con la sua data, note. Un cliente che non è in anagrafica diventa un **potenziale cliente** della trattativa, con il telefono e l'email del foglio. Si importano in corso: vinte e perse si chiudono dalla scheda. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="trattative-previsione"></a>Previsione

- **Per mese di chiusura**: le trattative in corso nei prossimi sei mesi (più quelle in ritardo, quelle più avanti e quelle senza data), con il valore e il **pesato**, cioè quanto ci si può ragionevolmente aspettare.
- **Per fase**, **Vinte e perse** negli ultimi 12 mesi (tasso di vittoria per numero e per valore, giorni medi per chiudere), **Perché si perdono** e **Da dove arrivano** (provenienze con in corso, vinte, perse e il vinto).
- Nella Home, a chi gestisce i preventivi, il riquadro **Trattative** mostra il pesato di quelle in corso.

---

[← Fatture ricevute](fatture-fornitori.md) · [Indice](README.md) · [Preventivi →](preventivi.md)
