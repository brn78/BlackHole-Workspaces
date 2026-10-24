[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="ricerca"></a>Ricerca

Una sola casella per trovare qualsiasi cosa: clienti, documenti e cartelle, attività, progetti, impianti, certificazioni, rapporti di manutenzione, richieste di assistenza (anche dal ticket del cliente o dal telefono di chi ha chiamato), personale, mezzi e attrezzature, voci del listino, preventivi, DDT, fatture e note di credito, ordini e richieste d'offerta, fatture dei fornitori (per numero, cliente o fornitore, partita IVA, oggetto, commessa, righe; dalla 1.113.0), controlli del monitoraggio, appunti, password, colleghi, i file dell'[archivio di rete](archivio-rete.md) e le pagine di questa guida. Dei documenti cerca anche il [testo scritto dentro i file](documenti.md#documenti-testo). Si cerca solo in ciò che puoi vedere, con le stesse regole delle pagine.

## <a id="ricerca-aprire"></a>Aprire la ricerca

- la lente 🔍 nella barra in alto apre la [pagina della ricerca](#ricerca-risultati), con la casella pronta per scrivere (se sei già lì, ci porta il cursore);
- la tastiera apre la **ricerca veloce**: <kbd>Ctrl</kbd>+<kbd>K</kbd> (<kbd>⌘</kbd>+<kbd>K</kbd> sul Mac) da qualsiasi pagina, oppure <kbd>/</kbd> quando non stai scrivendo in un campo. Negli editor di testo <kbd>Ctrl</kbd>+<kbd>K</kbd> resta il collegamento dell'editor.

La ricerca veloce è una finestra in alto. Mentre scrivi compaiono i primi risultati; con <kbd>↑</kbd> e <kbd>↓</kbd> scegli, <kbd>Invio</kbd> apre il risultato scelto, <kbd>Ctrl</kbd>+<kbd>Invio</kbd> (o **Tutti i risultati**) apre la pagina dei risultati, <kbd>Esc</kbd> chiude. A finestra vuota trovi le **ricerche recenti** (ricordate solo nel browser che stai usando, con **Cancella** per toglierle) e le pagine principali.

## <a id="ricerca-risultati"></a>La pagina dei risultati

- In alto la casella, per cercare di nuovo, il pulsante **Filtri** e le **linguette** con quanti risultati ci sono per tipo: **Tutti**, **Clienti**, **Documenti**, **Attività**, **Progetti**, **Impianti**, **Certificazioni**, **Manutenzioni**, **Assistenza**, **Personale**, **Mezzi e attrezzature**, **Monitoraggio**, **Appunti**, **Password**, **Utenti**, **Archivio di rete**, **Guida**; compaiono quelle con almeno un risultato.
- Ogni risultato ha il **percorso** (per esempio *Clienti › C00012 › Gruppo Rossi*, oppure le cartelle di un documento), il **titolo**, che lo apre, un **estratto** con le parole cercate in grassetto e, sotto, quando è stato modificato e il suo stato. Un collega senza scheda si apre nella [chat](chat.md).
- I più pertinenti vengono prima: chi ha le parole nel titolo, poi in codici, email e altri campi principali, poi nel resto; a parità, il più recente.
- Se il primo risultato è un **cliente** o un **collega** ed è chiaramente quello cercato (il nome esatto, il suo codice, la partita IVA, il codice fiscale o il telefono, oppure è l'unico trovato), a destra compare la sua **scheda riassuntiva**; con una parola comune a tanti, come un nome di battesimo, no: partita IVA, indirizzo, telefono ed email (cliccabili), referenti, etichette, con **Apri la scheda** e i collegamenti ai suoi documenti e alle sue password; per un collega ruolo, reparto, presenza e **Scrivi in chat**.
- Scorrendo, in fondo arrivano da soli altri venti risultati alla volta (anche con **Altri risultati**).
- **Filtri** apre i filtri avanzati, che valgono per i risultati e per i numeri delle linguette e restano nell'indirizzo della pagina (una ricerca nuova li tiene; **Azzera** li toglie):
   - **Tutto**, **Solo cartelle** o **Solo file**: le cartelle e i file dei Documenti e dell'archivio di rete;
   - **quando sono stati modificati**: nelle ultime 24 ore, nell'ultima settimana, nell'ultimo mese o nell'ultimo anno;
   - **estensioni** dei file, separate da virgole: per esempio «pdf, dwg»;
   - **Parole solo nel nome**: escludono chi ha le parole solo nel percorso o negli altri campi (per esempio i file dentro una cartella che si chiama come la parola).

## <a id="ricerca-cosa"></a>Che cosa si trova

| Dove | Si cerca in |
| --- | --- |
| Clienti | Nome e ragione sociale, codice, partita IVA, codice fiscale, codice destinatario, PEC, sito, tutte le email e i telefoni, indirizzi, referenti, IBAN, gruppo, etichette, categoria e note. |
| Documenti | Nome di file e cartelle, descrizione, produttore, prodotto e versione, etichette, categoria e cliente collegato (se lo puoi vedere). Non nel contenuto dei file. |
| Attività | Titolo, descrizione ed etichette delle attività che vedi, anche con il codice o il nome del progetto collegato («rossi sopralluogo»); «#12» trova l'attività numero 12. Le attività dei modelli di progetto non compaiono. |
| Progetti | Codice, nome, tipo, cliente, responsabile, etichette e descrizione dei progetti che vedi (con il permesso **Vedere i progetti**). Il risultato apre la pagina del progetto. |
| Impianti | Nome, tipo, cliente con il suo codice, sede, Leggimi e scheda tecnica (indirizzi IP, matricole, modelli…) degli impianti che vedi (con il permesso **Vedere gli impianti**); i dismessi vengono dopo. Il risultato apre la pagina dell'impianto e, se si è trovato nella scheda tecnica, dice dove. |
| Monitoraggio | Nome, indirizzo, cliente, impianto e note dei controlli (con il permesso **Vedere il monitoraggio**), con lo stato; quelli non raggiungibili vengono prima. Il risultato apre la scheda del controllo. |
| Appunti | Titolo, testo, voci degli elenchi ed etichette dei tuoi appunti e di quelli condivisi con te. |
| Password | Nome, utente, email, link, dove si usa, cliente, etichette, descrizione e campi non riservati. **Mai** nelle password, nelle note riservate né negli altri segreti. |
| Utenti | Nome, nome utente, ruolo aziendale e reparto dei colleghi con l'account abilitato; email e telefoni solo per chi può consultare gli utenti. |
| Archivio di rete | Nomi di file e cartelle (e le cartelle in cui stanno) delle cartelle dell'[archivio di rete](archivio-rete.md) che puoi vedere. Non nel contenuto dei file. Prima chi ha le parole nel nome, e in cima chi si chiama proprio così: cercando «work» la cartella *work* viene prima dei file che stanno dentro di lei. Il risultato apre il file nella pagina dell'archivio, o la cartella. |
| Guida | Titoli e testo di ogni sezione di questa guida: il risultato porta alla sezione. |

## <a id="ricerca-trucchi"></a>Come cercare

- **Maiuscole e accenti non contano**: «citta» trova «Città». Si trovano gli elementi che contengono **tutte** le parole scritte, anche come inizio o parte di una parola («fotov» trova «fotovoltaico»).
- **Telefoni** in qualunque forma: «0932123456», «0932 12 34 56», «+39 0932 123456». Lo stesso per la **partita IVA**, con o senza il paese davanti («IT01234567897»), e per il **codice fiscale**: il cliente con quel codice va in cima.
- **Codici**: il codice di un cliente («C00012») o di un progetto («2026-001») mette quell'elemento in cima; «#12» cerca l'attività numero 12 (il numero è unico tra tutte le attività).
- **Forse cercavi**: con pochi risultati la ricerca propone la parola giusta tra quelle che conosce (nomi di clienti, progetti, appunti, password, colleghi, guida). Senza risultati mostra direttamente quelli della parola corretta, con *Risultati per «rossi». Cerca invece «rosi»* per tornare a quella scritta.
- **Vai a**: scrivendo il nome di una pagina («backup», «posta», «profilo», «controllo password») compare il collegamento per aprirla, se la puoi usare.
- **Calcoli**: «12\*3+4», «(1500+300)/2», «2^10», «1500 + 22%» (aggiunge il 22%), «1500 - 10%» (toglie il 10%), «20% di 150». Il risultato compare in cima, con **Copia**.
- **Festività**: «pasqua», «pasquetta», «natale», «ferragosto», «2 giugno», «patrono»… danno la data della prossima, oppure quella dell'anno scritto («pasqua 2030»), e quanti giorni mancano.

> [!NOTE]
> La ricerca non apre porte: un contatto privato di un collega, una cartella o un progetto riservati ad altri, un'attività, un appunto o una password che non ti riguardano o non ti sono condivisi non compaiono, nemmeno nei conteggi. Le ricerche non finiscono nel registro attività.

---

[← Strumenti di rete](strumenti-rete.md) · [Indice](README.md) · [Chat e presenze →](chat.md)
