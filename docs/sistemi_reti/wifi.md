# **Wi-Fi**

Il **Wi-Fi** è una tecnologia di comunicazione wireless che consente a dispositivi elettronici di connettersi a una rete locale senza cavi.  <br>
È uno standard di rete basato sui protocolli **IEEE 802.11** che opera nelle bande di frequenza **2,4 GHz** e **5 GHz**. <br>

Il Wi-Fi opera principalmente ai livelli 1 e 2:<br>
- Il **livello 1** si occupa della **trasmissione dei bit**,<br>
- Il **livello 2** si occupa dell'**indirizzo MAC** e dell'**LLC** (suddivisione del messaggio in pacchetti, mentre il **CSMA/CA** gestisce le collisioni).  <br>
  Si hanno 4 indirizzi MAC, di cui **3 utilizzati sempre** (mittente, destinatario, access point).<br>

**Access point**: condivide l'**SSID**, fa da bridge tra due protocolli, in questo caso tra l'**802.3** (Ethernet) e l'**802.11**.  
Viene garantita la connessione trasmettendo l'SSID ma non può essere considerato sistema di sicurezza poiché **mascherabile**. <br>

Si hanno due tipi di reti:<br>
- **Infrastructure**: alla stazione di trasmissione si connettono dei client, che devono essere entro il raggio di portata della stazione.<br>
- **Ad Hoc**: ogni dispositivo fa da access point per il dispositivo successivo.<br>

- La frequenza 2,4 GHz copre **lunghe distanze** ma a **bassa frequenza**.<br>
- La frequenza 5 GHz copre **brevi distanze** ma ad **alta frequenza**. <br>

Il protocollo **802.11** ha subito delle rivisitazioni, ogni versione è identificata da una lettera, che si differenzia per la banda di frequenza utilizzata. <br>

In Ethernet la connessione è **bilaterale**: si hanno due canali (uno per l'invio e uno per la ricezione). <br>

Nel Wi-Fi questo non avviene perché la potenza della trasmissione è più alta della ricezione e interferisce. Alla luce di ciò, si hanno due problemi:<br>
- **Stazione nascosta**: si hanno due host lontani tra loro (che non si vedono) e un terzo a metà strada che vedono entrambi. Se entrambi gli host inviano il pacchetto alla stazione si ha una collisione, perciò l'host che intende comunicare deve inviare un **RTS** (richiesta di comunicazione) alla stazione.<br>
- **Stazione esposta**: si hanno 4 host vicini tra loro (A-B-C-D): se A e B stanno parlando fra loro, C non può comunicare con D perché sente B. Stessa cosa se comunicano C e D e B intende parlare con A. <br>

Il Wi-Fi utilizza due protocolli per garantire la sicurezza:<br>
- **WEP**: è il primo standard di sicurezza per reti Wi-Fi, utilizza l'algoritmo di cifratura RC4 (basato sul flusso), una chiave condivisa + un IV variabile ma molto corto e cifra i dati trasmessi tra dispositivo e access point.  <br>
- **WPA**: è una versione aggiornata del WEP, poiché introduce TKIP e chiavi dinamiche più sicure. TKIP è un protocollo introdotto con WPA per migliorare la sicurezza del WEP, utilizzando chiavi dinamiche e un IV più lungo.  <br>
- **WPA2**: è il WPA, ma con l'AES al posto dell'RC4. <br>

Da sottolineare che l'**RC4** dà problemi con l'**handshake**, poiché se un dispositivo fa una richiesta di disconnessione, un altro dispositivo si può connettere con le credenziali del dispositivo appena disconnesso.<br>