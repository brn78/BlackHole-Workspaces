[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="magazzino"></a>Magazzino

**Magazzino → Magazzino** tiene la merce dei **magazzini** dell'azienda e dei **furgoni**: quanta ce n'è, dove, quanto vale, da dove è arrivata e dove è andata. La merce sono le voci **materiali** del [listino](listino.md): non c'è un'anagrafica degli articoli a parte. Ogni carico, scarico o spostamento è una **registrazione** numerata per anno, con la sua [causale](#magazzino-causali); le giacenze, il costo medio e le matricole si calcolano da sole dalle registrazioni. In alto **Nuovo movimento**, **Nuovo magazzino**, **Cerca una matricola** e **Stampa**; le linguette sono Giacenze, Movimenti, Magazzini, Inventari e Da riordinare.

## <a id="magazzino-magazzini"></a>Magazzini e furgoni

Nella linguetta **Magazzini** (o con **Nuovo magazzino**) si creano quattro tipi di magazzino:

- **Aziendale**: un magazzino dell'azienda. **Dove si trova** si riempie con la sede dei [dati dell'azienda](impostazioni.md#impostazioni-azienda) (il pulsante accanto propone le altre sedi) e si può scrivere a mano. Uno è il **principale**: è proposto nei movimenti e da lì si riforniscono i furgoni.
- **Cliente**: la merce lasciata presso un cliente, per esempio in un **cantiere in lavorazione**. Si scelgono il cliente, la sua sede (**dove si trova** la prende da lì) e la commessa; il nome proposto è «Cantiere …». La merce ci arriva con un trasferimento dal magazzino, resta dell'azienda (conta nella giacenza e nel valore) e si scarica sulla commessa man mano che si monta; non conta tra la merce disponibile per il riordino, perché è già destinata a quel lavoro. Quando la commessa è chiusa la scheda lo segnala: la merce avanzata si riporta in magazzino e il magazzino si archivia.
- **Furgone**: la merce a bordo di un mezzo da lavoro. Si sceglie il mezzo tra quelli di [Azienda → Mezzi](mezzi.md); il tecnico che ha il mezzo in consegna è quello del furgone (se il mezzo passa a un altro, il furgone lo segue).
- **Merce da controllare**: dove va la merce rientrata aperta, usata o guasta finché non si decide se rimetterla in magazzino (con un trasferimento), renderla al fornitore o buttarla.

Ogni scheda mostra quante voci ci sono, quanto valgono (a chi vede i costi), quante sono sotto la dotazione e quanti movimenti ha avuto; **Giacenza** apre le giacenze di quel magazzino e **Rifornisci** prepara il trasferimento dal principale. Un magazzino con dei movimenti non si elimina: si **archivia**, dopo averlo svuotato.

## <a id="magazzino-giacenze"></a>Giacenze

L'elenco delle voci a magazzino con la quantità di ogni magazzino (fino a cinque colonne, poi il totale), la scorta minima, il costo medio, il valore e il giorno dell'ultimo movimento. Si filtra per magazzino (che mostra anche la sua dotazione) e con **Sotto scorta**, **A zero o sotto**, **Con matricola**; si cerca per codice, descrizione, marca o codice a barre, anche con (Leggi codice) accanto al filtro. Un clic apre la **scheda di magazzino** della voce:

- **Giacenze**: quanto c'è in ogni magazzino, con la dotazione e l'ubicazione, il costo medio e il valore.
- **Movimenti**: tutte le registrazioni della voce, con il segno, il costo e le matricole; un clic apre la registrazione.
- **Matricole**: dove si trova ogni pezzo, o a quale cliente e impianto è andato.
- **Consumi e acquisti**: le uscite mese per mese dell'ultimo anno e, a chi vede i costi, gli acquisti per fornitore (vedi [Costo medio e prezzi d'acquisto](#magazzino-costo)).
- **Impostazioni** (a chi gestisce il magazzino): **A magazzino**, **Con la matricola**, scorta minima, quantità da riordinare, giorni per averla e, per ogni magazzino, la **dotazione** minima e massima e l'**ubicazione** (vedi [Dove sta la merce](#magazzino-ubicazione)).

Una voce diventa «a magazzino» da sola al primo movimento; dal [Listino](listino.md), nel menu di una riga (tasto destro o ⋯), **Magazzino** apre la sua scheda di magazzino. Una voce con dei movimenti non si elimina dal listino: si toglie dal listino, così resta la sua storia.

## <a id="magazzino-ubicazione"></a>Dove sta la merce: corridoio, scaffale, ripiano e posto

Dalla 1.107.0 ogni voce ha, per ogni magazzino o furgone, la sua **ubicazione**: **Corridoio**, **Scaffale**, **Ripiano** e **Posto** (il cassetto, il contenitore, la cassetta), più una **Nota** libera («in alto», «cassetta rossa»). Si scrive nella scheda di magazzino della voce, linguetta **Impostazioni**, nel riquadro di ogni magazzino, accanto alla dotazione minima e massima; basta quello che serve (in un furgone magari solo il posto). Le lettere si scrivono in maiuscolo da sole e ogni campo propone i valori già usati, prima quelli dello stesso magazzino, così le ubicazioni restano scritte tutte allo stesso modo. Quello che prima era scritto nel campo Ubicazione resta come nota.

Dove si vede: nelle **Giacenze**, quando guardi un magazzino (o ce n'è uno solo), la colonna **Ubicazione** («Corr. A · Scaff. 3 · Rip. 2 · Posto 5»), che si ordina nell'ordine del giro del magazzino, con i numeri come numeri (lo scaffale 2 prima del 10) e le voci senza ubicazione in fondo; la ricerca trova anche l'ubicazione. Nei **movimenti**, sotto ogni riga e nella ricerca della voce, dove sta nel magazzino scelto: chi scarica sa dove andare a prenderla, chi carica dove metterla. Negli **inventari** le righe e il foglio da stampare seguono lo stesso giro. In **Da rifornire** c'è dove prendere la voce nel magazzino principale.

## <a id="magazzino-movimenti"></a>Registrare un movimento

**Nuovo movimento** apre il pannello a destra: si sceglie la **causale**, la **data** (non nel futuro) e il **magazzino** (nei trasferimenti anche quello di arrivo). Secondo la causale compaiono il **fornitore** o il **cliente** (dall'anagrafica, oppure scritto), il **riferimento** del documento (per esempio «DDT 123 del 10/10/2026»), la **richiesta di assistenza**, la **commessa** e l'**impianto**. Le righe si aggiungono cercando la voce (codice, descrizione, marca, codice del produttore o del fornitore) o leggendo il codice a barre con il lettore o la fotocamera: il codice della confezione mette già la quantità della confezione. Accanto a ogni voce c'è quanto ce n'è nel magazzino scelto. Nei carichi con il costo, a chi vede i costi del listino, si scrive il **costo unitario** (proposto dal listino o dal costo medio) e in fondo compare il valore.

Se un movimento porta una giacenza sotto zero (manca un carico o un trasferimento) la piattaforma lo dice, voce per voce, e registra solo confermando. La linguetta **Movimenti** elenca le registrazioni per periodo, magazzino e causale; un clic apre la registrazione per **correggerla**, **eliminarla** (le giacenze tornano come prima) o **stamparla**, per esempio da consegnare con la merce. Ogni registrazione finisce nel [registro attività](registro.md).

## <a id="magazzino-da-documento"></a>Carico da un documento (DDT o fattura)

Dalla 1.100.0, con l'[assistente](assistente-ai.md) attivo per le analisi, **Da un documento** (in alto nella pagina del magazzino) prepara il carico dalla **scansione** (PDF o foto) o dal **PDF** del documento del fornitore:

1. Scegli il file, trascinalo nel riquadro oppure incolla con <kbd>Ctrl</kbd>+<kbd>V</kbd> una scansione copiata. I PDF con il testo si leggono subito; le scansioni e le foto le legge il server con il [riconoscimento del testo](documenti.md#documenti-ocr) (circa un secondo per pagina, fino a 12 pagine).
2. L'assistente riconosce se è un **DDT**, una **fattura** o una conferma d'ordine, il **fornitore**, il numero, la data, gli ordini citati e le **righe** (codice, descrizione, quantità, unità, prezzo e sconto se ci sono).
3. La piattaforma cerca il fornitore in anagrafica (partita IVA, codice fiscale, nome), le righe dei suoi **ordini aperti** che il documento evade (codice del fornitore o descrizione simile, con quanto manca da ricevere) e, per le altre, la **voce del listino** dal codice del fornitore, dal codice a barre, dal codice del produttore o dal nostro. Una voce trovata solo per la descrizione simile è segnata *da controllare*.
4. Controlli la proposta: spunti le righe da caricare, correggi le quantità, per le righe senza voce cerchi la voce nel listino (**Cambia** per sceglierne un'altra). **Prepara il carico** apre il movimento **Acquisto** già compilato (fornitore, riferimento «DDT n. … del …», righe con il costo e l'ordine evaso, nelle note le righe non caricate): lo registri come sempre. Niente si registra da solo.

Una fattura si carica allo stesso modo; la fattura elettronica (XML) resta quella che arriva in [Fatture ricevute](fatture-fornitori.md). Il testo va all'assistente configurato (se è un servizio esterno, esce dall'azienda) e non si conserva. Le voci con la matricola chiedono le matricole nel carico.

## <a id="magazzino-causali"></a>Le causali

| Entrate | **Giacenza iniziale** (la merce che c'è quando si comincia, con il suo costo) · **Carico da fornitore** (con il DDT e il costo) · **Rientro da cantiere o intervento** (il materiale non usato che torna) · **Reso dal cliente** · **Rientro dalla riparazione** · **Rettifica in aumento** |
| --- | --- |
| Uscite | **Scarico per intervento** (con la richiesta di assistenza) · **Scarico per commessa o impianto** · **Vendita o consegna al cliente** · **Reso al fornitore** · **Invio in riparazione** · **Uso interno** · **Guasto o rottamazione** · **Rettifica in diminuzione** |
| Tra magazzini | **Trasferimento**: per esempio dal magazzino al furgone, o dalla merce da controllare al magazzino |
| Inventari | **Rettifica d'inventario**: la crea da sola la chiusura di un inventario |

> [!TIP]
> **Merce rientrata spacchettata.** Il materiale che torna dal cantiere aperto o di cui non si è sicuri si registra con **Rientro da cantiere o intervento** nel magazzino *Merce da controllare*; controllato, un trasferimento lo rimette in magazzino, oppure un reso al fornitore o un guasto lo fanno uscire.

## <a id="magazzino-furgoni"></a>Furgoni, dotazione e rifornimento

Ogni furgone ha la sua **dotazione**: per ogni voce, quanto deve esserci almeno e al massimo (si scrive nelle impostazioni della scheda di magazzino della voce). Quando un furgone scende sotto il minimo di qualche voce compare in **Da riordinare → Da rifornire** e nella sua scheda: **Rifornisci** prepara il trasferimento dal magazzino principale fino al massimo, da controllare e registrare. Il tecnico con il permesso **Il proprio furgone** vede solo il suo furgone: scarica il materiale per interventi e commesse, registra i rientri, l'uso interno e i guasti, prende la merce dal magazzino e la riporta con un trasferimento.

## <a id="magazzino-assistenza"></a>Il materiale dell'assistenza

Nel [consuntivo](assistenza.md#assistenza-consuntivo) di una richiesta di assistenza, **Scarica dal magazzino** prepara lo **scarico per intervento** con il materiale del listino non ancora scaricato, dal furgone di chi lo apre (se ne ha uno) o dal magazzino principale. Ogni riga resta legata alla sua riga del consuntivo, così lo stesso materiale non si scarica due volte; il costo dello scarico è il costo medio del momento. Le matricole uscite risultano presso il cliente e l'impianto della richiesta. Lo stesso si fa dal movimento, scegliendo la richiesta: **Prendi il materiale del consuntivo**.

## <a id="magazzino-matricole"></a>Matricole

Per gli articoli che lo richiedono (telecamere, centrali, videoregistratori…) si attiva **Con la matricola** nelle impostazioni della voce, quando la sua giacenza è a zero. Da allora ogni movimento vuole una matricola per pezzo: si scrivono una per riga, si leggono con **Leggi matricola** e, nelle uscite, si scelgono con **Scegli tra quelle in magazzino**; la quantità è il numero delle matricole. Una matricola non entra due volte e non esce da un magazzino in cui non c'è. **Cerca una matricola** dice dov'è un pezzo, oppure quando è uscito, verso quale cliente, impianto, richiesta o commessa, e da quale fornitore era arrivato.

## <a id="magazzino-inventari"></a>Inventari

Nella linguetta **Inventari**, chi gestisce il magazzino apre un **Nuovo inventario**: magazzino, data, eventualmente una categoria (con le sue sottocategorie, per contare un pezzo alla volta) e se farlo **alla cieca** (chi conta non vede la quantità attesa). Si conta scrivendo le quantità oppure leggendo i codici: ogni lettura trova la voce e aggiunge uno (o la confezione); una voce trovata sullo scaffale e non in elenco si aggiunge da sola. Si salva quando si vuole e si conta anche in più persone; **Foglio da stampare** prepara l'elenco per contare a mano, in ordine di ubicazione. **Chiudi l'inventario** trasforma le differenze in una **rettifica d'inventario**: le voci non contate restano come sono, oppure vanno a zero se si sceglie l'inventario completo. Le voci con la matricola non si rettificano: si sistemano con un movimento con le matricole, e la chiusura le elenca.

## <a id="magazzino-riordino"></a>Da riordinare

La linguetta **Da riordinare** elenca le voci a magazzino sotto la **scorta minima** (contando magazzini e furgoni, non la merce da controllare né quella presso i clienti), finite mentre si consumano, o che finiranno prima dei **giorni per averle** al consumo medio degli ultimi 90 giorni. Per ognuna: giacenza, consumo al mese, giorni di copertura, la **quantità proposta** (fino alla scorta minima più il consumo nei giorni per averla, almeno la quantità da riordinare, arrotondata alla confezione), il fornitore e l'ultimo costo. Si stampa, si esporta in Excel e, con il permesso degli acquisti, **Crea gli ordini** prepara gli [ordini ai fornitori](acquisti.md#acquisti-proposte) in bozza. Sotto, **Da rifornire**: i magazzini e i furgoni sotto la dotazione.

## <a id="magazzino-costo"></a>Costo medio e prezzi d'acquisto

Ogni voce ha il suo **costo medio ponderato**: i carichi con il costo (giacenza iniziale, carico da fornitore, rettifica in aumento) lo aggiornano, tutte le uscite valgono il costo medio del momento. Correggendo o eliminando un carico, costo medio e valore delle uscite si ricalcolano. Nella scheda di magazzino, **Consumi e acquisti** mostra per ogni fornitore quante volte e quanto si è comprato, l'**ultimo prezzo**, il **medio**, il minimo e il massimo: un ultimo prezzo sopra il medio è evidenziato. Costi e valori li vede solo chi ha i [costi del listino](listino.md#listino-permessi).

## <a id="magazzino-importa"></a>Importare ed esportare le giacenze

**Esporta** scarica le giacenze in **Excel** o **CSV**: codice, descrizione, unità, marca, codice a barre, una colonna per ogni magazzino e furgone, il totale e la scorta minima. **Importa** porta le quantità da un foglio (codice o codice a barre e quantità, il costo se serve) in un magazzino scelto, in due modi:

- **Giacenza iniziale**: un carico solo con le quantità del foglio, da fare all'inizio (si somma a quello che c'è già), con il costo unitario per chi vede i costi.
- **Inventario** (a chi gestisce il magazzino): le quantità contate vanno nell'inventario aperto del magazzino (o in uno nuovo). Lo controlli e lo chiudi dalla linguetta **Inventari**, che fa la rettifica delle differenze.

Gli articoli con la matricola si caricano a mano, una matricola per pezzo. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="magazzino-permessi"></a>Permessi

| Vedere il magazzino | Giacenze di tutti i magazzini e furgoni, movimenti, matricole, inventari e voci da riordinare (valori e costi solo con i costi del listino). |
| --- | --- |
| Registrare i movimenti | Carichi, scarichi, trasferimenti, rientri e resi in tutti i magazzini, anche dal consuntivo dell'assistenza; contare negli inventari; correggere ed eliminare le proprie registrazioni. |
| Il proprio furgone | Solo il furgone del mezzo in consegna: vederne la merce, scaricarla per interventi e commesse, registrare rientri, uso interno e guasti, prendere e riportare la merce con i trasferimenti. |
| Gestire il magazzino | Magazzini e furgoni, impostazioni delle voci (matricola, scorte, dotazioni), inventari, correzione ed eliminazione di ogni registrazione. |

---

[← Listini fornitori](listini-fornitori.md) · [Indice](README.md) · [Ordini fornitori →](acquisti.md)
