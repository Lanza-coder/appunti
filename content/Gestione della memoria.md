Codice rilocabile:  
Quando un programma viene caricato in memoria, gli indirizzi relativi (logici) sono trasformati in indirizzi assoluti (fisici).

- Rilocazione statica: calcolo fatto al caricamento del programma, sommando l'indirizzo base agli offset.
    
- Rilocazione dinamica: durante l'esecuzione, ogni indirizzo logico è sommato al valore del registro base.
    

MMU (Memory Management Unit):  
Dispositivo hardware che traduce indirizzi logici in fisici. Usa la formula:  
Indirizzo fisico = Indirizzo logico + Registro di rilocazione.

Linking e Binding:

- Linking: calcola indirizzi logici.
    
- Binding: converte indirizzi logici in fisici:
    

- Durante la compilazione (indirizzi assoluti).
    
- Durante il caricamento (rilocazione statica).
    
- Durante l'esecuzione (rilocazione dinamica).
    

  

Gestione della memoria:

- Per caricare un processo, la memoria deve avere spazio contiguo e sufficiente.
    
- Problemi:
    

- Programmi grandi che superano la RAM.
    
- Frammentazione dovuta al continuo caricamento e scaricamento di [[processi]].
    
- Solo alcune istruzioni sono realmente eseguite.
    

Soluzioni:

1. Swapping: spostare processi inattivi su disco (rallentamenti possibili).
    
2. Caricamento dinamico: caricare solo le parti del programma necessarie.
    
3. Overlay: frazionare il programma e caricare le parti in memoria alternandole.
    
4. Partizionamento: dividere la memoria in blocchi di dimensioni fisse o variabili.
    

Partizioni fisse:

- Blocchi creati staticamente all'inizializzazione del sistema.
    
- Le partizioni possono essere di dimensioni diverse.
    
- Problemi:
    

- Frammentazione esterna: memoria totale sufficiente ma non contigua.
    
- Frammentazione interna: memoria sprecata quando processi piccoli occupano partizioni grandi.
    
- Soluzione: singola coda d'ingresso per assegnare i job.
    

Partizioni variabili:

- Blocchi creati dinamicamente.
    
- Strategie di allocazione:
    

- First-fit: prima zona libera abbastanza grande.
    
- Best-fit: zona più piccola sufficiente, ma può lasciare zone inutilizzabili.
    
- Worst-fit: zona più grande.
    
- Next-fit: cerca da dove è avvenuta l’ultima allocazione.
    

  

Memoria virtuale:  
Permette di ridurre la frammentazione, caricando in memoria centrale solo le parti del programma in uso.

Paginazione:

- La memoria è divisa in frame (fisici) e pagine (logiche) della stessa dimensione.
    
- Page fault: avviene quando una pagina necessaria non è in memoria e il SO la carica dal disco.
    
- Ogni programma ha una tabella delle pagine che indica quali sono in RAM e quali su disco (bit di validità: 1 se in memoria, 0 altrimenti).
    

Segmentazione:

- La memoria è divisa in segmenti di dimensioni variabili, associati a funzioni del programma (codice, dati, stack).
    
- Ogni segmento ha un indirizzo base e un limite.
    
- Segmentazione fault: avviene se un indirizzo supera il limite del segmento.
    

  
  

Segmentazione con paginazione:

- Combina i vantaggi di entrambe.
    
- Ogni segmento è suddiviso in pagine logiche, caricate in frame fisici senza frammentazione.
    
- Gli indirizzi logici hanno tre componenti: segmento, pagina, spiazzamento, tradotti in frame e spiazzamento fisico tramite MMU e tabelle.
