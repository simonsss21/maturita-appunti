# **Crittografia**

La **crittografia** è un insieme di procedure ideate allo scopo di nascondere il significato di un messaggio, tranne al destinatario.  <br>
Alla base si ha un **cifrario**, nel quale ogni carattere del testo da cifrare viene trasformato in un altro carattere, attraverso un processo chiamato algoritmo di cifratura.<br>  
Esistono anche tecniche che utilizzano codici, il quale ognuno può rappresentare un concetto o un informazione.<br>

Per cifrare un testo, occorre:<br>
- un **algoritmo**, che deve essere pubblico,<br>
- una **chiave**, privata e quanto più sicura possibile.<br>

La chiave, deve essere la stessa sia per mittente che per destinatario, e serve per criptare e decriptare il messaggio.<br>

Abbiamo diversi sistemi crittografici:<br>
- A **sostituzione**: ogni elemento, è trasformato in un altro elemento.<br>
- A **permutazione**: gli elementi del testo vengono riorganizzati.<br>
- A **blocchi**: il testo viene diviso in blocchi di bit, e ogni blocco viene elaborato.<br>
- A **flusso**: elabora un quantitativo di bit variabile. <br>

Abbiamo due tipi di crittografia, simmetrica e asimmetrica:<br>
- **Simmetrica**: si utilizza una chiave soltanto, che cripta e decripta il messaggio. Il problema sostanziare sta nell'inviare la chiave al destinatario in maniera sicura.<br>

- **Asimmetrica**: si utilizzano due chiavi per ogni soggetto, una pubblica e una privata. Il mittente, cripta il messaggio con la chiave pubblica del destinatario, il quale decripterà il messaggio con la propria chiave privata.  <br>

  È la spiegazione dell'algoritmo RSA, il quale problema sostanziale è garantire l'identità del mittente. Per ovviare a questo si utilizzano enti certificati, in grado di generare delle chiavi certificate.  <br>
  Gli enti certificati, garantiscono: privacy, autenticità, integrità e non ripudio.<br>

  Tramite la crittografia Asimmetrica, possiamo inviare la chiave, permettendoci di utilizzare una crittografia Simmetrica, che risulta piu veloce. <br>

Alcuni algoritmi:<br>
- **Simmetrici**: DES (a permutazione), AES (utilizza funzioni lineari, basandosi sul calcolo).<br>
- **Asimmetrici**: RSA: genera due chiavi (A e B) sia per mittente che per destinatario, una cripta e l'altra decripta (la stessa chiave non puo fare entrambe le cose).<br>