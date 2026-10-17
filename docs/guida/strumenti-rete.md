[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="strumenti-rete"></a>Strumenti di rete

**Strumenti → Strumenti di rete** (dalla 1.142.0) raccoglie gli strumenti per capire che cosa non va in rete, fatti **dal server**: è lui che fa il ping, il traceroute e le prove, quindi si vede la rete come la vede il monitoraggio. La pagina compare a chi può **Vedere il monitoraggio**; la diagnostica e le prove le fa chi lo gestisce, e finiscono nel registro attività.

## <a id="strumenti-rete-diagnostica"></a>Diagnostica

- **Ping**: da 4 a 50 ping di fila, anche grandi (1472 byte, il massimo senza frammentare) e in IPv6: risposte, tempo medio, minimo e massimo, **perdita** e **jitter** (quanto cambia il tempo da un ping all'altro), il sistema operativo dal TTL e una barra per ogni ping.
- **Traceroute**: la strada fino al dispositivo, router per router, con tre tempi per salto e il nome dei router. I salti partono tutti insieme, così dura pochi secondi. Un router che non risponde (*\* \* \**) non è un errore se i salti dopo rispondono.
- **DNS**: i record di un nome (A, AAAA, CNAME, MX, NS, TXT, SOA, CAA, SRV) o il nome di un indirizzo IP, dal DNS del server o da uno scelto (per confrontare, per esempio 1.1.1.1 o il DNS del provider), con il tempo di risposta.
- **WHOIS**: di chi è un dominio o un indirizzo IP: registrar, intestatario, date di creazione e scadenza, name server, stato; per un indirizzo la rete, il nome della rete, l'AS e il contatto per gli abusi. Se la porta 43 è chiusa dal firewall si usa RDAP.
- **Porte**: le porte aperte di un dispositivo (un gruppo già pronto o quelle scritte, fino a 1024, anche UDP), con che cosa dice ogni servizio.

Dal [monitoraggio](monitoraggio.md), nella scheda di un controllo, **Diagnostica** apre il traceroute verso quel dispositivo.

## <a id="strumenti-rete-traffico"></a>Traffico

Le schede di rete del server, una alla volta (si sceglie sotto le linguette, con il periodo da 1 a 30 minuti): quanto ricevono e mandano adesso e da quando è acceso, l'andamento dei dati ricevuti e di quelli inviati, indirizzi, gateway, DNS, DHCP, MAC e velocità del collegamento.

## <a id="strumenti-rete-prove"></a>Prove della connessione

**Prova la connessione**, in alto, misura in circa 20 secondi la connessione del server: latenza, jitter e perdita verso il **gateway** (la rete locale) e verso **internet** (1.1.1.1), il tempo di risposta del **DNS** e, se scelto, la velocità di **download** e **upload** verso i server di prova di Cloudflare. Sotto i numeri, una nota dice per che cosa basta la connessione (navigazione, videochiamate, telefonia, telecamere da remoto, streaming); poi il grafico del download nel tempo e la storia delle prove. In **⋯ Altro → Impostazioni delle prove** si sceglie la **prova automatica**, che il server fa da solo ogni tante ore (si vede quando il provider rallenta), e se misurare download e upload, che muovono qualche decina di MB: con una connessione a consumo, toglili.

---

[← Rete locale](rete-locale.md) · [Indice](README.md) · [Ricerca →](ricerca.md)
