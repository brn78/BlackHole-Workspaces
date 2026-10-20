[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="rubrica"></a>Rubrica

**La mia giornata → Rubrica** (dalla 1.143.0) tiene i contatti che non sono clienti né fornitori: parenti, amici, il medico, i tecnici di fiducia, i numeri utili. Restano fuori dalle anagrafiche dell'azienda, così non finiscono tra i clienti, nelle valutazioni o nelle scadenze. La usano tutti gli utenti, senza permessi; l'amministratore la spegne, se non serve, in [Impostazioni → Sezioni](impostazioni.md#impostazioni-sezioni).

- **Il contatto**: nome, cognome, azienda, ruolo, soprannome, compleanno (con il calendario e il segno zodiacale, come le altre date di nascita; uno senza anno arrivato dal telefono si vede sotto il campo, *12 giugno, anno non indicato*, e resta finché non scegli la data completa o lo togli), sito, etichette (Famiglia, Amici, Tecnici…) e note; nella linguetta **Recapiti** email e telefoni con l'etichetta (Cellulare, Casa, Ufficio…), in **Indirizzi** gli indirizzi con le coordinate e la mappa, come nei [clienti](clienti.md).
- **Foto o icona**: in cima alla scheda, come nei clienti, la foto si prende **Dal PC**, si **Incolla** (anche con <kbd>Ctrl</kbd>+<kbd>V</kbd> in qualunque punto della scheda) o si scarica **Da un indirizzo web**, e prima di salvarla la ritagli (tonda per le persone, quadrata per le aziende); **Rimuovi** la toglie. In alternativa **Icona e colore** (o **Proponi**, che la cerca dal nome e dal ruolo), che si vede quando non c'è la foto. Le foto arrivano anche con l'[import dal telefono](#rubrica-import) e vanno nel file dell'export. Vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini).
- **Chi lo vede**: un contatto è **personale** finché non lo condividi nella linguetta **Condivisione**: con **tutti** (in sola lettura o con la modifica) oppure con colleghi e gruppi, scegliendo per ciascuno **Può vedere** o **Può modificare**. Chi può modificare cambia i dati, ma non la condivisione; solo chi l'ha creato lo mette nel cestino. Nell'elenco la colonna **Visibilità** lo dice (*Personale*, *Condiviso*, *Con tutti*, *Da* chi te l'ha condiviso); i filtri **Miei** e **Condivisi con me** separano gli uni dagli altri.
- **Preferiti**: la stella nella scheda; ognuno ha i suoi, anche sui contatti condivisi, nella vista **Preferiti**.
- Dall'elenco il numero di telefono e l'email si toccano per **chiamare** o **scrivere**; il menu della riga ha anche **Esporta in vCard**. La [ricerca generale](ricerca.md) trova i contatti anche dal numero di telefono.
- **Cestino**: i contatti nel cestino li vede solo chi li ha creati; si ripristinano entro 30 giorni, poi vengono eliminati da soli.
- **Più contatti insieme** (dalla 1.143.5): l'icona **Scegli più righe** a sinistra della ricerca mostra le caselle; con i contatti scelti la barra propone **Aggiungi ai preferiti**, **Togli dai preferiti**, **Esporta in vCard** e **Sposta nel cestino** (solo per quelli creati da te: quelli condivisi dai colleghi restano, e il messaggio lo dice); nel **Cestino Ripristina** ed **Elimina definitivamente**.

## <a id="rubrica-import"></a>Importare i contatti dal telefono o da Excel

Con **Importa** (in **Altro**, o nella pagina ancora vuota) si carica il file esportato dal telefono o dal computer, oppure un **foglio Excel o CSV qualunque** con i nomi delle colonne nella prima riga: scegli che cosa c'è in ogni colonna (nome, cognome o nome e cognome insieme, azienda, ruolo, due email, cellulare, telefono, telefono dell'ufficio e di casa, fax, indirizzo, compleanno, sito, etichette, note) e poi segue la stessa anteprima. **Scarica il modello Excel** dà il foglio già pronto da compilare (vedi [Importare ed esportare](interfaccia.md#interfaccia-import-export)). Dal telefono:

- **Google Contatti** (Android): su *contacts.google.com* → **Esporta** → *vCard* oppure *CSV di Google*. Le etichette di Google diventano le etichette della rubrica.
- **iPhone**: su *icloud.com* → Contatti → seleziona → **Esporta vCard**; oppure dall'app Contatti, condividi i contatti come file.
- **Android** senza Google: app Contatti → Importa/Esporta → **Esporta in un file .vcf**.
- **Outlook**: Esporta in un file *CSV*.

L'anteprima mostra i contatti letti, i nuovi in cima: **Nuovo**, **Già in rubrica** (stessa email o stesso telefono di un tuo contatto, anche con o senza +39; quelli senza email né telefono si riconoscono dal nome, senza badare a maiuscole e accenti) o **Da scartare** (senza nome né recapiti). Due righe uguali nello stesso file fanno un contatto solo. Togli la spunta a quelli che non vuoi; per quelli già in rubrica scegli se **lasciarli**, **aggiungere i dati nuovi** (recapiti in più e campi vuoti riempiti, senza cancellare nulla) o **crearli comunque**. Un'etichetta facoltativa, per esempio *Dal telefono*, si aggiunge a tutti. I contatti importati sono personali: poi li condividi se vuoi. Il registro attività annota quanti contatti sono stati importati.

**Le foto**: quelle scritte nel file (le vCard dell'iPhone e di Android le contengono) arrivano subito, e nell'anteprima si vedono accanto al nome. Il CSV e la vCard di **Google Contatti** indicano invece la foto con un indirizzo web: con **Scarica anche le foto** (acceso) si scaricano dopo l'import, poche alla volta, solo da internet, e compaiono da sole nell'elenco. Una foto che non si trova più o non è un'immagine viene saltata: il contatto resta con le iniziali. A un contatto già in rubrica la foto si aggiunge solo con **Aggiungi i dati nuovi** e se non ne ha già una.

**Esporta** (in **Altro**, o dalla barra dei contatti scelti) scarica i contatti scelti, quelli mostrati o tutti quelli che vedi: in **vCard** (*.vcf*, con le foto, che si importa in Google Contatti, sull'iPhone, in Outlook o nel telefono) oppure in **Excel** o **CSV** con le colonne scelte, che si reimportano così come sono.

## <a id="rubrica-clienti"></a>Usare un contatto come cliente o fornitore

Preventivi, trattative, assistenza, attività, progetti, documenti, impianti, password, vendite, acquisti e pratiche lavorano con le schede dei [clienti e dei fornitori](clienti.md), che hanno i dati fiscali, le sedi e la storia. Un contatto della rubrica si usa lì in due modi:

- **Dal campo Cliente** (o Fornitore): scrivendo il nome, sotto i clienti trovati compaiono anche i contatti della rubrica che non hanno ancora una scheda, con la scritta *Rubrica*. Scelto uno, si apre la **scheda cliente nuova già compilata** con i suoi dati (persona se ha nome o cognome, con l'azienda nelle note; altrimenti azienda), i recapiti, gli indirizzi, il compleanno come data di nascita, la foto e l'icona: controlli, aggiungi se servono i dati fiscali e premi **Crea**. Il preventivo (o la richiesta, l'attività…) prende subito la scheda nuova; chiudendo senza crearla non si sceglie niente. Negli acquisti la scheda nasce come fornitore, nelle trattative come potenziale cliente.
- **Dalla scheda del contatto**: in fondo alla linguetta **Contatto**, il riquadro **Clienti e fornitori** mostra le schede collegate (**Apri la scheda**, **Scollega**), quelle con la stessa email o lo stesso telefono da **Collegare**, oppure **Crea la scheda cliente**. Nell'elenco i contatti collegati hanno l'etichetta *Cliente* (o *Fornitore*).

Collegato, il contatto non si propone più nei campi Cliente: si trova come cliente, con il suo codice. I dati si copiano solo quando la scheda nasce: dopo, contatto e scheda si cambiano ognuno per conto suo. La scheda nuova è **normale**, come quelle create da Clienti (dalla 1.143.5; prima un contatto solo tuo diventava un contatto privato, con la cartella in Documenti riservata); è un **contatto privato** solo per chi può creare soltanto quelli. Si cambia nella linguetta **Visibilità** prima di crearla. Chi vede un contatto condiviso vede la scheda collegata solo se può vedere quel cliente. I contatti si propongono a chi può creare clienti (condivisi o privati).

---

[← Appunti](appunti.md) · [Indice](README.md) · [Password →](password.md)
