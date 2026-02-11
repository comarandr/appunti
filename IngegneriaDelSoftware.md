# INGEGNERIA DEL SOFTWARE

## 1. CONCETTI FONDAMENTALI

### Tipologie di Software Professionale

SOFTWARE: insieme dei programmi e relativa documentazione (modelli di progetto, manuali utente, siti web di supporto)

- **software generico**: prodotto autonomamente, incontra la necessità di svariati clienti. Il produttore ha controllo sulle specifiche
- **software su richiesta**:sviluppato da un'organizzazione per un specifico cliente. Il produttore deve attenersi alle specifiche del cliente

### Sviluppo professionale di software di qualità

Caratteristiche qualitative di un software professionale_

- **accettabilità**: deve essere accettabile per il cliente
- **Fidatezza e Protezione**: non deve causare danni fisici e economici iun caso di malfunzionamento. Non vulnerabile ad attacchi da parte di utenti malintenzionati
- **Efficienza**: le risorse non devono essere sprecate
- **Manutenibilità**: deve poter evolvere per soddisfare nuove richieste dei clienti

### Definizione di Ingegneria del Software

Adottare approcci ingegneristici alla produzione di software, disciplina ingegneristica.

### Processi di Sviluppo del Software

**Processo software**: attività che portano a creazione/evoluzione di un software

- **Acquisizione, analisi e specifica dei requisiti**: definizione delle funzionalità e dei vincoli operativi del software
- **Progettazione e sviluppo**: progettazione e programmazione
- **Verifica e validazione**: verifica che il software soddisfi i requisiti
- **Evoluzione**: modifiche al software per correggere errori o migliorare funzionalità

Si distingue in metodi e strumnenti:

- **metodi**: approcci strutturati per sviluppare software di qualità, con costi contenuti e nei tempi previsti
- **strumenti**: sistemi software per aiutare le attività dei processi software (analisi, modellazione, debugging, testing)

Alcune sfide per processi software:

- **diversità**: metodi per produrre software su dispositivi eterogenei
- **consegna**: consentirla in tempi rapidi
- **fiducia**: tecniche che rendano il software affidabile e sicuro agli occhi del cliente
- **scala**: software distribuito su sistemi diversi 

I **principi fondamentali** sono:

- metodi specifichi dipendono dal contesto del progetto
- non esistono metodi universalmente applicabili
- i concetti fondamentali sono indipendenti dal linguaggio di programmazione

(... ultime slide)

## 2. PROCESSI SOFTWARE: ATTIVITÀ FONDAMENTALI

### Code and Fix

Consiste nel

- scrivere codice
- aggiustare errori, migliorarlo, aggiungere funzionalità

Approccio **molto limitato** in contesti di grandi dimensioni

### Definizione di Processo Software

Il processo software è quell'insieme strutturato di attività che portano alla creazione di un software. Un processo di qualità migliora qualità del software, tempi di sviluppo e costi.

### Attività Fondamentali

- **Acquisizione, analisi e specifica dei requisiti**: definizione delle funzionalità e dei vincoli operativi del software
- **Progettazione e sviluppo**: progettazione e programmazione
- **Verifica e validazione**: verifica che il software soddisfi i requisiti
- **Evoluzione**: modifiche al software per correggere errori o migliorare funzionalità

**Studio di fattibilità**: stabilisce se sviluppo debba essere avviato, determinando

- se esiste un mercato
- se il progetto è tecnicamente ed economicamente fattibile

Fornisce un report con definizione problema, valutazione costi/benefici, risorse necessarie, soluzioni alternative, tempi di consegna e modalità sviluppo

### 1 - Acquisizione, Analisi e Specifica dei Requisiti

Serve a determinare **cosa** farà il software.
Specifica le **funzionalità e le qualità** che deve possedere, **senza vincolare progettazione** e implementazione.
Definisce **funzioni e vincoli** con il cliente
Un errore in questa fase è molto costoso

**Ingegneria dei Requisiti**: metodi per raccogliere, analizzare, documentare e gestire i requisiti del software

#### Deduzione e analisi dei requisiti

DEDUZIONE: spirito critico e coinvolge osservazione di sistemi esistenti, discussioni con possibili utenti

