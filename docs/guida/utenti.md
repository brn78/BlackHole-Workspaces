[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="utenti"></a>Utenti

**Sistema → Utenti** (la voce **Sistema** è [in basso a sinistra nel menu](interfaccia.md#interfaccia-menu)) elenca le persone che usano la piattaforma, con ruolo, gruppi, stato della sicurezza e ultimo accesso. La scheda di un utente ha quattro sezioni (la tua, che è anche [Profilo e sicurezza](profilo.md), ne ha sei):

- **Anagrafica**: nome, cognome, genere (proposto dal nome, se il [genere dai nomi](impostazioni.md#impostazioni-genere) è attivo), data di nascita, codice fiscale, ruolo aziendale, reparto, note. Per un utente collegato a una [scheda del personale](personale.md#personale-accesso) nome, dati anagrafici, ruolo aziendale e reparto vengono da lì e si cambiano lì (un avviso lo dice, con **Apri la scheda**). A un utente senza scheda, chi gestisce il personale la crea con **Crea la scheda nel personale**: una scheda nuova con i suoi dati, già collegata.
- **Contatti**: l'**email dell'account** (serve per accedere e per ricevere inviti e link di recupero), altre email e telefoni.
- **Indirizzi**: residenza, domicilio…, con le coordinate e la mappa, come nei clienti.
- **Accesso**: nome utente (non si cambia dopo la creazione), **ruolo**, gruppi (l'interruttore **Account abilitato** sta in basso, nella fascia dei pulsanti). Per un nuovo utente scegli la prima password, **impostandola ora** (di norma da cambiare al primo accesso; sotto la conferma compare subito se le due password coincidono) oppure **inviando un invito via email** con cui la sceglie da solo.
- **Sicurezza**: impostare una password o inviare il link per sceglierla, richiedere il cambio al prossimo accesso, reimpostare o rendere obbligatoria la verifica in due passaggi, revocare i browser di fiducia, chiudere tutte le sessioni aperte. In fondo, i **permessi effettivi** dell'utente.

**Duplica** (nel menu della riga e in fondo alla scheda, per chi può creare utenti) apre un **nuovo utente** con lo stesso ruolo aziendale e reparto e, se sei amministratore, gli stessi gruppi e lo stesso ruolo: utile per un collega che entra a fare lo stesso lavoro. I dati personali e l'accesso (nome utente, email, password) sono da scrivere.

Nome e cognome, ruolo aziendale, reparto, le etichette di recapiti e indirizzi e gli indirizzi stessi prendono da soli maiuscole e minuscole (`ROSSI MARIO` diventa *Rossi Mario*, `UFFICIO TECNICO` *Ufficio tecnico*), le email il minuscolo; il **nome utente** resta come lo scrivi. Vedi [Maiuscole e minuscole automatiche](interfaccia.md#interfaccia-formato).

## <a id="utenti-ruoli"></a>Ruoli

- **Amministratore**: controllo completo, compresi gruppi, policy, impostazioni, archiviazione, backup e aggiornamenti.
- **Utente**: i permessi arrivano dalle policy dei gruppi a cui appartiene.

**Un amministratore non può essere declassato**: nella sua scheda il ruolo è bloccato. Se non deve più amministrare la piattaforma, l'account si **disabilita** o si **elimina**. Per questo, quando porti un utente ad amministratore, al salvataggio viene chiesta conferma: avrà il controllo completo, uscirà da tutti i gruppi e il ruolo non si potrà più togliere. Gli amministratori **non fanno parte dei gruppi** e le [policy](gruppi-policy.md) non si applicano a loro: nell'elenco, al posto dei gruppi, hanno *Tutti i permessi*.

Anche chi non è amministratore può gestire gli utenti, se una policy gli dà i permessi:

| Permesso | Consente |
| --- | --- |
| Visualizzare gli utenti | L'elenco degli utenti e le loro schede, in consultazione. |
| Creare utenti | Nuovi utenti (mai amministratori); il ruolo e i gruppi li assegna poi un amministratore. |
| Modificare gli utenti | Anagrafica, contatti e stato (abilitato o no) degli utenti non amministratori. L'**email dell'account** di un altro utente si cambia solo avendo anche la gestione della sicurezza, perché a quell'indirizzo arrivano i link per reimpostare la password. |
| Eliminare gli utenti | Eliminare utenti non amministratori. |
| Gestire la sicurezza degli utenti | Le operazioni della sezione Sicurezza sugli utenti non amministratori. |

Ognuno, anche senza questi permessi, cambia da sé i propri telefoni, indirizzi e altre email, dalla scheda Contatti di [Profilo e sicurezza](profilo.md).

Chi non è amministratore non può mai modificare o eliminare un amministratore, né assegnare ruoli e gruppi. Nessuno può disabilitare o eliminare sé stesso, e nella propria scheda la sezione Sicurezza è quella di [Profilo e sicurezza](profilo.md) (password e verifica in due passaggi del proprio account); resta sempre almeno un amministratore abilitato. Un account **disabilitato** non può accedere e le sue sessioni si chiudono subito: per sospendere un accesso è preferibile all'eliminazione.

> [!WARNING]
> **Eliminando un utente** si eliminano anche i suoi messaggi della chat e i suoi [appunti](appunti.md#appunti-riservatezza), compresi quelli che aveva condiviso con i colleghi, e le sue [password personali](password.md#password-riservatezza) (quelle condivise restano ai destinatari): non si possono recuperare. Disabilitandolo restano dove sono.

---

[← Sistema](sistema.md) · [Indice](README.md) · [Gruppi e policy →](gruppi-policy.md)
