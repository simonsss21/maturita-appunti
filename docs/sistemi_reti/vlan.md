# **VLAN**

Una VLAN (Virtual LAN) è una rete locale virtuale che permette di dividere logicamente una rete fisica in più reti separate.<br>

In pratica, anche se più dispositivi sono collegati allo stesso switch fisico, possono appartenere a reti diverse.<br>

Esempio:<br>

VLAN 10 → Amministrazione  <br>
VLAN 20 → Studenti  <br>
VLAN 30 → Server  <br>
VLAN 40 → Ospiti  <br>

Ogni VLAN rappresenta un dominio di broadcast separato: un broadcast inviato nella VLAN 10 non arriva ai dispositivi della VLAN 20.<br>

Le VLAN servono principalmente per:
- **Segmentare la rete**: separano gruppi di dispositivi in base al ruolo, al reparto o al livello di sicurezza.<br>
- **Aumentare la sicurezza**: un utente della VLAN ospiti, ad esempio, non può comunicare direttamente con la VLAN amministrazione.<br>
- **Ridurre il traffico broadcast**: ogni VLAN limita i broadcast solo ai dispositivi appartenenti alla stessa VLAN.<br>
- **Organizzare meglio la rete**: non serve spostare fisicamente i cavi, basta cambiare la configurazione dello switch.<br>

**Livello OSI**<br>
Le VLAN lavorano principalmente al livello 2 (Data Link) della pila ISO/OSI, perché si basano sugli switch e sugli indirizzi MAC.<br>  
Lo standard usato è **IEEE 802.1Q**, che inserisce un’etichetta chiamata VLAN tag dentro il frame Ethernet.<br>

**Trunk port**<br>
Una trunk port può trasportare traffico di più VLAN contemporaneamente.<br>

È usata per collegare:<br>
switch ↔ switch  <br>
switch ↔ router  <br>
switch ↔ firewall  <br>
switch ↔ access point aziendale <br> 

Nel trunk, i frame vengono marcati con un tag 802.1Q (VLAN ID indica a quale VLAN appartiene il frame), così il dispositivo ricevente sa a quale VLAN appartiene ogni frame.  <br>
Tra due switch passa un unico cavo trunk che trasporta VLAN 10, VLAN 20 e VLAN 30.<br>

**Router-on-a-stick**<br>

Il router-on-a-stick è una configurazione in cui un router gestisce più VLAN usando una sola interfaccia fisica.<br>  
Tra switch e router si usa una porta trunk. Sul router si creano più sub-interface, una per ogni VLAN.<br>

Esempio:  <br>
G0/0.10 → VLAN 10  <br>
G0/0.20 → VLAN 20  <br>
G0/0.30 → VLAN 30  <br>

Ogni sub-interface ha il gateway della rispettiva VLAN.<br>