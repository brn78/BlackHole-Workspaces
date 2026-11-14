[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="mezzi"></a>Mezzi e attrezzature

**Azienda → Mezzi** e **Azienda → Attrezzature** sono i due elenchi dei **beni dell'azienda**: il parco auto e i mezzi da lavoro (targa, km, carburante e carta carburante) e le attrezzature (scale, elettroutensili, giuntatrici, strumenti di misura, DPI anticaduta…). Per ognuno le **scadenze** (revisione, bollo, assicurazione, tagliando, verifiche periodiche), anche a **km**, con i promemoria; lo storico delle **manutenzioni** con km, costi e fornitori; a chi è **consegnato**; i file e la foto. Le pagine compaiono a chi può **Vedere mezzi e attrezzature** (vedi [Permessi](#mezzi-permessi)).

## <a id="mezzi-elenco"></a>L'elenco

Le due pagine funzionano allo stesso modo. Le linguette **In uso** e **Dismessi** dicono quanti beni ci sono; se ci sono [altre aziende del gruppo](impostazioni.md#impostazioni-gruppo), sotto si sceglie l'azienda. La ricerca trova numero, descrizione, marca e modello, targa, telaio o matricola, tipo, persona, dove si trova e carta carburante; gli elenchi scelgono il **tipo**, lo **stato** (in uso, in riparazione, fuori uso) e se è **in consegna** o no. Ogni riga ha il bene (foto o icona del tipo, numero, descrizione, tipo, marca e modello), la targa e i km per i mezzi, a chi è consegnato (per le attrezzature, altrimenti, dove si trova) e la **prossima scadenza**: la più urgente, con quando scade, quanto manca e lo stato (**+2** accanto al nome: altre due da guardare). In alto **Stampa**, **Tipi di mezzi** (o **Tipi di attrezzature**) e **Nuovo mezzo** (o **Nuova attrezzatura**); un clic apre la scheda, il tasto destro (o ⋯) la apre alle Scadenze, alle Manutenzioni o alle Consegne, la stampa, **Duplica** ed **Elimina**.

## <a id="mezzi-importa"></a>Importare ed esportare con Excel

**Esporta** ⬇ scarica in **Excel** o in **CSV** i mezzi o le attrezzature che vedi (filtri compresi) o tutti, con le colonne scelte tra quelle che l'importazione riconosce: il file si sistema in Excel e si reimporta così com'è.

**Importa** ⬆ (a chi può creare le schede) apre l'importazione guidata da un foglio **Excel** (.xlsx, .xls, .ods) o **CSV**, una riga per mezzo o attrezzatura, nel pannello a destra:

1. **Il file**, anche trascinandolo nel riquadro (al massimo 20 MB e 5.000 righe). **Scarica il modello Excel** dà il foglio già pronto con la riga dei campi e le istruzioni: compilato e importato così com'è, salta la scelta delle colonne. Un file con più fogli mostra quali importare (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)).
2. **Che cosa c'è in ogni colonna**: quelle con il nome giusto sono già scelte, le altre si scelgono a mano oppure, con l'assistente AI attivo, con **✨ Proponi con l'assistente**. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda.
3. **L'anteprima**: ogni riga con il suo esito (**Nuova**, **Da aggiornare**, **Già presente**, **Con errori**), i filtri per esito e una casella per scegliere che cosa importare. Un bene è già presente con lo stesso numero, la stessa targa o lo stesso telaio o matricola: se il foglio cambia qualcosa è **Da aggiornare**, e sotto c'è scritto che cosa cambia (per esempio «Proprietà: Di proprietà → In leasing · Noleggiatore: — → …»); se non cambia niente è **Già presente** e si salta.
4. Il pulsante blu dice che cosa fa (**Importa 3**, **Aggiorna 12**, **Importa 3 e aggiorna 12**): prima aggiorna le schede che ci sono già, poi crea quelle nuove, una dopo l'altra, con l'avanzamento e **Ferma**. Alla fine il riepilogo dice quante sono state importate e aggiornate, che cosa è cambiato in ognuna e, riga per riga, quelle non riuscite con il motivo.

Per una scheda **nuova** niente si perde: un valore che non va (un tipo che non c'è, uno stato o un'alimentazione sconosciuti, una data o dei km illeggibili) non ferma la riga, finisce nelle **note** della scheda dopo «Da controllare:».

Si importa nell'elenco aperto: dalla pagina Mezzi i mezzi, da Attrezzature le attrezzature. Il **tipo** si riconosce dal nome e porta le sue **scadenze proposte**, come in una scheda nuova (la revisione dalla data di immatricolazione, le scadenze a km dai km iniziali). C'è anche una colonna per ogni scadenza che i tipi propongono (**Revisione**, **Bollo**, **Assicurazione**, **Tagliando**…): la data della prossima o, per i mezzi, i km. Dalla 1.216.0 **Esporta** scrive anche la data d'acquisto e, per i mezzi, l'alimentazione, il gestore e la scadenza della carta carburante: un elenco esportato e importato su un'altra installazione li ritrova.

### Aggiornare i beni che ci sono già (dalla 1.196.0)

Il modo più semplice: **Esporta** in Excel, compila le colonne che servono (proprietà, noleggiatore, dal… al…, tipo, immatricolazione, km, carta carburante, le date delle scadenze) e reimporta lo stesso file. Valgono queste regole:

- Si scrivono solo le **celle piene**: una cella vuota lascia il dato com'è. Per togliere un dato si usa la scheda.
- Un valore che non si riconosce (un tipo che non c'è, uno stato, una proprietà o una data che non si leggono) **ferma la riga** con il motivo: nelle note di una scheda che c'è già non finisce niente di nascosto. Le colonne non scelte non vanno nelle note.
- I **km**: su un mezzo che non ne ha diventano quelli iniziali; più di quelli attuali diventano una **lettura dei km** di oggi; meno di quelli attuali restano quelli attuali, e l'anteprima lo dice.
- Le **scadenze** scritte per nome spostano quella aperta con lo stesso nome o, se non c'è, ne aprono una con il periodo e il preavviso del tipo. Quando il foglio dà il tipo, l'immatricolazione, l'acquisto o i km, si aggiungono le scadenze del tipo che la scheda non ha ancora (la revisione dall'immatricolazione, il tagliando dai km); per quelle che non hanno una data da cui partire (bollo, assicurazione) l'anteprima dice di scriverla nella sua colonna.
- Proprietà, noleggiatore e periodo come nella scheda: la data di fine diventa la scadenza **Fine del noleggio**; chi lo dà e le date senza la proprietà fermano la riga, se il bene è di proprietà.
- Ogni scheda aggiornata ha nello **Storico** la voce «Aggiornata da un foglio» con tutto quello che è cambiato, e il [registro attività](registro.md) lo riporta.

## <a id="mezzi-da-testo"></a>Una scheda nuova da un testo

Si usa in [due modi](assistente-ai.md#assistente-senza), con l'[assistente AI](assistente-ai.md) o senza. **✨ Da un testo** (per chi può gestire mezzi e attrezzature) apre un pannello dove incollare, per un mezzo, il **libretto di circolazione** trascritto (anche letto da una foto con il testo dalle immagini), un'offerta o una fattura; per un'attrezzatura un'offerta, una fattura d'acquisto o la scheda del prodotto. **Proponi con l'assistente** chiede all'assistente descrizione, marca, modello, targa, telaio o matricola, data di immatricolazione, alimentazione, km e data di acquisto (per le attrezzature niente targa, immatricolazione, alimentazione e km) e apre la **scheda nuova già compilata**: scegli il tipo, controlla e salva come sempre; le scadenze proposte dal tipo partono dalle date e dai km arrivati. Come per i [clienti](clienti.md#clienti-da-testo): solo ciò che c'è nel testo, i dati in un formato sbagliato tolti e scritti in cima alla scheda, niente salvato da solo e il testo non conservato.

## <a id="mezzi-scheda"></a>La scheda

- **Dati**: la **foto** (dal PC, incollata o da un indirizzo web, vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini); la ritagli prima di salvarla) oppure **Icona e colore** (senza, quella del tipo), il **numero** in azienda (vuoto = il prossimo libero: M01, M02… per i mezzi, A001, A002… per le attrezzature; è unico nell'elenco), il **tipo**, la descrizione, marca e modello, l'azienda del gruppo e lo **stato**. Per i mezzi la **targa**, il **telaio**, le date di **immatricolazione** e di acquisto, i **km iniziali** (poi i km attuali sono l'ultima lettura) e il **carburante**: alimentazione, numero della **carta carburante**, il suo **PIN** (vedi sotto), chi l'ha emessa e la sua scadenza. Per le attrezzature la **matricola**, la data di acquisto e **dove si trova** quando non è in consegna (magazzino, furgone, cantiere).
- **Scadenze**, **Manutenzioni**, **Consegne** e **File**: si salvano subito, senza il pulsante Salva (vedi sotto); sulla linguetta Scadenze un pallino se c'è qualcosa da guardare.
- **Utilizzi**: per i mezzi (a chi vede le presenze di tutti) chi aveva il mezzo in un giorno e a un'ora, per una multa o un danno, e il diario di chi l'ha usato; per le attrezzature chi l'aveva in un giorno, dalle consegne. Vedi [Gli utilizzi e le multe](#mezzi-utilizzi).
- **Storico**: chi ha cambiato che cosa, e quando: dati, scadenze fatte, consegne e ritiri, file.

Un bene nuovo si crea con i dati e le **scadenze proposte dal tipo**: la **revisione** si calcola dalla data di immatricolazione (per auto e furgoni la prima dopo 4 anni, poi ogni 2), le scadenze a km dai km iniziali (per esempio il tagliando a 20.000 km in più); le altre date (bollo, assicurazione, l'ultima verifica) le scrivi tu, dal libretto o dalla polizza. Un clic su «ogni…» cambia ogni quanto si ripete; ✕ toglie quelle che non servono. Le scadenze si possono aggiungere anche dopo. In basso **Elimina**, **Duplica** (una scheda nuova con lo stesso tipo, descrizione, marca, modello e azienda: comoda per una flotta di furgoni uguali) e **Stampa** (la scheda con le scadenze e le ultime manutenzioni).

> [!TIP]
> **Un bene venduto o rottamato** non si elimina: basta lo stato **Dismesso**. Passa tra i Dismessi con tutto il suo storico, le sue scadenze escono dallo scadenzario e, se era in consegna, viene ritirato; le attrezzature a bordo di un mezzo dismesso tornano libere (dalla 1.194.0). Uno a noleggio restituito passa tra i Dismessi come **Restituito** (vedi [Noleggio, leasing e comodato](#mezzi-noleggio)). **In riparazione** e **Fuori uso** restano nell'elenco; le scadenze di un bene fuori uso escono dallo scadenzario e non mandano promemoria.

## <a id="mezzi-pin"></a>Il PIN della carta carburante (dalla 1.195.0)

Nei Dati del mezzo, accanto al numero della carta carburante, c'è il **PIN della carta**, così l'ufficio ritrova subito il PIN della carta data a una persona. Lo vede solo chi ha il permesso **PIN delle carte carburante**: per gli altri il campo non c'è, e non lo possono né vedere né cambiare.

- Si salva **cifrato** e resta coperto (••••): l'**occhio** lo mostra, ⧉ lo copia senza mostrarlo. Ogni volta che qualcuno lo mostra o lo copia resta scritto nello **Storico** del mezzo e nel [registro attività](registro.md) (chi e quando, mai il PIN).
- Ha solo cifre, da 4 a 12, e serve il numero della carta. Per cambiarlo si scrive quello nuovo; per toglierlo lo si mostra e lo si cancella, poi **Salva**.
- Se cambia il numero della carta, il PIN di prima resta, con la nota «È il PIN della carta …, non di quella di adesso»: si scrive quello della carta nuova.
- Non compare mai negli elenchi, nella ricerca, nelle stampe, nei fogli esportati, nelle email e su Telegram.

## <a id="mezzi-scadenze"></a>Le scadenze

Ogni scadenza ha un nome, la **data**, per i mezzi anche i **km** (vale quella che arriva prima: il tagliando a 45.800 km o entro marzo), **ogni quanto si ripete** (mesi e, per i mezzi, km), se la successiva si conta **dalla scadenza** (revisione, bollo, assicurazione) o **dal giorno in cui è fatta** (tagliando, verifiche), il preavviso in giorni e le note. Lo stato: **Scaduta**, **In scadenza** (entro il preavviso o, a km, quando ne mancano meno di 1.000), **In regola**, **Chiusa** (fatta e senza ripetizione); **Km da registrare** quando una scadenza solo a km non ha ancora una lettura dei km con cui confrontarsi: così compare anche nello [scadenzario](scadenze.md), tra quelle da gestire, finché non si registrano i km.

- **Fatta** apre la finestra con il giorno, i km, il costo, il fornitore, le note e i file (fattura, verbale): diventa una voce delle [manutenzioni](#mezzi-manutenzioni) e la scadenza passa alla **successiva**, proposta nella finestra (la data più il periodo, i km più quelli del periodo) e modificabile. Una scadenza che non si ripete, senza una prossima scritta a mano, si chiude. «Fatta» si usa anche dallo [scadenzario](scadenze.md), dal menu della riga. I promemoria di quella scadenza che qualcuno ha ancora da leggere nella campanella si segnano letti da soli: non c'è più niente da fare.
- **Registra i km** aggiorna i km attuali (e con loro le scadenze a km) senza un intervento.
- **Carta carburante** (dalla 1.194.0): la scadenza della carta, scritta nei Dati, diventa da sola una scadenza con 30 giorni di preavviso. Quando arriva, **Rinnovo** chiede la scadenza della carta nuova: la scadenza si sposta lì e i Dati la seguono.

## <a id="mezzi-noleggio"></a>Noleggio, leasing e comodato (dalla 1.194.0)

Nei Dati, sotto **Proprietà**, si sceglie **di chi è** il bene: **di proprietà**, **a noleggio**, **in leasing** o **in comodato d'uso**. Per quelli che non sono di proprietà si scrivono chi lo dà (il noleggiatore, la società di leasing, chi lo presta: i suggerimenti propongono quelli già scritti, i noleggiatori degli interventi e i fornitori dell'anagrafica), il periodo **dal… al…** e, per chi vede i costi, il **canone** con ogni quanto si paga (al giorno, alla settimana, al mese, all'anno o in tutto).

- La data di fine diventa da sola la scadenza **Fine del noleggio** (o del leasing, del comodato), con il preavviso di 30 giorni (7 per un periodo sotto i 3 mesi, così un cestello preso per due settimane non risulta subito in scadenza): compare nello [scadenzario](scadenze.md) e manda i promemoria come le altre. Segue i Dati: cambiando la data si sposta, svuotandola (o tornando a «di proprietà») sparisce; dalla scadenza si cambiano solo il preavviso e le note.
- Quando arriva, **Restituzione o rinnovo** (nella scheda o dal menu della riga dello scadenzario) chiede com'è finita. **Restituito**: il bene passa tra i Dismessi come «Restituito», la consegna si chiude quel giorno, le attrezzature a bordo di un mezzo restituito tornano libere e le sue scadenze escono dallo scadenzario. **Rinnovato**: si scrive la nuova fine, la scadenza si sposta lì e la data nei Dati la segue. In tutti e due i casi nelle [manutenzioni](#mezzi-manutenzioni) resta una voce, con il costo (se lo vedi), le note e i file (il verbale di riconsegna, il contratto rinnovato).
- Nell'elenco, sotto il nome, compare «a noleggio fino al…»; la ricerca trova anche «noleggio» e il nome del noleggiatore. La stampa della scheda e quella dell'elenco dicono di chi è; l'importazione e l'esportazione dei fogli hanno le colonne Proprietà, Noleggiatore, Noleggio dal e Noleggio al.

## <a id="mezzi-responsabili"></a>I responsabili (dalla 1.195.0)

**Responsabili**, in **Altro** nella pagina Mezzi (o Attrezzature), sceglie chi segue l'elenco: chi gestisce le scadenze, i rinnovi, le riconsegne e gli scambi. Possono essere una o più persone del [personale](personale.md), anche senza accesso alla piattaforma: più sono, meglio è, così se sfugge a uno l'altro è informato. Per ognuno si sceglie **Per email** e/o **Su Telegram**.

- Ricevono **tutte le scadenze** dell'elenco (revisioni, bolli, fine dei noleggi, carte carburante, verifiche…), una volta quando entrano nel preavviso e una quando passano, con un messaggio scritto per chi deve organizzare: che cosa scade, di quale bene, quando, quanto manca, **dove o con chi sta** (in consegna a Mario Rossi, sul mezzo M03, in Magazzino), a chi va riconsegnato e come segnarlo nella scheda quando è fatto.
- Chi di loro ha l'accesso alla piattaforma lo vede anche nella **campanella**. Con almeno un responsabile così, la campanella va solo ai responsabili e non più a tutti quelli che gestiscono i beni; senza, resta come prima.
- La finestra dice, per ognuno, che cosa manca perché gli arrivi tutto: l'indirizzo email, il bot attivo, l'accesso. Chi lascia l'azienda resta nell'elenco, segnato, ma non riceve più niente.
- Nella scheda di ogni bene, sotto **Avvisi delle scadenze**, compaiono i responsabili del suo elenco; la stampa della scheda li riporta.
- Li sceglie chi ha il permesso **Gestire i tipi e i responsabili**; gli altri li vedono soltanto.

> [!TIP]
> **Non sfugge niente:** qualunque cosa arrivi o non arrivi per email, su Telegram o nella campanella, tutte le scadenze dei mezzi e delle attrezzature in uso o in riparazione sono sempre nello [scadenzario](scadenze.md), per chi vede mezzi e attrezzature.

## <a id="mezzi-avvisi"></a>Gli avvisi a chi ha il bene in consegna (dalla 1.194.0)

Nei Dati, **Avvisi delle scadenze** mostra i [responsabili](#mezzi-responsabili) dell'elenco e ha due caselle per la persona che ha il bene: **Per email** e **Su Telegram**. Accese, le scadenze della scheda (revisione, bollo, fine del noleggio, carta carburante, verifiche…) arrivano anche a lei, una volta quando entrano nel preavviso e una quando passano, con un messaggio scritto per esteso: che cosa scade, di quale bene, quando, quanto manca e che cosa fare (per la fine del noleggio, a chi va riconsegnato), e con chi parlarne: i responsabili per nome, oppure l'ufficio se non ce ne sono.

- **Per email** all'indirizzo del suo utente o, se non ce l'ha, al primo della sua [scheda del personale](personale.md); **su Telegram** nella chat del bot delle [presenze](presenze.md), se la persona l'ha collegata e il bot è attivo per lei. Lo stesso vale per i responsabili.
- Partono solo con l'invio delle email o Telegram accesi nelle [impostazioni](impostazioni.md): spenti, non parte niente, e quando si riaccendono arriva lo stato di quel momento. Senza indirizzo o senza chat, per quella persona non parte.
- Chi ha l'accesso alla piattaforma vede comunque l'avviso nella campanella; per email e su Telegram gli arriva una volta sola (quello diretto). Un responsabile che ha anche il bene in consegna riceve un messaggio solo. La linguetta Consegne dice se gli avvisi sono accesi.

## <a id="mezzi-manutenzioni"></a>Le manutenzioni

Lo storico degli interventi, dal più recente: **manutenzione**, **riparazione**, **revisione o verifica**, **gomme**, **guasto o segnalazione**, **lettura dei km** e **nota**, ciascuno con la data, che cosa (per esempio «Sostituzione della frizione»), i km, il costo, il fornitore, le note e i suoi file. In cima la **spesa registrata**, in tutto e nell'anno: è la somma esatta dei costi, che si arrotondano al centesimo (12,345 diventa 12,35). Le voci fatte da una scadenza si creano da sole con «Fatta»; **Nuova voce** aggiunge le altre. I km più alti tra le letture sono i **km attuali**: eliminando una voce, tornano all'ultima lettura rimasta.

## <a id="mezzi-consegne"></a>Le consegne

Un bene si **consegna** a una persona del [personale](personale.md), anche se non usa la piattaforma, con la data e una nota (per esempio «con chiavi e carta carburante»); la persona si cerca scrivendo il nome, la mansione o il reparto (dalla 1.202.1, prima una tendina). **Consegna a un altro** chiude la consegna attuale lo stesso giorno; **Ritira** lo rende di nuovo libero. Sotto, **chi l'ha avuto**: tutte le consegne, dalla più recente, con le date. La persona che ha la sua scheda collegata a un utente trova i beni che ha in consegna nella sua [Home](home.md) (**In consegna a te**) e riceve i promemoria delle loro scadenze, anche senza i permessi di mezzi e attrezzature. Nella scheda del personale, chi vede i mezzi trova che cosa la persona ha in consegna.

**Le attrezzature** (dalla 1.176.0) si spostano anche senza una persona: **Consegna** (o **Sposta**, se sono già da qualche parte) offre tre scelte, **A una persona**, **Su un mezzo** (sta sul furgone) e **In un luogo** (il magazzino, la sede, un cantiere), con il giorno da cui vale. La consegna di prima si chiude lo stesso giorno, e la data non può venire prima di quella attuale: lo storico va avanti giorno per giorno. Il deposito in un luogo aggiorna anche «Dove si trova». Nell'elenco la colonna **Dove o a chi** dice la persona, il mezzo o il luogo con la data; nella scheda del mezzo, in Consegne, compaiono le **attrezzature a bordo**. Da questo storico la linguetta Utilizzi dell'attrezzatura dice chi l'aveva in un giorno: vedi [Gli utilizzi e le multe](#mezzi-utilizzi).

## <a id="mezzi-utilizzi"></a>Gli utilizzi e le multe (dalla 1.175.0)

Quando arriva una multa, il verbale dice la targa, il giorno e l'ora. Apri il mezzo (nell'elenco si cerca anche per targa), vai sulla linguetta **Utilizzi**, scrivi il **giorno** e l'**ora** e premi **Cerca chi l'aveva**. La risposta viene dalle [presenze](presenze.md): alla chiusura di un'attività il bot chiede il mezzo e se la persona era alla guida o a bordo, e l'ufficio lo può correggere. Il programma scrive un riepilogo, per esempio: «Il mezzo M03 · Furgone (AB123CD) il 12/03/2026 alle 10:42 era in uso: alla guida Mario Rossi, dalle 07:30 alle 12:10 (Cantiere San Giovanni); a bordo Anna Rossi, passeggera, dalle 07:30 alle 12:05. Quel giorno era in consegna a Mario Rossi.»

- Se a quell'ora il mezzo **non era in un'attività** (nella pausa pranzo, la sera dopo il rientro), mostra l'**ultimo utilizzo prima** e il **primo dopo** nello stesso giorno, con chi guidava: chi è rientrato o partito insieme, entro mezz'ora l'uno dall'altro, compare nello stesso gruppo.
- Dice sempre **a chi era in consegna** il mezzo quel giorno (dalle [consegne](#mezzi-consegne)): nel giorno di un passaggio, tutte e due le persone.
- **Attenzione** quando la guida non torna: due persone hanno detto di essere alla guida nello stesso momento, nessuno l'ha detto, oppure qualcuno non ha risposto alla domanda.
- **Stampa il risultato** prepara il foglio da tenere con il verbale: il riepilogo, le attività con orari, cantiere e luoghi di partenza e di arrivo, e la consegna.

Sotto c'è il **diario del mezzo**: le attività fatte con il mezzo nel periodo scelto (di serie dal primo del mese a oggi), con chi l'ha usato, se era alla guida o a bordo, gli orari, il cantiere e i km di chi guidava, così due persone sullo stesso furgone non li contano due volte. Il clic su una riga apre l'attività nelle presenze; **Stampa il diario** ne fa un elenco. La linguetta la vede solo chi vede le presenze di tutti, e ogni ricerca resta nel [registro attività](registro.md).

**Per le attrezzature** (dalla 1.176.0) la linguetta Utilizzi ha **Chi l'aveva**: scrivi il giorno e, se lo sai, l'ora. La risposta viene dalle [consegne](#mezzi-consegne): a chi era affidata, su quale mezzo o in quale luogo stava quel giorno, anche quando quel giorno è passata di mano («era in consegna a Mario Rossi, poi sul mezzo M03»). Se era su un mezzo e c'è l'ora, sotto compare chi usava il mezzo in quel momento, come per le multe: solo a chi vede le presenze di tutti; gli altri vedono il mezzo. Anche qui **Stampa il risultato** e il registro attività.

## <a id="mezzi-multe"></a>Le multe (dalla 1.201.0)

Nella scheda del mezzo, linguetta **Multe**, ci sono i verbali del mezzo, dal più recente: quando, dove, l'importo, chi guidava, lo stato e, se è da pagare, entro quando. **Nuova multa** ne registra una; il clic su una riga la apre.

- **Il verbale**: numero, ente, giorno e ora dell'infrazione (l'unico dato che serve), dove, che cosa, importo, i **punti** tolti dalla patente e il giorno in cui è stato **notificato**. Sotto, il programma scrive i termini: da pagare entro 60 giorni dalla notifica, con il 30% in meno nei primi 5; con i punti, i dati di chi guidava da comunicare entro 60 giorni.
- **Chi guidava**: una persona del personale, cercata scrivendo il nome, la mansione o il reparto, oppure, se non è tra il personale, il suo nome. A chi vede le presenze di tutti, **Chi aveva il mezzo?** legge gli [utilizzi](#mezzi-utilizzi) al giorno e all'ora dell'infrazione e propone le persone: un clic sceglie chi guidava. **Dati comunicati il** chiude la scadenza della comunicazione.
- **Pagamento e addebito**: lo stato (da pagare, pagata, in ricorso, annullata) con il giorno e l'importo pagato; **A carico di chi**: da decidere, da addebitare a chi guidava, addebitata (con il giorno e l'importo) oppure a carico dell'azienda. Gli importi li vede e li scrive solo chi vede i costi dei mezzi: quando salva un collega senza questo permesso, restano quelli scritti.
- I **file** della multa (il verbale scansionato, la ricevuta del pagamento) stanno con lei, non tra quelli della scheda.

Con la data di notifica nascono le [scadenze](#mezzi-scadenze) del mezzo: *Multa n. …: pagamento* e, con i punti, *Multa n. …: dati del conducente*. Vanno nello [scadenzario](scadenze.md) con i promemoria, come le altre del mezzo, e risultano subito «in scadenza» per non perdere i 5 giorni della riduzione. La loro data viene dalla multa e si cambia lì. Seguono la multa: segnata pagata, o con i dati comunicati, la scadenza si chiude; in ricorso o annullata si chiude quella del pagamento, che durante il ricorso è sospeso (se il ricorso non va, si torna a «Da pagare» e la scadenza si riapre). Dallo scadenzario **Pagata** e **Dati comunicati** aprono la multa con il giorno di oggi già scritto, da controllare e salvare. Ogni passo resta nello storico del mezzo e nel registro attività.

## <a id="mezzi-multe-elenco"></a>Tutte le multe (dalla 1.202.0)

Nella pagina dei Mezzi la linguetta **Multe** mostra le multe di tutti i mezzi insieme, per sapere che cosa c'è da fare senza aprire un mezzo alla volta. Il numero sulla linguetta dice quante hanno ancora qualcosa da fare: da pagare, in ricorso, con i dati di chi guidava da comunicare o da addebitare a chi guidava.

- **In testa i numeri**: da pagare (con l'importo e il primo termine), in ricorso, dati di chi guidava da comunicare, da addebitare. Un clic su un numero mostra solo quelle; un altro clic torna a tutte.
- **I filtri**: la ricerca (verbale, mezzo, targa, luogo, chi guidava), lo stato, l'addebito, chi guidava (si scrive il nome e si sceglie; c'è anche «Chi guidava da indicare») e l'anno. In cima le multe con un termine più vicino.
- **In fondo il riepilogo scritto** di quelle a vista, per esempio: «2 multe per 223,00 €: 2 da pagare (223,00 €), la prima entro il 10/01/2027; da addebitare a Rossi Mario 50,00 €». Gli importi li vede solo chi vede i costi.
- Il clic su una riga apre la multa; con il tasto destro (o ⋯) si apre la scheda del suo mezzo. **Nuova multa**, il pulsante blu della linguetta, chiede prima di quale mezzo e poi apre la multa da compilare.
- **Stampa** stampa le multe a vista, con i filtri scritti sotto il titolo e il riepilogo in fondo (prima l'[anteprima](interfaccia.md#stampa)); **Esporta** le scrive in Excel o CSV, per esempio per chi prepara le buste paga.

## <a id="mezzi-tipi"></a>I tipi

**Tipi di mezzi** (o **Tipi di attrezzature**), in **Altro** nella pagina, elenca i tipi di mezzi (Autovettura, Furgone, Autocarro) o di attrezzature (Scala, Elettroutensile, Giuntatrice, Strumento di misura, DPI anticaduta, Piattaforma di lavoro elevabile) con le **scadenze che propongono** a un bene nuovo: per ognuna ogni quanti mesi (e, per i mezzi, km) si ripete, **la prima** (facoltativa: dopo quanti mesi dall'immatricolazione o dall'acquisto cade la prima volta), il preavviso e se si conta **dal fatto**. Cambiare un tipo non tocca i beni già creati; eliminandolo, i beni restano senza tipo con le loro scadenze. Ogni tipo ha anche **icona e colore**, che prendono i beni senza foto e senza un'icona loro (vedi [Icone e colori](interfaccia.md#interfaccia-icone)). Li gestisce chi ha il permesso **Gestire i tipi e i responsabili**.

> [!NOTE]
> **Le periodicità proposte sono indicative.** Revisione, verifiche delle attrezzature e tarature dipendono dal codice della strada, dalle norme (per esempio D.Lgs. 81/2008 per le attrezzature di lavoro), dal costruttore e dall'uso: verificale con il libretto, il manuale o il vostro consulente per la sicurezza e correggile nei tipi o nelle singole scadenze.

## <a id="mezzi-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere mezzi e attrezzature | I due elenchi e le schede, con scadenze, manutenzioni, consegne, file e storico; le loro scadenze nello scadenzario. |
| Gestire mezzi e attrezzature | Creare e modificare le schede, consegnare e ritirare, registrare km, manutenzioni e scadenze fatte, caricare i file; ricevere i promemoria delle loro scadenze quando l'elenco non ha [responsabili](#mezzi-responsabili). |
| Costi di mezzi e attrezzature | Vedere il costo di manutenzioni e interventi e la spesa totale di ogni scheda; con la gestione anche scriverlo. Senza, le voci dello storico si vedono e si registrano senza il costo (quello già scritto resta). Sono [dati riservati](gruppi-policy.md#policy-riservati). |
| PIN delle carte carburante | Vedere e copiare il [PIN della carta carburante](#mezzi-pin) di ogni mezzo; con la gestione anche scriverlo e cambiarlo. Ogni lettura resta nello storico del mezzo. Senza, il PIN non compare e non si può cambiare. È un [dato riservato](gruppi-policy.md#policy-riservati). |
| Eliminare mezzi e attrezzature | Eliminare una scheda con le sue scadenze, lo storico e i file. |
| Gestire i tipi e i responsabili | I [tipi](#mezzi-tipi) con le scadenze che propongono e i [responsabili](#mezzi-responsabili) di mezzi e attrezzature. |

---

[← Indicatori](indicatori.md) · [Indice](README.md) · [Banca →](banca.md)
