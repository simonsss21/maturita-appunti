# **Firewall**

Il **firewall** è uno strumento di sicurezza di rete, che controlla e filtra il traffico di dati in ingresso e in uscita da una rete, sulla base di un insieme di regole di sicurezza.  <br>
Analizza i pacchetti, verificando IP sorgente, IP destinazione, porte, protocolli e stato di connessioni.<br>

Può operare a diversi livelli della pila ISO/OSI:<br>
- **LIVELLO 3**: IP filtering. <br>
- **LIVELLO 4**: port filtering. <br>
- **LIVELLO 7**: application-level filtering.<br>

Esistono due posizioni di Firewall:<br>
- **Perimetrale**: protegge l'intera rete in ingresso e in uscita.<br>
- **Privato**: protegge il singolo host sia in ingresso che in uscita. <br>

Nei firewall il traffico viene controllato tramite regole di tipo allow e deny: <br>
- le regole **allow** permettono il passaggio dei pacchetti.<br>
- le regole **deny**, invece, bloccano il passaggio dei pacchetti<br>

A livello di politica generale, esistono due approcci:<br>
- **default allow**, in cui tutto è permesso tranne ciò che è esplicitamente negato (blacklist).<br>
- **default deny**, in cui tutto è bloccato tranne ciò che è esplicitamente consentito (whitelist).<br>

Esistono anche delle modalità di funzionamento dei firewall:<br>
- **Stateless**: il firewall stateless analizza ogni pacchetto in modo indipendente, senza memoria delle connessioni, controllando IP sorgente e destinazione, porte e protocollo, ma non sa se il pacchetto proviene da una connessione già esistente. <br>
- **Stateful**: il firewall stateful tiene conto di una tabella di stato delle connessioni, controllando le connessioni attive e il TCP state (stati e fasi della connessione). <br>
- **Proxy**: il firewall proxy, a differenza degli altri due, non è trasparente all'utente, poiché si interpone tra client e server: il client invia la richiesta al firewall, il firewall la analizza e, se consentita, la inoltra al server; quindi la connessione viene interrotta e ricreata.<br>