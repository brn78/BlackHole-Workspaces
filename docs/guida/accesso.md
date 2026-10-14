[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="accesso"></a>Primo avvio e accesso

## <a id="accesso-primo-avvio"></a>Configurazione iniziale

Il programma di installazione può creare subito l'account amministratore (pagina **Account amministratore**): in quel caso accedi con quel nome utente e quella password da qualsiasi PC della rete, e scrivi il nome dell'organizzazione in **Impostazioni**. Altrimenti, al primo avvio non esiste alcun account: aprendo la piattaforma **dal PC del server** (`http://localhost:5180`) compare la pagina **Configurazione iniziale**, che chiede il nome dell'organizzazione e crea l'amministratore. Per sicurezza questa pagina non è disponibile dagli altri PC né attraverso un proxy. In entrambi i casi, mentre scrivi la conferma della password compare subito se le due password [coincidono](interfaccia.md#interfaccia-campi).

Un'installazione nuova **parte vuota**: nessun tipo di impianto, tipo dei progetti, categoria, tipo delle password o di mezzo, catalogo del personale, modello di scheda tecnica o di certificazione, schema dei file. Ognuno si crea nella sua pagina, oppure si porta dal server di prova con [Modelli tra server](impostazioni.md#impostazioni-modelli). Solo per prove e dimostrazioni, `"BlackHole": { "SeedDefaults": true }` in `appsettings.Local.json` prima del primo avvio fa partire il programma con i tipi, le categorie e i modelli proposti; su un database già in uso non cambia niente.

## <a id="accesso-login"></a>Accedere e uscire

Sugli schermi larghi la pagina di accesso ha a sinistra la parte blu con il vortice, la versione e i diritti; nelle finestre strette e sul telefono resta il modulo, con sopra il marchio di BlackHole Workspaces e sotto la versione. Il campo in cui stai scrivendo ha un bordo blu pieno; un campo sbagliato resta rosso finché non lo correggi.

Inserisci **nome utente o email** e password. L'opzione **Mantieni l'accesso su questo dispositivo** conserva la sessione anche chiudendo il browser, sempre entro il tempo di inattività impostato dall'amministratore. Per uscire usa **Esci** nel menu con il tuo nome, in alto a destra: fallo sempre sui PC condivisi.

- Dopo **5 tentativi errati** l'accesso per quell'utente da quell'indirizzo è sospeso per 5 minuti; dopo 30 tentativi da uno stesso indirizzo, per 15 minuti. Questi blocchi valgono per i **browser sconosciuti**: da un browser in cui sei già entrato i tentativi si contano a parte (5 errori, 5 minuti), così nessuno può tenerti fuori sbagliando apposta la tua password, nemmeno da fuori sede, dove tutti possono arrivare dallo stesso indirizzo. Il browser se lo ricorda per un anno dall'ultimo accesso; cancellando i dati del sito torna sconosciuto.
- La sessione si chiude da sola dopo un periodo di **inattività**: contano solo le tue azioni, non gli aggiornamenti automatici della pagina (chat, presenze).
- Se la password non viene accettata, guarda sotto il campo: con il **Blocco maiuscole** inserito compare *Blocco maiuscole attivo* e il bordo diventa arancione.

## <a id="accesso-otp"></a>Verifica in due passaggi

Se è attiva sul tuo account, dopo la password viene chiesto il **codice a 6 cifre** dell'app di autenticazione sul telefono (Google Authenticator, Microsoft Authenticator e simili). Senza telefono puoi usare uno dei **codici di recupero** ricevuti all'attivazione: ognuno vale una volta sola. Puoi anche scegliere di **non ricevere più la richiesta su quel browser** per il periodo stabilito dall'amministratore. Si attiva e si gestisce da [Profilo e sicurezza](profilo.md).

## <a id="accesso-obblighi"></a>Cambio password e attivazione obbligatori

L'amministratore o una policy possono richiedere di **scegliere una nuova password** (primo accesso, password scaduta) o di **attivare la verifica in due passaggi**. In quel caso, dopo la password, la pagina di accesso ti guida nel passaggio richiesto: finché non lo completi la piattaforma non si apre. Quando scegli la nuova password, sotto il campo di conferma compare subito se le due password coincidono.

## <a id="accesso-recupero"></a>Password dimenticata

Se l'amministratore ha configurato la posta, nella pagina di accesso trovi **Password dimenticata?**: indica nome utente o email e ricevi un link, valido per un tempo limitato e usabile una volta sola, per scegliere una nuova password. Per riservatezza la risposta è la stessa anche quando l'account non esiste. Senza posta configurata, chiedi all'amministratore di impostarti una password provvisoria.

---

[← Panoramica](panoramica.md) · [Indice](README.md) · [L'interfaccia →](interfaccia.md)
