[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="sicurezza"></a>Buone pratiche di sicurezza

- **Un account per persona**, con i permessi minimi necessari; niente account condivisi: il registro attività deve poter dire chi ha fatto cosa.
- **Verifica in due passaggi** almeno per gli amministratori: per loro si rende obbligatoria sull'account (scheda utente → Sicurezza), per gli altri con una policy.
- **Pochi amministratori**: il ruolo non si può togliere, quindi assegnalo solo a chi deve davvero amministrare la piattaforma; agli altri bastano le policy.
- **Backup cifrati** su un altro disco o su un NAS, con la password conservata fuori dal server; ogni tanto **Verifica integrità** di un backup.
- Per sospendere un accesso **disabilita** l'account invece di eliminarlo: l'eliminazione cancella anche i suoi messaggi, i suoi appunti (compresi quelli condivisi) e le sue password personali.
- Da Internet solo tramite **VPN** o **proxy HTTPS**, mai inoltrando direttamente la porta.
- Sui PC condivisi usa sempre **Esci** e non selezionare **Mantieni l'accesso**.
- **Documenti**: per ciò che non tutti devono vedere usa le [cartelle riservate](documenti.md#documenti-permessi). Prima di installare un setup preso dai documenti controlla nel visualizzatore la sua **firma digitale**: un programma non firmato, o firmato da chi non ti aspetti, merita una verifica. La piattaforma non avvia mai i programmi e non apre mai come pagine i file HTML caricati.
- **Password**: conservale nella [gestione password](password.md) invece che in file, fogli o appunti; usa il [generatore](password.md#password-generatore), una password diversa per ogni accesso, e guarda ogni tanto il [controllo](password.md#password-controllo). Condividi con i gruppi più che con le singole persone, così chi cambia reparto smette di vederle da solo. Con la gestione password i backup vanno **cifrati**.

---

[← Server e installazione](server.md) · [Indice](README.md) · [Risoluzione dei problemi →](problemi.md)
