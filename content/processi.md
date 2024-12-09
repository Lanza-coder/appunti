Un intero sistema o un insieme di processi che possono essere eseguiti in parallelo sui processori alternando nell’esecuzione.

  

Ogni processo è costituito da due parti: 

● codice (composto dalle istruzioni); 

● dati del programma, a loro volta suddivisi in:

 – variabili globali, allocate nella RAM nell’area dati globali

 – variabili locali e non locali memorizzate in uno stack 

 – variabili temporanee introdotte dal compilatore (tra cui PC o IP) caricate nei registri del processore

 – variabili allocate dinamicamente durante l’esecuzione, memorizzate in un heap.

  

E’ possibile avere in esecuzione contemporaneamente più istanze di un programma, ossia più [[processi]] originati dallo stesso codice. I processi possono essere:

  

● Indipendenti: un processo può evolvere autonomamente senza necessità di scambiare dati con altri processi 

● Cooperanti: due o più processi per evolvere necessitano di scambiarsi informazioni 

● Competitori: due processi possono ostacolarsi a vicenda, per usare la medesima risorsa, compromettendo la terminazione delle loro elaborazioni

  
  

un programma può generare più processi, ma ogni processo è associato ad un solo programma.

  

processo utente: processo generato da un programma scritto dall’utente

processo supervisore: processo generato da un programma del SO( es. gestore dell attività)

  

i processi supervisori in esecuzione sulla cpu (in background) hanno un’importanza maggiore rispetto ai processi utente.

  

quando un programma va in esecuzione viene creato il processo(memorizzato in memoria centrale).

Ciclo di vita di un processo 

Mancano gli stati new ready running….

- Quando è creato un nuovo processo, gli viene assegnato un identificatore (PID, Process Identifier, contenuto nella "[[Struttura PCB]]") e viene inserito nell’elenco dei [[processi]] pronti.
    
- Quando gli viene assegnata la CPU, il processo passa nello stato di esecuzione, dal quale può uscire per tre motivi: 
    

– termina la sua esecuzione, 

– termina il suo tempo nel [[processore]], cioè il quanto di tempo a sua disposizione.

– gli manca la disponibilità di una risorsa: per poter evolvere necessita di una risorsa al momento non disponibile e quindi il processo si sospende e passa nello stato di attesa formando

-  Dallo stato di sospeso (in WL) un processo esce solo quando ottiene la risorsa attesa.
