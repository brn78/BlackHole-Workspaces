[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="backup"></a>Backup e ripristino

**Sistema → Backup**. Un backup è un unico file `.bhbak` con database, impostazioni, chiavi e documenti; viene verificato prima di comparire nell'elenco e un backup esistente non viene mai sovrascritto.

## <a id="backup-impostazioni"></a>Impostazioni

- **Cartella dei backup**: meglio un altro disco o un NAS, così un guasto del disco dei dati non colpisce anche i backup. Si sceglie con **Sfoglia** e si controlla con **Prova** (vedi [Backup su un NAS](#backup-nas)).
- **Backup automatico giornaliero** all'ora indicata, conservando gli ultimi N. Se un backup automatico non riesce (per esempio la cartella di destinazione non è raggiungibile) viene **ritentato ogni 10 minuti**, fino a sei volte; nella pagina resta l'errore dell'ultimo tentativo finché uno non va a buon fine, e nel registro attività il fallimento compare una volta sola.
- **Includi i documenti**: attivo all'inizio, mette nel backup tutti i file della pagina [Documenti](documenti.md), con le revisioni. Con un archivio molto grande puoi spegnerlo e salvare la cartella `files\documents` in un altro modo (copia su NAS, backup del disco): i backup restano piccoli e veloci, ma **non contengono i documenti**. Nell'elenco quei backup hanno l'indicazione **Senza documenti** (e la stessa parola nel nome del file).
- **Cifratura** con password: un backup cifrato si ripristina anche su un altro server; senza cifratura le chiavi restano legate al PC che lo ha creato, e su un altro server non si leggono più i segreti: verifica in due passaggi, password della posta, chiavi dei servizi e le [password della gestione password](password.md#password-riservatezza). La password si scrive due volte: sotto la conferma compare subito se le due coincidono.

> [!WARNING]
> **Conserva la password dei backup fuori dal server** (gestore di password, cassaforte): senza, un backup cifrato non si può ripristinare.

## <a id="backup-nas"></a>Backup su un NAS

Dalla 1.139.0 la cartella dei backup si sceglie con **Sfoglia** e, se il NAS lo chiede, si salva l'utente con cui il server ci entra.

1. **Sfoglia** accanto alla **Cartella dei backup**: compaiono i dischi del server. Con **Cartella di rete (NAS)…** scrivi *\\\\nas* (o il suo indirizzo IP, per esempio *\\\\192.168.1.20*) e premi **Vai**: compaiono le cartelle condivise del NAS. Entra con un clic, crea se serve una **Nuova cartella** (per esempio *BlackHole*) e premi **Scegli**.
2. Se il NAS chiede chi entra, «Sfoglia» mostra **Utente del NAS** e **Password**: scrivi un utente del NAS con il permesso di lettura e scrittura sulla cartella (per esempio *nas\\backup*) e premi **Entra**. Scelta la cartella, utente e password tornano nel modulo.
3. La **Prova** parte da sola: dice se il server scrive nella cartella, con quale utente, e quanto spazio c'è. Poi **Salva impostazioni**: prima di salvare la piattaforma riprova a scriverci.

I campi **Utente della cartella di rete** e **Password** compaiono solo per le cartelle di rete; vuoti, il server entra con l'account del servizio. La password si salva cifrata e non si rivede: il campo vuoto la lascia com'è, **Rimuovi la password salvata** la toglie. Il server entra nella cartella prima di ogni backup (anche quelli automatici della notte, dopo un riavvio del server o del NAS) e con la riga di comando `--backup`. Se non ci riesce, il messaggio dice con quale account ha provato e cosa fare.

**Solo nella rete dell'ufficio** (dalla 1.164.2): le cartelle di rete dei backup, dell'archivio e di «Sfoglia» devono stare su un computer della rete locale (un nome come *\\\\nas* o un indirizzo come *\\\\192.168.1.20*). Un indirizzo su Internet, o un nome che porta su Internet, viene rifiutato prima di provarci: per entrare il server manda l'impronta della password, e la riceverebbe chi controlla quel computer. Per lo stesso motivo la password salvata vale solo per la sua cartella condivisa: se la cartella passa su un altro NAS va riscritta.

> [!NOTE]
> **Perché serve l'utente.** Il servizio della piattaforma gira con un account di sistema che in rete si presenta come il computer del server (per esempio *SERVER$*): un NAS fuori dal dominio non lo conosce e non lo lascia scrivere. Windows ammette **un solo utente per ogni NAS**: se il server ci entra già con un altro utente (per esempio per l'[archivio di rete](archivio-rete.md)), usa lo stesso, oppure scrivi il NAS una volta con il nome e una volta con l'indirizzo IP.

## <a id="backup-elenco"></a>Elenco dei backup

**Esegui backup ora** crea un backup manuale; **Carica backup** aggiunge un file ricevuto da un altro server. Su ogni riga: **Verifica integrità**, **Scarica**, **Ripristina…**, **Elimina**. I tipi sono **Manuale**, **Automatico**, **Caricato**, **Pre-ripristino** e **Pre-aggiornamento** (creato prima di un [aggiornamento dalla piattaforma](server.md#server-aggiornamento); restano gli ultimi 3).

## <a id="backup-ripristino"></a>Ripristinare

**Ripristina…** chiede la tua password, verifica il backup e lo prepara; al riavvio i dati attuali vengono messi da parte in `recovery\pre-ripristino-<data>` (restano gli ultimi 3) e sostituiti. In caso di errore tornano al loro posto.

Ripristinando un backup **Senza documenti**, i documenti presenti sul server **restano dove sono**: tornano database, impostazioni e chiavi del backup, mentre i file della pagina Documenti non vengono toccati. Le schede dei documenti sono nel database: se il backup è più vecchio, i file caricati dopo restano sul disco ma non compaiono più nella pagina finché non li carichi di nuovo, e i file eliminati dopo il backup compaiono ma non si aprono.

## <a id="backup-emergenza"></a>Ripristino di emergenza

Se la piattaforma non parte, sul server da un prompt dei comandi nella cartella del programma, **a servizio fermo**:

`BlackHoleWorkspaces.exe --verify backup.bhbak`<br> `BlackHoleWorkspaces.exe --restore backup.bhbak`<br> `BlackHoleWorkspaces.exe --backup [cartella]`

Aggiungi `--password <password>` se il backup è cifrato con una password diversa da quella salvata.

---

[← Pulizia dei file](pulizia-file.md) · [Indice](README.md) · [Impostazioni →](impostazioni.md)
