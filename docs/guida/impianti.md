[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="impianti"></a>Impianti

**Progettazione → Impianti** raccoglie ciò che è **installato presso i clienti**, sede per sede: un antintrusione, una videosorveglianza, un controllo accessi, un impianto KNX, un fotovoltaico, un quadro elettrico. È lo stesso ordine con cui si tengono i lavori sul PC (*clienti / cliente / sede / impianto*, con dentro il leggimi, le configurazioni e i backup), ma in un posto solo e con i permessi: quelle cartelle si portano dentro con [Da una cartella del PC](#impianti-cartella). La pagina compare a chi può **Vedere gli impianti** (vedi [Permessi](#impianti-permessi)).

> [!TIP]
> **La commessa finisce, l'impianto resta.** Una [commessa](progetti.md) è il lavoro che realizza o modifica un impianto e prima o poi si chiude; l'impianto rimane presso il cliente, con il suo storico, e si continua a seguirlo: il suo [piano di manutenzione](manutenzioni.md#manutenzioni-piano), i rapporti, le riparazioni e le modifiche ([interventi](#impianti-interventi)), anche senza commessa.

## <a id="impianti-pagina"></a>L'elenco e la pagina dell'impianto

Le linguette **In servizio** e **Dismessi** elencano gli impianti che vedi: in evidenza il **cliente** (l'impianto è suo), sotto il nome dell'impianto con il tipo (anche nel colore dell'icona), poi la sede, le commesse collegate e la data di installazione. La ricerca trova nome, cliente, sede, tipo e commesse; il filtro mostra un tipo, o quelli senza tipo. In alto **Nuovo impianto** e, in **Altro**, **Stampa**, **Tipi di impianto** (l'elenco dei [tipi](#impianti-tipi)) e **Modelli delle schede tecniche** (i [modelli](#impianti-modelli)). Un clic su un impianto apre la sua **pagina**:

- in testa cliente (un clic apre la sua scheda), sede, tipo, stato, data di installazione e le **commesse** collegate, con i pulsanti **Condividi** (un link alla [documentazione dell'impianto](condivisioni.md#condivisioni-impianto), anche come etichetta con il QR code), **Stampa** (scheda, Leggimi e interventi), **Elimina**, **⋯** (nuovo intervento, cartella in Documenti, scheda del cliente, **Duplica**) e **Modifica**;
- **Leggimi**: quello che serve sapere prima di intervenire;
- **Scheda tecnica**: i [dati tecnici](#impianti-scheda-tecnica) dell'impianto, parte per parte (EVAC, TVCC…), con i dispositivi;
- **Interventi**: le [attività collegate](#impianti-interventi), con il numero di quelle ancora aperte;
- **Certificazioni**: le sue [dichiarazioni](certificazioni.md) (conformità, rispondenza, quadri…), con **Nuova certificazione**, per chi può vederle;
- **Manutenzioni**: il suo [piano di manutenzione](manutenzioni.md#manutenzioni-piano) e i [rapporti](manutenzioni.md#manutenzioni-rapporti) degli interventi, per chi può vedere le manutenzioni;
- **Assistenza**: le sue [richieste di assistenza](assistenza.md), con **Nuova richiesta** già compilata con il cliente e l'impianto, per chi può vedere l'assistenza;
- **Documenti**: la [cartella dell'impianto](#impianti-sedi);
- **Password**: le password collegate al cliente (accessi alla centrale, al router, al cloud del costruttore), per chi usa la [gestione password](password.md#password-clienti);
- **Storico**: chi ha cambiato che cosa (dati, sede, stato, commesse collegate, cartella, scheda tecnica, interventi, certificazioni create, emesse, annullate ed eliminate).

L'indirizzo della pagina (`#/installations?installation=…`) si può mandare a un collega. La pagina si aggiorna da sola quando un collega cambia l'impianto o i suoi interventi; gli impianti si trovano anche con la [ricerca](ricerca.md).

## <a id="impianti-scheda"></a>La scheda dell'impianto

- **Cliente**: presso cui è installato. Dopo la creazione non si cambia: l'impianto, la sua cartella e il suo storico appartengono a quel cliente.
- **Sede**: una delle sedi della scheda del cliente, da cercare scrivendo, anche tra decine di punti vendita (vedi [Sedi e cartelle](#impianti-sedi)). Si può lasciare vuota.
- **Tipo** e **Nome**: il nome è una descrizione per riconoscere l'impianto (marca, modello o dove sta: *Ksenia Lares 4.0*, *TVCC parcheggio*); lasciato vuoto, diventa quello del tipo. La cartella in Documenti si chiama come il **tipo** (*Antintrusione*), come sul PC, non come il nome (dalla 1.143.5); un secondo impianto dello stesso tipo nella stessa sede prende un numero (*Antintrusione 2*), e la cartella si può sempre rinominare in Documenti.
- **Icona e colore**: per riconoscere l'impianto negli elenchi e in testa alla sua pagina. Senza, vale quella del tipo (vedi [Icone e colori](interfaccia.md#interfaccia-icone)).
- **Stato**: **In servizio** oppure **Dismesso** (smontato o sostituito: resta, con tutto il suo storico, nella linguetta Dismessi). **Installato il**: la data, anche lontana nel passato.
- **Leggimi**, con testo formattato e ✨ [Migliora testo](assistente-ai.md#assistente-moduli): com'è fatto l'impianto, dove sono centrale e apparati, accorgimenti, contatti sul posto.
- **Commesse collegate**: si cercano per codice o nome, prima quelle del cliente.
- Per un impianto nuovo la casella **Crea la cartella in Documenti**, spuntata, crea subito la sua cartella; altrimenti la crea poi **Crea la cartella**, nella scheda o nella linguetta Documenti.

**Duplica**, in fondo alla scheda o nel menu **⋯**, apre un impianto nuovo già compilato come questo (stesso cliente, sede, tipo, Leggimi e commesse, nome con «(copia)»): comodo per lo stesso impianto in più sedi. **Elimina** toglie l'impianto con il suo Leggimi e il suo storico: gli interventi restano, senza impianto, e la cartella resta in Documenti; il suo piano di manutenzione se ne va con lui. Un impianto con [certificazioni](certificazioni.md) nel registro o con [rapporti di manutenzione](manutenzioni.md#manutenzioni-rapporti) non si elimina: se è stato smontato, mettilo **Dismesso**. Se due persone modificano lo stesso impianto insieme, il secondo salvataggio chiede di riaprire la scheda per vedere la versione aggiornata.

## <a id="impianti-scheda-tecnica"></a>La scheda tecnica

La linguetta **Scheda tecnica** della pagina dell'impianto raccoglie i suoi dati tecnici, divisi in **parti**: una per ogni sistema, da un [modello](#impianti-modelli) (EVAC, TVCC, Antintrusione…). Un impianto può averne più d'una, per esempio TVCC ed EVAC nello stesso punto vendita, anche due dello stesso modello (*TVCC 2*, che puoi rinominare *TVCC parcheggio*).

- **Proposte del tipo** aggiunge le parti che il tipo dell'impianto propone (Videosorveglianza → TVCC); **Aggiungi una parte** sceglie un qualsiasi modello e apre subito la parte da compilare.
- Ogni parte mostra le **sezioni singole** come elenco di dati (la centrale, il registratore, l'accesso da remoto) e le **sezioni ripetibili** come tabelle, una riga per dispositivo (le telecamere, le zone, gli amplificatori), con le sole colonne che hanno qualcosa di scritto.
- **Modifica** apre la parte: il nome, i campi delle sezioni singole e, per le ripetibili, una scheda per riga con **Aggiungi** (per esempio *Aggiungi telecamera*), per spostarla, per duplicarla (comodo per telecamere tutte uguali) e 🗑 per toglierla; in fondo le note. Le righe lasciate vuote non si salvano.
- Dal menu ⋯ della parte: **Sposta su**, **Sposta giù** e **Togli la parte**, con tutti i suoi dati.
- **Stampa**, in alto, apre l'anteprima della scheda tecnica con il [modello di stampa](modelli-stampa.md) delle schede tecniche: il cliente, la sede e ogni parte con le sue tabelle, da allegare alla documentazione dell'impianto.

Mentre scrivi, ogni campo di testo propone i valori già scritti nello stesso campo delle altre schede, prima quelli delle parti dello stesso modello; uscendo dal campo, il valore prende le maiuscole del campo (la marca come le aziende, il modello e il numero di serie maiuscoli…: vedi [Maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato)).

La compila chi può **Modificare gli impianti**; chi può vederli la consulta. I valori si trovano con la [ricerca](ricerca.md): un indirizzo IP, una matricola o un modello portano all'impianto, con il punto della scheda in cui sono scritti.

> [!NOTE]
> **Password nella scheda tecnica.** Un modello può avere campi **Password**: nella scheda restano nascoste (*••••••*), con l'occhio 👁 per vederle e il pulsante per copiarle; si salvano cifrate e non vanno mai nella stampa, nei link condivisi con i clienti, nella ricerca né tra i suggerimenti. Le vede chi vede l'impianto: le credenziali da dare solo ad alcune persone vanno nella linguetta **Password**, con i suoi permessi.

## <a id="impianti-sedi"></a>Sedi e cartelle

- Le **sedi** sono gli [indirizzi della scheda del cliente](clienti.md#clienti-contatti), ciascuno con la sua etichetta: *Casa città* e *Casa al mare* per una persona, *PV 01*, *PV 02*, *Magazzino* per un'azienda. Un impianto resta legato alla sua sede anche se ne cambi il nome o l'indirizzo; se la sede viene tolta dalla scheda del cliente, l'impianto la mostra com'era scritta, con una nota, finché non ne scegli un'altra.
- La **cartella** dell'impianto nasce in Documenti con lo stesso ordine del PC: **Documenti → Clienti → *cliente* → *sede* → *tipo dell'impianto***, con dentro le sottocartelle del suo [tipo](#impianti-tipi) (per un KNX: *Configurazioni/ETS*, *Configurazioni/Home Assistant* e *Backup*). Senza sede, la cartella dell'impianto sta direttamente in quella del cliente. Le cartelle del cliente e delle sedi nascono con il primo impianto e servono anche ai successivi; quella del cliente è collegata al cliente.
- Se il cliente è un [contatto privato](clienti.md#clienti-privati), la sua cartella è riservata al proprietario, e si riallinea da sola se la scheda diventa condivisa o cambia proprietario.
- Eliminando l'impianto la cartella resta in Documenti, con i suoi file.

## <a id="impianti-cartella"></a>Da una cartella del PC

**Da una cartella** , nella pagina Impianti (o nella linguetta **Impianti** della scheda di un cliente, per quel cliente), porta nella piattaforma il lavoro tenuto finora nelle cartelle del PC: scegli o trascini una cartella, con tutte le sottocartelle, e ne escono il cliente, i suoi impianti con il Leggimi e la scheda tecnica, le password e i file. Compare a chi può **Creare impianti**.

1. **La cartella**: dai nomi delle cartelle si capisce che cosa c'è.
   - *Rossi Mario\\Antintrusione*: **un impianto**. Il tipo viene dal nome (Antintrusione, TVCC o Videosorveglianza, Allarme, Rete o Router, KNX o Home Assistant, Citofonia…); una cartella con dentro *configurazioni*, *backup* o un *leggimi* (anche *INFO.txt*) è un impianto anche se il nome non dice il tipo. I nomi scritti tutti in maiuscolo diventano normali (*ANTINTRUSIONE* → *Antintrusione*), le sigle restano (*KNX*, *TVCC*).
   - *Rossi Mario*, con dentro *Antintrusione* e *Videosorveglianza*: **un cliente con i suoi impianti**; le altre sottocartelle (le foto, i contratti) sono i file del cliente. Una sottocartella con impianti dentro (*Rossi Mario\\Casa al mare\\Citofonia*) è una **sede**.
   - **Il nome della cartella** si divide dove c'è un trattino tra spazi: *ROSSI SRL - FILIALE NORD - BERGAMO* propone il cliente *Rossi S.r.l.* con la sede *Filiale Nord* a *Bergamo*; *PIZZERIA CENTRALE - MONZA* il cliente e la città. I nomi scritti tutti in maiuscolo diventano come nelle schede (*SAN LORENZO* → *San Lorenzo*; le sigle come KNX, UPS e NVR restano). È solo una proposta: nella revisione la correggi.
   - **Un cliente o un impianto?** Se la cartella non ha il nome di un tipo e dentro non ci sono cartelle di impianti (per esempio solo un *INFO.txt* e qualche file), si chiede che cos'è. Da **cliente**, gli impianti vengono dalle sezioni dei suoi file INFO (*\*\*\* NVR Hikvision \*\*\** → Videosorveglianza) e dai file con il nome di un tipo (*ROUTER.txt* → Rete dati, di cui diventa il Leggimi; *TVCC.7z* → Videosorveglianza): uno per tipo, da togliere nella revisione se non serve.
   - **Cartelle da riconoscere**: se il cliente ha sottocartelle che non hanno il nome di un tipo (per esempio *CENTRALINO*) e non sono le solite cartelle di documenti (Foto, Contratti, Preventivi…), prima della lettura si sceglie per ognuna se restano **file del cliente** oppure sono un **impianto** di uno dei tipi che ci sono o di un **tipo nuovo**, con il nome della cartella: il tipo nuovo si crea con l'importazione (a chi può gestire i [tipi](#impianti-tipi)) e vale anche per i clienti che si importano dopo. Colore, cartelle e modelli della scheda tecnica gli si danno poi da **Impianti → Tipi**.
   - *Clienti*, con una cartella per cliente: **una cartella di clienti**. Si vede l'elenco, con chi è già in anagrafica, e si importano uno alla volta (alla fine si torna all'elenco). Se invece sono le sedi di un solo cliente, lo dici con il link nell'avviso.
2. **La lettura**: i documenti (PDF, Word, Excel, file di testo) si leggono nel browser, i più utili prima (i Leggimi), fino a 60. Vi si trovano indirizzi IP e MAC, matricole e modelli, partite IVA e codici fiscali, email, telefoni, indirizzi, utenti e password; i dati della tua azienda (che compaiono, per esempio, nelle DiCo) non si propongono come quelli del cliente. **Ferma** torna indietro.
3. **L'assistente** ✨, se c'è (vedi [Assistente AI](assistente-ai.md)), legge per ogni impianto un riassunto: i nomi dei file e il testo dei documenti, con le password sostituite da segnaposto (le password non gli arrivano mai). Con un server esterno, come Google Gemini, quel riassunto va al suo servizio: per le cartelle dei clienti vale ciò che hai deciso per l'assistente. Propone i dati del cliente, il nome e il tipo dell'impianto e i valori della scheda tecnica, campo per campo. Si tengono solo i campi dei modelli e i valori che passano gli stessi controlli dei moduli; partita IVA, codice fiscale, email e telefono valgono solo se sono scritti davvero nei documenti. Con molti documenti conviene un contesto più grande (8.192 o più, in [Impostazioni → Assistente AI](impostazioni.md#impostazioni-ai)): ciò che non entra resta fuori, e la revisione lo dice. Senza l'assistente i dati vengono dal nome delle cartelle e da quelli trovati nei testi.
4. **La revisione**: tutto si controlla e si corregge prima di creare.
   - **Cliente**: quello già in anagrafica (trovato con la partita IVA, il codice fiscale o il nome; puoi sceglierne un altro) oppure uno nuovo, con i dati proposti e, accanto a ogni dato, il file da cui viene. Un **omonimo**, cioè un cliente con lo stesso nome ma un codice fiscale o una partita IVA diversi da quelli dei documenti, non si propone: si propone un cliente nuovo, e l'avviso lo dice. L'**indirizzo** e le **sedi** (a sinistra il nome della sede, poi l'indirizzo) hanno la stessa riga delle schede dei clienti: la lente nel campo della via cerca l'indirizzo completo, con CAP, città e provincia (se un amministratore ha attivato la [ricerca degli indirizzi](impostazioni.md#impostazioni-indirizzi)), e la città propone i comuni con il loro CAP.
   - **Impianti**: per ognuno tipo, nome, sede (per un cliente nuovo il suo indirizzo, o la sede della sottocartella; per uno in anagrafica una delle sue sedi), data di installazione (proposta dai file, con accanto quello da cui viene: la data scritta nella prima riga del file INFO o Leggimi, come *12/03/2021*, la data nel nome delle foto, come *IMG\_20230915\_…* o *WhatsApp Image 2023-09-15 …*, oppure la data di modifica dei file di lavoro, come configurazioni, backup e disegni; vale la più vecchia, e PDF, Word ed Excel non contano, perché spesso sono manuali e schede del produttore), Leggimi (il testo del file leggimi o INFO), i valori proposti per la scheda tecnica (ognuno con la spunta e il file da cui viene) e i file da caricare. Togli la spunta all'impianto per non importarlo. Per un impianto senza tipo, nell'elenco dei tipi c'è anche **Nuovo tipo** con il nome della cartella.
   - **Password trovate**: nome, utente e password (anche PIN, codici installatore e chiavi di cifratura dei backup), da salvare nella [gestione password](password.md) collegate al cliente, come tue: da lì si condividono con i colleghi. Il nome viene da ciò che le accompagna (*Codice installatore*, *Password utente*) o dal titolo del documento (*NVR Hikvision DS-7616NI-K2*). Quelle che salvi nel Leggimi dell'impianto diventano *••••••*: restano solo nella gestione password, cifrate (il file originale, se lo carichi, resta com'è).
   - **I file INFO**: si leggono con gli [schemi dei file](#impianti-schemi). Con quello iniziale, a sezioni (*\*\*\* NVR Hikvision \*\*\**, oppure un titolo con sotto una riga di trattini) e righe *chiave: valore*, se ne leggono le credenziali: *auth: utente / password* (altri utenti sulle righe sotto, rientrate), *auth ssh*, *hik account*, *account Google*, *ezcloud*; *ssid: rete / password* (o *ssid* e sotto *pass*, *key*, *password wifi*); *user* o *email* con la password nella riga sotto; *pin*, *puk*, *installer*, *verifica*, *code hikconnect*, *segno sblocco*; la password dentro un indirizzo *rtsp://utente:password@…*. Ogni utente è una voce della gestione password, con il titolo della sezione e il collegamento all'indirizzo della sezione (*ip*, *ip lan*, *web*). Le sezioni del file INFO del cliente, con le loro password, vanno all'impianto del tipo che il titolo indica (*NVR*, *Hikvision* → Videosorveglianza; *TecnoAlarm*, *Ksenia* → Antintrusione; *Router*, *AP*, *Unifi* → Rete dati; *Home Assistant* → KNX e domotica) e finiscono nel suo Leggimi. Undici cifre sono una partita IVA solo con *P.IVA*, *partita IVA* o *VAT* sulla riga (o su quella sopra) oppure con *IT* davanti: un numero di telefono fisso di 11 cifre non lo diventa per caso.
   - **Telecamere e registratori**: dalle foto salvate dagli strumenti Hikvision, che hanno nel nome modello, numero di serie e indirizzo IP (*DS-2CD1043G2-I2025…\_192.168.1.64.jpg*), e dagli elenchi dei dispositivi in Excel (la *Lista Dispositivi*, con indirizzo IP, modello, numeri di serie, firmware, MAC, utente e password) si compilano le righe **Telecamere** e **Registratori** della scheda tecnica: marca, modello, indirizzo IP, numero di serie, firmware, posizione (il nome del canale) e il MAC nelle note. Una telecamera con lo stesso indirizzo IP in più file (o già proposta dall'assistente) è una riga sola. Utenti e password dell'elenco vanno nelle **Password trovate**, una voce per ogni coppia utente e password con un collegamento a ciascun dispositivo; all'assistente arrivano solo i segnaposto.
   - **File**: all'inizio sono scelti tutti; la casella di una cartella sceglie o toglie tutti i suoi file. In fondo alla finestra, quanti file si caricano e quanto pesano.
   - **Dati trovati nei documenti**: IP, MAC, matricole, email, telefoni… con il file da cui vengono e il pulsante per copiarli, utili per completare la scheda tecnica.
   - **Elimina dal PC dopo il caricamento**: vedi [Eliminare gli originali dal PC](documenti.md#documenti-originali).
5. **Importa** crea, nell'ordine, il cliente (se è nuovo), gli impianti con la loro cartella in Documenti, la scheda tecnica e le password; poi carica i file: quelli degli impianti nelle loro cartelle (con le stesse sottocartelle; *configurazioni* e *backup* prendono i nomi del [modello del tipo](#impianti-tipi)), quelli del cliente nella cartella del cliente. I passi si vedono uno per uno; i caricamenti continuano nella [campanella](notifiche.md#notifiche-campanella) anche chiudendo la finestra.

> [!NOTE]
> Le scansioni senza testo (i PDF fatti con lo scanner) non si leggono durante l'analisi: dopo l'importazione si rendono leggibili con il [riconoscimento del testo](documenti.md#documenti-ocr), dalla scheda del file in Documenti.

## <a id="impianti-schemi"></a>Schemi dei file

Ognuno scrive i file di testo delle cartelle a modo suo: tu con le sezioni *\*\*\* NVR Hikvision \*\*\** e *auth: utente / password*, un collega magari con altri segni e altre parole. Uno **schema** lo descrive, e serve due volte: le sue **istruzioni** le legge l'assistente quando analizza una cartella, per capire titoli, chiavi e valori; le sue **parole** guidano la lettura delle password nel browser (all'assistente le password non arrivano mai). Si aprono da **Impianti → Da una cartella → Schemi dei file**; li cambia chi può gestire i [tipi d'impianto](#impianti-tipi), gli altri li vedono.

- **Nome** e **Attivo**: valgono tutti gli schemi attivi insieme (le loro parole si sommano).
- **Istruzioni per l'assistente**: come sono fatti i file, che cosa vuol dire ogni chiave, dove stanno utenti e password.
- **Segni dei titoli delle sezioni**: per esempio *\*\*\** o *[[*; un titolo con sotto una riga di trattini vale sempre.
- **Chiavi con utente e password** (*auth*, *account*…: basta la parola dentro la chiave, quindi vale anche *auth ssh*), **Reti Wi-Fi** (*ssid*…), **Password** (da sole: vanno alla rete o all'utente della riga sopra), **Codici** (*pin*, *puk*, *verifica*…) e **Utente** (con la password nella riga sotto), separate da virgole.
- **Esempio, con valori inventati**: un file scritto come si fa davvero; l'**anteprima** sotto mostra le password che lo schema vi trova, con il titolo della sezione, l'utente e il collegamento al dispositivo.
- **Nuovo**, **Duplica** (per partire da uno che c'è) e **Elimina**; tutto si salva con **Salva**.
- ⬇ esporta lo schema aperto o tutti in un file e ⬆ importa gli schemi da un file di un altro server (vedi [Modelli tra server](impostazioni.md#impostazioni-modelli)): si esporta ciò che è salvato.

## <a id="impianti-interventi"></a>Interventi

- Un **intervento** è un'[attività](attivita.md) collegata all'impianto: l'installazione, una manutenzione, una riparazione, una modifica. Nella [scheda dell'attività](attivita.md#attivita-scheda) il campo **Impianto**, sotto Commessa e Cliente, propone gli impianti del cliente scelto, prima quelli in servizio e poi i dismessi.
- La linguetta **Interventi** della pagina dell'impianto li elenca tutti, anche quelli di commesse già chiuse, con stato, priorità, persone e scadenza; **Nuovo intervento** crea un'attività già collegata al cliente e all'impianto. Come sempre, ognuno vede gli interventi che può vedere.
- Collegare o togliere l'impianto resta nello storico dell'attività e in quello dell'impianto; un'attività che si ripete porta l'impianto anche nelle volte successive.
- Le manutenzioni periodiche hanno il loro [piano](manutenzioni.md): **Pianifica** ne fa un intervento, e nella scheda di quell'attività **Registra il rapporto** la chiude. Allo stesso modo le [richieste di assistenza](assistenza.md#assistenza-interventi) pianificate: **Registra l'intervento**.

## <a id="impianti-progetti"></a>Impianti e commesse

- Un impianto si collega alle commesse che lo hanno realizzato o modificato dalla sua scheda (**Commesse collegate**) oppure dalla pagina della commessa, linguetta **Impianti**: lì **Nuovo impianto** ne crea uno presso il cliente della commessa, già collegato, **Collega un impianto del cliente** sceglie tra quelli che ci sono e la **×** lo scollega (l'impianto resta).
- Collegamenti e scollegamenti compaiono nello storico della commessa e in quello dell'impianto. Una commessa [riservata](progetti.md#progetti-scheda) compare tra le commesse di un impianto solo a chi la vede.

## <a id="impianti-tipi"></a>Tipi di impianto

Il **tipo** si sceglie da un elenco uguale per tutti (per esempio Antintrusione, Videosorveglianza, Controllo accessi, Antincendio, Rete dati, KNX e domotica, Fotovoltaico, Elettrico e quadri, Citofonia: in un'installazione nuova l'elenco è vuoto, ognuno scrive i suoi). Chi ha il permesso **Gestire i tipi di impianto** trova **Tipi di impianto** nel menu **Altro** della pagina Impianti, e anche di Assistenza e Manutenzioni, dove il tipo si sceglie: aggiunge, rinomina, sceglie icona e colore ed elimina i tipi nel pannello dei [tipi e delle categorie](interfaccia.md#interfaccia-tipi) (eliminandone uno, i suoi impianti restano senza tipo) e, con il pulsante accanto a ciascuno, ne scrive il **modello delle cartelle**: una per riga, con «/» per le sottocartelle (*Configurazioni/Centrale*). Il modello vale per gli impianti creati da lì in avanti: le cartelle di quelli che ci sono già non cambiano. Nella scheda del tipo (clic sulla riga) si sceglie l'**icona** (vedi [Icone e colori](interfaccia.md#interfaccia-icone)), che prendono gli impianti senza un'icona loro. Con il pulsante si scrivono le [manutenzioni proposte](manutenzioni.md#manutenzioni-tipi) dal tipo; le parti della scheda tecnica che propone si scelgono nei [modelli](#impianti-modelli). Con ⬇ un tipo si esporta in un file (cartelle, manutenzioni proposte, icona e modelli proposti per nome) e in fondo **Esporta tutti** e **Importa…** portano i tipi su un altro server: vedi [Modelli tra server](impostazioni.md#impostazioni-modelli).

## <a id="impianti-modelli"></a>I modelli delle schede tecniche

**Modelli delle schede tecniche**, in **Altro** nella pagina Impianti, elenca i modelli per chi può **Gestire i tipi di impianto**, con quante sezioni e campi hanno, in quante schede sono usati e per quali tipi d'impianto sono proposti (in un'installazione nuova non ce ne sono: si creano qui o si importano da un altro server). **Proposti…** (dalla 1.121.0) aggiunge i modelli pronti che mancano, per esempio **Wallbox** (punto di ricarica, protezioni e misura, rete e gestione dei carichi, tessere RFID), anche con il tipo d'impianto che non c'è ancora. **Nuovo modello** ne crea uno, lo duplica, ⬇ lo esporta in un file e **Importa…** ed **Esporta tutti** portano i modelli su un altro server (vedi [Modelli tra server](impostazioni.md#impostazioni-modelli)). La scheda di un modello ha tre linguette:

- **Generale**: nome, colore, **icona e colore** (in testa a ogni parte della scheda tecnica), descrizione e i **tipi d'impianto che lo propongono**.
- **Sezioni**: nell'ordine in cui si compilano, ognuna **Singola** (si compila una volta per impianto) o **Ripetibile** (una riga per dispositivo; *Ogni riga è* dice come si chiama, per esempio *Telecamera*). Ogni campo ha un **tipo** (nella tabella qui sotto), il valore proposto e il suggerimento sotto il campo; nelle sezioni singole anche i titoli, per dividere i campi. Per i testi, **Maiuscole** sceglie come si sistema il valore: *Automatiche* le ricava dall'etichetta (Marca come le aziende, Modello come i modelli, Numero di serie tutto maiuscolo…), *Come si scrive* lo lascia com'è, oppure un formato preciso (frase, nomi di persona, aziende e marche, modelli, codici, indirizzi, comuni, email); per i testi su più righe solo la prima lettera.
- **Anteprima**: la parte come si compila, con i valori proposti.

I tipi dei campi: quando si compila la scheda, il valore si controlla secondo il tipo (bordo rosso se è sbagliato) e si scrive sempre nello stesso modo. Gli stessi tipi, tranne la password, valgono per le [certificazioni](certificazioni.md#certificazioni-modelli).

| Tipi | Come si compilano |
| --- | --- |
| Testo, Testo su più righe | Testo libero, con le **Maiuscole** scelte. |
| Numero con decimali, Numero intero | Con l'**unità** facoltativa (W, kWp, porte, giorni); il numero intero non ha decimali e si può scrivere con i punti delle migliaia (*1.000*). |
| Importo (€) | Con al massimo due decimali: l'ultimo punto o virgola è quello dei decimali (*1.234,50*, *1234.5*); si mostra con il simbolo dell'euro. |
| Data, Ora | Con il calendario e l'orologio del browser. |
| Email, Telefono, Sito web o link | Controllati come nell'anagrafica; in lettura sono link da cliccare. |
| Codice fiscale, Partita IVA | Con il controllo del carattere finale; la partita IVA anche con «IT» davanti. |
| Indirizzo IP, Indirizzo MAC | IPv4 o IPv6, anche una rete con il prefisso (*192.168.1.0/24*); il MAC, con o senza separatori, diventa *00:11:22:AA:BB:CC*. |
| Coordinate GPS | Latitudine e longitudine, oppure il link di Google Maps o di OpenStreetMap; in lettura si aprono sulla mappa. |
| Password (nascosta) | Solo nelle schede tecniche: nascosta mentre si scrive e in lettura, salvata cifrata, mai stampata né condivisa; senza valore proposto. |
| Una scelta, Più scelte, Casella (sì/no) | Tra le voci scritte nel modello; la casella si spunta. |

Le modifiche valgono anche per le schede già compilate. Rinominare un campo o una sezione non perde nulla; togliendoli, i valori già scritti restano nella parte (in fondo, *dati di campi tolti dal modello*) finché nella sua finestra non si sceglie **Toglili**. Un modello usato da qualche scheda non si elimina.

## <a id="impianti-importa"></a>Importare ed esportare

**Esporta** scarica in **Excel** o **CSV** gli impianti mostrati, scelti o tutti: cliente (con il codice davanti), nome, tipo, sede, stato, data di installazione e Leggimi. **Importa** (a chi crea gli impianti) li porta da un foglio, una riga per impianto. Il foglio si legge come una tabella di database: la prima riga ha i nomi dei campi, sotto una riga per scheda. Le colonne con il nome giusto si riconoscono da sole; **Scarica il modello Excel** dà il foglio già pronto con le istruzioni, e un file esportato da qui si reimporta così com'è (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Prima di importare l'anteprima mostra ogni riga: quelle già presenti si saltano, quelle con errori dicono perché.

- Il **cliente** si riconosce dal codice, dalla partita IVA, dal codice fiscale o dal nome com'è in anagrafica (anche senza la forma societaria): deve esserci, altrimenti la riga non si importa.
- Il **tipo** si cerca tra i tipi degli impianti, la **sede** tra quelle del cliente (via o città). Quello che non si trova finisce nel Leggimi, sotto «Da controllare». Ogni impianto nuovo ha la sua cartella in Documenti.

## <a id="impianti-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere gli impianti | Aprire la pagina Impianti e vedere gli impianti dei clienti condivisi e dei propri contatti privati, con il Leggimi e la scheda tecnica; documenti, interventi e password si vedono secondo i propri diritti. |
| Creare impianti | Nuovi impianti presso i clienti, con la loro cartella in Documenti. |
| Modificare gli impianti | Modificare la scheda, il Leggimi e la scheda tecnica di qualsiasi impianto visibile, crearne la cartella e collegarlo alle commesse. |
| Eliminare gli impianti | Eliminare un impianto: interventi e cartella in Documenti restano. |
| Gestire i tipi di impianto | Aggiungere, rinominare, colorare ed eliminare i tipi di impianto con il loro modello di cartelle, e i modelli delle schede tecniche, uguali per tutti. |

Le cartelle degli impianti le crea la piattaforma, senza il permesso di caricare documenti; per vederne i file serve **Visualizzare i documenti**. Gli amministratori possono tutto.

---

[← Commesse](progetti.md) · [Indice](README.md) · [Certificazioni →](certificazioni.md)
