[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="listini-fornitori"></a>Listini fornitori

**Magazzino → Listini fornitori** tiene i listini dei fornitori nel formato **METEL**, lo standard del materiale elettrico (si importano anche da [Excel, CSV e dal vecchio gestionale](#listini-fornitori-altri)). Sono file di testo che il fornitore manda o pubblica sul portale METEL, per esempio `VIMLSG021.TXT`: sigla dell'azienda, **LSG** per il listino al rivenditore o **LSP** per quello al pubblico, e la versione. Dentro ci sono, per ogni articolo:

- marchio, codice, EAN e descrizione;
- prezzo al rivenditore e prezzo al pubblico;
- unità di misura, confezione e quantità minima;
- stato (nuovo, in esaurimento, annullato…);
- **famiglia di sconto**.

Gli sconti non sono nel file: li concorda il fornitore e si scrivono qui, famiglia per famiglia. Un listino può avere decine di migliaia di articoli: per questo restano qui e nel [listino](listino.md) finiscono solo quelli che usate.

## <a id="listini-fornitori-importa"></a>Importare un listino

1. **Importa listini** e scegli i file .TXT, oppure uno ZIP che li contiene. Insieme al listino puoi caricare il file delle famiglie di sconto (`…FSC.TXT`), che ne dà le descrizioni, e quello delle ricodifiche (`…RIC.TXT`). Un file `.EXE` autoestraente va prima aperto sul PC per estrarre i .TXT.
2. **Controllo**: la piattaforma mostra che cosa ha letto: Se il listino dello stesso fornitore c'è già, propone di **aggiornarlo**, oppure di importarlo **come listino a parte** (per un listino diviso in più file). Se il file è **più vecchio** di quello già importato lo dice e chiede la conferma: di solito è una copia vecchia rimasta nella cartella, e importandola i prezzi tornerebbero indietro.
   - la testata (listino, sigla, partita IVA, tipo, decorrenza, versione del tracciato) e quanti articoli;
   - i marchi, gli annullati e quelli in un'altra valuta, che si saltano;
   - le **righe non lette**, con il numero di riga e il motivo; si saltano e il resto si importa;
   - i primi articoli, per controllare prezzi e descrizioni.
3. **Produttore, fornitore e sconti**:
   - il nome del listino;
   - il **produttore**: è già proposto quello con la stessa sigla METEL o partita IVA. Se non c'è, si crea con il nome proposto dalla descrizione del listino (lo puoi correggere), con la sua cartella in Documenti;
   - il **fornitore** dell'anagrafica: è già proposto quello con la stessa partita IVA. Chi può creare clienti lo crea anche al volo, con il ruolo Fornitore e la partita IVA del listino;
   - su quale prezzo si applicano gli sconti: al rivenditore oppure al pubblico. Se il prezzo scelto manca per un articolo, si usa l'altro;
   - lo **sconto generale**, che vale per le famiglie senza uno sconto proprio;
   - gli **sconti per famiglia**, anche in cascata (50+10); in un aggiornamento sono già scritti quelli di prima;
   - se saltare gli articoli annullati;
   - se salvare i **file originali** nella cartella del produttore (Documenti › Produttori › nome › Listini), come nuova revisione: è già spuntato.
4. **Esito**: articoli nuovi, aggiornati, con il prezzo in aumento o in calo, tolti dal fornitore e saltati, e le voci del listino ricalcolate.

Gli articoli si scrivono a blocchi: anche durante un listino grande gli altri possono continuare a salvare. Alcuni fornitori scrivono il file in UTF-8 contando le lettere accentate come un carattere solo: la piattaforma se ne accorge e rilegge quelle righe nel modo giusto.

## <a id="listini-fornitori-altri"></a>Da Excel, da CSV, da PDF e dal vecchio gestionale

**Importa listini** accetta anche:

- **Un foglio Excel (.xlsx, .xls, .ods) o un CSV**, un listino per file. Si sceglie che cosa c'è in ogni colonna: codice, descrizione (breve), **descrizione estesa**, codice a barre, unità di misura, prezzo al rivenditore, prezzo al pubblico, famiglia di sconto, sconto, pezzi nella confezione, marca, sigla METEL. Quelle con il nome giusto sono già scelte; con l'assistente AI attivo c'è anche **✨ Proponi con l'assistente**. Servono il codice, un prezzo e la **sigla del produttore** (VIM, BTI…: un listino nuovo con la stessa sigla aggiorna quello già importato). Uno sconto scritto per articolo diventa lo sconto della sua famiglia (quello della maggior parte degli articoli). Poi i passi sono quelli di un listino METEL. La **descrizione estesa** si vede nei dettagli dell'articolo, la trova la ricerca e passa alla voce del listino quando lo aggiungi; se manca la breve, vale l'inizio dell'estesa.
- **Un listino in PDF**: lo legge l'assistente, pagina per pagina, e diventa una tabella da controllare come un foglio Excel; vedi [Importare da un PDF](assistente-ai.md#importare-pdf).
- **Il file JSON con più listini**: quello estratto dal vecchio gestionale (listini\_fornitori.json, con i listini caricati, uno per sigla, e gli sconti concordati) e quello di **Esporta → Tutti i listini**. Al posto del controllo c'è la tabella dei listini del file: per ognuno la sigla, il nome, gli articoli, gli sconti che porta e se è **nuovo** o **aggiorna** quello già importato (gli sconti già scritti restano); il **fornitore** (ritrovato dalla partita IVA, dal codice fiscale o dal codice dell'anagrafica, altrimenti creato, una volta sola anche se ha più listini) e il **produttore** (ritrovato dalla sigla o dal nome, altrimenti creato) sono già proposti. Si spuntano quelli da importare (**Tutti**, **Nessuno**, la ricerca) e **Importa** li importa uno dopo l'altro, con l'avanzamento; **Ferma dopo questo listino** si ferma senza lasciare un listino a metà. L'esito riassume listini importati e aggiornati, articoli nuovi, rincari e listini non importati, con il motivo.

Un listino con la decorrenza più vecchia di quello già importato arriva senza spunta: i prezzi tornerebbero indietro.

> [!TIP]
> I listini del vecchio gestionale si portano così: sul PC con la cartella del vecchio gestionale si esegue esporta\_listini\_fornitori.py, che scrive listini\_fornitori.json, un riepilogo e, nella cartella listini\_altri, gli altri listini (non METEL) in CSV, da importare uno per volta scegliendo le colonne.

## <a id="listini-fornitori-esporta"></a>Esportare

**Esporta** scarica il listino scelto in **Excel**, in **CSV** (con le colonne che l'importazione riconosce da sola, sconto della famiglia compreso), in **JSON** o in **METEL**, oppure **tutti i listini** in JSON, per portarli su un altro server. Il file METEL è come quello del produttore (`<sigla>LSP.TXT` o `LSG`, con le famiglie di sconto in uno ZIP) e si reimporta qui o in un gestionale che legge METEL. Prezzi al rivenditore e sconti ci sono solo per chi vede i costi: per gli altri, nel file METEL il prezzo al rivenditore resta a zero.

## <a id="listini-fornitori-articoli"></a>Cercare gli articoli e metterli nel listino

In alto si sceglie un listino oppure **Tutti i listini**. La ricerca trova l'inizio del codice, parole della descrizione e l'EAN esatto. Per chi vede i costi le colonne mostrano anche il prezzo al rivenditore, lo **sconto** della famiglia e il **costo netto**. L'elenco filtra:

- gli articoli disponibili;
- quelli con il **prezzo cambiato con l'ultimo listino**, con la variazione;
- quelli già nel nostro listino;
- gli annullati;
- quelli **tolti dal fornitore** (non più nel file nuovo).

Con un listino scelto filtra anche per famiglia di sconto. Gli articoli arrivano a cento per volta: **Altri**, in fondo, carica i successivi.

Un clic apre i dettagli dell'articolo. Con le caselle, **Aggiungi al listino** crea le voci: si scelgono la categoria e il ricarico (quello della categoria oppure uno per queste voci). Le voci nuove sono materiali collegati al listino del fornitore:

- codice *marchio + codice*, per esempio «VIM 20001»;
- il produttore del listino come marca;
- senza una categoria scelta, quella principale del produttore;
- prezzo di listino e sconto presi da lì, e il costo che li segue;
- la colonna «Nel listino» apre la voce del listino sopra la pagina in cui sei.

Un articolo senza prezzo non diventa una voce a zero.

## <a id="listini-fornitori-sconti"></a>Sconti, listino nuovo, eliminazione

Con un listino scelto, la riga sopra l'elenco ne riassume i dati; **Produttore** apre la sua scheda. Gli altri pulsanti sono:

- **Sconti e dati** cambia nome, produttore, fornitore, prezzo di partenza, sconto generale e sconti per famiglia. Le voci del listino collegate si ricalcolano subito e prendono il produttore del listino.
- **Listino nuovo** riapre l'importazione per la versione successiva dello stesso fornitore:
   - i prezzi cambiati si ricordano, per la variazione e per lo storico;
   - gli sconti già scritti restano;
   - gli articoli che non ci sono più diventano «tolti dal fornitore»;
   - le **ricodifiche** spostano le voci collegate sul codice nuovo;
   - le voci del listino prendono il **costo nuovo**: il prezzo segue il ricarico, quello scritto a mano resta, e nello storico compare «Listino … del …».
- 🗑 elimina il listino del fornitore. Le voci prese da lì restano nel listino, con l'ultimo prezzo di listino e sconto, ma non si aggiornano più da sole.

Una voce collegata si può anche **staccare** dalla sua scheda: da lì in poi prezzo di listino e sconto si scrivono a mano.

> [!TIP]
> **Quali listini importare.** Importa i listini dei fornitori da cui comprate davvero, nella versione in vigore: ogni articolo occupa spazio nel database e nei backup. Le versioni vecchie servono solo se volete l'andamento dei prezzi: importale dalla più vecchia alla più nuova.

---

[← Listino aziendale](listino.md) · [Indice](README.md) · [Magazzino →](magazzino.md)
