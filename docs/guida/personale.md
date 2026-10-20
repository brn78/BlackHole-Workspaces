[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="personale"></a>Personale

**Azienda → Personale** raccoglie le **persone dell'azienda**, anche quelle che non usano la piattaforma (per esempio chi lavora solo in cantiere): anagrafica, mansione e reparto, contratto, contatti, foto, [orario di lavoro, tariffa e costo](#personale-orario), e per ciascuno i **corsi** con gli attestati, i **documenti personali** e le **visite mediche**, ognuno con la sua scadenza. Il [catalogo](#personale-catalogo) dice quanto vale ogni corso e per quali mansioni è obbligatorio: così la piattaforma sa chi è in regola, che cosa sta per scadere e che cosa manca. La pagina compare a chi può **Vedere il personale** (vedi [Permessi](#personale-permessi)).

## <a id="personale-elenco"></a>L'elenco

Le linguette **In forza** e **Cessati** dicono quante persone ci sono; se ci sono [altre aziende del gruppo](impostazioni.md#impostazioni-gruppo), sotto si sceglie l'azienda (**Tutte** o una sola). La ricerca trova nome, matricola, mansione, reparto, telefono, email e utente; i due elenchi scelgono una mansione o un reparto. Ogni riga ha la persona (foto o iniziali, matricola, azienda), la mansione con il reparto e la colonna **Scadenze**: quante voci sono **scadute**, quante **in scadenza** (entro il preavviso) e quante obbligatorie **mancano**, oppure **In regola**; a finestra larga anche telefono, utente della piattaforma, **ore e tariffa** (le ore alla settimana, la tariffa di vendita e, per chi vede i costi, il costo orario), assunzione e ultima modifica. In alto **Stampa** (l'elenco come lo stai guardando, oppure i [tesserini di riconoscimento](#personale-tesserino) delle persone in forza mostrate), **Catalogo** e **Nuova scheda**. Un clic apre la scheda; il tasto destro (o ⋯) apre la scheda alla linguetta Formazione, Documenti o Visite, la stampa della scheda, il tesserino, **Duplica** ed **Elimina**.

## <a id="personale-importa"></a>Importare ed esportare con Excel

**Esporta** ⬇ scarica in **Excel** o in **CSV** le persone che vedi (filtri compresi) o tutti, con le colonne scelte tra quelle che l'importazione riconosce: il file si sistema in Excel e si reimporta così com'è. Niente costi né visite: solo i dati dell'elenco.

**Importa** ⬆ (a chi può creare le schede) apre l'importazione guidata da un foglio **Excel** (.xlsx, .xls, .ods) o **CSV**, una riga per persona, nel pannello a destra:

1. **Il file**, anche trascinandolo nel riquadro (al massimo 20 MB e 5.000 righe). **Scarica il modello Excel** dà il foglio già pronto con la riga dei campi e le istruzioni: compilato e importato così com'è, salta la scelta delle colonne. Un file con più fogli mostra quali importare (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)).
2. **Che cosa c'è in ogni colonna**: quelle con il nome giusto sono già scelte, le altre si scelgono a mano oppure, con l'assistente AI attivo, con **✨ Proponi con l'assistente**. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda.
3. **L'anteprima**: ogni riga con il suo esito (**Nuova**, **Già presente**, **Con errori**), i filtri per esito e una casella per scegliere che cosa importare. Una persona è già presente con lo stesso codice o lo stesso cognome e nome; si salta, a meno di spuntarla.
4. **Importa** crea le schede una dopo l'altra, come dal modulo, con l'avanzamento e **Ferma**; l'esito dice quante sono state importate e, riga per riga, quelle non importate con il motivo.

Niente si perde: un valore che non va (una data illeggibile, un contratto che non è nel catalogo, un genere sconosciuto, un codice fiscale o un'email non validi) non ferma la riga, finisce nelle **note** della scheda dopo «Da controllare:».

Il nome si legge da «Cognome» e «Nome», oppure da una colonna sola «Cognome e nome» (prima il cognome). Le date vanno bene come gg/mm/aaaa, aaaa-mm-gg o come date di Excel.

## <a id="personale-da-testo"></a>Una scheda nuova da un testo

Con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (per chi può gestire il personale) apre un pannello dove incollare un **curriculum**, un'email, una lettera di assunzione o i dati di un documento. **Proponi i dati** chiede all'assistente nome e cognome, genere, data e luogo di nascita, codice fiscale, mansione, reparto, data di assunzione, email, telefoni e indirizzi, e apre la **scheda nuova già compilata**, da controllare e salvare come sempre. Come per i [clienti](clienti.md#clienti-da-testo): solo ciò che c'è nel testo, i dati in un formato sbagliato (una data impossibile, un codice fiscale che non ha 16 caratteri) tolti e scritti in cima alla scheda, la provincia dall'elenco dei comuni, niente salvato da solo e il testo non conservato.

## <a id="personale-scheda"></a>La scheda

- **Dati**: la **foto** (dal PC, incollata o da un indirizzo web, vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini); la ritagli prima di salvarla), nome e cognome, genere, data e luogo di nascita e il **codice fiscale**, controllato mentre scrivi: **Calcola** lo ricava dall'anagrafica e da un codice già scritto si leggono data, genere e luogo (**Compila i dati mancanti**). Sotto, il **lavoro**: matricola (facoltativa e unica), azienda del gruppo, **mansione** e **reparto** (si sceglie tra quelli già usati oppure se ne scrive uno nuovo), tipo di contratto, data di assunzione, **scadenza del contratto** (per i contratti a termine: è una scadenza, con il promemoria 30 giorni prima), **data di cessazione** e note. In fondo l'[accesso alla piattaforma](#personale-accesso), la stessa persona tra i clienti ([Anche cliente](#personale-cliente)), a chi può vedere mezzi e attrezzature ciò che la persona ha **in consegna** (un clic apre la scheda del bene) e il riquadro **Privacy** con l'[informativa ai dipendenti](privacy.md#privacy-dipendenti).
- **Contatti** e **Indirizzi**: email e telefoni in una linguetta, gli indirizzi (residenza, domicilio…) con la mappa nell'altra, come nei clienti e con gli stessi controlli.
- **Orario e costo**: l'[orario di lavoro](#personale-orario) (a fasce oppure le ore al giorno e alla settimana), la **tariffa oraria di vendita** e, per chi ha il permesso dei costi, il **costo aziendale**.
- **Formazione**, **Documenti** e **Visite**: le [voci](#personale-voci) della persona; sulla linguetta, quante sono e un pallino se c'è qualcosa da guardare.
- **Indicatori** (dalla 1.147.0, con il [dettaglio per persona](indicatori.md#indicatori-persone) acceso, a chi può vedere la persona): i suoi indicatori e quelli del reparto nell'anno, le valutazioni, le note dei colloqui e, a chi vede i premi, il premio; con la stampa del riepilogo da firmare.
- **Storico**: chi ha cambiato che cosa, e quando.

In basso **Elimina**, **Duplica** (una scheda nuova con la stessa azienda, mansione, reparto, contratto, orario e tariffa, comoda quando si assumono più persone per lo stesso lavoro) e **Stampa**: la scheda con i corsi e, per chi li vede, documenti e visite, oppure il [tesserino di riconoscimento](#personale-tesserino). Una scheda nuova si crea con i dati e i contatti, anche dalla scheda di un [cliente](clienti.md#clienti-personale) o di un [utente](utenti.md), con i loro dati già scritti; corsi, documenti e visite si registrano subito dopo, nella scheda che si riapre da sola.

> [!TIP]
> **Chi lascia l'azienda.** Basta la **data di cessazione**: la persona passa tra i **Cessati** con tutta la sua storia e le sue scadenze non contano più. **Elimina** serve per le schede sbagliate o quando i dati vanno cancellati del tutto: se ne vanno anche voci, file e foto, e i mezzi e le attrezzature che aveva in consegna tornano liberi. Se la persona usava la piattaforma, il suo utente si disabilita da Sistema → Utenti: la scheda lo ricorda.

## <a id="personale-orario"></a>Orario e costo

La linguetta **Orario e costo** della scheda raccoglie quanto lavora la persona, quanto costa all'azienda e quanto si fa pagare al cliente un'ora del suo lavoro: sono la base per l'assistenza, gli interventi e i preventivi.

- **Orario di lavoro**: con **Orario a fasce** scegli per ogni giorno della settimana **Fasce orarie** (fino a quattro, per esempio 08:00–12:00 e 13:00–17:00) oppure **Riposo**; i **Modelli** riempiono la settimana con un clic. Le **ore al giorno** e **alla settimana** allora si calcolano dalle fasce (quelle al giorno sono la media dei giorni lavorati) e non si scrivono. Senza fasce si scrivono a mano, per esempio 8 e 40. Nei festivi non si lavora. L'editor è lo stesso degli [orari di accesso dei gruppi](gruppi-policy.md#gruppi-orari), ma i due orari sono indipendenti: quello dei gruppi decide quando si entra nella piattaforma.
- **Tariffa oraria di vendita**: quanto si fa pagare al cliente un'ora di lavoro della persona, IVA esclusa. La vede chi vede il personale.
- **Costo aziendale**, solo per chi ha il permesso **Costi del personale**. **Come si calcola**: Mentre scrivi, sotto compaiono contributi, TFR, costo annuo, **costo orario** e il **margine** sulla tariffa di vendita, in euro e in percentuale del prezzo (in rosso se la tariffa è **sotto costo**).
   - **Dalla retribuzione annua**: la **retribuzione annua lorda** (RAL), più i **contributi a carico dell'azienda** (in percentuale della retribuzione, li indica il consulente del lavoro), più il **TFR** (la retribuzione divisa per 13,5, se la spunta è accesa), più gli **altri costi annui** (buoni pasto, formazione, DPI, auto aziendale, premi…) danno il **costo annuo**; diviso per le **ore lavorate in un anno** dà il **costo orario**. **Proponi** calcola le ore dall'orario: le ore della settimana per 48 settimane (52 meno 4 di ferie), meno le festività dell'anno in corso che cadono nei giorni di lavoro (nazionali e il santo patrono delle Impostazioni). Togli tu i permessi retribuiti previsti dal contratto (ROL, ex festività) e, se vuoi, una stima di malattie e formazione.
   - **Costo orario già calcolato**: lo scrivi direttamente, per esempio quello del consulente del lavoro o la tariffa di un collaboratore. I dati della retribuzione restano salvati, se c'erano.

Le modifiche finiscono nello **Storico** della scheda: quelle del costo le vede solo chi vede i costi. Chi gestisce il personale senza il permesso dei costi modifica la scheda (orario e tariffa compresi) senza vedere né cambiare il costo. La stampa della scheda riporta orario e tariffa e, a chi li vede, il costo orario e quello annuo.

## <a id="personale-voci"></a>Corsi, documenti e visite

Ogni linguetta elenca le sue voci, nell'ordine del catalogo, ciascuna con lo **stato**: **Scaduto**, **Scade il…** (entro il preavviso del suo tipo), **Valido fino al…**, **Senza scadenza** oppure **Rinnovato**. **Aggiungi** apre la finestra della voce:

- **Corso**: il tipo dal catalogo, la data del corso, le ore, l'ente formatore, il numero dell'attestato;
- **Documento**: carta d'identità, patente, passaporto, permesso di soggiorno…, con numero, chi l'ha rilasciato, la data di rilascio e la scadenza stampata sul documento;
- **Visita**: la data, il **giudizio di idoneità** (idoneo, idoneo con prescrizioni o con limitazioni, non idoneo temporaneamente, non idoneo), il medico competente, le prescrizioni o limitazioni e la data della **prossima visita**. Si registra solo l'esito, non i dati sanitari.

La **scadenza si propone** dalla validità del tipo nel catalogo (la data della voce più la validità: per un corso da aggiornare ogni 5 anni, cinque anni dopo); si può cambiare, e per i documenti si scrive quella del documento. Ogni voce ha i suoi **file**: l'attestato, la scansione del documento, il giudizio di idoneità (PDF anche firmati `.p7m`, immagini, Word, Excel), che si aprono nel visualizzatore con un clic sul nome.

- **Rinnova** (dal menu ⋯ della voce; per le visite **Registra la visita successiva**) apre una voce nuova dello stesso tipo, con ente e ore già scritti: vale sempre la **più recente**, quella vecchia resta nello storico come **Rinnovato**. Per un aggiornamento non serve eliminare il corso di prima.
- In cima a ogni linguetta, un avviso elenca le voci **obbligatorie** per tutti o per la mansione della persona che non sono mai state registrate: un clic su un nome apre la voce nuova di quel tipo.
- **Dalla scansione** (dalla 1.103.0, con l'assistente attivo), in cima alla finestra di una voce nuova: scegli il PDF o la foto dell'attestato, del documento o del giudizio di idoneità e l'assistente compila tipo (dal catalogo), numero, ente o medico, date, ore, giudizio e note; il file finisce tra quelli da allegare e si carica con il salvataggio. Se il nome scritto sul documento non è quello della persona, lo dice.

## <a id="personale-catalogo"></a>Il catalogo

**Catalogo**, in alto nella pagina, è l'elenco uguale per tutti dei **corsi**, dei **documenti** e delle **visite**. Per ognuno: nome, colore, **validità** in mesi (la scadenza proposta; 0 = non scade da solo), **preavviso** in giorni (da quando la voce risulta «in scadenza» e parte il promemoria: per i corsi conviene largo, vanno organizzati) e se è **obbligatorio**: **No**, **Per tutti** oppure **Per alcune mansioni**, scritte come nelle schede (per esempio i lavori elettrici PES/PAV per gli elettricisti, la patente per chi guida i mezzi). Un tipo già usato non cambia categoria e non si elimina. Lo gestisce chi ha il permesso **Gestire i corsi, i documenti e le visite**.

In un'installazione nuova il catalogo è vuoto; dove il programma è partito con i cataloghi proposti si parte dai più comuni: formazione generale (obbligatoria per tutti) e specifica dei lavoratori per rischio basso, medio e alto, preposto, dirigente, RLS, addetti al primo soccorso e all'antincendio, lavori elettrici PES/PAV, lavori in quota, piattaforme elevabili, carrelli elevatori, installatori FER; carta d'identità, patente, passaporto, permesso di soggiorno, tessera sanitaria, tesserino di riconoscimento; la visita medica della sorveglianza sanitaria.

> [!NOTE]
> **Le durate proposte sono indicative.** Validità e obbligatorietà dei corsi dipendono dalle norme (D.Lgs. 81/2008, accordi Stato-Regioni, che cambiano nel tempo), dal settore e dalla valutazione dei rischi dell'azienda: verificale con il vostro consulente per la sicurezza e correggile nel catalogo. La periodicità delle visite la stabilisce il medico competente.

## <a id="personale-accesso"></a>Accesso alla piattaforma

La persona è una sola: la scheda del personale. L'**accesso** è facoltativo: chi usa la piattaforma ha anche un [utente](utenti.md), gli altri restano con la sola scheda. In fondo alla linguetta **Dati**:

- **Collega a un utente…** sceglie un utente che esiste già (uno senza scheda); **Crea l'accesso**, per chi può creare utenti, apre la scheda di un utente nuovo con i dati della persona già scritti (anagrafica, ruolo aziendale e reparto; la prima email diventa quella di accesso, le altre, i telefoni e gli indirizzi vanno tra i suoi contatti) e, creato l'utente, lo collega.
- Al contrario, nella scheda di un [utente](utenti.md) che non ha ancora una scheda del personale, chi gestisce il personale trova **Crea la scheda nel personale**: una scheda nuova con i suoi dati, già collegata.
- Collegata la scheda, l'utente prende da lì **nome, genere, data di nascita, codice fiscale, ruolo aziendale** (la mansione) e **reparto**: nella scheda dell'utente quei campi non si cambiano più, e **Apri la scheda** porta qui. Email dell'account, gruppi e sicurezza restano dell'utente.
- Un utente ha una scheda sola; un amministratore lo collega solo un amministratore. **Scollega** separa di nuovo scheda e utente, senza toccarli.

## <a id="personale-cliente"></a>Anche cliente

Una persona del personale può essere anche tra i [clienti](clienti.md), come persona fisica (per esempio chi ha un impianto a casa). Le due schede si collegano: nella linguetta **Dati**, sotto l'accesso alla piattaforma, il riquadro **Anche cliente** mostra a chi può vedere i clienti il cliente collegato, con **Apri il cliente**.

- Se tra i clienti c'è già una persona con lo stesso **codice fiscale**, il riquadro la propone: **Collega**.
- Altrimenti **Crea il cliente**, per chi può creare clienti o contatti privati, apre la scheda di un cliente nuovo con anagrafica, codice fiscale, email, telefoni, indirizzi e foto già scritti: salvato, il cliente è collegato.
- Al contrario, dalla [scheda del cliente](clienti.md#clienti-personale) si crea la scheda nel personale.
- I dati si copiano solo quando una scheda nasce dall'altra: dopo, ognuna si cambia per conto suo. Il cliente ha i suoi dati commerciali, visti da chi lavora con i clienti; la scheda del personale quelli del lavoro, visti da pochi.
- Un cliente va su una scheda sola, e solo se è una persona fisica. **Scollega** separa le due schede senza toccarle. Un cliente nel cestino resta collegato (con la scritta *nel cestino*); eliminato del tutto, sparisce dal riquadro.

## <a id="personale-tesserino"></a>Il tesserino di riconoscimento

Il **tesserino di riconoscimento** che i lavoratori espongono negli appalti, nei subappalti e nei cantieri (D.Lgs. 81/2008, articoli 18, 20, 21 e 26; legge 136/2010, articolo 5) si stampa dalla piattaforma: **Stampa → Il tesserino di riconoscimento** nella scheda, **Tesserino di riconoscimento** nel menu della riga, oppure **Stampa → I tesserini di riconoscimento** sopra l'elenco, per tutte le persone in forza mostrate (con i filtri applicati).

- Sul tesserino: la **foto**, cognome e nome, la data di nascita, la mansione, la **data di assunzione**, la matricola e il **datore di lavoro**, cioè l'azienda del gruppo per cui la persona lavora, con il logo, la partita IVA e la sede (da [Impostazioni → Generale](impostazioni.md#impostazioni-azienda)).
- Il formato è quello delle carte di credito (85,6 × 54 mm): un **foglio A4 da ritagliare**, con dieci tesserini e il bordo tratteggiato, oppure **una tessera per pagina**, per le stampanti di badge. Nella finestra di stampa del browser scegli la stampante e le dimensioni reali (scala 100%). La piattaforma ricorda il formato scelto.
- La finestra mostra l'anteprima e avvisa se a qualcuno mancano la foto (resta il riquadro per incollarla) o la data di assunzione, che la legge chiede (resta una riga da compilare a mano).

## <a id="personale-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere il personale | L'elenco e le schede: anagrafica, lavoro e contratto, contatti, corsi e attestati con i loro file, storico; le scadenze del personale (corsi, contratti) nello scadenzario. |
| Documenti personali e visite mediche | Vedere anche i documenti personali e le visite con il giudizio di idoneità, con i loro file, nelle schede, nello storico e nello scadenzario; con la gestione del personale anche registrarli. Sono dati delicati: da dare solo a chi ne ha bisogno. |
| Costi del personale | Vedere la retribuzione e il [costo aziendale](#personale-orario) di ogni persona (costo annuo, costo orario, margine sulla tariffa), anche nell'elenco e nello storico; con la gestione del personale anche cambiarli. Sono dati riservati: da dare solo a chi fa i conti dell'azienda. |
| Gestire il personale | Creare e modificare le schede, registrare le voci, caricarne i file, collegare la scheda a un utente o a un cliente; ricevere i promemoria delle scadenze del personale (quelli di documenti e visite solo con il permesso dei dati delicati). |
| Eliminare le schede del personale | Eliminare una scheda con le sue voci, i file e lo storico. |
| Gestire i corsi, i documenti e le visite | Il [catalogo](#personale-catalogo): tipi, validità, preavviso, obbligatorietà. |

---

[← Preventivi](preventivi.md) · [Indice](README.md) · [Reperibilità →](reperibilita.md)
