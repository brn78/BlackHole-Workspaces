[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="manutenzioni"></a>Manutenzioni

**Commesse → Manutenzioni** segue le **manutenzioni periodiche degli impianti dei clienti**: per ogni [impianto](impianti.md) un **piano di manutenzione** (che cosa si fa, ogni quanto, la prossima scadenza, i controlli, il contratto), gli **interventi pianificati** come attività e i **rapporti** numerati, con l'esito e i controlli, da stampare e far firmare al cliente. Le scadenze compaiono anche nello [scadenzario](scadenze.md), con i promemoria. La pagina compare a chi può **Vedere le manutenzioni**, con le stesse regole degli impianti: quelle dei contatti privati le vede solo il proprietario (vedi [Permessi](#manutenzioni-permessi)).

## <a id="manutenzioni-pagina"></a>La pagina Manutenzioni

- **Da fare**: le manutenzioni scadute o entro il preavviso, le più urgenti prima.
- **Piano**: tutte le manutenzioni degli impianti in servizio, con la prossima scadenza.
- **Rapporti**: il registro dei rapporti, dal più recente, con il numero, il giorno, l'impianto, la manutenzione (o *intervento straordinario*), i tecnici e l'esito.

La ricerca trova impianto, cliente, manutenzione e tecnici; l'elenco dei tipi d'impianto restringe, e per i rapporti anche l'esito e l'anno. Ogni manutenzione mostra la scadenza con quanto manca, l'impianto con il cliente e la sede, ogni quanto si fa (e se il contratto è scaduto o sta per scadere), l'intervento pianificato e lo stato: **Scaduta**, **In scadenza**, **In regola**. Un clic apre la manutenzione; il tasto destro (o ⋯) **Registra il rapporto**, **Pianifica l'intervento**, apre l'attività, la manutenzione o la pagina dell'impianto, oppure la toglie dal piano. **Stampa** stampa l'elenco come lo stai guardando. **Nuova manutenzione** (per chi gestisce le manutenzioni) e **Nuovo rapporto** (per chi registra i rapporti) chiedono prima l'impianto: un elenco degli impianti in servizio con la ricerca per impianto, cliente, sede e tipo, e per ciascuno quante manutenzioni ha già nel piano; poi si apre la scheda, come dall'impianto. Le stesse cose si fanno dalla linguetta **Manutenzioni** della pagina di ogni impianto, che ha in più il piano completo e i suoi rapporti.

## <a id="manutenzioni-piano"></a>Il piano di manutenzione

Nella linguetta **Manutenzioni** dell'impianto, chi può **Gestire le manutenzioni** aggiunge le voci del piano una per una (**Aggiungi**) oppure tutte insieme con **Proposte del tipo**: quelle del [tipo dell'impianto](#manutenzioni-tipi), con la prima scadenza proposta dalla data di installazione, da confermare. Per ogni voce:

- **Che cosa** (per esempio *Manutenzione ordinaria*, *Controllo periodico*), **ogni quanto** si fa (una volta sola, ogni mese, 2, 3, 4 o 6 mesi, ogni anno, 2, 3, 4 o 5 anni, oppure un numero di mesi a scelta), la **prossima scadenza** e il **preavviso** in giorni;
- se la successiva si conta **dal giorno in cui è fatta** invece che dalla scadenza;
- i **controlli da fare**, uno per riga: diventano la lista del rapporto e le voci da spuntare dell'intervento;
- il **contratto** di manutenzione con il cliente (riferimento e data di fine), facoltativo: la sua fine compare nello scadenzario 60 giorni prima (una sola volta per cliente, anche se copre più impianti);
- le note.

Modificando una voce chiusa (fatta e senza ripetizione) la si riapre. **Elimina** (o **Togli dal piano** dal menu) la toglie dal piano: i rapporti già fatti restano, con il suo nome. Le manutenzioni di un impianto **dismesso** non compaiono nello scadenzario.

## <a id="manutenzioni-pianificare"></a>Pianificare l'intervento

**Pianifica** (dalla manutenzione o dal suo menu) chiede il giorno, chi lo fa e una nota, e crea un'[attività](attivita.md) collegata al cliente e all'impianto, con i controlli come voci da spuntare: chi la riceve la trova tra le sue attività e nel calendario, con i soliti promemoria. La manutenzione mostra *pianificata il …* con le persone; per cambiare giorno o persone si modifica l'attività. Nella scheda dell'attività un riquadro ricorda la manutenzione, con **Registra il rapporto**: salvando il rapporto l'attività si completa (se chi lo registra può lavorarci; altrimenti resta aperta e lo dice).

## <a id="manutenzioni-rapporti"></a>I rapporti

**Registra il rapporto** (dalla manutenzione, dall'attività o con **Nuovo rapporto** nella pagina dell'impianto, dove si sceglie la manutenzione oppure *intervento straordinario*, fuori dal piano) apre il rapporto:

- il **giorno** (non nel futuro), le **ore** e i **tecnici** (proposti dal personale e dagli utenti, anche più di uno);
- l'**esito**: **Regolare**, **Con anomalie** o **Non funzionante**;
- i **controlli** del piano, ognuno con ✓ (regolare), ✗ (non regolare) o N.A. e una nota; **Tutti regolari** segna quelli ancora vuoti, **Aggiungi** ne mette altri per questo intervento;
- **lavori eseguiti**, **anomalie riscontrate**, **interventi consigliati**, il nome di chi **firma per il cliente** e le note;
- la **prossima scadenza**, proposta dal piano (la scadenza o il giorno dell'intervento più il periodo) e modificabile; vuota, per una manutenzione che non si ripete, la chiude;
- i **file** (foto, il rapporto firmato, verbali): vanno nella cartella dell'impianto in Documenti, sotto **Manutenzioni → RM 2026-012**, e si aprono dal rapporto anche senza i permessi dei documenti. Togliere un file dal rapporto lo lascia in Documenti.

Salvato, il rapporto prende il **numero** successivo dell'anno (*RM 2026-012*) e la manutenzione passa alla scadenza successiva. **Salva e stampa** (o **Stampa** da un rapporto) apre l'anteprima del rapporto pronto da firmare, con il [modello di stampa](modelli-stampa.md) delle manutenzioni: numero e giorno, cliente, sede, impianto, tecnici, esito, la tabella dei controlli, i lavori, le anomalie, i consigli, la prossima scadenza e, in fondo all'ultimo foglio, le firme del tecnico e del cliente. Chi ha scritto un rapporto lo corregge; chi gestisce le manutenzioni corregge ed elimina quelli di tutti (eliminandolo, i file restano in Documenti e la manutenzione non torna indietro).

## <a id="manutenzioni-tipi"></a>Le manutenzioni proposte dai tipi

Ogni [tipo di impianto](impianti.md#impianti-tipi) propone le sue manutenzioni (che cosa, ogni quanti mesi, il preavviso, i controlli): si scrivono dalla pagina Impianti, **Tipi**, con il pulsante accanto al tipo, per chi può **Gestire i tipi di impianto**. Dove il programma è partito con i tipi proposti si parte da Antintrusione, Videosorveglianza e Controllo accessi (ogni anno), Antincendio (controllo periodico ogni 6 mesi), KNX e domotica (verifica e backup), Fotovoltaico, Elettrico e quadri (manutenzione del quadro ogni anno e verifica periodica dell'impianto di terra DPR 462/01 ogni 5 anni). Cambiarle non tocca i piani che ci sono già.

> [!NOTE]
> **Le periodicità proposte sono indicative.** Quelle vere dipendono dalle norme (per esempio i controlli antincendio, le verifiche DPR 462/01, le guide CEI), dal costruttore, dall'uso e dai contratti con i clienti: verificale e correggile nei tipi o nel piano di ogni impianto.

## <a id="manutenzioni-importa"></a>Importare ed esportare il piano

**Esporta** scarica il piano delle manutenzioni in **Excel**, in **CSV** oppure come **calendario** (.ics), un evento il giorno di ogni scadenza da aprire in Outlook, Google Calendar o sul telefono. **Importa** (a chi gestisce le manutenzioni) porta il piano da un foglio: impianto, cliente (serve se più clienti hanno un impianto con lo stesso nome), manutenzione, ogni quanto (in mesi, oppure semestrale, annuale, una volta sola), prossima scadenza, preavviso, controlli separati da punto e virgola, contratto e la sua fine. Si collegano solo agli impianti in servizio. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

## <a id="manutenzioni-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere le manutenzioni | La pagina Manutenzioni e la linguetta dell'impianto: piani, interventi pianificati, rapporti con i loro file e la stampa; le scadenze delle manutenzioni nello scadenzario. |
| Registrare i rapporti di manutenzione | Compilare i rapporti (controlli, esito, lavori, file) e correggere i propri: di solito i tecnici. |
| Gestire le manutenzioni | Preparare i piani di manutenzione, pianificare gli interventi, correggere ed eliminare i rapporti di tutti; ricevere i promemoria delle scadenze. |

Per vedere la pagina dell'impianto serve **Vedere gli impianti**: senza, un tecnico lavora dalla pagina Manutenzioni e dalla scheda dell'attività. Le cartelle dei rapporti le crea la piattaforma. Gli amministratori possono tutto.

---

[← Certificazioni](certificazioni.md) · [Indice](README.md) · [Pratiche →](pratiche.md)
