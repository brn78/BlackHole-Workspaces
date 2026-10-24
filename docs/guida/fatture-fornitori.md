[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="fatture-fornitori"></a>Fatture ricevute

**Amministrazione → Fatturazione → Ricevute** raccoglie le fatture elettroniche ricevute: si controllano con gli ordini e con la merce arrivata, si pagano e restano tutte in un posto, con il file originale. Dalla 1.162.0 è una linguetta della [Fatturazione](vendite.md), con la stessa intestazione delle emesse. Sotto le linguette i filtri Da controllare, Contestate, Da pagare, Scadute, Note di credito, Tutte e, in fondo, **Per fornitore** (quante fatture, l'imponibile dell'anno, quanto resta da pagare, le note di credito ancora da usare). Le rate da pagare stanno in [Incassi e pagamenti](incassi-pagamenti.md).

## <a id="fatture-fornitori-importa"></a>Importare le fatture

**Importa** accetta i file come li scarichi dal portale *Fatture e Corrispettivi* o dall'intermediario: l'**XML**, l'XML **firmato .p7m** e gli **ZIP**, anche con cartelle e altri ZIP dentro (come lo storico esportato da un portale). Si trascinano nel riquadro o si scelgono, anche tanti insieme.

- Il **fornitore** si riconosce dalla partita IVA o dal codice fiscale. Se in anagrafica c'è come cliente, diventa anche fornitore; se non c'è, si aggiunge da solo con i dati della fattura (nome, partita IVA, sede, email). Un dato che l'anagrafica non accetta finisce nelle note della scheda, con l'etichetta *Da controllare*.
- Restano fuori, con il motivo: le fatture **già importate** (anche se il file ha un altro nome), le **ricevute** dello SDI, le fatture **emesse dalla tua azienda**, quelle **intestate a un'altra azienda**, le integrazioni e autofatture (TD16–TD27: sono documenti dell'azienda, li tratterà la contabilità) e quelle non in euro. Gli altri file dello ZIP (PDF, testi) si contano soltanto.
- Un file con più fatture (lotto) dà una fattura per documento. Il file dei metadati dello SDI, se c'è nello ZIP, dà l'**identificativo SDI**.
- **Data di ricezione**: conta per l'IVA. Vuota = la data del documento; si corregge poi nella fattura.
- **Storico già controllato e pagato** (chi paga le fatture): per gli anni passati. Le fatture entrano già controllate, con le rate pagate alla scadenza, senza abbinarle agli ordini.
- **Dalla PEC**: se la PEC delle vendite è l'indirizzo con cui l'azienda riceve le fatture, nelle impostazioni delle vendite **Importa anche le fatture dei fornitori** le fa entrare da sole quando il server legge la casella, con la data del messaggio come data di ricezione.

## <a id="fatture-fornitori-controllo"></a>Il controllo

Una fattura si apre nel pannello a destra. In testa i **controlli**, in rosso quelli da guardare prima di pagare:

- **IBAN mai usato** con quel fornitore (né nelle fatture precedenti né nella sua scheda): prima di pagare verificalo al telefono, con un numero che già conosci. È il modo in cui arriva la truffa del cambio di IBAN.
- Riga con il **prezzo più alto dell'ordine** oltre la soglia degli acquisti (la stessa dei prezzi da verificare).
- Riga con **più merce fatturata di quella arrivata** o di quella ordinata (contano anche le altre fatture e le note di credito sulla stessa riga dell'ordine).
- Importi che non tornano: righe e riepilogo IVA (oltre un euro, la tolleranza dello SDI), IVA calcolata, totale, rate; possibile **doppione** (stesso fornitore, stesso giorno, stesso totale, numero diverso).
- Da sapere: righe senza ordine, inversione contabile, scissione dei pagamenti, ritenuta d'acconto (si paga il netto, la ritenuta va con l'F24 entro il 16 del mese dopo), nota di credito senza la sua fattura.

Le **righe** si abbinano da sole alle righe degli ordini dello stesso fornitore: prima gli ordini e i DDT scritti nella fattura (il DDT trova l'arrivo con quel riferimento), altrimenti gli ordini degli ultimi 18 mesi; conta il codice (del fornitore, del produttore, a barre), poi la descrizione e la quantità. Accanto a ogni riga: l'ordine, quanti ordinati, arrivati e fatturati e il prezzo dell'ordine (a chi vede gli acquisti). Con **⋯** sulla riga: **Scegli la riga dell'ordine**, **Senza ordine** (trasporto, spese, servizi) o di nuovo l'abbinamento automatico. **Azioni → Rifai l'abbinamento** lo ripete per tutta la fattura (quelle scelte a mano restano).

Poi **Controllata**, oppure **Contesta al fornitore** con il motivo (va nelle note; la fattura contestata non va nei promemoria dei pagamenti). Si scelgono anche la **commessa** a cui va il costo, la data di ricezione e le note interne. In fondo il file com'è arrivato, l'XML senza firma e gli allegati (di solito il PDF di cortesia); **Stampa** (nel menu **Azioni**) ne fa una copia leggibile, con il fornitore in testa (è il suo documento: niente modello di stampa) e il riporto tra i fogli.

## <a id="fatture-fornitori-pagamenti"></a>Pagamenti e note di credito

- Le **rate** vengono dalla fattura; se il fornitore non le ha scritte, una sola alla data del documento. **Cambia le rate** (finché non ci sono pagamenti) le rifà: date, importi, modalità, IBAN.
- **Paga** (dalla fattura o da [Incassi e pagamenti](incassi-pagamenti.md)) registra un pagamento, anche in parte, con la data e il modo (bonifico, contanti, carta, assegno, altro); **Togli** lo annulla.
- Una **nota di credito** si usa per pagare una fattura dello stesso fornitore: **Azioni → Usa per pagare una fattura**, tutto o una parte; tutte e due risultano pagate per quell'importo (compensazione). Togliendo la compensazione da una parte sparisce anche dall'altra.
- Le rate scadute e quelle della settimana vanno nello [Scadenzario](scadenze.md) (area *Pagamenti*) e nei promemoria di chi paga le fatture.
- In [Incassi e pagamenti → Prossime settimane](incassi-pagamenti.md) quanto resta da pagare (e da incassare) già scaduto e in ognuna delle prossime otto settimane.

## <a id="fatture-fornitori-permessi"></a>Permessi

| Vedere le fatture dei fornitori | Riservato: le fatture con righe, importi e IBAN, i controlli, le rate e i pagamenti. |
| --- | --- |
| Importare e controllare le fatture dei fornitori | Importare i file, abbinare le righe agli ordini (per scegliere a mano serve anche *Vedere gli acquisti*), segnarle controllate o contestate, data di ricezione, commessa e note. |
| Pagare le fatture dei fornitori | Pagamenti, rate, compensazioni, lo storico già pagato, eliminare una fattura importata per sbaglio (si può reimportare dal file). |

Le policy proposte: *Ufficio* importa e controlla, *Amministrazione* paga.

---

[← Fatturazione](vendite.md) · [Indice](README.md) · [Incassi e pagamenti →](incassi-pagamenti.md)
