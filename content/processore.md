gestore del processore: 

I [[SO]] moderni sfruttano le potenzialità di parallelismo dell’hardware per minimizzare i tempi di risposta del sistema ed aumentare il throughput del sistema (numero di programmi eseguiti per unità di tempo).

 Importante distinguere tra:

● Programma: insieme di istruzioni, memorizzato su memoria di massa.

● [[processi]] o task: istanza di programma in evoluzione, cioè che è eseguito dal processore, quindi deve risiedere in RAM.

  

L’ottimizzazione del tempo di elaborazione del processore si ha con la multiprogrammazione (ossia la contemporanea presenza di più programmi in memoria). La gestione del sistema prevede:

 ● Scheduling dei job: insieme di strategie e meccanismi usati per la scelta dei programmi che dal disco devono essere caricati in RAM 

● Scheduling della CPU: insieme di strategie e meccanismi usati per assegnare e sospendere l’utilizzo della CPU da parte dei vari processi 

I [[SO]] multitasking aumentano il throughput “portando avanti” in parallelo più processi e riducendo al minimo l’inattività del [[processore]].
