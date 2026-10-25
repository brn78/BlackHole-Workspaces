[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="pulizia-file"></a>Pulizia dei file

**Sistema → Pulizia dei file** (solo amministratori; si apre anche da Impostazioni → Server) analizza i **dati della piattaforma**, cioè la cartella di lavoro sul server, e propone che cosa togliere. L'archivio di rete non si guarda e non si tocca mai. In alto si sceglie da quanti anni un file non si apre (1, 2, 3, 5 o 10) e **Analizza** rifà l'analisi; le caselle del riepilogo portano alla loro linguetta.

- **File zombi**: file sul disco che non appartengono più a niente, rimasti per un intoppo (un file in uso, il servizio fermato a metà): contenuti di documenti eliminati, conversioni in PDF e DXF, cartelle e allegati di schede del personale, mezzi e produttori eliminati, immagini di clienti e voci del listino tolte, temporanei rimasti da più di un giorno, cartelle vuote sul disco. Sono tutti proposti; con ⬇ si scaricano per vedere che cosa sono.
- **Doppioni**: documenti con lo stesso contenuto in posti diversi. Per ogni gruppo ne resta uno (quello collegato a una scheda, altrimenti il primo caricato), le altre copie sono proposte. Il contenuto è salvato una volta sola: le copie non occupano spazio in più, ma confondono chi cerca.
- **Cartelle vuote** dei Documenti, con quante sottocartelle vuote contengono. Le cartelle principali (Clienti, Commesse…) e quelle collegate a una scheda (cliente, impianto, commessa, attività…) non si possono scegliere; quelle dentro una cartella collegata sono senza spunta, perché spesso fanno parte della sua struttura (le cartelle Backup e Configurazioni di un impianto).
- **Non aperti**: i documenti che nessuno apre (né modifica) da almeno gli anni scelti, i più vecchi prima. Nessuno è scelto in partenza. Le aperture si registrano dalla versione 1.62.0 (anche quelle da un link di condivisione): per i documenti non ancora aperti da allora vale la data dell'ultima modifica.
- **File mancanti**: documenti, allegati e immagini il cui file sul disco non c'è più (cancellato a mano, disco rovinato, ripristino parziale). Qui non si toglie niente: si apre la scheda e si ricarica il file, o si recupera da un backup.
- **Quarantena**: i gruppi di file tolti, con chi, quando e perché. **Vedi** mostra dov'erano (e li scarica), **Ripristina** li rimette al loro posto (quelli il cui posto è nel frattempo occupato restano in quarantena), **Elimina ora** li cancella subito. Dopo 30 giorni un gruppo si elimina da solo.

Si spuntano le voci (**Tutte**, **Nessuna**, la ricerca) e si conferma: i file zombi vanno **in quarantena**, documenti e cartelle **nel cestino dei Documenti**, da cui si ripristinano. Ogni voce si ricontrolla prima di toglierla: ciò che nel frattempo è cambiato (un file riusato, una cartella in cui è arrivato un file, un documento collegato) resta, e l'esito lo dice. Ogni pulizia finisce nel [registro attività](registro.md).

> [!TIP]
> Ogni notte la **pulizia dei resti** fa da sola la parte dei file zombi: anche lei mette i file in quarantena invece di cancellarli, e toglie i gruppi scaduti.

---

[← Cestino](cestino.md) · [Indice](README.md) · [Backup e ripristino →](backup.md)
