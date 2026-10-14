[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="reperibilita"></a>Reperibilità

**Azienda → Reperibilità** dice **chi è reperibile e quando**: fuori orario (le sere, i giorni non lavorativi, le domeniche e i festivi) il reperibile di turno riceve le [richieste di assistenza nuove e gli avvisi del monitoraggio](#reperibilita-avvisi), e i colleghi sanno chi chiamare. Ognuno vede i propri turni nella [Home](home.md); la pagina compare a chi può **Vedere la reperibilità** (vedi [Permessi](#reperibilita-permessi)).

In alto, la riga **Adesso**: chi è reperibile in questo momento con il suo **telefono** (un clic lo chiama dal telefonino) e fino a quando, se si è in orario o fuori orario e il prossimo turno. Il telefono è il primo del profilo dell'utente oppure, se non ce l'ha, quello della sua [scheda del personale](personale.md#personale-accesso).

- **Calendario**: il mese con i turni di ogni giorno (le frecce cambiano mese, **Oggi** torna a questo); l'orario compare solo nei giorni in cui un turno comincia o finisce (*08:00 →*, *→ 08:00*); i tuoi turni sono evidenziati; le domeniche hanno il numero in rosso, i festivi anche la casella rossa tenue con il nome della festa. Il clic su un turno lo apre; il **+** di un giorno ne crea uno che comincia quel giorno all'ora del cambio turno. Il mese scorre dentro il suo riquadro; sul telefono sta tutto nella larghezza, con le iniziali di chi è di turno (il nome è nella scheda del turno).
- **Turni**: l'elenco **Da adesso** (o **Passati**, dell'ultimo anno) con chi, dal, al, durata, telefono e note; quello in corso ha il segno a sinistra. In fondo il totale delle ore.
- **Ore**: il [riepilogo](#reperibilita-ore) del mese o dell'anno per persona, da esportare.

## <a id="reperibilita-turni"></a>I turni

**Nuovo turno** chiede il **reperibile** (tra gli utenti attivi), **dal** e **al** (la fine è esclusa: un turno fino alle 08:00 lascia il posto alle 08:00 a quello dopo) e le **note** (il furgone, le chiavi…); i pulsanti della **durata** (12 ore, 1, 2, 3 giorni, 1 o 2 settimane) mettono la fine partendo dall'inizio. Un turno dura al massimo 31 giorni. Più persone possono essere reperibili insieme (per esempio un elettricista e un tecnico delle reti), ma la stessa persona non può avere due turni che si sovrappongono. Chi riceve un turno (o se lo vede cambiare o togliere) riceve una [notifica](notifiche.md#notifiche-tipi), e il giorno prima il [promemoria](#reperibilita-impostazioni). Nel turno aperto c'è la **storia**: chi l'ha creato, cambiato, sostituito.

## <a id="reperibilita-cambi"></a>Cambi e sostituzioni

- **Cambio**: nel turno si sceglie un altro reperibile; il turno resta com'è e porta scritto *al posto di* chi era previsto. Tutti e due ricevono un avviso.
- **Sostituzione per una parte**: un collega copre solo un pezzo del turno (una notte, un pomeriggio): si sceglie chi e da quando a quando, dentro il turno. Il turno si divide: prima e dopo restano di chi era, la parte in mezzo diventa un turno del collega, con scritto al posto di chi.
- **Elimina** (il cestino rosso) toglie il turno; resta nella storia e chi lo aveva riceve un avviso.

## <a id="reperibilita-rotazione"></a>I turni a rotazione

**Turni a rotazione** fa i turni di settimane o mesi in un colpo solo: si spuntano le **persone** nell'ordine dei turni (le frecce cambiano l'ordine), il **primo turno dal** (proposto il prossimo lunedì all'ora del cambio turno), **fino al** e quanti giorni **dura ogni turno** (7 per la settimana). Il primo turno è della prima persona, poi della seconda e così via, ricominciando dalla prima; l'ultimo si accorcia per finire alla data scelta. Con **Sostituisci i turni già presenti nel periodo** quelli che c'erano si tolgono (quelli a cavallo dell'inizio o della fine si accorciano); senza, restano, ma la stessa persona non può avere due turni sovrapposti. **Anteprima** mostra i turni prima di crearli; chi riceve turni (o se li vede togliere) riceve un avviso solo.

## <a id="reperibilita-impostazioni"></a>Orario e avvisi

**Impostazioni** (chi gestisce la reperibilità; gli altri le vedono con **Orario e avvisi**):

- **Orario di lavoro** dell'azienda: i giorni e le fasce (fino a quattro al giorno), con i modelli pronti. Fuori da qui si è **fuori orario**; i festivi (nazionali e il patrono delle impostazioni) e le domeniche sono sempre fuori orario. Finché non lo si sceglie vale quello proposto, dal lunedì al venerdì dalle 8 alle 18.
- **Richieste di assistenza nuove al reperibile**: **Solo fuori orario** (proposto), **Sempre** o **Mai**.
- **Ora del cambio turno**: quella proposta per i turni nuovi e la rotazione.
- **Fuori orario gli avvisi del monitoraggio vanno solo al reperibile**: vedi sotto.
- **Promemoria al reperibile il giorno prima del turno**: dalle 8 del giorno prima, oppure due ore prima per un turno fatto all'ultimo (chi riceve un turno che comincia entro un giorno ha già la notifica del turno nuovo).

## <a id="reperibilita-avvisi"></a>Chi riceve gli avvisi

- **Assistenza**: una [richiesta nuova](assistenza.md#assistenza-apertura), anche aperta dal [monitoraggio](monitoraggio.md#monitoraggio-avvisi), arriva anche a chi è reperibile in quel momento (se vede l'assistenza e non l'ha aperta lui), come scelto nelle impostazioni: nella campanella e, come ha scelto lui, per email e su Telegram.
- **Monitoraggio**: in un controllo, tra i destinatari degli avvisi, **Il reperibile di turno** manda gli avvisi anche a chi è reperibile quando partono (se vede il monitoraggio). Con **Fuori orario gli avvisi del monitoraggio vanno solo al reperibile**, fuori orario gli altri destinatari non vengono disturbati; se in quel momento non c'è nessun reperibile, gli avvisi vanno a tutti come sempre.

## <a id="reperibilita-ore"></a>Ore e giorni

La linguetta **Ore** conta, per persona, i turni del mese (o dell'anno, con **Anno**): **turni**, **ore** (solo quelle dentro il periodo), **fuori orario** (le ore fuori dall'orario di lavoro: le altre sono già lavorate), i **giorni** di reperibilità, **feriali**, **non lavorativi** (i giorni senza fasce, di solito il sabato) e **domeniche e festivi**, e le **uscite**. Ogni 24 ore di turno, dal suo inizio, fanno un giorno, del giorno in cui cominciano: la settimana da lunedì alle 8 a lunedì alle 8 fa 5 giorni feriali, un sabato e una domenica; il fine settimana da venerdì alle 18 a lunedì alle 8 fa un feriale, un sabato e una domenica. Le **uscite** sono gli interventi dell'assistenza con la [reperibilità nel consuntivo](assistenza.md#assistenza-consuntivo) fatti durante il turno da chi era reperibile (dalla sua scheda del personale). **Esporta** scrive il riepilogo in Excel o CSV, per le buste paga.

## <a id="reperibilita-permessi"></a>Permessi

| Permesso | Consente |
| --- | --- |
| Vedere la reperibilità | La pagina: il calendario e l'elenco dei turni di tutti, chi è reperibile adesso con il telefono, il riepilogo delle ore; le impostazioni in consultazione. I propri turni ognuno li vede comunque nella Home. |
| Gestire la reperibilità | Fare, cambiare ed eliminare i turni, le sostituzioni, i turni a rotazione, l'orario di lavoro e gli avvisi al reperibile. |

---

[← Personale](personale.md) · [Indice](README.md) · [Mezzi e attrezzature →](mezzi.md)
