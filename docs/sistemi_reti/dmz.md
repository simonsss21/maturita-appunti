# **DMZ**

La **DMZ** (DeMilitarized Zone) è una zona di rete intermedia tra Internet e la rete interna, utilizzata per ospitare servizi pubblici.  <br>
Serve ad isolare la LAN: anche in caso di compromissione dei servizi nella DMZ, l'attaccante non può accedere direttamente alla rete interna. <br>

La DMZ è tipicamente separata da uno o due firewall:<br>

Internet ↔ Firewall ↔ DMZ ↔ Firewall ↔ LAN<br>

All'interno della DMZ, **non vanno assolutamente depositati dati sensibili/importanti per l'azienda**, perché ovviamente accessibili da tutti.<br>

I due firewall (uno **deny** e uno **allow**) sono progettati in modo tale da garantire l'accesso a chiunque alla DMZ ma a nessuno alla LAN. <br>

Firewall **esterno**: allow, permette l'accesso a tutti<br>
 
Firewall **interno**: deny, non permette l'accesso a nessuno, tranne a chi inserito nella access list.<br>