[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="contabilita"></a>Contabilità

**Amministrazione → Contabilità** tiene la contabilità in **partita doppia** senza doverla scrivere a mano: ogni fattura emessa, ogni fattura di un fornitore, ogni incasso e ogni pagamento diventa da solo una **registrazione** con i conti giusti, dal giorno scelto nelle impostazioni. Si aggiungono a mano solo le cose che non hanno un documento (versamenti con l'F24, stipendi, spese bancarie). Il commercialista trova tutto pronto: registri IVA, liquidazioni, mastrini, bilancio di verifica, la prima nota da esportare e, a fine anno, le scritture di assestamento proposte, la chiusura dei conti e il bilancio nello schema CEE. L'[Andamento](#contabilita-andamento) mette in grafico ricavi, costi, risultato e IVA.

> [!TIP]
> **In due parole.** Ogni registrazione ha uno o più conti in **dare** e uno o più in **avere**, e i due totali sono sempre uguali. Esempio: una fattura di 1.220 € a un cliente mette 1.220 € in dare su *Crediti verso clienti* (il cliente ci deve dei soldi) e in avere 1.000 € su *Ricavi* e 220 € su *IVA sulle vendite* (l'IVA che dovremo versare). Quando il cliente paga: 1.220 € in dare sulla *Banca* e in avere su *Crediti verso clienti*, che torna a zero.

## <a id="contabilita-avvio"></a>Per cominciare

1. **Il piano dei conti**: **Crea il piano dei conti proposto** mette i conti di una piccola impresa di impianti e servizi (crediti verso clienti, debiti verso fornitori, banca, IVA, merci, servizi, personale, ricavi…), ognuno con la sua voce del bilancio e, dove serve, il **ruolo** che usano le registrazioni automatiche. Poi si adatta con il commercialista (linguetta **Piano dei conti**).
2. **Impostazioni**: il giorno da cui tenere la contabilità qui (di solito l'inizio di un anno o di un trimestre: i documenti di prima restano fuori), la liquidazione IVA **mensile** o **trimestrale**, il mese di inizio dell'esercizio e la forma del bilancio. Con **Contabilità attiva** partono le registrazioni.
3. Quando si registra un incasso o un pagamento, sotto c'è **Su** / **Da**: il conto di banca o la cassa (proposta la banca con quel ruolo).

## <a id="contabilita-prima-nota"></a>La prima nota

Tutte le registrazioni del periodo scelto (questo mese, il mese scorso, il trimestre, l'anno o dal giorno al giorno), in ordine di data, con i conti in dare e in avere. Un clic apre la registrazione: per quelle dei documenti c'è il collegamento al documento, per le fatture dei fornitori **Conti delle righe**.

- **Fattura emessa**: clienti in dare per il totale, ricavi (vendita di merci per le voci di materiale, lavori e prestazioni per il resto) e IVA sulle vendite in avere. Con la **scissione dei pagamenti** al cliente resta solo l'imponibile: l'IVA va nel registro ma la versa il cliente. La **nota di credito** è tutto al contrario.
- **Fattura di un fornitore**, alla data di ricezione: i costi in dare (merci se la riga viene da un ordine o è un materiale del listino, altri servizi per il resto), l'IVA detraibile, il fornitore in avere. La **cassa previdenziale** va con il costo; la **ritenuta d'acconto** passa dal fornitore all'*Erario c/ritenute da versare*; il **bollo** va nell'imposta di bollo. Con l'**inversione contabile** (reverse charge) l'IVA si calcola qui (22%, si cambia) e va in tutti e due i registri: si detrae e si versa insieme.
- **Conti delle righe**: per ogni riga il conto di costo (carburanti, consulenze, noleggi…) e quanta IVA si detrae (per esempio 40% per le auto aziendali, 0% per le spese di rappresentanza; la parte che non si detrae va in *IVA indetraibile*). La registrazione si rifà con lo stesso numero.
- **Incassi e pagamenti**: banca o cassa contro clienti o fornitori. Le compensazioni con le note di credito non muovono la banca e non si registrano.
- Le registrazioni dei documenti seguono i documenti: se una fattura cambia o torna in bozza, la sua registrazione cambia o sparisce, finché il periodo non è chiuso. Dopo, una fattura del periodo liquidato non torna in bozza e una fattura di un fornitore non si elimina: si corregge con una nota di credito.

**Scrittura libera** (chi può registrare in contabilità): data, descrizione, documento e le righe con conto, dare o avere (sui conti di clienti e fornitori anche il nome). Sotto le righe si vede se quadra. I **modelli** riempiono i conti dei casi di tutti i giorni: versamento IVA e ritenute con l'F24, contributi, stipendi e loro pagamento, spese bancarie, imposta di bollo, prelievi e versamenti di contanti, la destinazione del risultato dopo l'approvazione del bilancio. Si modificano e si eliminano finché l'esercizio è aperto.

## <a id="contabilita-iva"></a>Registri IVA e liquidazioni

- **Registri IVA**: vendite e acquisti del periodo, un documento per riga con l'imponibile e l'imposta per aliquota (le scissioni e le inversioni contabili segnate), il riepilogo per aliquota; negli acquisti il **protocollo**, provvisorio finché il periodo non è liquidato, e la parte detraibile.
- **Liquidazioni IVA**, per ogni mese o trimestre dalla data di inizio: IVA sulle vendite (non quella in scissione) meno IVA detraibile sugli acquisti ricevuti nel periodo, più il **riporto** del periodo prima (il credito, o un debito sotto i 25,82 € che non si versa); per i trimestrali l'**1% di interessi** sul debito. La scadenza del versamento: il 16 del mese dopo (mensili); 16 maggio, 20 agosto, 16 novembre e 16 marzo (trimestrali).
- **Chiudi** (chi gestisce la contabilità, un periodo finito, dopo quelli prima): fissa gli importi e il protocollo degli acquisti, registra il **giroconto** dell'IVA sull'*Erario c/IVA* e blocca le registrazioni con l'IVA del periodo. Nell'ultimo periodo dell'anno si toglie l'**acconto** di dicembre. **Versata** registra il pagamento con l'F24 dalla banca scelta. L'ultima liquidazione chiusa (non versata) si riapre.

## <a id="contabilita-mastrini"></a>Mastrini e bilancio di verifica

- **Mastrini**: i movimenti di un conto nel periodo con il saldo iniziale e il saldo progressivo; sui conti di clienti e fornitori anche di uno solo (**partitario**: quanto ci deve un cliente, quanto dobbiamo a un fornitore). Un clic su un movimento apre la registrazione.
- **Bilancio di verifica**: per ogni conto dare, avere e saldo (i conti patrimoniali fino alla data, quelli economici nel periodo), raggruppati per natura e per mastro, con i totali; in testa ricavi, costi e **utile o perdita** del periodo e il controllo dare = avere; sotto i saldi di clienti e fornitori. Se il periodo comincia a metà esercizio, costi e ricavi di prima sono una riga a parte (**utile** o **perdita prima del periodo**): il loro effetto è già nei conti patrimoniali e così dare e avere quadrano. Un clic su un conto apre il suo mastrino.
- **Esporta** scarica la prima nota del periodo in CSV (si apre con Excel) per il commercialista; **Stampa** stampa la linguetta che stai guardando.

## <a id="contabilita-cee"></a>Bilancio CEE

Lo **stato patrimoniale** alla fine dell'esercizio (attivo e passivo) e il **conto economico** nello schema del codice civile (articoli 2424 e 2425), nella forma scelta nelle impostazioni: **ordinaria** con tutte le voci, **abbreviata** o **delle micro-imprese** con le voci raggruppate (immobilizzazioni, crediti, debiti, disponibilità liquide al netto dei fondi). Accanto c'è l'esercizio prima. I saldi vengono dalla **voce del bilancio** di ogni conto; i conti con il saldo dalla parte opposta passano nell'altra sezione (l'*Erario c/IVA* a credito tra i crediti tributari, la banca scoperta tra i debiti verso banche, i clienti in avere tra gli acconti). Nel patrimonio netto la voce **A.IX** è il risultato del conto economico; il risultato dell'esercizio prima non ancora destinato si vede tra gli **utili (perdite) portati a nuovo**. In testa il controllo **attivo = passivo**. **Stampa** lo stampa con le due colonne.

## <a id="contabilita-cespiti"></a>Cespiti

Il **registro dei cespiti**: furgoni, attrezzature, computer, mobili, software. Per ognuno il costo, il giorno in cui entra in funzione, l'**aliquota** annua e se nel primo anno si ammortizza la **metà** (la regola più usata); il conto del bene e quello del fondo di ammortamento (scegliendo la categoria si propongono l'aliquota più comune e i conti, scegliendo il conto del bene si propone il suo fondo). Per i beni comprati prima di tenere la contabilità qui si scrive il **fondo già accumulato**; un bene venduto o rottamato ha il giorno della **dismissione** e dall'esercizio dopo non si ammortizza più (la plusvalenza o minusvalenza con una scrittura libera). Si può collegare al mezzo o all'attrezzatura del gestionale.

- L'elenco mostra per l'esercizio scelto la **quota**, il **fondo** (compresa la quota) e quanto resta **da ammortizzare**; sotto l'editor il piano in breve (quota annua e in quanti esercizi).
- **Dalle fatture**: le righe delle fatture dei fornitori registrate su un conto di immobilizzazioni e non ancora nel registro; **Crea** apre il cespite già compilato (descrizione, importo, data, conto).
- Le aliquote proposte sono i coefficienti più comuni: le conferma il commercialista.

## <a id="contabilita-fine-anno"></a>Fine anno: assestamento, chiusura e riapertura

La linguetta **Fine anno** propone le scritture di assestamento dell'esercizio scelto (di solito quello appena finito), una per riquadro, all'ultimo giorno dell'esercizio. Ogni riquadro mostra l'importo, il **dettaglio** da cui viene e se è già registrato; **Registra** la scrive, **Rifai** la riscrive con l'importo di adesso (se i dati sono cambiati è segnata in rosso), il cestino la toglie.

1. **Ammortamenti**: le quote dei cespiti (ammortamento in dare, fondo in avere, una riga per bene).
2. **Rimanenze finali**: le quantità in magazzino alla fine dell'esercizio (dai movimenti di tutti i magazzini) al **costo medio** dei carichi fino a quel giorno; il valore si corregge se l'inventario fisico dice altro. Nella riapertura diventano le **rimanenze iniziali** dell'esercizio dopo.
3. **Fatture da emettere**: i DDT consegnati entro la fine e non ancora fatturati (il ricavo è di quest'anno).
4. **Fatture da ricevere**: la merce arrivata dagli ordini e non ancora fatturata dal fornitore, al prezzo d'ordine (il costo è di quest'anno).
5. **Ratei e risconti**: **Aggiungi** sceglie il tipo (risconto attivo, rateo passivo, risconto passivo, rateo attivo), il conto di costo o di ricavo da rettificare e l'importo, con il **calcolo per giorni**: importo totale e periodo, la quota si calcola da sola. Esempio: un'assicurazione di 1.200 € dal 1° luglio al 30 giugno ha 181 giorni nell'anno dopo, quindi un risconto attivo di 595,07 €.
6. **TFR** e **imposte** (IRES e IRAP): gli importi del consulente del lavoro e del commercialista.

Fatture da emettere e da ricevere, ratei e risconti si **stornano da soli** all'apertura dell'esercizio dopo: quando arriva la fattura vera il costo o il ricavo non si conta due volte.

**Chiudi l'esercizio** (chi gestisce la contabilità): quando l'esercizio è finito, quello prima è chiuso e le liquidazioni IVA dei suoi periodi sono chiuse. In un passo solo registra l'**epilogo** di costi e ricavi sul *Conto economico*, il **risultato** sull'*Utile (perdita) dell'esercizio*, la **chiusura** dei conti patrimoniali sullo *Stato patrimoniale finale* (clienti e fornitori uno per uno) e la **riapertura** al primo giorno dell'esercizio dopo, con le rimanenze iniziali e gli storni. Da quel momento le scritture dell'esercizio non si cambiano più; **Riapri** toglie chiusura e riapertura (se l'esercizio dopo non è chiuso). Dopo l'approvazione del bilancio la **destinazione del risultato** (a riserva o a nuovo) si registra con una scrittura libera: c'è il modello.

> [!TIP]
> Le proposte si possono registrare anche prima della fine dell'esercizio, per vedere un bilancio provvisorio: si rifanno quando i dati cambiano.

## <a id="contabilita-flussi"></a>Flussi di cassa

Quanti soldi entrano ed escono nelle prossime settimane (due, tre o sei mesi): parte dal saldo di oggi di banche e cassa (dalla contabilità, se è attiva), aggiunge le rate delle fatture emesse da incassare e toglie quelle dei fornitori da pagare e l'IVA delle liquidazioni chiuse e non versate. Le rate scadute sono nella prima settimana; un clic sulla settimana mostra le rate. In testa incassi, pagamenti, il saldo alla fine e, in rosso, da quale settimana si andrebbe sotto zero. Stipendi, F24 e spese senza fattura non ci sono: tienine conto.

## <a id="contabilita-andamento"></a>L'andamento

La linguetta **Andamento** mostra come va l'anno (si sceglie tra quello in corso e i due prima), con i numeri della prima nota senza le scritture di chiusura e di riapertura:

- in testa **ricavi**, **costi** e **risultato** da gennaio a questo mese, con la variazione rispetto agli stessi mesi dell'anno prima (in verde se va meglio: ricavi in su, costi in giù), e il **margine** sui ricavi;
- **Ricavi e costi per mese**, una coppia di colonne per mese; passandoci sopra anche il risultato del mese, quello da inizio anno e lo stesso mese dell'anno prima;
- **Risultato del mese**: in verde gli utili, in rosso le perdite;
- **Dove vanno i costi** e **Da dove vengono i ricavi**: i conti più grandi dell'anno in una barra, il resto insieme; un clic su un conto apre il suo mastrino dell'anno;
- **IVA per periodo**: per ogni liquidazione l'IVA delle vendite e quella degli acquisti, con quanto c'è da versare nell'anno.

## <a id="contabilita-conti"></a>Piano dei conti

Mastri e conti con codice, nome, **natura** (attività, passività e netto, costi, ricavi, conti tecnici), **voce del bilancio** (lo schema CEE dello stato patrimoniale e del conto economico), **ruolo** nelle registrazioni automatiche (un ruolo, un conto) e **partitario** per i conti di clienti e fornitori. Un conto usato non si elimina: si archivia. Le banche si aggiungono sotto *Disponibilità liquide* (voce C.IV.1), con l'IBAN.

## <a id="contabilita-permessi"></a>Permessi

| Vedere la contabilità | Riservato: prima nota, registri, liquidazioni, mastrini, bilancio, esportazione. |
| --- | --- |
| Registrare in contabilità | Scritture libere, conti e detraibilità delle righe delle fatture dei fornitori, cespiti, scritture di assestamento, ratei e risconti. |
| Gestire la contabilità | Impostazioni, piano dei conti e ruoli, chiusura e riapertura delle liquidazioni, versamenti, chiusura e riapertura dell'esercizio. |

Le policy proposte: *Amministrazione* gestisce fatture, incassi, banca e contabilità; *Commercialista* (per lo studio) vede contabilità, vendite, fatture dei fornitori e banca senza cambiare niente.

---

[← Banca](banca.md) · [Indice](README.md) · [Scadenze →](scadenze.md)
