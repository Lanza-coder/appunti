Il kernel è un insieme di programmi del [[SO]] che:

● permette l’interazione tra HW e SW 

● è l’unico autorizzato ad accedere direttamente all’hardware, 

● gestisce le risorse HW nel modo più efficiente possibile controllandone tutti gli accessi 

● è responsabile dei driver più importanti 

● è responsabile per la trasmissione e la mediazione dei comandi

  

le funzioni sono:

● Gestire la memoria: controlla quanta RAM viene usata e dove. 

● Gestire i processi: determina quali processi possono usare la CPU, quando e per quanto tempo. 

● Interagire coi Driver del dispositivo: si occupa dell’intermediazione tra l’hardware e i processi. 

● Gestire chiamate di sistema: accetta richieste di servizio dai [[processi]].

  

l’utente può accedere alle chiamate di sistema grazie alla shell (interfaccia grafica) che avvolge il kernel per proteggerlo, l’interfaccia può essere grafica (GUI) o a linea di comando (CUI).
