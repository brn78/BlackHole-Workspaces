[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="mezzi"></a>Mezzi e attrezzature

**Azienda → Mezzi** e **Azienda → Attrezzature** sono i due elenchi dei **beni dell'azienda**: il parco auto e i mezzi da lavoro (targa, km, carburante e carta carburante) e le attrezzature (scale, elettroutensili, giuntatrici, strumenti di misura, DPI anticaduta…). Per ognuno le **scadenze** (revisione, bollo, assicurazione, tagliando, verifiche periodiche), anche a **km**, con i promemoria; lo storico delle **manutenzioni** con km, costi e fornitori; a chi è **consegnato**; i file e la foto. Le pagine compaiono a chi può **Vedere mezzi e attrezzature** (vedi [Permessi](#mezzi-permessi)).

## <a id="mezzi-elenco"></a>L'elenco

Le due pagine funzionano allo stesso modo. Le linguette **In uso** e **Dismessi** dicono quanti beni ci sono; se ci sono [altre aziende del gruppo](impostazioni.md#impostazioni-gruppo), sotto si sceglie l'azienda. La ricerca trova numero, descrizione, marca e modello, targa, telaio o matricola, tipo, persona, dove si trova e carta carburante; gli elenchi scelgono il **tipo**, lo **stato** (in uso, in riparazione, fuori uso) e se è **in consegna** o no. Ogni riga ha il bene (foto o icona del tipo, numero, descrizione, tipo, marca e modello), la targa e i km per i mezzi, a chi è consegnato (per le attrezzature, altrimenti, dove si trova) e la **prossima scadenza**: la più urgente, con quando scade, quanto manca e lo stato (**+2** accanto al nome: altre due da guardare). In alto **Stampa**, **Tipi** e **Nuovo mezzo** (o **Nuova attrezzatura**); un clic apre la scheda, il tasto destro (o ⋯) la apre alle Scadenze, alle Manutenzioni o alle Consegne, la stampa, **Duplica** ed **Elimina**.

## <a id="mezzi-importa"></a>Importare ed esportare con Excel

**Esporta** ⬇ scarica in **Excel** o in **CSV** i mezzi o le attrezzature che vedi (filtri compresi) o tutti, con le colonne che l'importazione riconosce: il file si sistema in Excel e si reimporta così com'è.

**Importa** ⬆ (a chi può creare le schede) apre l'importazione guidata da un foglio **Excel** (.xlsx, .xls, .ods) o **CSV**, una riga per mezzo o attrezzatura, nel pannello a destra:

1. **Il file**, anche trascinandolo nel riquadro (al massimo 20 MB e 5.000 righe).
2. **Che cosa c'è in ogni colonna**: quelle con il nome giusto sono già scelte, le altre si scelgono a mano oppure, con l'assistente AI attivo, con **✨ Proponi con l'assistente**. **Metti nelle note le colonne da non importare** (già spuntato) conserva il resto nelle note della scheda.
3. **L'anteprima**: ogni riga con il suo esito (**Nuova**, **Già presente**, **Con errori**), i filtri per esito e una casella per scegliere che cosa importare. Un bene è già presente con lo stesso numero, la stessa targa o lo stesso telaio o matricola.
4. **Importa** crea le schede una dopo l'altra, come dal modulo, con l'avanzamento e **Ferma**; l'esito dice quante sono state importate e, riga per riga, quelle non importate con il motivo.

Niente si perde: un valore che non va (un tipo che non c'è, uno stato o un'alimentazione sconosciuti, una data o dei km illeggibili) non ferma la riga, finisce nelle **note** della scheda dopo «Da controllare:».

Si importa nell'elenco aperto: dalla pagina Mezzi i mezzi, da Attrezzature le attrezzature. Il **tipo** si riconosce dal nome e porta le sue **scadenze proposte**, come in una scheda nuova (la revisione dalla data di immatricolazione, le scadenze a km dai km iniziali).

## <a id="mezzi-da-testo"></a>Una scheda nuova da un testo

Con l'[assistente AI](assistente-ai.md) attivo, **✨ Da un testo** (per chi può gestire mezzi e attrezzature) apre un pannello dove incollare, per un mezzo, il **libretto di circolazione** trascritto (anche letto da una foto con il testo dalle immagini), un'offerta o una fattura; per un'attrezzatura un'offerta, una fattura d'acquisto o la scheda del prodotto. **Proponi i dati** chiede all'assistente descrizione, marca, modello, targa, telaio o matricola, data di immatricolazione, alimentazione, km e data di acquisto (per le attrezzature niente targa, immatricolazione, alimentazione e km) e apre la **scheda nuova già compilata**: scegli il tipo, controlla e salva come sempre; le scadenze proposte dal tipo partono dalle date e dai km arrivati. Come per i [clienti](clienti.md#clienti-da-testo): solo ciò che c'è nel testo, i dati in un formato sbagliato tolti e scritti in cima alla scheda, niente salvato da solo e il testo non conservato.

## <a id="mezzi-scheda"></a>La scheda

- **Dati**: la **foto** (dal PC, incollata o da un indirizzo web, vedi [Immagini, loghi e foto](interfaccia.md#interfaccia-immagini); la ritagli prima di salvarla) oppure **Icona e colore** (senza, quella del tipo), il **numero** in azienda (vuoto = il prossimo libero: M01, M02… per i mezzi, A001, A002… per le attrezzature; è unico nell'elenco), il **tipo**, la descrizione, marca e modello, l'azienda del gruppo e lo **stato**. Per i mezzi la **targa**, il **telaio**, le date di **immatricolazione** e di acquisto, i **km iniziali** (poi i km attuali sono l'ultima lettura) e il **carburante**: alimentazione, numero della **carta carburante**, chi l'ha emessa e la sua scadenza. Per le attrezzature la **matricola**, la data di acquisto e **dove si trova** quando non è in consegna (magazzino, furgone, cantiere).
- **Scadenze**, **Manutenzioni**, **Consegne** e **File**: si salvano subito, senza il pulsante Salva (vedi sotto); sulla linguetta Scadenze un pallino se c'è qualcosa da guardare.
- **Storico**: chi ha cambiato che cosa, e quando: dati, scadenze fatte, consegne e ritiri, file.

Un bene nuovo si crea con i dati e le **scadenze proposte dal tipo**: la **revisione** si calcola dalla data di immatricolazione (per auto e furgoni la prima dopo 4 anni, poi ogni 2), le scadenze a km dai km iniziali (per esempio il tagliando a 20.000 km in più); le altre date (bollo, assicurazione, l'ultima verifica) le scrivi tu, dal libretto o dalla polizza. Un clic su «ogni…» cambia ogni quanto si ripete; ✕ toglie quelle che non servono. Le scadenze si possono aggiungere anche dopo. In basso **Elimina**, **Duplica** (una scheda nuova con lo stesso tipo, descrizione, marca, modello e azienda: comoda per una flotta di furgoni uguali) e **Stampa** (la scheda con le scadenze e le ultime manutenzioni).

> [!TIP]
> **Un bene venduto o rottamato** non si elimina: basta lo stato **Dismesso**. Passa tra i Dismessi con tutto il suo storico, le sue scadenze escono dallo scadenzario e, se era in consegna, viene ritirato. **In riparazione** e **Fuori uso** restano nell'elenco; le scadenze di un bene fuori uso escono dallo scadenzario e non mandano promemoria.

## <a id="mezzi-scadenze"></a>Le scadenze

Ogni scadenza ha un nome, la **data**, per i mezzi anche i **km** (vale quella che arriva prima: il tagliando a 45.800 km o entro marzo), **ogni quanto si ripete** (mesi e, per i mezzi, km), se la successiva si conta **dalla scadenza** (revisione, bollo, assicurazione) o **dal giorno in cui è fatta** (tagliando, verifiche), il preavviso in giorni e le note. Lo stato: **Scaduta**, **In scadenza** (entro il preavviso o, a km, quando ne mancano meno di 1.000), **In regola**, **Chiusa** (fatta e senza ripetizione); **Km da registrare** quando una scadenza solo a km non ha ancora una lettura dei km con cui confrontarsi.

- **Fatta** apre la finestra con il giorno, i km, il costo, il fornitore, le note e i file (fattura, verbale): diventa una voce delle [manutenzioni](#mezzi-manutenzioni) e la scadenza passa alla **successiva**, proposta nella finestra (la data più il periodo, i km più quelli del periodo) e modificabile. Una scadenza che non si ripete, senza una prossima scritta a mano, si chiude. «Fatta» si usa anche dallo [scadenzario](scadenze.md), dal menu della riga.
- **Registra i km** aggiorna i km attuali (e con loro le scadenze a km) senza un intervento.

## <a id="mezzi-manutenzioni"></a>Le manutenzioni

Lo storico degli interventi, dal più recente: **manutenzione**, **riparazione**, **revisione o verifica**, **gomme**, **guasto o segnalazione**, **lettura dei km** e **nota**, ciascuno con la data, che cosa (per esempio «Sostituzione della frizione»), i km, il costo, il fornitore, le note e i suoi file. In cima la **spesa registrata**, in tutto e nell'anno: è la somma esatta dei costi, che si arrotondano al centesimo (12,345 diventa 12,35). Le voci fatte da una scadenza si creano da sole con «Fatta»; **Nuova voce** aggiunge le altre. I km più alti tra le letture sono i **km attuali**: eliminando una voce, tornano all'ultima lettura rimasta.

## <a id="mezzi-consegne"></a>Le consegne

Un bene si **consegna** a una persona del [personale](personale.md), anche se non usa la piattaforma, con la data e una nota (per esempio «con chiavi e carta carburante»). **Consegna a un altro** chiude la consegna attuale lo stesso giorno; **Ritira** lo rende di nuovo libero. Sotto, **chi l'ha avuto**: tutte le consegne, dalla più recente, con le date. La persona che ha la sua scheda collegata a un utente trova i beni che ha in consegna nella sua [Home](home.md) (**In consegna a te**) e riceve i promemoria delle loro scadenze, anche senza i permessi di mezzi e attrezzature. Nella scheda del personale, chi vede i mezzi trova che cosa la persona ha in consegna.

## <a id="mezzi-tipi"></a>I tipi

**Tipi**, in alto nella pagina, elenca i tipi di mezzi (Autovettura, Furgone, Autocarro) o di attrezzature (Scala, Elettroutensile, Giuntatrice, Strumento di misura, DPI anticaduta, Piattaforma di lavoro elevabile) con le **scadenze che propongono** a un bene nuovo: per ognuna ogni quanti mesi (e, per i mezzi, km) si ripete, **la prima** (facoltativa: dopo quanti mesi dall'immatricolazione o dall'acquisto cade la prima volta), il preavviso e se si conta **dal fatto**. Cambiare un tipo non tocca i beni già creati; eliminandolo, i beni restano senza tipo con le loro scadenze. Ogni tipo ha anche **icona e colore**, che prendono i beni senza foto e senza un'icona loro (vedi [Icone e colori](interfaccia.md#interfaccia-icone)). Li gestisce chi ha il permesso **Gestire i tipi di mezzi e attrezzature**.

> [!NOTE]
> **Le periodicità proposte sono indicative.** Revisione, verifiche delle attrezzature e tarature dipendono dal codice della strada, dalle norme (per esempio D.Lgs. 81/2008 per le attrezzature di lavoro), dal costruttore e dall'uso: verificale con il libretto, il manuale o il vostro consulente per la sicurezza e correggile nei tipi o nelle singole scadenze.

## <a id="mezzi-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere mezzi e attrezzature | I due elenchi e le schede, con scadenze, manutenzioni, consegne, file e storico; le loro scadenze nello scadenzario. |
| Gestire mezzi e attrezzature | Creare e modificare le schede, consegnare e ritirare, registrare km, manutenzioni e scadenze fatte, caricare i file; ricevere i promemoria delle loro scadenze. |
| Costi di mezzi e attrezzature | Vedere il costo di manutenzioni e interventi e la spesa totale di ogni scheda; con la gestione anche scriverlo. Senza, le voci dello storico si vedono e si registrano senza il costo (quello già scritto resta). Sono [dati riservati](gruppi-policy.md#policy-riservati). |
| Eliminare mezzi e attrezzature | Eliminare una scheda con le sue scadenze, lo storico e i file. |
| Gestire i tipi di mezzi e attrezzature | I [tipi](#mezzi-tipi) con le scadenze che propongono. |

---

[← Reperibilità](reperibilita.md) · [Indice](README.md) · [Banca →](banca.md)