ANALISI: sviluppo di uno o più modelli e prototipi

#### Specifica dei requisiti

traduce le informazioni raccolte in un insieme di requisiti

- _requisiti di sistema_: funzionalità e caratteristiche che devono essere fornite
- _requisiti utente_: proposizioni astratte dei requisiti del sistema per i clienti

#### Convalida dei requisiti

Fase in cui si controlla che i requisiti siano realistici, coerenti e completi. Possibile rilevazione di errori nel documento dei requisiti

#### Documento dei requisiti

Documento più o meno formale contenente l'insieme dei requisiti. In questa fase viene predisposto un piano di test

**[immagine diagramma requisiti]**

### 2 - Progettazione e Sviluppo

Parte che si occupa della conversione dei requisiti in un sistema eseguibile. In due fasi:

- **progettazione**: progettare struttura software che realizzi le specifiche
- **sviluppo**: implementazione dei componenti definiti nel progetto

La distinzione o meno dipende dal tipo di processo software adottato.

#### Progettazione

Le fasi di progettazione sono intrecciate e interdipendenti, continue revisioni anche delle fasi precedenti

**input di progettazione**: requisiti, descrizione dei dati, informazioni sulla piattaforma software in cui sarà eseguito (sistema operativo, database, altre applicazioni)

##### Attività di progettazione

- **progettazione dell'architettura**: progetto alto livello, identificazione struttura complessiva e componenti principali
- **progettazione dell'interfaccia**: definizione interfaccia tra componenti, non ambigua
- **progettazione e scelta dei componenti**: scelta dei componenti già disponibili, progettazione nuovi componenti. Progetto dettagliato ma generalmente senza dettagli di implementazione
- **progettazione del database**: definizione struttura del database, tabelle, relazioni e vincoli

L'output della progettazione è un progetto software che descrive struttura, modelli e strutture dati usati dal sistema e interfacce usate.

[immagine diagramma progettazione - slide 22]

#### Sviluppo

Lo sviluppo è strettamente dipendente dal singolo programmatore, ma è possibile che ci siano standard aziendali e convenzioni condivise.

### 3 - Verifica e Validazione

**Verifica**: mostrare conformità del sistema alle specifiche

**Validazione**: mostrare che il sistema soddisfa le aspettative del cliente

Generalmente ottenute tramite **testing** medianti dati di prova ricavati dalle specifiche.

#### Testing

Suddivisibile in tre fasi:

- **test dei componenti**: test di singoli componenti in isolamento (unità o gruppi di funzioni e classi)
- **test del sistema**: testare il sistema completo, oppure in più stadi con diverse componenti integrate, verificando conformità requisiti funzionali e non funzionali
- **test del cliente**: sistema testato dal cliente con dati reali, verificando che soddisfi le sue aspettative

La fase di testing è **iterativa**, se emergono difetti può essere necessario ripercorrere le altre fasi di testing

### 4 - Evoluzione

Il software viene costantemenete riusato, evoluto e mantenuto, modificandolo ripetutamente durtante il suo ciclo di vita. Questo avviene per

- correggere errori
- migliorare funzionalità
- adattarlo a nuovi ambienti operativi

## 3. MODELLI DI PROCESSI SOFTWARE

**CSV - modello del ciclo di vita del software**: caratterizzazione descrittiva o prescrittiva di come dovrebbe essere sviluppato un software

**modello di processo software**: descrizione semplificata e astratta di un processo software

Ogni processo può essere descritto tramite

- **descrizione architetturale**: descrive la sequenza di attività senza fornire dettagli
- **data-flow**: evidenzia trasformazioni dei dati dalle attività del processo
- **role/action**: ruole e responsabilità di chi svolge le attività del processo

La descrizione del processo software include:

- **attività**: cosa deve essere fatto e in che ordine
- **prodotti**: risultati di ogni attività
- **ruoli**: chi deve svolgere le attività
- **pre e post condizioni**: condizioni che devono essere soddisfatte prima e dopo ogni attività, criteri di transizione

Ci sono diversi tipologie di modelli, tra cui:

- **plan-driven**: pianificazione dettagliata di tutte le attività prima di iniziare lo sviluppo
- **agile**: sviluppo iterativo e incrementale, con frequenti revisioni e