[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="profilo"></a>Profilo e sicurezza

Il menu con il tuo nome, in alto a destra, riassume il tuo account (nome utente, ultimo accesso, ultimo cambio di password, verifica in due passaggi). **Profilo e sicurezza** apre la **tua scheda utente**, la stessa di [Sistema → Utenti](utenti.md), sopra la pagina in cui sei: chiudendola torni dove eri, e nulla di quello che stavi scrivendo va perso. Tutto il tuo account è lì, in sei schede:

- **Anagrafica** e **Accesso**: i tuoi dati, il nome utente, il ruolo e i gruppi. Li cambia chi ha il permesso di modificare gli utenti: per gli altri sono in consultazione, e un avviso lo dice. Se hai una [scheda nel personale](personale.md#personale-accesso), nome e dati anagrafici vengono da lì.
- **Contatti** e **Indirizzi**: **telefoni**, **indirizzi** e **altre email** li cambi tu, anche senza permessi sugli utenti, e li salvi con **Salva** in fondo. Gli indirizzi hanno le **coordinate** e la [mappa](clienti.md) come nei clienti (lo stesso nelle schede del personale). L'**email dell'account** invece la cambia chi gestisce gli utenti, perché serve per accedere e per ricevere i link per reimpostare la password.
- **Sicurezza**: ultimo accesso e ultimo cambio della password, poi i comandi del tuo account:
   - **Password → Cambia**: chiede quella attuale e la nuova due volte (almeno 8 caratteri con lettere e numeri o simboli; sotto la conferma compare se le due coincidono). Le altre sessioni aperte con il tuo account si chiudono.
   - **Verifica in due passaggi → Attiva**: mostra un codice QR da inquadrare con l'app di autenticazione e poi i **codici di recupero**, da conservare in un posto sicuro. **Disattiva** chiede la password e un codice; se per il tuo account è obbligatoria non c'è.
   - **Browser di fiducia**: quelli su cui il codice non viene chiesto, da revocare uno per uno o tutti.
   - **Permessi effettivi**: che cosa puoi fare, secondo le [policy](gruppi-policy.md) dei tuoi gruppi.
- **Aspetto**: il tema e il carattere della piattaforma su questo browser: vedi [Aspetto: tema e carattere](#profilo-aspetto).
- **Notifiche**: quali [notifiche di attività e progetti](notifiche.md) ricevere e se averle anche per email o su Telegram (**Collega Telegram**); vedi [Preferenze](notifiche.md#notifiche-preferenze) e [Su Telegram](notifiche.md#notifiche-telegram). L'icona ⚙ della campanella apre la scheda direttamente qui.

In Sicurezza, Aspetto e Notifiche ogni comando vale subito (o ha il suo **Salva**), per questo in fondo non c'è il pulsante Salva della scheda.

## <a id="profilo-aspetto"></a>Aspetto: tema, densità, ombre e carattere

Nella scheda **Aspetto** scegli il **tema**, **Chiaro**, **Scuro** o **Automatico** (segue il sistema operativo), la **Densità** (**Comoda**, com'è sempre stata, oppure **Compatta**: righe degli elenchi, campi e pulsanti più bassi e margini più stretti, per vedere più cose insieme sullo schermo del computer; sul telefono resta comoda), le **Ombre** (dalla 1.101.0: quanto si staccano dallo sfondo riquadri, numeri, pannelli, finestre e menu; di serie **Morbide**, a più strati come le ombre vere; **Leggere** sono quelle di prima, **Profonde** più presenti, con i bordi più leggeri e i riquadri cliccabili che si alzano al passaggio del mouse; lo sfondo resta com'è; le ombre valgono nel tema chiaro: dalla 1.109.1 nel tema scuro riquadri, numeri e pulsanti non hanno ombre (le staccano il bordo e la superficie), solo menu e finestre ne hanno una scura e raccolta; le Sospese non ci sono più (chi le aveva torna alle Morbide); dalla 1.105.0 le Morbide stanno sotto l'oggetto e non intorno, così gli spazi tra i riquadri restano puliti, e menu, avvisi e finestrelle hanno un'ombra più raccolta di quella delle finestre) e sotto il **Carattere** con cui è scritta tutta la piattaforma. Dalla 1.101.0 i numeri dei riquadri (Home e strisce in cima alle pagine) salgono da zero al valore, accelerando e poi rallentando; se cambiano mentre la pagina è aperta vanno dal vecchio al nuovo. Ogni pulsante è scritto con il proprio carattere e porta una frase di esempio con lettere accentate e cifre: un clic e la pagina cambia subito, senza salvare.

| Carattere | Com'è |
| --- | --- |
| **Predefinito (sistema)** | Il carattere del sistema operativo: su Windows è Segoe UI. È la scelta iniziale. |
| **Inter** | Senza grazie, nitido e neutro. |
| **Source Sans 3** | Senza grazie, classico e scorrevole. |
| **IBM Plex Sans** | Senza grazie, dal taglio tecnico. |
| **Nunito Sans** | Senza grazie, morbido e arrotondato. |
| **Atkinson Hyperlegible** | Disegnato per la massima leggibilità: lettere e cifre simili restano ben distinte. |
| **Lora** | Con grazie, elegante. |

- Tema, densità e carattere **valgono per il browser in uso**, non per l'account: su un altro computer o in un altro browser vanno scelti di nuovo, e chi usa lo stesso browser dopo di te li ritrova. Valgono anche per la pagina di accesso.
- I sei caratteri sono **inclusi nel programma**, con licenza libera: funzionano anche su una rete senza Internet e nulla viene scaricato da siti esterni.
- Le stesse scelte sono nel menu del pulsante del tema, nella barra superiore: vedi [Tema, carattere e sfondo](interfaccia.md#interfaccia-aspetto).

## <a id="profilo-calendario"></a>Nel calendario del telefono

Dalla 1.116.0, nelle notifiche del profilo, **Nel calendario del telefono** porta in Google Calendar, Outlook o nel calendario dell'iPhone (o di Android) quello che ti riguarda, senza ricopiarlo:

- scegli che cosa: **le tue attività con una data** (dall'inizio alla scadenza, ancora aperte), **i tuoi turni di reperibilità** (con l'ora) e, se vedi lo [Scadenzario](scadenze.md), **le scadenze** che vedi lì (documenti e corsi del personale, mezzi, manutenzioni, scadenze dell'azienda…);
- **Crea l'indirizzo del calendario**: compare un indirizzo segreto da aggiungere al calendario; quando ti serve di nuovo (un altro telefono, un altro calendario) lo ricopi con **Copia l'indirizzo**. Un indirizzo creato prima della versione 1.143.3 non è conservato: **Copia l'indirizzo** propone di rifarlo una volta. In Google Calendar dal computer: Altri calendari → + → Da URL. Sull'iPhone: Impostazioni → Calendario → Account → Aggiungi account → Altro → Aggiungi calendario. In Outlook: Aggiungi calendario → Da Internet. **Apri nel calendario** lo propone direttamente al calendario del dispositivo;
- il calendario rilegge l'indirizzo da solo (Google ogni qualche ora, gli altri anche ogni ora): un'attività spostata o completata si aggiorna senza fare niente. Sotto vedi quando l'hanno letto l'ultima volta;
- chi ha l'indirizzo vede quello che vedi tu, con i tuoi permessi di adesso: non darlo ad altri. **Rifai l'indirizzo** lo cambia (quello di prima smette di funzionare), **Togli il calendario** lo spegne; se il tuo account viene disattivato, l'indirizzo non mostra più niente;
- Google legge l'indirizzo dai suoi server: serve l'**indirizzo pubblico** della piattaforma (Impostazioni → Accesso remoto). Senza, l'indirizzo funziona solo dentro la rete dell'ufficio (per Outlook o il telefono collegato al Wi-Fi dell'ufficio).

---

[← Impostazioni](impostazioni.md) · [Indice](README.md) · [Server e installazione →](server.md)
