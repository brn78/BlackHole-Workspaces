[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="indicatori"></a>Indicatori

**Azienda → Indicatori** sono le **statistiche e gli andamenti che sceglie l'azienda**: quanto si produce per ora lavorata, quante rilavorazioni ogni cento pezzi, quante commesse si chiudono in tempo, quanti preventivi vanno a buon fine, quanto ci vuole a incassare, quante assenze… Ogni indicatore si costruisce con una **formula** sulle **misure**: quelle che il programma calcola da sé dai moduli che usi e quelle che non ha (pezzi prodotti, metri quadri, infortuni) e che si inseriscono a mano o si importano da Excel. Si leggono per tutta l'**azienda**, per **reparto** e, se lo accendi, per **persona**, mese per mese, per trimestre o per anno, con l'**obiettivo**, la **soglia di allarme**, il confronto con il periodo prima e con lo stesso periodo dell'anno prima.

> [!TIP]
> **Niente è fisso.** I nomi degli indicatori e delle misure, le loro unità, le voci della valutazione, i nomi delle parti e delle fasce dei premi, le forme del premio («Denaro», «Welfare», «Giorno di permesso»…) li scrive l'azienda e si cambiano quando si vuole: lo storico resta, perché i dati sono legati alla voce e non al suo nome. Tutta la sezione è facoltativa: si spegne da [Impostazioni → Sezioni](impostazioni.md#impostazioni-sezioni), e dentro sono facoltativi anche il dettaglio per persona e i premi (spenti di partenza).

Chi può vedere che cosa lo dicono i [permessi](#indicatori-permessi): l'azienda e i reparti chi ha **Vedere gli indicatori**, un reparto anche il suo **responsabile**, le persone solo chi ne ha il permesso, il loro responsabile e ognuno per sé.

## <a id="indicatori-primi-passi"></a>Come si comincia

1. in **Configurazione → Modelli** carica il modello più vicino al tuo lavoro: **Produzione (fabbrica)**, **Impianti e assistenza**, **Ufficio**. Aggiunge misure e indicatori con obiettivi di esempio; puoi caricarne più d'uno;
2. in **Configurazione → Indicatori** togli quelli che non ti servono (o togli «Attivo»), cambia nomi, obiettivi e soglie, aggiungine di tuoi con **Nuovo indicatore**;
3. per le misure da inserire, scegli in ognuna **chi la inserisce**: riceverà il promemoria quando mancano i dati;
4. inserisci (o importa) i dati dei mesi passati nella linguetta **Dati**: gli indicatori calcolati dal programma hanno già tutta la loro storia;
5. in **Configurazione → Impostazioni** scegli i responsabili di reparto e, se servono, il dettaglio per persona e i premi.

## <a id="indicatori-andamento"></a>L'andamento

La linguetta **Andamento** mostra un riquadro per indicatore, per l'azienda, un reparto o una persona (si sceglie in alto; il primo è quello che puoi vedere). In ogni riquadro:

- il valore dell'**ultimo periodo finito** (il mese scorso per un indicatore mensile, il trimestre scorso per uno trimestrale), con l'**obiettivo** e un lucchetto se il periodo è chiuso;
- lo **stato**: Obiettivo raggiunto, Sotto (o sopra) l'obiettivo, Oltre la soglia di allarme; il colore segue l'andamento buono dell'indicatore (per le rilavorazioni più basso è meglio);
- il confronto con il **periodo prima** e con lo stesso periodo di **un anno prima**: verde se va meglio, rosso se va peggio; per le percentuali la differenza è in punti;
- il **grafico** degli ultimi 12 mesi (8 trimestri, 5 anni), con la linea tratteggiata dell'anno prima e quella punteggiata dell'obiettivo; passandoci sopra con il mouse si leggono i valori;
- in fondo, il valore del **periodo in corso**, che cambia fino alla fine del periodo.

Un clic su un riquadro apre il **dettaglio**: 24 periodi di andamento, le misure della formula con i loro valori (per capire da dove viene il numero), l'azienda con i reparti e le persone che puoi vedere, e la tabella periodo per periodo. Un clic su un reparto o su un periodo aggiorna il dettaglio.

## <a id="indicatori-tabella"></a>La tabella

La linguetta **Tabella** mette gli indicatori in righe e i periodi in colonne: **Mesi**, **Trimestri** o **Anni**, gli ultimi 6, 12 o 24 (nei filtri). Le celle sono colorate come lo stato. Un indicatore mensile si legge anche per trimestre e per anno (le misure si mettono insieme come detto nelle [misure](#indicatori-misure)); uno annuale non si divide in mesi. **Esporta** la scrive in Excel o CSV.

## <a id="indicatori-misure"></a>Le misure

Le misure sono i numeri di partenza. Ce ne sono di due tipi:

| Tipo | Che cosa sono |
| --- | --- |
| Calcolate dal programma | Commesse completate, completate entro la scadenza, aperte in ritardo; ore registrate (tutte o solo sulle commesse); richieste di assistenza aperte, risolte, con il primo intervento in tempo, su impianti installati da poco; manutenzioni fatte; preventivi inviati, accettati, rifiutati e il loro valore; fatturato, fatture emesse e scartate dallo SDI, crediti scaduti, giorni medi di incasso; ricavi, costi e risultato della contabilità; persone in forza, assunzioni, cessazioni, corsi scaduti. Compaiono solo quelle dei moduli accesi (la contabilità solo se è tenuta nel programma). Alcune hanno una scelta (il tipo di commessa, sul posto o in laboratorio, da quanti mesi è installato l'impianto). |
| Inserite a mano o importate | Quello che il programma non sa: pezzi prodotti, metri quadri, rilavorazioni, ore lavorabili e ore di assenza (dal consulente del lavoro), infortuni, quasi-incidenti segnalati, ordini consegnati entro la data… Si creano con **Nuova misura**. |

Una misura inserita ha:

- **nome**, **unità** e decimali;
- **si inserisce** per l'azienda (un valore), **per reparto** o **per persona** (con il dettaglio per persona acceso), **ogni** mese, trimestre o anno. Periodo e raggruppamento si cambiano solo finché non ci sono valori;
- **più periodi o più gruppi insieme**: **somma** (pezzi, ore, infortuni), **media** (un tasso già calcolato, un voto) o **ultimo valore** (persone, giacenze: per l'anno vale dicembre, per l'azienda la somma dei reparti);
- **chi la inserisce** e il **promemoria**: tanti giorni dopo la fine del periodo, se mancano dati, gli arriva una notifica (una volta per periodo).

Le misure calcolate dal programma attribuiscono i numeri alle persone quando possono (il responsabile della commessa, chi ha la richiesta di assistenza, il commerciale del preventivo, chi ha registrato le ore: attraverso l'utente collegato alla scheda del personale) e quindi ai reparti. Quelle che non si possono dividere (fatturato, contabilità, manutenzioni) valgono per l'azienda: in un indicatore per reparto, per ogni reparto vale il totale.

## <a id="indicatori-dati"></a>Inserire e importare i dati

La linguetta **Dati** c'è per chi ha **Inserire i dati degli indicatori** e per chi deve inserire una misura. Si sceglie la misura e l'anno: le righe sono i reparti o le persone (dalle schede del personale), le colonne i periodi. Scrivi i numeri (con la virgola per i decimali), poi **Salva**; una cella svuotata toglie il valore. Passando sopra una cella si vede chi l'ha scritta e quando. I periodi [chiusi](#indicatori-periodi) e quelli non ancora cominciati non si cambiano.

**Importa** legge un file Excel o CSV con **una riga per valore**:

| Colonna | Come si scrive |
| --- | --- |
| Misura | Il nome della misura, come nel programma (maiuscole a parte). |
| Periodo | 10/2026, ottobre 2026, 2026-10, una data del mese; 3° trimestre 2026, Q3 2026, 2026-Q3; 2026. |
| Reparto o persona | Il reparto come nelle schede del personale; la persona con il nome della scheda (anche con nome e cognome invertiti) o la matricola; vuoto per l'azienda. |
| Valore | Il numero. |
| Nota | Facoltativa. |

Le colonne si riconoscono dal nome (o si scelgono a mano, anche con l'assistente); **Controlla** dice quante righe sono buone e perché le altre si saltano, **Importa** le scrive. **Modello da compilare** scarica un file Excel con le colonne giuste e una riga per misura.

## <a id="indicatori-crearli"></a>Creare un indicatore

**Nuovo indicatore** (o un clic su un indicatore in **Configurazione → Indicatori**) apre la scheda:

- **Nome** e **descrizione** (che cosa misura e perché conta);
- la [formula](#indicatori-formule);
- il [raggruppamento](#indicatori-raggruppamenti), il **periodo** (mese, trimestre, anno) e l'**andamento buono**: più alto è meglio o più basso è meglio;
- **unità** e decimali per leggerlo;
- [obiettivo, soglia e avvisi](#indicatori-obiettivi);
- **Nella Home**: il riquadro Indicatori della Home lo mostra a chi lo può vedere;
- **Attivo**: spento, non compare più ma i dati restano.

In **Configurazione → Indicatori** le frecce cambiano l'ordine in cui compaiono ovunque.

## <a id="indicatori-formule"></a>Le formule

Una formula si compone scegliendo, senza scrivere niente:

| Come si calcola | Esempio |
| --- | --- |
| Il valore di una misura | Infortuni; Fatturato; Persone in forza. |
| A diviso B | Rilavorazioni ÷ Pezzi prodotti × 100 = rilavorazioni ogni cento pezzi (%); Metri quadri lavorati ÷ Ore lavorate = produttività (mq/h); Preventivi accettati ÷ Preventivi inviati × 100. |
| A meno B | Ricavi − Costi; Ordini consegnati − Ordini consegnati entro la data (= in ritardo). |
| A più B | Infortuni + Quasi-incidenti. |

Il **moltiplicatore** vale 100 per le percentuali (il pulsante **Percentuale** lo mette da solo). Senza il dato di A, o con B a zero in una divisione, l'indicatore non ha valore in quel periodo (si vede «—»), invece di un numero sbagliato. Una misura inserita ogni trimestre non può stare in un indicatore mensile.

> [!TIP]
> **Indicatori che si bilanciano.** Conviene misurare la produttività sui pezzi buoni o per ora lavorata (non cambia con il numero di persone) e affiancarle le rilavorazioni: così correre a scapito della qualità non conviene.

## <a id="indicatori-raggruppamenti"></a>Azienda, reparti e persone

- **Azienda**: un valore solo.
- **Per reparto**: un valore per ogni reparto delle schede del personale in forza nel periodo, più il totale dell'azienda.
- **Per persona**: anche un valore per ogni persona (serve il **dettaglio per persona**, acceso nelle impostazioni).

Il valore di un gruppo più largo nasce dalle misure del gruppo, non dalla media degli indicatori: le rilavorazioni dell'azienda sono la somma delle rilavorazioni diviso la somma dei pezzi di tutti i reparti. Il reparto di una persona è quello della sua scheda di oggi.

## <a id="indicatori-obiettivi"></a>Obiettivi, soglie e avvisi

- **Obiettivo**: raggiunto (verde) se il valore è almeno l'obiettivo, o al massimo l'obiettivo se più basso è meglio; altrimenti giallo.
- **Soglia di allarme**: oltre (o sotto) diventa rosso.
- **Chi avvisare oltre la soglia**: utenti e gruppi. Una volta l'ora il programma guarda l'**ultimo periodo finito** e, se un gruppo (l'azienda, un reparto, una persona) è oltre la soglia, manda la notifica **una volta sola** per indicatore, periodo e gruppo, e solo a chi può vedere quel gruppo (nella campanella, per email e su Telegram come ognuno ha scelto). Cambiando la soglia gli avvisi ripartono. In **Configurazione → Impostazioni**, **Controlla adesso avvisi e promemoria** non aspetta l'ora.

## <a id="indicatori-periodi"></a>Periodi chiusi

In **Configurazione → Periodi chiusi** si chiude un mese, un trimestre o un anno finito. Chiudere un periodo **ferma i valori** di tutti gli indicatori di quel tipo (azienda, reparti, persone) con l'obiettivo di allora: se poi cambiano formule, obiettivi o persone, lo storico resta com'era (e il lucchetto lo ricorda). I **dati inseriti** del periodo, e dei periodi più corti dentro, e le **valutazioni** non si cambiano più. **Riapri** toglie i valori fermati e si torna a calcolarli. Chiudere i periodi conta soprattutto quando gli indicatori servono per i premi o per le valutazioni: nessuno può cambiare dopo quello su cui ci si è accordati.

## <a id="indicatori-persone"></a>Le persone

Con il **dettaglio per persona** acceso, gli indicatori «per persona» si leggono anche per ognuno, nella linguetta **Persone** della pagina e nella linguetta **Indicatori** della [scheda del personale](personale.md). Per la persona si vedono, per l'anno scelto:

- i **suoi indicatori**: il valore dell'anno con l'obiettivo e l'andamento periodo per periodo;
- gli indicatori del suo **reparto**, come contesto (se chi guarda vede il reparto);
- le [valutazioni](#indicatori-valutazioni) e le note dei **colloqui**;
- a chi vede i premi, il suo **premio** (provvisorio finché l'anno non si chiude).

**Stampa il riepilogo** prepara un foglio con indicatori, valutazioni, colloqui e premio e lo spazio per le firme del responsabile e della persona, da consegnare al colloquio. Con **Ognuno vede i propri**, chi ha la scheda del personale collegata al suo utente vede la propria linguetta (mai quelle dei colleghi) e gli indicatori del suo reparto; non può valutarsi.

> [!WARNING]
> Valutazioni, colloqui e indicatori delle persone sono **dati personali**: vanno indicati nell'[informativa ai dipendenti](privacy.md) e nel registro dei trattamenti (per esempio «Valutazione delle prestazioni»). Le ore di assenza vanno inserite **come totali**, già senza maternità, legge 104 e infortuni seri, senza le cause.

## <a id="indicatori-valutazioni"></a>Valutazioni e colloqui

Il responsabile del reparto (o chi ha **Indicatori delle persone**) valuta una persona ogni trimestre o ogni anno (si sceglie nelle impostazioni): un voto da **1 a 5** per ogni voce (le voci le scrive l'azienda: di partenza affidabilità, collaborazione, precisione e cura, rispetto delle procedure), «—» se una voce non si valuta, e la **motivazione**. La media dei voti va nel riepilogo e, se il piano lo prevede, nella parte individuale del premio. Nessuno valuta sé stesso; senza voti e senza motivazione la valutazione si toglie. Le **note dei colloqui** (giorno e testo) restano nella linguetta e nella stampa; le toglie chi le ha scritte o chi configura gli indicatori.

## <a id="indicatori-premi"></a>Premi

Facoltativi: si accendono in **Configurazione → Impostazioni** e la linguetta **Premi** la vede solo chi ha il permesso **Premi**. Per ogni anno c'è un **piano**:

- **Che cosa dà**: **Punti e importi**, oppure **Solo punti** per usarlo come statistica o classifica interna senza soldi;
- **Premio pieno a persona**: quanto prende chi è nella fascia al 100% ed è stato in forza tutto l'anno; chi è entrato o uscito durante l'anno prende in proporzione ai giorni;
- **Il fondo**: scritto, oppure una **percentuale del risultato** della contabilità (ricavi meno costi dell'anno, se la contabilità è tenuta nel programma) con un massimo. Se i premi lo superano, si riducono tutti nella stessa proporzione;
- **Le tre parti** con il loro peso (di partenza 40, 40 e 20) e il loro nome, che scegli tu (per esempio Azienda, Squadra, Persona). **Pesi diversi per un reparto**: per esempio 40/30/30 dove una funzione è una persona sola;
- **Le voci**: un indicatore, la parte in cui conta, il peso, il **minimo** (lì vale 0) e l'**obiettivo** (lì vale il punteggio pieno; vuoto: quello dell'indicatore); in mezzo i punti crescono in proporzione, anche per gli indicatori in cui più basso è meglio. Una voce può valere solo per alcuni reparti (per esempio le rilavorazioni per la produzione, i preventivi per l'ufficio). Gli indicatori si leggono sull'anno intero;
- **Peso della valutazione** del responsabile nella parte individuale (0 = non conta);
- **Da punti a premio**: le fasce, da quanti punti in su e quanta parte del premio pieno (per esempio sotto 60 niente, da 60 il 50%, da 75 il 100%, da 90 il 130%), ognuna con il suo nome;
- **Forme del premio**: come si può ricevere («Denaro», «Welfare», «Giorno di permesso»…); nei risultati si sceglie per ognuno;
- **Reparti fuori dal piano**.

I **risultati** sono calcolati subito, provvisori: per ogni persona i punti delle tre parti (una parte senza voci non conta e le altre pesano di più), il totale, la fascia, la parte dell'anno in forza e il premio; sopra il fondo, quanto si è calcolato e la riduzione. Un clic su una persona mostra voce per voce valore, minimo, obiettivo e punti, e i dati che mancano. **Chiudi l'anno** ferma i risultati; **Riapri** li ricalcola. **Esporta** li scrive in Excel.

> [!WARNING]
> Il programma fa i conti, non le regole: perché un premio di risultato abbia la **tassazione agevolata** servono un accordo aziendale o territoriale depositato e obiettivi di incremento misurabili; il premio in welfare ha i suoi limiti. Chiedi al consulente del lavoro prima di usare gli importi.

## <a id="indicatori-modelli"></a>Modelli di settore e configurazione

In **Configurazione → Modelli**:

- **Produzione (fabbrica)**: pezzi, metri quadri e ore per reparto, rilavorazioni, ordini consegnati e in tempo, infortuni, segnalazioni, ore lavorabili e di assenza, con produttività, rilavorazioni %, puntualità delle consegne, tasso di assenza;
- **Impianti e assistenza**: commesse puntuali, assistenza nei tempi, richieste dopo la posa, commesse in ritardo, ore sulle commesse, manutenzioni (tutti calcolati dal programma);
- **Ufficio**: preventivi accettati e loro valore, giorni medi di incasso, crediti scaduti, fatture scartate, fatturato.

Un modello aggiunge solo le misure e gli indicatori con un nome che non c'è ancora; quelli con le misure di una sezione spenta si saltano; senza il dettaglio per persona, ciò che è per persona diventa per reparto. **Esporta** scrive in un file JSON misure e indicatori (senza i valori), da caricare con **Importa** su un'altra installazione.

## <a id="indicatori-permessi"></a>Permessi e responsabili

| Permesso o ruolo | Consente |
| --- | --- |
| Vedere gli indicatori | La pagina: azienda e reparti, andamento, tabella, dettaglio. |
| Inserire i dati degli indicatori | Scrivere e importare i valori di tutte le misure inserite. |
| Configurare gli indicatori | Misure, indicatori, impostazioni, responsabili, modelli, periodi chiusi. |
| Indicatori delle persone | Con il dettaglio per persona acceso: le persone, le valutazioni, i colloqui (dati riservati). |
| Premi | Il piano e i risultati con gli importi (dati riservati; comprende gli indicatori delle persone). |
| Responsabile di reparto | Senza permessi: il suo reparto e le sue persone (senza gli importi), le loro valutazioni e i colloqui. Si sceglie in **Configurazione → Impostazioni**. |
| Chi inserisce una misura | Scrive e importa i dati di quella misura e ne riceve il promemoria. |
| Ognuno vede i propri | Con la scheda del personale collegata al proprio utente: il proprio reparto e, con il dettaglio per persona, i propri indicatori, valutazioni e colloqui. |

Nel [registro attività](registro.md), sotto «Indicatori», restano le modifiche a misure, indicatori, impostazioni, periodi e premi, i dati inseriti o importati, le valutazioni e i colloqui (mai i valori delle persone).

---

[← Presenze](presenze.md) · [Indice](README.md) · [Mezzi e attrezzature →](mezzi.md)
