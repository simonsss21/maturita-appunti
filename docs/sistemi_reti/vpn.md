# **VPN**

La VPN (Virtual Private Network) è un'infrastruttura di rete, che consente di **estendere in modo sicuro una rete privata** in una rete pubblica mediante l'uso combinato di tunneling, crittografia e autenticazione.  
Viene creato un tunnel logico cifrato tra i due end-point (mittente e destinatario), all'interno del quale i pacchetti vengono incapsulati, cifrati e autenticati. 

Quando un dispositivo si connette ad una VPN, avviene una fase di **handshake**, durante la quale vengono stabiliti algoritmi di cifratura, algoritmi di hashing e le chiavi. Il traffico IP originale viene **incapsulato in un nuovo pacchetto IP**, e il contenuto viene cifrato prima di essere trasmesso. 

Tipi di VPN:
- **Peer-to-peer**: agisce tra mittente e destinatario, garantisce un accesso da remoto alla LAN, tramite autenticazione dell'utente (credenziali).
- **Site-to-site**: collega tra di loro due reti. È trasparente per gli utenti, nel senso che non devono connettersi manualmente. Crea un tunnel stabile tra router e/o firewall. 

Livelli di applicazione:
La VPN può operare in diversi livelli della pila ISO/OSI, a seconda delle esigenze:
- **LIVELLO 2 (DATALINK)**: viene creato un tunnel a livello di frame Ethernet, permettendo di estendere una LAN remota come se fosse locale.

- **LIVELLO 3 (NETWORK)**: si utilizzano protocolli come l'IPsec, in questo contesto l'AH (Authentication Header, garantisce integrità e autenticazione) e l'ESP (oltre a garantire integrità e autenticazione, garantisce la cifratura del payload).

L'IPsec ha due modalità operative: **TRANSPORT MODE** (viene cifrato soltanto il payload, e l'IP header originale resta lo stesso), **TUNNEL MODE** (viene cifrato l'intero pacchetto IP originale header + payload).  

Possiamo combinare queste due modalità con i protocolli **AH** ed **ESP** per ottenere diversi tipi di cifratura. 

- **LIVELLI 4-7** (TRANSPORT/APPLICATION): qui le VPN lavorano tramite protocolli sicuri come SSL o DTLS, che operano sopra il TCP (orientato alla connessione) e l'UDP (non orientato alla connessione). 

Tramite il protocollo **TCP** viene inviato l'**ACK** della sequenza di pacchetti ricevuti; se sono stati inviati 100 pacchetti e il destinatario invia l'ACK al pacchetto 60 significa che gli altri 40 pacchetti non sono stati ricevuti, ciò porta alla riduzione della **Window Size** (quantità di pacchetti inviati di seguito).  
Se invece l'utente invia l'ACK del 100° pacchetto, possiamo aumentare la **Window Size**.