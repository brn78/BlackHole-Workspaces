[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="panoramica"></a>Panoramica

La piattaforma è composta da due parti:

- **Il server**, installato su un PC o server Windows sempre acceso: conserva tutti i dati in una [cartella di lavoro](archiviazione.md) (database, documenti, impostazioni) e ne fa il backup.
- **Le pagine web** che stai usando: si aprono da qualsiasi browser recente (Edge, Chrome, Firefox, Safari; Internet Explorer non è supportato) su PC, tablet o telefono, all'indirizzo `http://<nome-o-IP-del-server>:5180`. Più persone lavorano insieme, ciascuna con il proprio account.

## <a id="panoramica-concetti"></a>I concetti chiave

- **Utente**: Chi usa la piattaforma, con un account personale. Può essere **amministratore** (controllo completo) oppure **utente**, che vede e fa ciò che gli concedono le policy dei suoi gruppi. Gli amministratori non fanno parte dei gruppi e il loro ruolo non si può togliere.
- **Gruppo di utenti**: Un insieme di utenti (un reparto, un ruolo) a cui si applicano una o più policy.
- **Policy**: Un elenco di **permessi** (cosa si può vedere e fare: per esempio visualizzare, creare, modificare o eliminare i clienti, tutti oppure solo quelli creati da sé) e di **regole di sicurezza** (verifica in due passaggi obbligatoria, scadenza della password).
- **Cliente**: Una persona fisica o un'azienda con dati fiscali, contatti, indirizzi e coordinate bancarie. Può essere **condiviso** oppure **privato** (un contatto personale). La stessa anagrafica tiene anche i potenziali clienti e i fornitori, con i loro **ruoli**.
- **Gruppo di clienti**: Un'etichetta che riunisce clienti collegati: per esempio tutte le sedi di una stessa azienda.
- **Documento**: Un file (o una cartella) dell'archivio comune, con le sue **revisioni**, la categoria, le etichette e l'eventuale cliente collegato. Una cartella può essere **riservata** a utenti e gruppi scelti.
- **Appunto**: Una nota di testo o un elenco di cose da fare: **personale**, oppure **condiviso** con colleghi e gruppi di utenti. Lo vedono solo chi lo scrive e le persone con cui è condiviso.
- **Password (voce)**: Le credenziali di un accesso, di un dispositivo, di una rete o di un servizio, con i suoi segreti cifrati sul server: **personale**, oppure **condivisa** con colleghi, gruppi o tutti, in lettura o con la modifica.
- **Attività**: Una cosa da fare, con stato, priorità, scadenza, persone assegnate, voci da spuntare, sottoattività, commenti, file e ore lavorate. Può passare da una **revisione** e ripetersi nel tempo. Sta in piedi da sola e, se serve, si collega a un **cliente** e a un **progetto**; la vedono chi la crea, chi ci lavora e chi la riceve in **condivisione**.
- **Progetto**: Una lavorazione da organizzare: un cantiere, una commessa, uno sviluppo. Ha un codice, un responsabile, i membri, un eventuale cliente e una **pagina propria** con le attività collegate e la cartella dei documenti; può essere **riservato** a chi ci lavora.
- **Notifica**: Ciò che ti riguarda nelle attività e nei progetti (un'assegnazione, una condivisione, un commento, una revisione, una scadenza): arriva nella campanella in alto e, se vuoi, per email.
- **Cartella di lavoro**: La cartella sul server con tutti i dati della piattaforma; da lì nascono i **backup**.

---

[Indice](README.md) · [Primo avvio e accesso →](accesso.md)
