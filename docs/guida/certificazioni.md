[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="certificazioni"></a>Certificazioni

**Commesse → Certificazioni** è il **registro delle dichiarazioni degli impianti**: la dichiarazione di conformità (**DiCo**), la dichiarazione di rispondenza (**DiRi**), la dichiarazione di conformità del **quadro elettrico** e gli altri modelli che servono all'azienda. Al posto delle cartelle per anno, ogni certificazione ha un **numero** per modello e anno (*DiCo 12/2026*), appartiene a un [impianto](impianti.md) (e quindi a un cliente e a una sede), si compila con i campi del suo modello, raccoglie allegati e copia firmata nella cartella dell'impianto e si **stampa pronta da firmare**. La pagina compare a chi può **Vedere le certificazioni** (vedi [Permessi](#certificazioni-permessi)).

> [!TIP]
> **Bozza, emessa, annullata.** In **bozza** la certificazione si compila e segue il modello e i dati di adesso. **Emessa**, dati, testo del modello, dati dell'azienda e del cliente e allegati spuntati si fermano: ristampata anche dopo anni, è identica a quella firmata. **Annullata**, resta nel registro con il suo numero e il motivo.

## <a id="certificazioni-registro"></a>Il registro

Le linguette **Tutte**, **Bozze**, **Emesse** e **Annullate** dicono quante ce ne sono; il filtro sceglie un modello o un anno, la ricerca trova numero, cliente, impianto, sede e progetto. Ogni riga ha numero e modello, data, impianto con cliente e sede, stato e, a finestra larga, gli **allegati** presenti su quelli previsti (con se manca uno «sempre necessario») e **firmata** se c'è la copia firmata. In alto **Stampa** (il registro come lo stai guardando), **Modelli** (per chi li gestisce, vedi [Modelli](#certificazioni-modelli)) e **Nuova certificazione**. Un clic apre la scheda; il tasto destro o **⋯** stampa, apre la pagina dell'impianto o la cartella in Documenti, duplica, elimina.

Le certificazioni di un impianto si trovano anche nella linguetta **Certificazioni** della [pagina dell'impianto](impianti.md#impianti-pagina), e quelle di un progetto nella linguetta **Certificazioni** della [pagina del progetto](progetti.md#progetti-pagina): da lì **Nuova certificazione** parte già dall'impianto (dal progetto si sceglie tra i suoi impianti). La pagina si aggiorna da sola quando un collega cambia una certificazione, e le certificazioni si trovano con la [ricerca](ricerca.md) (anche per numero: *DiCo 12/2026*).

## <a id="certificazioni-scheda"></a>La scheda della certificazione

- **Nuova certificazione**: si sceglie il modello (DiCo, DiRi, quadro…) e, partendo dal registro, si cerca l'impianto scrivendo il suo nome, il cliente o la sede. I campi si compilano da soli con i dati dell'impianto (committente, comune, via e civico della sede, proprietà…) e con quelli scritti una volta nel modello (dichiarante, responsabile tecnico).
- **Impianto**: dopo la creazione non si cambia. **Numero** e **Data**: vedi [Numeri e date](#certificazioni-numeri). **Progetto**: facoltativo, tra i progetti collegati all'impianto; la certificazione compare anche nella pagina del progetto.
- I **campi del modello**, divisi in sezioni; quelli con l'\* vanno compilati prima di emettere. Sotto un campo può esserci un suggerimento su che cosa scrivere; mentre scrivi, i campi di testo propongono i valori già scritti nelle altre certificazioni, prima quelle dello stesso modello, e uscendo dal campo il valore prende le maiuscole del campo.
- **Note interne**: per l'ufficio (consegna al cliente, deposito, promemoria). Non vanno in stampa.
- Le linguette **Allegati** (vedi [Allegati](#certificazioni-allegati)), **Anteprima** (il foglio come esce in stampa, con quello che è scritto nella scheda anche prima di salvare) e **Storico**.
- In fondo **Stampa**, **Salva la bozza** (o **Salva**) e **Emetti**, per chi può emettere; nel menu **⋯ Duplica** (una bozza nuova con gli stessi dati, per lo stesso impianto), la pagina dell'impianto, la cartella in Documenti, **Riporta in bozza**, **Annulla la certificazione**, **Ripristina come bozza** ed **Elimina**.

## <a id="certificazioni-emissione"></a>Emettere, correggere, annullare

- **Emetti** salva, controlla i campi obbligatori e, prima di confermare, avvisa se manca un allegato «sempre necessario». Da quel momento dati del modulo, testo del modello, dati dell'azienda, del cliente e della sede e allegati spuntati restano quelli dell'emissione, anche se poi cambiano. Si possono ancora cambiare progetto, note e file: la copia firmata arriva dopo.
- **Riporta in bozza** serve a correggere una certificazione emessa: torna modificabile e segue di nuovo modello e dati attuali, con lo stesso numero; poi la si emette di nuovo.
- **Annulla la certificazione** chiede il motivo: resta nel registro con il suo numero e in stampa porta la scritta ANNULLATA. **Ripristina come bozza** la rimette in compilazione.
- **Elimina**, con il permesso apposito, la toglie dal registro, anche se emessa: il numero resta libero e i file restano in Documenti. Di solito si annulla, non si elimina.
- Un impianto con certificazioni nel registro non si elimina; con l'eliminazione definitiva di un cliente dal cestino se ne vanno anche i suoi impianti e le loro certificazioni (le cartelle restano).

## <a id="certificazioni-numeri"></a>Numeri e date

- Il numero è per **modello** e **anno**: DiCo, DiRi e quadri hanno ciascuno la sua numerazione, che riparte da 1 ogni anno (l'anno è quello della data). Una certificazione nuova propone il prossimo numero libero; se ne scrivi un altro, deve essere libero.
- Iniziando a usare il registro a metà anno, basta scrivere nella prima certificazione il numero da cui partire: le successive proseguono da lì.
- Cambiando l'anno della data di una bozza, il numero diventa il primo libero di quell'anno, salvo indicarne uno. Il numero di una certificazione eliminata resta libero.
- La sigla (DiCo, DiRi, QE) è quella del modello: una certificazione tiene la sigla con cui è nata. La cartella dei suoi file si chiama come il numero, per esempio *DiCo 2026-012*, e cambia nome se il numero cambia.

## <a id="certificazioni-allegati"></a>Allegati, copia firmata e cartella

- La linguetta **Allegati** elenca gli allegati previsti dal modello (per la DiCo: progetto, relazione con le tipologie dei materiali, schema dell'impianto realizzato, dichiarazioni precedenti, certificato dei requisiti tecnico-professionali, attestazione per i materiali non normalizzati). Ognuno si **spunta**, se c'è anche solo su carta, oppure riceve il suo file con **Carica** o **Collega** (un documento che sta già in Documenti): in stampa la sua casella è spuntata. «Sempre necessario» segnala quelli che non devono mancare.
- **Copia firmata**: la scansione della dichiarazione firmata e timbrata, da caricare dopo averla stampata e firmata; nel registro la certificazione risulta **firmata**. **Altri file**: foto, misure, verbali delle verifiche.
- I file vanno nella cartella della certificazione, dentro quella dell'impianto: **Documenti → Clienti → *cliente* → *sede* → *impianto* → Certificazioni → DiCo 2026-012**, creata dalla piattaforma al primo file. Per caricarli serve il permesso **Caricare documenti**; scollegati, restano in Documenti.
- Emessa la certificazione, le spunte restano quelle dell'emissione (per cambiarle si riporta in bozza); i file si possono ancora aggiungere.

## <a id="certificazioni-stampa"></a>La stampa

**Stampa**, nella scheda, nell'anteprima o nel menu della riga, apre l'anteprima dei fogli con il [modello di stampa](modelli-stampa.md) delle certificazioni (la linguetta **Anteprima** della scheda mostra gli stessi fogli) e da lì la stampa, pronta da firmare: in testa logo e dati dell'azienda che emette il modello (da [Impostazioni → Generale](impostazioni.md#impostazioni-azienda): l'azienda principale o un'[altra azienda del gruppo](impostazioni.md#impostazioni-gruppo)), il modello, il numero e la data, e sotto la sua **dicitura nei documenti** (per esempio la certificazione ISO 9001 o l'attestazione SOA); poi titolo e riferimento normativo del modello e il testo con i dati al loro posto. Una scelta si stampa con tutte le voci e la casella spuntata su quella scelta (oppure, se il modello lo dice, con la sola voce scelta); una casella è spuntata o vuota; un campo vuoto diventa una riga da compilare a mano; le firme hanno il loro spazio. Una bozza esce con la scritta BOZZA di traverso, un'annullata con ANNULLATA. In fondo a ogni pagina il piè del modello di stampa, il numero, il **codice e la revisione del modulo** (se il modello li ha) e le pagine; un testo lungo continua sul foglio dopo, anche l'elenco dei campi. Per avere un PDF si sceglie **Salva come PDF** nella stampa del browser.

## <a id="certificazioni-modelli"></a>Modelli

Chi ha il permesso **Gestire i modelli delle certificazioni** trova il pulsante **Modelli** nel registro: l'elenco dei modelli con quante certificazioni li usano, **Duplica**, **Elimina** (solo per i modelli che nessuna certificazione usa) e **Nuovo modello**. Un'installazione nuova non ha modelli: si scrivono qui oppure si importano da un altro server. Dove il programma è partito con i modelli proposti ci sono tre modelli predefiniti: **DiCo** (D.M. 37/08, Allegato I), **DiRi** (art. 7, comma 6) e **Quadro elettrico** (CEI EN 61439), da controllare con il proprio modulo e da completare una volta con i valori dell'azienda (per esempio il dichiarante e il responsabile tecnico). La scheda di un modello ha le linguette:

- **Generale**: nome, **sigla** (davanti al numero e nel nome della cartella), colore, **Emessa da** (quando ci sono [altre aziende del gruppo](impostazioni.md#impostazioni-gruppo): l'azienda che emette le certificazioni del modello e ne intesta la stampa), **codice** e **revisione del modulo** (come il modulo è registrato nel vostro sistema di gestione, per esempio «MOD 7.5-04» e «rev. 2 del 10/01/2025»: si stampano in fondo a ogni pagina), titolo di stampa, riferimento normativo e **firme** (una per riga, al massimo quattro).
- **Campi**: quelli da compilare, nell'ordine della scheda. Per ciascuno il tipo (gli stessi dei [modelli delle schede tecniche](impianti.md#impianti-modelli), con il controllo del valore, tranne la password, perché la certificazione si stampa e si consegna; in più il titolo di sezione), l'etichetta, il **segnaposto** con cui si scrive nel testo di stampa, se va compilato prima di emettere, le voci delle scelte e come si stampano, il **valore proposto** (anche con i segnaposto: `{{cliente.nome}}`), un suggerimento e, per i testi, le **Maiuscole** del valore, come nei [modelli delle schede tecniche](impianti.md#impianti-modelli). Le frecce cambiano l'ordine.
- **Allegati**: quelli previsti, come vanno in stampa, con **Sempre necessario** per quelli che non devono mancare.
- **Testo di stampa**: il testo della dichiarazione, con stili, grassetto, dimensione, allineamento ed elenchi. I pulsanti **Inserisci** mettono dove c'è il cursore i [segnaposto](#certificazioni-segnaposto) della certificazione, i blocchi (allegati, firme, tutti i campi), i campi del modello e i dati di azienda, cliente, sede e impianto.
- **Anteprima**: il foglio con i dati dell'azienda che emette e un cliente di esempio.

Le modifiche a un modello valgono per le bozze; le certificazioni emesse restano come sono state emesse. ⬇ esporta un modello in un file, **Esporta tutti** e **Importa…** portano i modelli su un altro server, con l'azienda che emette per nome (vedi [Modelli tra server](impostazioni.md#impostazioni-modelli)).

> [!TIP]
> **Moduli registrati (ISO 9001, SOA).** Quando il modulo cambia, nel modello si aggiorna la **revisione**: le certificazioni già emesse tengono la revisione con cui sono state emesse, le bozze prendono quella nuova.

> [!TIP]
> **Quando cambia la legge.** Il testo si cambia nel modello, senza toccare il registro: sigla e numerazione proseguono, le certificazioni già emesse restano quelle firmate e le bozze seguono il testo nuovo. Se un aggiornamento della piattaforma porta una versione nuova di un modello predefinito, nell'elenco dei modelli compare **testo aggiornato** e la sua scheda propone **Aggiorna dal predefinito**: titolo, campi, allegati, firme e testo diventano quelli nuovi, e restano nome, sigla, colore e i valori proposti già scritti. **Ripristina il predefinito** riporta in ogni momento il testo del programma.

## <a id="certificazioni-segnaposto"></a>I segnaposto

Nel testo di stampa (e nei valori proposti) una parola tra doppie graffe diventa un dato della certificazione. Un segnaposto scritto male resta in stampa così com'è, in rosso, e si corregge nel modello.

| Segnaposto | Diventa |
| --- | --- |
| `{{numero}}` · `{{data}}` · `{{tipo}}` · `{{sigla}}` | Numero (12/2026), data, nome e sigla del modello. |
| `{{allegati}}` | Gli allegati previsti, ciascuno con la casella spuntata se è presente. |
| `{{firme}}` | Le firme del modello, affiancate, ognuna con lo spazio per firmare. |
| `{{campi}}` | Tutti i campi con etichetta e valore (comodo per un modello nuovo). |
| `{{chiave}}` di un campo | Il valore scritto nella scheda; una scelta con le sue caselle, una casella spuntata o vuota, un campo vuoto come riga da compilare. |
| `{{azienda.nome}}`, `.indirizzo`, `.via`, `.civico`, `.cap`, `.comune`, `.provincia`, `.telefono`, `.email`, `.pec`, `.piva`, `.cf`, `.rea`, `.cciaa`, `.sito`, `.capitale`, `.dicitura` | I dati dell'azienda che emette il modello (Impostazioni → Generale): *via* è senza «Via» davanti e senza numero, *cciaa* è la Camera di commercio per esteso (dalla provincia del REA), *dicitura* è la dicitura nei documenti. |
| `{{cliente.nome}}`, `.indirizzo`, `.piva`, `.cf`, `.telefono`, `.email`, `.pec` | Il cliente dell'impianto: nome e cognome per una persona, ragione sociale con la forma giuridica per un'azienda; l'indirizzo è il primo della scheda. |
| `{{sede.nome}}`, `.indirizzo`, `.via`, `.civico`, `.cap`, `.comune`, `.provincia` | La sede dell'impianto (senza sede, il primo indirizzo del cliente). |
| `{{impianto.nome}}`, `.tipo`, `.data` · `{{progetto.codice}}`, `.nome` | L'impianto (con la data di installazione) e il progetto collegato. |

## <a id="certificazioni-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere le certificazioni | Il registro e le schede delle certificazioni degli impianti dei clienti condivisi e dei propri contatti privati, con l'anteprima e la stampa; i file si vedono secondo i permessi dei documenti. |
| Compilare le certificazioni | Creare certificazioni in bozza e modificarle, spuntare gli allegati e collegare i file e la copia firmata. |
| Emettere le certificazioni | Emettere, riportare in bozza, annullare e ripristinare: di solito il responsabile tecnico. Comprende il compilare. |
| Eliminare le certificazioni | Togliere una certificazione dal registro, anche emessa. |
| Gestire i modelli delle certificazioni | Aggiungere, modificare, duplicare, aggiornare ed eliminare i modelli, uguali per tutti. |

Le cartelle delle certificazioni (e, se manca, quella dell'impianto) le crea la piattaforma, anche a chi non può modificare gli impianti. Chi compila le certificazioni non ha bisogno del permesso di vedere la pagina Impianti per sceglierne uno. Gli amministratori possono tutto.

---

[← Impianti](impianti.md) · [Indice](README.md) · [Manutenzioni →](manutenzioni.md)
