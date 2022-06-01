# How to use GitHub
## This is the Heading two
c'est project d'assemblage de génome bacterien

### this is heading 3
````bash
cp mon fichier target/dir
````

### this step is for trimming
````bash
code for trimming
````
## Diagram
```mermaid
graph TD

    X(Sequence Read Archives) -- SRAtools --> A(Raw Reads)
    A -->|seqtk| Q(Collecting raw read stats)
    A -->|kmc| B(Estimating genome size)
    Q --> C
    B --> D
    A --> |Trimmomatic| C(Trimming reads)
    C --> |Lighter| D(Correcting reads)
    D --> | FLASh| P(Overlapping reads)
    P --> |SPAdes| E(Assembling reads)
    E --> |bwa mem & SAMtools & Pilon| S(Checking for assembly errors)
    
    S --> O(Final Assembly)
    S --> |QUAST & BUSCO| G(Assessing Assembly)
    O --> Annotation
    O --> Phylogenomics
    O --> t(Comparative Genomics)
     classDef green fill:#9f6,stroke:#333,stroke-width:2px
     classDef orange fill:#f96,stroke:#333,stroke-width:4px
     class X,A green
     class C,D,E orange
```
