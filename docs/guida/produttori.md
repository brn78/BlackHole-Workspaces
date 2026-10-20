[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="produttori"></a>Produttori

**Anagrafiche → Produttori** raccoglie le **marche** dei materiali, distinte dai fornitori che li vendono: il listino METEL di Vimar è del produttore Vimar, mentre il grossista da cui comprate è il fornitore. La pagina la vede chi lavora con clienti, documenti, impianti o listino; i produttori li crea e li modifica chi gestisce il listino o i clienti. Non sono dati riservati: costi e sconti restano nel [listino](listino.md#listino-permessi).

## <a id="produttori-importa"></a>Importare ed esportare con Excel

**Esporta** ⬇ scarica in **Excel** o in **CSV** i produttori che vedi (filtri compresi) o tutti, con le colonne scelte tra quelle che l'importazione riconosce: il file si sistema in Excel e si reimporta così com'è.

**Importa** ⬆ (a chi può creare le schede) apre l'importazione guidata da un foglio **Excel** (.xlsx, .xls, .ods) o **CSV**, una riga per produttore, nel pannello a destra:

1. **Il file**, anche trascinandolo nel riquadro (al massimo 20 MB e 5.000 righe). **Scarica il modello Excel** dà il foglio già pronto con la riga dei campi e le istruzioni: compilato e importato così com'è, salta la scelta delle colonne. Un file con più fogli mostra quali importare (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)).
2. **Che cosa c'è in ogni colonna**: quelle con il nome giusto sono già scelte, le altre si scelgono a mano oppure, con l'assistente AI attivo, con **✨ Proponi con l'assistente**. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda.
3. **L'anteprima**: ogni riga con il suo esito (**Nuova**, **Già presente**, **Con errori**), i filtri per esito e una casella per scegliere che cosa importare. Un produttore è già presente con lo stesso nome o una delle stesse sigle METEL.
4. **Importa** crea le schede una dopo l'altra, come dal modulo, con l'avanzamento e **Ferma**; l'esito dice quante sono state importate e, riga per riga, quelle non importate con il motivo.

Niente si perde: un valore che non va (una sigla di più di tre caratteri, un sito che non è un indirizzo, un'email non valida) non ferma la riga, finisce nelle **note** della scheda dopo «Da controllare:».

Le sigle METEL possono essere più d'una nella stessa cella, separate da virgola. Ogni produttore nuovo ha la sua cartella in Documenti, come quelli creati a mano.

## <a id="produttori-scheda"></a>La scheda

- **Logo**: dal PC, incollato (Incolla, oppure Ctrl+V in qualunque punto della scheda) o da un indirizzo web (vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini)); prima di salvarlo lo ritagli.
- **Nome** e **partita IVA**.
- **Sigle METEL**: le tre lettere con cui firma i suoi listini, per esempio VIM. Servono a riconoscerlo quando importi un suo listino, e si aggiungono da sole importando.
- **Categoria merceologica** principale e **altre categorie**, scelte tra le [categorie del listino](listino.md#listino-categorie). Quella principale si propone agli articoli che metti nel listino da un suo listino METEL. Le categorie si creano e si modificano in **Listino → Categorie**, oppure da qui con **Gestisci le categorie** (**Crea le categorie** se non ce n'è ancora nessuna), sotto la scelta: le nuove compaiono subito, senza chiudere la scheda.
- **Sito**.
- **Indirizzo della scheda prodotto**: apri sul sito la pagina di un prodotto qualsiasi, copia l'indirizzo e metti `{codice}` al posto del codice, per esempio `https://www.esempio.it/prodotto/{codice}`. Così ogni articolo di questo produttore nel listino ha il pulsante **Scheda del produttore**. **Prova** apre la pagina con un codice che scrivi tu.
- **Link utili**: catalogo online, configuratore, area riservata, assistenza tecnica…
- **Referente o agente**, con telefono ed email, e le note.

Le linguette **Listini** e **Documenti** mostrano i suoi listini METEL e la sua cartella in Documenti.

## <a id="produttori-documenti"></a>La cartella in Documenti

Ogni produttore ha la sua cartella, creata con la scheda: **Documenti › Produttori › nome**, con dentro **Listini**, **Cataloghi**, **Schede tecniche** e **Manuali**. Importando un suo listino METEL, il file originale va da solo in **Listini**: il listino dell'anno dopo, con lo stesso nome, diventa una nuova **revisione** dello stesso file. Così resta lo storico dei listini originali, come nella cartella PRODUTTORE\\LISTINI. Se il file è identico all'ultima revisione non si aggiunge niente. La cartella **Listini** la vede solo chi ha il permesso **Costi e ricarichi del listino** (i listini dei fornitori portano i prezzi di acquisto): per gli altri non esiste, con tutto quello che contiene; nell'elenco è segnata con il lucchetto.

Rinominando il produttore, la cartella e la marca delle sue voci del listino cambiano nome con lui. Eliminandolo, i suoi listini e le voci del listino restano, senza produttore, e la cartella resta in Documenti.

---

[← Clienti](clienti.md) · [Indice](README.md) · [Progetti →](progetti.md)
