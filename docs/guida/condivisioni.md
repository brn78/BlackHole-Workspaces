[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="condivisioni"></a>Condivisioni

Un **link di condivisione** fa vedere a chi non ha un account un file, una cartella o la documentazione di un impianto: lo mandi per email o in un messaggio e il cliente lo apre dal browser, anche dal telefono, senza installare nulla e senza accedere alla piattaforma. Il link mostra solo ciò che condividi, non il resto del programma. Puoi dargli una **scadenza** e una **password**, farti **mandare file**, vedere nel **registro** chi lo apre e **disattivarlo** quando vuoi. **Archivio → Condivisioni** elenca i link che hai creato. Serve il permesso **Condividere con link esterni** (vedi [Permessi](#condivisioni-permessi)).

## <a id="condivisioni-link"></a>Condividere un file o una cartella

1. In [Documenti](documenti.md), dal menu **⋯** (o con il tasto destro) di un file o di una cartella scegli **Condividi con un link…**. Se per quell'elemento ci sono già dei link li vedi in elenco, con **Nuovo link** per farne un altro (per esempio uno per il cliente e uno per l'architetto).
2. Nella finestra: **Nome del link** (facoltativo, lo vedete solo voi), **Cliente** (proposto da quello del documento o della sua cartella: il link compare nella scheda del cliente), **Scadenza** (7 giorni, 30 giorni, 3 mesi, un anno, nessuna oppure un giorno preciso; si parte da 30 giorni), **Password** (facoltativa: **Genera** ne propone una), per le cartelle **Accetta file** e il **Messaggio** che compare in cima alla pagina del link.
3. **Crea il link** apre la sua scheda: **Copia** mette l'indirizzo negli appunti, **Apri** lo prova, **QR code** lo mostra da inquadrare con il telefono, **Manda per email** lo spedisce dalla piattaforma (se la posta è configurata) con il tuo messaggio.

Il link usa l'**indirizzo pubblico** della piattaforma (Impostazioni → Accesso remoto), quello con cui la si apre da fuori: se non è impostato, la pagina lo segnala, perché un indirizzo dell'ufficio fuori dall'ufficio non funziona. La password **non va mai nell'email** con il link: comunicala a parte, per telefono o con un messaggio.

## <a id="condivisioni-pagina"></a>Che cosa vede chi apre il link

- Una pagina con il logo e il nome dell'azienda, il nome del file o della cartella, fino a quando vale il link e il messaggio; in fondo telefono, email e sito dell'azienda (dai [dati dell'azienda](impostazioni.md)). Si legge bene anche dal telefono, con il tema chiaro o scuro.
- Per una cartella: le sottocartelle e i file, con il percorso per tornare indietro; **Scarica tutto** (o **Scarica la cartella**) li dà in un archivio ZIP. Un clic su un file lo apre nel [visualizzatore](documenti.md#documenti-visualizzatore) (PDF, immagini, Word, Excel, disegni…), il pulsante ⬇ lo scarica.
- Non si vedono le [cartelle riservate](documenti.md#documenti-permessi) (una cartella riservata si condivide solo con un link fatto apposta su di lei), il cestino e le revisioni precedenti: di ogni file c'è solo l'ultima.
- I file aggiunti dopo nella cartella compaiono da soli; un file spostato fuori o messo nel cestino sparisce dal link.
- Con la password, la pagina la chiede prima di mostrare qualsiasi cosa; quella giusta vale 12 ore in quel browser.

## <a id="condivisioni-caricamenti"></a>Farsi mandare i file

Con **Accetta file**, chi apre il link a una cartella trova **Carica file** e un riquadro in cui trascinarli. La prima volta scrive il suo nome (il browser lo ricorda). I file finiscono nella cartella aperta, con autore «nome (tramite link)» e una nota nella revisione; un nome già usato diventa «nome (2)», così nessun file viene sostituito. A chi ha creato il link arriva una [notifica](notifiche.md) per ogni file: un clic lo apre in Documenti. Al massimo 2 GB per file e 20 GB in tutto per ogni link. Per accettare file, il link deve condividere una cartella in cui puoi caricare tu.

## <a id="condivisioni-impianto"></a>La documentazione dell'impianto e il QR code

Nella pagina di un [impianto](impianti.md), **Condividi** crea un link alla sua documentazione, da mandare al cliente o da stampare come **etichetta con il QR code** da attaccare alla centrale o al quadro: chi la inquadra con il telefono trova tutto senza chiedere. Nella finestra scegli che cosa mostra:

- **Documenti**: la cartella dell'impianto in Documenti (manuali, schemi, foto), con la scelta delle sue cartelle. Quelle di **configurazioni** e **backup** partono escluse, perché possono contenere password. Le cartelle riservate restano sempre fuori, e così «Certificazioni» e «Manutenzioni», che hanno le loro linguette, e «Assistenza».
- **Certificazioni**: solo quelle [emesse](certificazioni.md), con la copia firmata e gli allegati collegati (le bozze e le annullate no).
- **Manutenzioni**: i [rapporti](manutenzioni.md) con giorno, esito, controlli, lavoro svolto, anomalie, consigli, prossima manutenzione e i loro file firmati (le note interne no).
- **Scheda tecnica**: le [parti](impianti.md#impianti-scheda-tecnica) che scegli. Può contenere indirizzi, codici e dati della rete: condividi solo quelle che servono.
- **Nome del cliente e indirizzo** in testa alla pagina: toglili se l'etichetta sta in un luogo aperto al pubblico.

Il link alla documentazione parte **senza scadenza**. Dalla sua scheda (**⋯** → **Stampa l'etichetta con il QR code**, oppure **QR code** → **Stampa l'etichetta**) l'etichetta di 85,6 × 54 mm si stampa su un foglio A4 da ritagliare oppure una per pagina, per le stampanti di etichette. Se disattivi o elimini il link, il QR code non apre più nulla.

## <a id="condivisioni-registro"></a>Il registro e la pagina Condivisioni

- La scheda del link mostra quante volte è stato aperto, i file visti o scaricati, quelli ricevuti e il **registro**: aperture, file, archivi ZIP, caricamenti, password sbagliate e invii per email, con data, ora e indirizzo. Aperture e file visti più volte di seguito dallo stesso indirizzo contano una volta ogni mezz'ora; il registro tiene le ultime 500 voci.
- **Archivio → Condivisioni** elenca i link **Attivi** e quelli **Scaduti e disattivati** (anche quelli il cui file non c'è più), con cliente, scadenza, ultimo accesso e stato. Un clic apre la scheda; dal menu **⋯** si copia, si apre, si manda, si modifica, si disattiva o si elimina. Chi gestisce tutti i link ha anche **Solo i miei**.
- La scheda **Documenti** di un [cliente](clienti.md#clienti-documenti) mostra in cima i link collegati a lui.
- **Disattiva** ferma il link (chi lo apre trova un avviso) e **Riattiva** lo rimette in funzione; una scadenza passata si sposta con **Modifica**. **Elimina** lo toglie per sempre con il suo registro: il file condiviso resta dov'è.

## <a id="condivisioni-sicurezza"></a>Sicurezza

- Il link contiene un codice casuale di 32 caratteri: non si indovina, ma chi lo ha può aprirlo. Per le cose delicate usa la password e una scadenza breve.
- Il codice non è salvato in chiaro nel database e la password è salvata come quelle degli account. Dopo 10 password sbagliate in 15 minuti il link non accetta altri tentativi per 15 minuti.
- La pagina del link non dà accesso al resto della piattaforma e non finisce nei motori di ricerca; i file si scaricano sempre come allegati, senza eseguire nulla.
- Nel [registro attività](registro.md) restano creazione, modifiche, invii per email, disattivazione ed eliminazione dei link, e i file arrivati con un link.

## <a id="condivisioni-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Condividere con link esterni | Creare link a file, cartelle (anche per farsi mandare file) e alla documentazione degli impianti che vedi, con scadenza e password; gestire i propri link e il loro registro. |
| Gestire tutti i link esterni | Vedere, modificare, disattivare ed eliminare i link creati da chiunque, con il loro registro. |

Si condivide solo ciò che si vede: non una cartella riservata ad altri, la documentazione di un impianto solo con il permesso di vedere gli impianti, le certificazioni e le manutenzioni solo con i loro permessi. Il link resta valido anche se chi l'ha creato cambia ruolo; chi gestisce tutti i link può disattivarlo.

---

[← Documenti](documenti.md) · [Indice](README.md) · [Monitoraggio →](monitoraggio.md)
