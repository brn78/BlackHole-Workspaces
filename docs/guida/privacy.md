[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="privacy"></a>Privacy

**Sistema → Privacy** (solo amministratori; si apre anche da Impostazioni → Server) raccoglie ciò che chiede il Regolamento UE 2016/679 (GDPR) a un'azienda che tiene i dati di clienti, fornitori e dipendenti: le **informative**, il **registro dei trattamenti**, le **richieste degli interessati**, le **violazioni dei dati** e le **nomine**. La pagina ha sei linguette:

- **Stato**: quante schede di clienti e fornitori hanno l'informativa, quanti hanno dato il consenso alle comunicazioni commerciali, quanti dipendenti hanno ricevuto la loro, le richieste aperte e quelle in ritardo, le violazioni aperte e da notificare, i responsabili esterni senza accordo firmato (un clic sui riquadri apre la linguetta). In rosso in cima la violazione da notificare al Garante con il termine. Sotto, le schede ancora senza informativa (le più recenti) e quelle da rivedere per la [conservazione](#privacy-conservazione): un clic apre la scheda.
- **Informative**: i testi per clienti e fornitori e per dipendenti e collaboratori, con il referente per la privacy e l'eventuale responsabile della protezione dei dati (DPO).
- **Registro dei trattamenti**: che cosa si fa con i dati, perché e per quanto tempo.
- **Richieste**: chi ha chiesto di vedere, correggere o cancellare i suoi dati, e entro quando rispondere.
- **Violazioni**: il [registro delle violazioni dei dati](#privacy-violazioni), con le 72 ore per la notifica al Garante.
- **Nomine**: i [responsabili esterni e le persone autorizzate](#privacy-nomine).

Le richieste aperte e le violazioni da notificare compaiono anche nelle [Scadenze](scadenze.md) degli amministratori, sotto **Privacy**.

> [!NOTE]
> I testi già pronti sono un buon punto di partenza, non un parere legale: falli rileggere al consulente o al commercialista e adattali all'attività dell'azienda.

## <a id="privacy-informative"></a>Le informative

Le informative partono da un **modello** già scritto (artt. 13 e 14 GDPR: titolare, finalità, basi giuridiche, destinatari, conservazione, diritti, reclamo al Garante). Al posto dei segnaposto tra graffe vanno i dati della [scheda dell'azienda](impostazioni.md#impostazioni-azienda): `{azienda}` (ragione sociale e forma), `{sede}` (il primo indirizzo), `{piva}`, `{email}` (quella del referente, altrimenti la prima dell'azienda), `{pec}`, `{telefono}`, `{sito}`, `{referente}`, `{dpo}` (la frase sul DPO, solo se c'è) e `{ai}`: la frase sull'assistente, che compare solo se qualche funzione usa un [servizio esterno](impostazioni.md#impostazioni-ai) (Claude, OpenAI, Gemini), perché in quel caso i testi escono dall'azienda. Il testo si modifica liberamente: **«# »** all'inizio della riga fa un titolo, **«- »** un punto di un elenco, una riga vuota separa i paragrafi. **Torna al modello** riporta il testo originale (si tiene salvando) e **Anteprima** stampa il testo salvato, con i dati dell'azienda. Finché il testo è uguale al modello, si aggiorna da solo con le versioni nuove della piattaforma.

## <a id="privacy-clienti"></a>Informativa e consenso dei clienti

Nella scheda di un cliente, potenziale cliente o fornitore, la linguetta **Privacy** mostra se l'informativa è stata fornita, quando e come. Si fornisce in tre modi:

- **Invia per email** (quando la [posta](impostazioni.md#impostazioni-posta) è configurata): l'indirizzo è il primo della scheda e si può cambiare; parte un'email nello stile della piattaforma con tutto il testo, e l'informativa risulta fornita oggi «per email».
- **Stampa da firmare**: il testo con, in fondo, il riquadro del consenso alle comunicazioni commerciali e lo spazio per luogo, data e firma. Firmata, si segna con **Segna come fornita → Oggi, firmata**.
- **Segna come fornita**: oggi (firmata, consegnata a mano, per email, sul sito o in altro modo) oppure **In un altro giorno…**, per esempio quando era già stata fornita con il vecchio gestionale. **Togli** la riporta a non fornita.

**Comunicazioni commerciali** registra il consenso a ricevere offerte e informazioni (art. 6.1.a): **Non chiesto**, **Acconsente** o **Non acconsente**, con la data della scelta. Il consenso è facoltativo e si può revocare: senza, al cliente si scrive solo per preventivi, contratti e assistenza. Segnare l'informativa e il consenso richiede il permesso di modificare la scheda; chi la vede soltanto legge lo stato. Ogni scelta finisce nel [registro attività](registro.md).

## <a id="privacy-dipendenti"></a>Informativa ai dipendenti

In fondo ai **Dati** della [scheda del personale](personale.md#personale-scheda), il riquadro **Privacy** mostra se l'informativa per dipendenti e collaboratori è stata consegnata: **Stampa** la prepara da firmare, **Segna consegnata oggi** registra la consegna (**Togli** la annulla). Lo vede chi vede il personale e lo segna chi lo gestisce. Nella linguetta Stato della pagina Privacy si contano i dipendenti in forza.

## <a id="privacy-registro"></a>Registro dei trattamenti

Il registro delle attività di trattamento (art. 30) arriva **già compilato** con ciò che fa la piattaforma: clienti e fornitori, preventivi e fatturazione, assistenza e impianti, videosorveglianza dei clienti (dove l'azienda è responsabile del trattamento per conto del cliente, art. 28), monitoraggio, personale, utenti e sicurezza, comunicazioni commerciali, assistente AI. Per ogni trattamento: finalità, base giuridica, interessati, categorie di dati, destinatari, trasferimenti fuori dall'UE, conservazione e misure di sicurezza. Si modifica, si aggiunge (**Nuovo trattamento**) e si toglie; **Stampa il registro** lo stampa in orizzontale, da tenere pronto per un controllo.

## <a id="privacy-richieste"></a>Richieste degli interessati

Chiunque può chiedere di **vedere** i suoi dati (art. 15), **correggerli** (16), **cancellarli** (17), **limitarne** l'uso (18), **portarli via** (20), **opporsi** (21) o **revocare il consenso** (7). La risposta va data **entro un mese**, prorogabile di due nei casi complessi avvisando la persona entro il primo mese (art. 12). **Nuova richiesta** registra chi l'ha fatta, che cosa chiede, come è arrivata e quando: la scadenza si mette da sola un mese dopo e si può spostare fino a tre mesi. Le aperte stanno in cima, con la scadenza in rosso quando è passata; chiusa come **Evasa** o **Respinta**, con l'esito, resta la traccia di chi l'ha chiusa e quando.

Dalla scheda di un cliente, **Registra una richiesta** la apre già con il nome; **Esporta i dati** scarica un file JSON con l'anagrafica, lo stato della privacy e, se puoi vederli, preventivi, assistenza e impianti del cliente: è la risposta pronta a una richiesta di accesso o di portabilità.

> [!TIP]
> Per una richiesta di cancellazione, prima di eliminare la scheda controlla che cosa va tenuto per legge (fatture e documenti fiscali per 10 anni): l'esito della richiesta lo spiega.

Nella scheda del personale, nel riquadro **Privacy**, **Esporta i dati** scarica allo stesso modo la scheda del dipendente (con i dati che puoi vedere) e la data dell'informativa.

## <a id="privacy-violazioni"></a>Violazioni dei dati

Una **violazione dei dati personali** è qualsiasi cosa che li fa vedere a chi non doveva, li modifica senza autorizzazione o li fa perdere: un portatile o un telefono rubato, un'email mandata alla persona sbagliata, una casella di posta violata, un attacco informatico, archivi cancellati per errore. Vanno **tutte registrate** (art. 33.5), anche quelle senza conseguenze. **Registra una violazione** chiede:

- **che cosa è successo** in breve, **quando ve ne siete accorti** (giorno e ora: da lì partono le **72 ore**), quando è successa, che cosa compromette (riservatezza, integrità, disponibilità) e la descrizione;
- le **persone e i dati coinvolti** (chi, quante circa, quali dati), le possibili conseguenze e le misure prese o da prendere;
- il **rischio per le persone**: *da valutare* (il termine corre lo stesso), *improbabile* (resta solo nel registro, con il motivo), *rischio* (da notificare al Garante), *elevato* (anche alle persone);
- la **notifica al Garante**, con il collegamento alla pagina del Garante: data e riferimento. Oltre le 72 ore serve il **motivo del ritardo** (art. 33.1);
- la **comunicazione alle persone** (rischio elevato, art. 34): quando e come, oppure perché non serve (dati cifrati, rischio tolto dalle misure, sforzo sproporzionato).

Nell'elenco la colonna **Garante** dice entro quando notificarla e quanto manca, in rosso quando il termine è passato. Una violazione si **chiude** quando il rischio è valutato, la notifica fatta (se serve) e, con il rischio elevato, le persone avvisate o spiegato perché no. **Stampa le violazioni** stampa il registro da mostrare al Garante. Eliminare una voce serve solo per quelle registrate per errore.

## <a id="privacy-nomine"></a>Responsabili esterni e persone autorizzate

**Responsabili esterni** (art. 28): chi tratta dati personali per conto dell'azienda, come il servizio di posta, l'assistente AI esterno, il commercialista, il consulente del lavoro, chi fa assistenza ai computer. Per ognuno: che cosa fa, quali dati, **dove** sono i dati (nell'UE o fuori, con le garanzie: clausole contrattuali standard o decisione di adeguatezza), il giorno dell'**accordo firmato** (contratto o nomina; per i grandi servizi in rete l'accordo sul trattamento dei dati accettato con le condizioni) e quando rivederlo. In cima, **proposti da ciò che la piattaforma usa**: il server di posta configurato, l'assistente AI esterno, Telegram, la casella PEC per lo SDI, la ricerca degli indirizzi, il genere dal nome, il commercialista e, se c'è il personale, il consulente del lavoro. Un clic apre la scheda già compilata; aggiunto, non viene più proposto. Senza accordo firmato il responsabile è segnato in rosso e contato nello Stato.

**Persone autorizzate** (art. 29 GDPR e art. 2-quaterdecies del Codice privacy): gli utenti abilitati con le **aree** della piattaforma a cui accedono, secondo i permessi delle loro policy (gli amministratori tutte), e quanti permessi con dati riservati hanno. **Stampa la lettera** prepara l'autorizzazione da firmare: le aree, i dati riservati e le istruzioni (riservatezza, credenziali personali, niente copie su supporti personali, segnalare subito le violazioni al referente privacy). **Consegnata oggi** la segna; **Stampa quelle da consegnare** le stampa tutte insieme, una per pagina. Quando cambiano i permessi di qualcuno, ristampagli la lettera.

## <a id="privacy-conservazione"></a>Conservazione

I dati si tengono solo finché servono (art. 5.1.e). Nello Stato, il riquadro **Conservazione** mostra le schede da rivedere: i **potenziali clienti** (non clienti né fornitori) senza attività da più dei mesi scelti (24 se non li cambi; contano la scheda, i preventivi e le richieste di assistenza) e gli **ex dipendenti** usciti da più degli anni scelti (10). **Aggiorna** salva i tempi. Niente si cancella da solo: apri la scheda e decidi, tenendo ciò che serve per legge.

---

[← Archivio di rete](archivio-rete.md) · [Indice](README.md) · [Modelli di stampa →](modelli-stampa.md)
