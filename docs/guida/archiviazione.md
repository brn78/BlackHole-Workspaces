[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="archiviazione"></a>Archiviazione

**Sistema → Archiviazione** mostra la **cartella di lavoro**, cioè dove il server tiene tutti i dati, e la **mappa delle cartelle** con contenuto e spazio occupato:

| Cartella | Contenuto | Nei backup |
| --- | --- | --- |
| `database` | Il database della piattaforma. | sì |
| `config` | Le impostazioni. | sì |
| `keys` | Le chiavi che proteggono sessioni e segreti. | sì |
| `files` | I file della pagina [Documenti](documenti.md), con tutte le revisioni, e le immagini dei servizi (per esempio i loghi dei clienti). | sì (i documenti [si possono escludere](backup.md#backup-impostazioni)) |
| `cache` | Conversioni in PDF, disegni DWG convertiti, anteprime dei documenti e l'indice dell'[archivio di rete](archivio-rete.md): si rigenerano da sole. | no |
| `backups` | I backup, se non hai scelto un'altra cartella. | no |
| `recovery` | Copie di sicurezza automatiche prima di aggiornamenti e ripristini, esiti e log. | no |
| `tools` | Programmi installati dalla piattaforma, come il convertitore dei [disegni DWG](documenti.md#documenti-dwg) e il motore dell'[assistente AI](impostazioni.md#impostazioni-ai): si reinstallano da Impostazioni. | no |
| `models` | I modelli dell'[assistente AI](impostazioni.md#impostazioni-ai) (file .gguf di qualche GB): si scaricano di nuovo da Impostazioni. | no |
| `temp` | File temporanei, svuotata a ogni avvio. | no |

Nel riquadro **Cartella di lavoro** il grafico a ciambella mostra il **disco** che la contiene: quanto spazio occupa la piattaforma, i [backup](backup.md) se stanno in un'altra cartella dello stesso disco, il resto (Windows, programmi, file di altri) e lo **spazio libero**, con la percentuale al centro. Le cartelle di rete non hanno il grafico.

## <a id="archiviazione-pulizia"></a>Pulizia dei resti

Ogni eliminazione toglie già i suoi file. Per sicurezza, un quarto d'ora dopo l'avvio e poi ogni notte la piattaforma controlla che non sia rimasto niente senza padrone, per esempio per un file in uso o un antivirus nel momento dell'eliminazione:

- contenuti dei documenti che nessuna revisione usa più, e le loro conversioni in PDF e DXF;
- file di mezzi e attrezzature, del personale e immagini dei clienti eliminati;
- annotazioni di cartelle tolte dall'[archivio di rete](archivio-rete.md) (quelle dei file spariti dalla cartella si tolgono a ogni aggiornamento completo dell'archivio).

Si tocca solo ciò che è fermo da almeno un'ora e ha un nome conosciuto dalla piattaforma: un caricamento in corso o un file messo a mano non si tocca. Quando trova qualcosa, il [registro attività](registro.md) (categoria *Sistema*) dice che cosa ha tolto e quanto spazio ha liberato.

## <a id="archiviazione-apri"></a>Aprire la cartella sul server

L'icona accanto al **Percorso** mostra la cartella di lavoro in Esplora risorse; quella accanto a **Backup in** apre la cartella dei backup. Le stesse due cartelle si aprono dal menu dell'[icona di stato](server.md#server-icona-stato). La finestra si apre **sul server**, non sul computer da cui stai lavorando: per questo funziona solo dal **browser del server**, con la piattaforma aperta all'indirizzo `http://localhost:5180` (o la porta scelta) e non attraverso un proxy. Con il servizio di Windows la finestra compare sul desktop dell'utente di Windows che l'ha chiesta; con il programma avviato con doppio clic si apre solo se il browser è nello stesso desktop di Windows in cui gira il programma.

La cartella dei backup su un **NAS**: la piattaforma ci entra con l'utente e la password salvati nei [backup](backup.md), ma il tuo utente di Windows potrebbe non essere collegato a quella condivisione (Esplora risorse aprirebbe Documenti). Allora la piattaforma la collega per te, con lo stesso utente, solo per questa sessione di Windows: al prossimo accesso non c'è più. Se Windows è già collegato a quel NAS con un altro utente (ne ammette uno solo alla volta) un messaggio dice come scollegarlo.

Da un altro computer il pulsante resta visibile, ma al posto della cartella apre una finestra che spiega il motivo e mostra il percorso: **Copia percorso** lo mette negli appunti, pronto da incollare in Esplora risorse sul server. Lo stesso accade su Windows Server Core, dove Esplora risorse non c'è. Ogni apertura viene annotata nel [registro attività](registro.md).

## <a id="archiviazione-cambio"></a>Cambiare la cartella di lavoro

1. **Cambia cartella…** e scegli: **Sposta i dati attuali in una nuova cartella** (vuota) oppure **Usa una cartella di lavoro esistente** (per esempio dopo una reinstallazione).
2. Scrivi il percorso completo sul server, oppure sceglilo con **Sfoglia** tra i dischi del server (anche con **Nuova cartella**), e premi **Controlla** (dopo «Sfoglia» parte da solo): la piattaforma verifica che la cartella sia adatta (vuota, scrivibile, con spazio sufficiente, non dentro quella attuale).
3. Conferma con la tua password, poi **Riavvia ora**: il cambio avviene al riavvio, prima di aprire il database.

Con **Sposta** ogni file viene copiato e verificato; la cartella precedente resta intatta come copia di sicurezza. Se qualcosa non va, la piattaforma riparte sulla cartella di prima.

La cartella di lavoro deve stare su un **disco del server**: non una cartella di rete né un NAS, perché il database si può rovinare se la rete si interrompe (la piattaforma lo rifiuta, come già il setup). Sul NAS tieni i [backup](backup.md#backup-nas); un disco del NAS collegato al server come disco iSCSI va invece bene, perché il server lo vede come un disco suo.

> [!WARNING]
> Con molti dati la copia richiede tempo: finché dura, la piattaforma non risponde e l'[icona di stato](server.md#server-icona-stato) sul server resta gialla con la scritta **Spostamento dei dati in corso**. Non riavviare il servizio né il server: la piattaforma torna disponibile da sola quando ha finito. Se il server si spegne durante la copia i dati non si perdono: la piattaforma riparte sulla cartella di prima e lo spostamento va richiesto di nuovo, verso una cartella vuota.

---

[← Registro attività](registro.md) · [Indice](README.md) · [Archivio di rete →](archivio-rete.md)
