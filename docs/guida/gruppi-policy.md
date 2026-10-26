[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="gruppi-policy"></a>Gruppi e policy

Riservati agli amministratori. Una **policy** (**Sistema → Policy**) raccoglie permessi e regole di sicurezza; un **gruppo** (**Sistema → Gruppi**) applica le sue policy a tutti i membri. L'accesso effettivo di un utente è l'**unione dei permessi** di tutte le policy dei suoi gruppi e la **regola di sicurezza più restrittiva**. Le modifiche valgono subito, senza chiedere un nuovo accesso. **Duplica** (nel menu della riga e in fondo alla scheda di una policy) crea una policy nuova con gli stessi permessi e le stesse regole, con il nome seguito da «(copia)» e non applicata a nessun gruppo: comoda per farne una variante. Anche un **gruppo** si duplica (nel menu della riga e in fondo alla sua scheda): il nuovo, con il nome seguito da «(copia)», ha la stessa descrizione, le stesse policy e gli stessi orari di accesso, e i membri da scegliere.

> [!NOTE]
> **Gruppi e policy non riguardano gli amministratori.** Hanno già tutti i permessi, quindi non compaiono tra i membri dei gruppi e non vi si possono aggiungere; né i permessi né le regole di sicurezza delle policy si applicano a loro. Per rendere obbligatoria la verifica in due passaggi a un amministratore la si imposta sul suo account, dalla sezione Sicurezza della [scheda utente](utenti.md). Da fuori dalla rete dell'ufficio un amministratore entra comunque solo con la verifica attiva (vedi [Accesso remoto](impostazioni.md#impostazioni-remoto)).

## <a id="gruppi-orari"></a>Orari di accesso

Nella scheda di un gruppo, **Limita l'accesso a giorni e orari** dice quando i membri possono usare la piattaforma: una riga per ogni giorno della settimana e una per i **festivi**, ciascuna con **Tutto il giorno**, **Fasce orarie** (fino a quattro, per esempio 08:00–13:00 e 14:00–18:00) o **Nessun accesso**. I **modelli** riempiono la tabella in un clic (lun–ven 8–18; lun–ven 8–13 e 14–18 con il sabato mattina; tutti i giorni feriali). Le ore si scrivono anche corte: «8» diventa 08:00, «1230» 12:30; per un turno oltre la mezzanotte si chiude la fascia a 24:00 e si riparte dalle 00:00 del giorno dopo. Sotto la tabella si vede se adesso si entrerebbe, fino a quando o quando si rientra, e i prossimi festivi.

- Fuori dalle fasce l'accesso è negato, anche con la password giusta, e il messaggio dice quando si potrà rientrare. Chi è collegato riceve un avviso dieci minuti e un minuto prima della fine della fascia; poi la sessione si chiude e la pagina di accesso spiega perché.
- Chi è in **più gruppi** con gli orari entra nelle fasce di tutti messe insieme. I gruppi senza orari non limitano e non aggiungono niente.
- I **festivi** sono le festività nazionali e il santo patrono indicato nelle [Impostazioni](impostazioni.md) (area informativa): quel giorno valgono le fasce della riga Festivi al posto di quelle del giorno della settimana.
- Gli **amministratori** non hanno mai limiti di orario, così nessuno resta chiuso fuori. L'ora è quella del server.
- Accessi negati e sessioni chiuse fuori orario finiscono nel [registro attività](registro.md).

## <a id="policy-permessi"></a>Permessi disponibili

Nella scheda di una policy i permessi sono raggruppati per area, ciascuno con la sua casella e una riga che lo spiega; **Tutti** e **Nessuno** spuntano o tolgono l'intera area. Le aree si aprono e si chiudono con un clic sul nome (accanto quanti permessi sono scelti, in blu se almeno uno; il browser ricorda quelle aperte), **Apri tutte** e **Chiudi tutte** le aprono o chiudono insieme. In cima, sempre a portata di mano mentre si scorre, **Cerca un permesso** (nel nome, nella spiegazione e nell'area: per esempio *fatture* mostra i permessi di vendite, fatture dei fornitori e contabilità) e **Solo quelli scelti** per rivedere la policy. Quelli segnati *dati riservati* danno accesso a costi, prezzi, retribuzioni, documenti personali o coordinate bancarie (vedi [Dati riservati e policy proposte](#policy-riservati)).

| Area | Permessi |
| --- | --- |
| Clienti | Visualizzare i clienti · Creare clienti · Modificare i clienti creati da sé · Modificare tutti i clienti · Eliminare i clienti creati da sé · Eliminare qualsiasi cliente · Svuotare il cestino dei clienti · Gestire i gruppi di clienti · Gestire le categorie dei clienti e dei fornitori · Esportare i clienti · Importare clienti · Rubrica personale · Dati amministrativi dei clienti (valgono anche per potenziali clienti e fornitori; il significato di ciascuno è nella [tabella dei Clienti](clienti.md#clienti-permessi)) |
| Documenti | Visualizzare i documenti · Caricare documenti · Modificare i documenti caricati da sé · Modificare tutti i documenti · Eliminare i documenti caricati da sé · Eliminare qualsiasi documento · Gestire le categorie dei documenti · Riservare le cartelle (vedi [Documenti](documenti.md#documenti-permessi)) · Condividere con link esterni · Gestire tutti i link esterni (vedi [Condivisioni](condivisioni.md#condivisioni-permessi)) |
| Attività | Vedere tutte le attività · Gestire tutte le attività · Vedere le ore di tutti (vedi [Attività](attivita.md#attivita-permessi)) |
| Commesse | Vedere le commesse · Gestire le attività delle commesse · Creare commesse · Gestire tutte le commesse · Gestire i tipi delle commesse · Budget e consuntivo delle commesse (vedi [Commesse](progetti.md#progetti-permessi)) |
| Impianti | Vedere gli impianti · Creare impianti · Modificare gli impianti · Eliminare gli impianti · Gestire i tipi di impianto (vedi [Impianti](impianti.md#impianti-permessi)) |
| Certificazioni | Vedere le certificazioni · Compilare le certificazioni · Emettere le certificazioni · Eliminare le certificazioni · Gestire i modelli delle certificazioni (vedi [Certificazioni](certificazioni.md#certificazioni-permessi)) |
| Manutenzioni | Vedere le manutenzioni · Registrare i rapporti di manutenzione · Gestire le manutenzioni (vedi [Manutenzioni](manutenzioni.md#manutenzioni-permessi)) |
| Assistenza | Vedere l'assistenza · Aprire le richieste e registrare gli interventi · Gestire l'assistenza (vedi [Assistenza](assistenza.md#assistenza-permessi)) |
| Personale | Vedere il personale · Documenti personali e visite mediche · Costi del personale · Gestire il personale · Eliminare le schede del personale · Gestire i corsi, i documenti e le visite (vedi [Personale](personale.md#personale-permessi)) |
| Reperibilità | Vedere la reperibilità · Gestire la reperibilità (vedi [Reperibilità](reperibilita.md#reperibilita-permessi)) |
| Indicatori | Vedere gli indicatori · Inserire i dati degli indicatori · Configurare gli indicatori · Indicatori delle persone · Premi (vedi [Indicatori](indicatori.md#indicatori-permessi)) |
| Mezzi e attrezzature | Vedere mezzi e attrezzature · Costi di mezzi e attrezzature · Gestire mezzi e attrezzature · Eliminare mezzi e attrezzature · Gestire i tipi di mezzi e attrezzature (vedi [Mezzi e attrezzature](mezzi.md#mezzi-permessi)) |
| Listino | Vedere il listino · Costi e ricarichi del listino · Gestire il listino (vedi [Listino](listino.md#listino-permessi)) |
| Magazzino | Vedere il magazzino · Registrare i movimenti · Il proprio furgone · Gestire il magazzino (vedi [Magazzino](magazzino.md#magazzino-permessi)) |
| Acquisti | Vedere gli acquisti · Gestire ordini e richieste d'offerta · Gestire gli acquisti (vedi [Acquisti](acquisti.md#acquisti-impostazioni)) |
| Vendite | Vedere le vendite · Preparare DDT e fatture · Gestire le vendite (vedi [Vendite](vendite.md#vendite-impostazioni)) |
| Contabilità | Vedere la contabilità · Registrare in contabilità · Gestire la contabilità (vedi [Contabilità](contabilita.md#contabilita-permessi)) |
| Fatture ricevute | Vedere le fatture dei fornitori · Importare e controllare · Pagare (vedi [Fatture ricevute](fatture-fornitori.md#fatture-fornitori-permessi)) |
| Preventivi | Vedere i preventivi · Compilare i preventivi · Gestire i preventivi (vedi [Preventivi](preventivi.md#preventivi-permessi)) |
| Strumenti | Vedere il monitoraggio · Gestire il monitoraggio (vedi [Monitoraggio](monitoraggio.md#monitoraggio-permessi); valgono anche per la [Rete locale](rete-locale.md)) |
| Scadenze | Vedere le scadenze dell'azienda · Gestire le scadenze dell'azienda (vedi [Scadenze](scadenze.md#scadenze-permessi)) |
| Password | Usare la gestione password · Condividere le password · Gestire tutte le password condivise · Gestire i tipi delle password · Esportare le password (vedi [Password](password.md#password-permessi)) |
| Assistente AI | Usare l'assistente AI (vedi [Assistente AI](assistente-ai.md)) |
| Utenti | Visualizzare gli utenti · Creare utenti · Modificare gli utenti · Eliminare gli utenti · Gestire la sicurezza degli utenti (vedi [Utenti](utenti.md#utenti-ruoli)) |
| Sistema | Consultare il registro attività · Esportare il registro attività |

- **Permessi compresi**: alcuni permessi ne comprendono altri. Chi può *Modificare tutti i clienti* può anche modificare i propri e visualizzarli; chi può *Eliminare qualsiasi cliente* può eliminare anche i propri; creare, modificare, eliminare e gestire i gruppi comprendono sempre il visualizzare. Spuntando un permesso, quelli che comprende si spuntano da soli, con la dicitura *compreso*, e restano bloccati finché serve.
- **Propri o tutti**: «creati da sé» vale per i clienti creati con il proprio account. Così si può dare a un collaboratore la gestione dei soli clienti che inserisce lui.
- Nell'elenco delle policy la colonna **Permessi** riassume per area quanti ne concede (*Clienti: 6 · Utenti: 2*); fermando il mouse compare l'elenco completo.

| Esempio di policy | Permessi da spuntare |
| --- | --- |
| Sola consultazione | Visualizzare i clienti. |
| Collaboratore | Creare clienti · Modificare i clienti creati da sé · Eliminare i clienti creati da sé. |
| Responsabile dei clienti | Modificare tutti i clienti · Creare clienti · Eliminare qualsiasi cliente · Svuotare il cestino dei clienti · Gestire i gruppi di clienti · Esportare · Importare. |
| Rubrica personale | Rubrica personale (con Esportare e Importare, se servono). |
| Gestione del personale | Creare utenti · Modificare gli utenti · Gestire la sicurezza degli utenti. |
| Tecnico | Vedere le commesse (vede i cantieri e le loro attività; sulle proprie attività lavora e registra le ore anche senza permessi). La policy proposta **Squadre in campo** è il punto di partenza per chi lavora sul campo. |
| Capo commessa | Creare commesse · Gestire le attività delle commesse · Vedere le ore di tutti. |
| Direzione lavori | Gestire tutte le commesse · Gestire tutte le attività · Vedere le ore di tutti. |
| Password del reparto | Condividere le password (comprende Usare la gestione password). |
| Responsabile IT | Gestire tutte le password condivise · Esportare le password. |
| Assistente AI | Usare l'assistente AI: nelle policy dei gruppi che devono averlo (per esempio i tecnici, per i rapportini e per Migliora testo nei moduli). |

> [!TIP]
> Le policy create con una versione precedente sono state **convertite da sole** ai permessi nuovi, senza togliere nulla: «Creare e modificare i clienti» è diventato Creare + Modificare tutti + Gestire i gruppi + Importare; «Consultare i clienti» ha avuto anche Esportare; «Rubrica personale» anche Esportare e Importare; «Creare e modificare gli utenti» è diventato Creare + Modificare; «Consultare il registro» ha avuto anche Esportare. Con la versione 1.7 le attività sono diventate una funzione per tutti: «Vedere le ore di tutti» è passato all'area Attività, insieme a Vedere le commesse che comprendeva. Conviene riguardarle una volta e togliere ciò che non serve.

La **chat**, le **attività**, gli **appunti** e la pagina del proprio **profilo** sono disponibili a tutti gli utenti, senza permessi; l'[assistente AI](assistente-ai.md) invece lo usa solo chi ha il permesso **Usare l'assistente AI**, perché fa lavorare il server. I gruppi di utenti servono anche a [condividere gli appunti](appunti.md#appunti-condividere): ogni utente può condividere un appunto con un gruppo, di cui vede il nome e il numero dei membri, e lo ricevono tutti i membri (non gli amministratori, che dei gruppi non fanno parte: vanno aggiunti per nome). Allo stesso modo si condividono le [password](password.md#password-condividere) e le [attività](attivita.md#attivita-condivisione). Eliminando un gruppo finiscono le condivisioni fatte con quel gruppo.

## <a id="policy-riservati"></a>Dati riservati e policy proposte

Chi lavora sul campo non deve arrivare ai dati amministrativi. Per questo alcuni permessi sono segnati **dati riservati** (nella scheda della policy, con il lucchetto, e nell'elenco delle policy che li concedono):

- **Dati amministrativi dei clienti**: coordinate bancarie e codice SDI di clienti e fornitori.
- **Valutazione dei clienti**: come pagano, quanto lavoro danno e quanto ci fanno guadagnare.
- **Costi e ricarichi del listino** (e quindi **Gestire il listino**): costi, prezzi di acquisto e sconti dei fornitori, ricarichi e margini, e la cartella **Listini** dei produttori in Documenti.
- **Costi del personale**: retribuzioni e costo aziendale.
- **Documenti personali e visite mediche**.
- **Costi di mezzi e attrezzature**: spese delle manutenzioni e totali.
- **Vedere gli acquisti**: ordini ai fornitori con i prezzi d'acquisto.
- **Vedere le vendite**: fatture, incassi e solleciti.
- **Vedere le fatture dei fornitori**: fatture ricevute, IBAN e pagamenti.
- **Vedere la contabilità**: prima nota, IVA, mastrini e bilancio.
- **Budget e consuntivo delle commesse**: ricavi, costi e margini delle commesse, con il costo delle ore.

Nessun permesso riservato si concede da solo: anche chi ha tutto il resto di un'area non li ha finché non vengono spuntati. Il resto del programma non mostra importi: le ore delle attività, le scadenze dell'azienda, l'assistenza e le manutenzioni non ne hanno; il listino mostra i prezzi di vendita a chi ha *Vedere il listino*, che le policy proposte danno solo a Progettazione e Acquisti.

**Policy proposte**, nella pagina Policy, apre una policy per reparto, da creare con un clic e poi adattare (si aprono nella scheda, dove si controllano i permessi prima di crearle; non sono applicate a nessun gruppo finché non lo decidi tu). Quello che un reparto non ha dentro e gli serve si dà a mano: la scheda di ogni policy dice quale.

| Policy | Per chi | Dati riservati |
| --- | --- | --- |
| Reception | Il banco e il telefono: apre e pianifica le richieste di assistenza, vede la reperibilità e le scadenze, crea e corregge i clienti. Da dare a mano, se servono: Gestire l'assistenza e Gestire la reperibilità. | Nessuno. |
| Progettazione (ufficio tecnico) | Preventivi, commesse con le loro attività, impianti, pratiche, certificazioni, manutenzioni e listino in lettura. Il SAL e il budget della commessa si danno a mano all'ingegnere che li prepara; emettere le certificazioni (di solito il responsabile tecnico) si dà a mano. | Nessuno. |
| Acquisti | Ordini e richieste d'offerta, solleciti, prezzi da verificare, listini dei fornitori con gli sconti, listino aziendale e magazzino in lettura. Per registrare l'arrivo della merce serve a mano Registrare i movimenti del magazzino. | Vedere gli acquisti e Costi e ricarichi del listino. |
| Magazziniere | Movimenti in tutti i magazzini e nei furgoni, inventari e riordino, senza costi né prezzi d'acquisto. Per gli ordini in arrivo serve a mano Vedere gli acquisti; per i DDT, Preparare DDT e fatture (mostrano gli importi). | Nessuno. |
| Amministrazione | Fatture e note di credito, DDT da fatturare, incassi e pagamenti, fatture dei fornitori, banca, contabilità e dati amministrativi dei clienti. Il budget delle commesse, i costi dei mezzi e quelli del personale si danno a mano. | Dati amministrativi dei clienti, vendite, fatture dei fornitori, banca e contabilità. |
| Squadre in campo | Le proprie attività e presenze, l'assistenza assegnata, il proprio furgone, le commesse con il materiale in quantità, senza prezzi. Compilare le certificazioni, registrare i rapporti di manutenzione e modificare gli impianti si danno a mano, se la squadra li fa. | Nessuno. |
| Commercialista | Lo studio che tiene o controlla la contabilità: prima nota, registri IVA, liquidazioni, mastrini, bilancio, fatture e banca. Non cambia niente. | Contabilità, vendite, fatture dei fornitori e banca. |
| Sola consultazione | Guarda senza cambiare nulla (anche il magazzino), listino escluso. | Nessuno. |

> [!TIP]
> **Revisione delle policy.** Apri la pagina Policy e guarda la colonna Permessi: le policy con *dati riservati* dovrebbero andare solo ai gruppi di Amministrazione, Acquisti e Commercialista. Se un'altra policy ha il lucchetto, aprila e togli i permessi riservati, oppure sostituiscila con la policy proposta del suo reparto.

## <a id="policy-regole"></a>Regole di sicurezza

- **Verifica in due passaggi obbligatoria**: chi non l'ha attiva deve configurarla al prossimo accesso.
- **Scadenza della password**: trascorsi i giorni indicati, al successivo accesso l'utente deve sceglierne una nuova.

Valgono per i membri dei gruppi, quindi non per gli amministratori. Chi viene promosso ad amministratore conserva l'obbligo della verifica in due passaggi, se lo aveva da una policy: passa sul suo account. La scadenza della password, invece, per gli amministratori non c'è.

---

[← Utenti](utenti.md) · [Indice](README.md) · [Registro attività →](registro.md)
