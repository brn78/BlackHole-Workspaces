[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="rete-locale"></a>Rete locale

**Strumenti → Rete locale** è lo **scanner della rete**: cerca i dispositivi delle reti dell'azienda (e delle VLAN scritte nei [gruppi del monitoraggio](monitoraggio.md#monitoraggio-gruppi)) e ne tiene l'inventario: che cosa sono, da quando ci sono, se sono fissi o di passaggio e se il monitoraggio li controlla già. La pagina compare a chi può **Vedere il monitoraggio**; scansionare e cambiare le impostazioni spetta a chi lo gestisce.

In alto i numeri: **Online**, **Nuovi** (comparsi negli ultimi 7 giorni), **Fissi non controllati** (sempre in rete ma non nel monitoraggio), **Doppioni** e l'ultima scansione; un clic sul numero mostra quei dispositivi. **Scansiona adesso** fa una scansione: durante la scansione si vede la fase e l'avanzamento, e **Ferma** la interrompe.

> [!NOTE]
> **Fin dove arriva.** Nella rete del server lo scanner vede tutti i dispositivi con il loro **MAC** e il **produttore**, anche quelli che non rispondono al ping. Nelle altre reti e VLAN, oltre il router, vede chi risponde al ping o ha una porta comune aperta, i nomi e le porte, ma il MAC solo dei PC Windows (con il NetBIOS): un dispositivo lì si riconosce dall'indirizzo.

## <a id="rete-locale-dispositivi"></a>I dispositivi

L'elenco, con i filtri **Tutti**, **Online**, **Nuovi**, **Conosciuti**, **Fissi**, **Di passaggio**, **Fissi non controllati** e **Ignorati** e la ricerca per nome, indirizzo, MAC o produttore: il pallino verde se c'era nell'ultima scansione, il **dispositivo** con il tipo, l'**indirizzo** con la rete e la VLAN, il **MAC** con il produttore, la **valutazione**, **da quando è online** (o quando è stato visto l'ultima volta), le **porte** aperte e il **monitoraggio**. Il tipo lo propone lo scanner dal produttore, dalle porte aperte, dai nomi e dal titolo della pagina web: telecamera o videoregistratore, centrale d'allarme, rete (router, switch, access point), stampante, NAS, PC, server, telefono o tablet, domotica, dispositivo con pagina web.

Un clic apre la **scheda**: indirizzo (con **apri la pagina** se ha una pagina web), MAC, produttore, nomi, rete, titolo della pagina, risposta al ping, porte aperte con il loro uso, quando è stato visto, la **presenza** nelle ultime scansioni, gli indirizzi avuti e i controlli del monitoraggio. Chi gestisce scrive il **nome** che usate voi, sceglie il **tipo**, scrive le **note**, lo segna come **Conosciuto** (non è più nuovo e non fa partire l'avviso) o **Ignorato** (sparisce dall'elenco e dai doppioni), oppure lo **elimina** dall'inventario (se è ancora in rete, torna come nuovo).

Un dispositivo **conosciuto** ha la spunta verde accanto al nome; uno **nuovo** ha la pastiglia *Nuovo* accanto alla valutazione. Per sistemarne tanti insieme (per esempio dopo la prima scansione) premi **Scegli più righe** in alto a sinistra, spunta i dispositivi (la casella in testa li sceglie tutti, anche filtrati) e nella barra che compare scegli **Segna come conosciuti**, **Non più conosciuti**, **Ignora**, **Non ignorare più** o **Elimina**.

## <a id="rete-locale-valutazione"></a>Fissi, di passaggio e nuovi

- **Fisso**: c'è almeno sei volte su dieci dalla prima scansione in cui è comparso.
- **Di passaggio**: c'è meno spesso, oppure ha un **MAC casuale**: i telefoni e i PC con la privacy delle reti Wi-Fi attiva ne usano uno inventato, quindi il produttore non si conosce e non contano tra i nuovi.
- **Nuovo**: comparso da meno di un giorno (e meno di tre scansioni).

## <a id="rete-locale-monitoraggio"></a>Nel monitoraggio e doppioni

Ogni dispositivo dice se il [monitoraggio](monitoraggio.md) lo controlla già, anche se il controllo usa il nome invece dell'indirizzo. **Aggiungi** apre un controllo nuovo con il nome, l'indirizzo e le note già scritti: se il dispositivo è già controllato (anche con un altro indirizzo o nome), il modulo lo dice e chiede conferma prima di farne un altro uguale.

La linguetta **Doppioni** confronta l'inventario con il monitoraggio:

- **Controlli doppi sullo stesso dispositivo**: due controlli dello stesso tipo sullo stesso dispositivo, per esempio un ping all'indirizzo e uno al nome;
- **Controllo su un indirizzo cambiato** (in rosso): il dispositivo per cui era il controllo adesso ha un altro indirizzo (il DHCP gliel'ha cambiato) e il controllo guarda quello vecchio, magari di un altro dispositivo;
- **Indirizzo conteso**: lo stesso indirizzo usato da due dispositivi diversi nelle ultime 24 ore (due indirizzi fissi uguali, oppure un indirizzo riassegnato mentre l'altro era spento);
- **Nome ripetuto**: lo stesso nome su dispositivi diversi (per esempio un PC clonato).

Ogni doppione ha i pulsanti per aprire i dispositivi e i controlli. La linguetta **Scansioni** elenca le scansioni, a mano e automatiche, con quanti dispositivi hanno trovato e quanti nuovi.

## <a id="rete-locale-impostazioni"></a>Impostazioni

- **Reti da scansionare**, una per riga (*192.168.1.0/24*, al massimo /20 per rete): **Proponi le reti del server** aggiunge quelle delle sue schede di rete. Con **Anche le reti dei gruppi del monitoraggio** si scansionano anche quelle scritte nei gruppi, con la loro VLAN. Nessuna rete si scansiona finché non la scegli. Le reti dei gruppi che non si possono scansionare si saltano, con il motivo scritto nella pagina, nelle impostazioni e nella storia delle scansioni, e le altre si scansionano lo stesso: troppo grandi (oltre /20), 127.x (è il server stesso), 169.254 (indirizzi automatici senza DHCP), multicast.
- **Scansione automatica**: solo a mano, oppure ogni 30 minuti, ora, 4 ore, 12 ore o ogni giorno; la storia delle scansioni si tiene per i giorni scelti (di serie 90).
- **Porte da provare** su ogni dispositivo trovato (vuoto: quelle di serie, cioè web, accesso remoto, condivisioni, telecamere, stampanti, domotica e Modbus) e **Oltre il router cerca anche chi non risponde al ping** (porte comuni: trova i PC con il firewall e molte telecamere, ma la scansione dura di più).
- **Avvisi** a chi gestisce il monitoraggio: i **dispositivi nuovi** (una notifica per scansione, non i MAC casuali) e quando un **dispositivo controllato cambia indirizzo**.
- **Produttori dal MAC**: dalla 1.141.0 l'elenco è già nel programma e il produttore si vede subito. L'elenco comprende i blocchi grandi dell'IEEE (**MA-L**) e quelli piccoli (**MA-M** e **MA-S**) in cui l'IEEE divide alcuni blocchi grandi: per ogni MAC si usa il blocco più preciso, così telecamere, domotica e apparati industriali mostrano il produttore vero e non «IEEE Registration Authority». **Scarica l'elenco dall'IEEE** fa scaricare al server i tre registri ufficiali (circa 6 MB), che hanno la precedenza su quello del programma (dalla 1.142.0, finché non ne è stato scaricato o caricato nessuno, il server li scarica da solo alla prima scansione); se il server non va su internet, scarica dal sito dell'IEEE *oui.csv*, *mam.csv* e *oui36.csv* (o il file *manuf* di Wireshark) e usa **Carica il file**, anche con più file insieme: ogni file aggiorna il suo registro e lascia gli altri.
- **Che cosa cercare** (dalla 1.142.0): **le porte UDP** più comuni (DNS, orario NTP, SNMP con la descrizione del dispositivo, UPnP), **che cosa dicono i servizi** sulle porte aperte (il programma e la versione di SSH, FTP, posta, pagina web e telecamere, il nome e la scadenza del certificato) e **gli indirizzi IPv6** dei dispositivi delle reti del server. Con **Avvisa quando su un dispositivo si apre una porta nuova** arriva una notifica per scansione con le porte comparse.

## <a id="rete-locale-servizi"></a>Sistema operativo, servizi, IPv6 e porte

Dalla 1.142.0 la scheda del dispositivo dice anche il **sistema operativo** probabile, dal TTL della risposta al ping (64 Linux, Android, macOS e iOS; 128 Windows; 255 gli apparati di rete: ogni router lungo la strada lo abbassa di uno), gli **indirizzi IPv6**, le **porte UDP** che rispondono, i **servizi** con quello che dicono di sé (utile per riconoscere il dispositivo e le versioni vecchie da aggiornare) e la storia delle **porte aperte e chiuse** da una scansione all'altra. Un dispositivo che prima non aveva il desktop remoto o Telnet e adesso sì salta all'occhio.

---

[← Voce da testo](voce-da-testo.md) · [Indice](README.md) · [Strumenti di rete →](strumenti-rete.md)
