[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="voce-da-testo"></a>Voce da testo

**Strumenti → Voce da testo** (dalla 1.132.0) crea **file audio da un testo scritto**: il messaggio di benvenuto, di attesa o di fuori orario del **centralino**, gli annunci e i messaggi di evacuazione per gli impianti di **diffusione sonora / EVAC**, la voce fuori campo per **video, sito e social**. Si scrive il testo, si sceglie un modello (motore, voce, come deve parlare, formato) e il programma crea il file: lo si ascolta e poi lo si **salva nei documenti** del cliente o dell'impianto a cui serve, oppure lo si **scarica** e basta. Nella voce da testo non resta nessun file (dalla 1.134.0). La pagina compare a chi può **Usare la voce da testo**; i modelli li gestisce chi ha **Gestire la voce da testo**, le chiavi dei servizi e lo scaricamento delle voci locali un amministratore.

## <a id="voce-da-testo-testo"></a>Il testo: enfasi, pause e tono

Si scrive come si parla; numeri, orari, date e sigle li legge il motore. Pochi segni, con i pulsanti sopra il testo:

| Scrivi | Che cosa succede |
| --- | --- |
| **\*Impianti Rossi\*** | Le parole tra asterischi si dicono con **enfasi** (pulsante **Enfasi** sulle parole scelte). |
| **[pausa]**, **[pausa 2s]**, **[pausa 500ms]** | Una **pausa**: un secondo, oppure quanto scrivi (fino a 10 secondi). |
| una riga vuota | Fine del paragrafo: la pausa del paragrafo del modello. |

Con OpenAI e Gemini il campo **Come deve parlare** descrive a parole il tono, l'emozione e il ritmo, per esempio «voce femminile cordiale e sorridente, ritmo calmo e ben scandito» oppure «voce maschile ferma e autorevole, senza fretta e senza allarmismo»: il servizio lo segue, con la velocità e l'enfasi. Piper e le voci di Windows non seguono un tono scritto a parole: velocità, pause ed enfasi (Windows) sì. Ogni parte tra due pause si legge a sé e il programma mette il silenzio giusto, così le pause sono sempre quelle scritte.

**Prova la voce** (in «Voce e formato») legge l'inizio del testo con le impostazioni di adesso, senza salvarlo; nel modello c'è una frase di prova.

## <a id="voce-da-testo-salvare"></a>Salvare nei documenti o scaricare

**Crea l'audio** prepara il file e lo mostra in cima al pannello, con il lettore per ascoltarlo. A quel punto:

- **Salva nei documenti** (il pulsante blu): scegli **Cliente** o **Impianto**, cerchi per nome, codice, comune o sede, e confermi il **nome del file** (l'estensione la mette il formato). Il file va nella cartella del cliente o dell'impianto in [Documenti](documenti.md), sottocartella **Audio** (creata se manca); con lo stesso nome già presente si numera. L'avviso finale ha **Apri nei documenti**. Per scegliere un cliente o un impianto servono i permessi per vederli.
- ⬇ **Scarica**: il file va sul tuo computer con il nome scritto nell'editor e nel programma non resta niente.
- **Crea di nuovo**: dopo aver cambiato il testo o la voce (il pannello avvisa che quello pronto è ancora il vecchio).

Chiudendo il pannello l'audio pronto si cancella. Se non è stato né salvato né scaricato il programma chiede prima conferma (**Audio non salvato**: «Torna all'audio» oppure «Chiudi e cancella»); lo stesso cambiando pagina. Sul server l'audio pronto resta al massimo 3 ore e si perde se il server si riavvia: in quel caso si ricrea.

La linguetta **Audio** elenca quelli salvati nei documenti, con **Dove** (il cliente o l'impianto): si ascoltano (▶) e si scaricano (⬇) dalla riga; la scheda mostra il testo e le impostazioni usate, con **Nuovo audio da questo** (lo stesso testo e la stessa voce, da cambiare e ricreare) e in «Altro» **Apri nei documenti** e **Togli dall'elenco** (il file resta nei documenti). Gli audio dei clienti privati di altri non compaiono. Se il documento è stato eliminato o è nel cestino la riga dice **Non più nei documenti** (ripristinandolo torna).

Gli audio creati con la 1.132.0 e la 1.133.0 hanno ancora il file nella voce da testo: sono segnati **Da sistemare** e un avviso sopra l'elenco li conta. Dalla loro scheda si salvano nei documenti (il file si sposta) oppure si scaricano e si eliminano.

## <a id="voce-da-testo-modelli"></a>Modelli

Il modello tiene motore e voce, il modello del servizio, come deve parlare, la velocità (e il tono per Windows), il formato del file e i ritocchi: **volume al picco** (−1 dB è il massimo senza distorsione, −3 dB per i centralini), volume in più o in meno, **silenzio prima e dopo**, **pausa tra i paragrafi**, silenzio tolto ai bordi di ogni parte. Nella linguetta **Modelli**, chi li gestisce trova i **modelli proposti**, da creare con un clic con il primo motore pronto e poi da adattare:

- **Centralino**: voce femminile cordiale, WAV 8 kHz mono 16 bit, −3 dB, un po' di silenzio prima e dopo;
- **Diffusione sonora / EVAC**: voce maschile ferma e scandita, un po' più lenta, WAV 48 kHz mono 16 bit;
- **Video, sito e social**: voce calda e coinvolgente, MP3 44,1 kHz stereo a 192 kbit/s.

Un audio prende le impostazioni del modello scelto e si possono cambiare solo per lui. Eliminando un modello gli audio creati restano, con le impostazioni che avevano.

## <a id="voce-da-testo-formati"></a>Formati

| Formato | Per che cosa |
| --- | --- |
| **WAV** 8, 16 o 24 bit | Quasi ovunque: centralini (8 kHz mono 16 bit), impianti EVAC e diffusione sonora (16 o 48 kHz), montaggio video (48 kHz). |
| **WAV µ-law / A-law (G.711)** | I centralini che li chiedono (8 kHz mono): µ-law nei sistemi americani e in molti VoIP, A-law in Europa. |
| **µ-law / A-law senza intestazione** | Asterisk e simili (file .ulaw e .alaw). |
| **MP3**, **M4A (AAC)** | Video, sito e social. Li crea il codificatore di Windows: su Windows Server serve la funzionalità «Media Foundation» (Server Manager → Aggiungi ruoli e funzionalità); se manca il programma lo dice. MP3 a 16-48 kHz, M4A a 44,1 o 48 kHz da 96 a 192 kbit/s. |

La frequenza scende senza disturbi (il programma filtra prima di ricampionare, anche fino agli 8 kHz del telefono) e il volume si porta al picco scelto dopo il ricampionamento. In **Audio** ogni audio si ascolta (▶) e si scarica (⬇) dalla sua riga; i formati che il browser non legge (G.711) si ascoltano convertiti, il file scaricato resta quello scelto.

## <a id="voce-da-testo-motori"></a>Motori

| Motore | Come funziona |
| --- | --- |
| **OpenAI** | In cloud, voce molto naturale, il tono descritto a parole (13 voci). Si paga a caratteri. Serve la chiave API di OpenAI: la scrive un amministratore nella linguetta **Motori**, oppure si usa quella dell'[assistente AI](assistente-ai.md) se è di OpenAI. |
| **Gemini** | In cloud, naturale, il tono descritto a parole (30 voci). Chiave di Google AI Studio, oppure quella dell'assistente AI se è di Gemini. |
| **Voce locale (Piper)** | Sul server, gratis e senza internet: voci neurali italiane (Paola, Riccardo). Un amministratore scarica il motore e le voci scelte dalla linguetta **Motori** (circa 20 MB più 30-60 MB a voce); restano nella cartella degli strumenti del server. |
| **Voci di Windows** | Le voci già installate su Windows (anche Elsa e Cosimo), gratis e senza internet, più robotiche. Le voci italiane si aggiungono da Impostazioni di Windows → Ora e lingua → Lingua. |

Nella linguetta **Motori** si vede se ogni motore è pronto e quanti caratteri ha letto nel mese (con le prove), utile per i costi dei servizi in cloud. Le chiavi si salvano cifrate. I file salvati sono documenti come gli altri (anche nei backup, con le regole e il cestino di Documenti).

---

[← Monitoraggio](monitoraggio.md) · [Indice](README.md) · [Rete locale →](rete-locale.md)
