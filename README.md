# Health-dataset-collection


## **DATASET1: Set di dati di balistocardiografia basata sul letto**
ARTICOLO :https://www.mdpi.com/1424-8220/21/1/156 
DATASET:https://ieee-dataport.org/open-access/bed-based-ballistocardiography-dataset

La Kansas State University ha raccolto un dataset cardiaco formato da 40 partecipanti( 4 dei quali erano stati o erano attualmente diagnosticati con una patologia cardiaca), di cui 17 maschi, secondo il protocollo IRB n. 9386 della Kansas State University, include segnali di ballistocardiogramma (BCG), elettrocardiogramma (ECG) sincronizzati nel tempo, fotopletismogramma (PPG) e onde di pressione sanguigna. 

I Dati acquisiti nel dataset sono tutti allineati nel tempo, abbiamo:

-BCG ( ottenuto tramite un sistema ballistocardiografico personalizzato, basato sul letto, 
   composto da quattro pellicole elettromeccaniche, cioè sensori "EMFI" e quattro celle di 
   carico);
   
-** segnali cardiopolmonari**, quali ECG e PPG, frequenza cardiaca stimata (FC), segnali di impedenza respiratoria e **segnali cardiovascolari**, quali pressione sanguigna, segnale su base battito per battito (sono stati acquisiti con un monitor paziente GE Datex CardioCap 5 e un Finapres Medical Systems Finometer PRO);

-pressione dell'arteria brachiale (reBAP), volume sistolico (SV), pendenza massima della forma d'onda della pressione del dito corrente (dP_dt) e l'intervallo tra i battiti (IBI) (sono stati ricostruiti utilizzando il metodo ModelFlow dopo aver corretto per età, sesso, peso e altezza.)

![image](https://github.com/user-attachments/assets/61182004-de30-4776-8f5a-ccf9769eb1d6)


L'età dei partecipanti variava da 18 a 65 anni e i loro indici di massa corporea (BMI) variavano da 18 a 48 kg/m 2 . Quattro dei partecipanti hanno indicato di avere avuto una qualche forma di condizione cardiovascolare passata o attuale: ipertensione, tachicardia sopraventricolare (trattata tramite ablazione cardiaca), fibrillazione atriale e malattia coronarica.

In totale, sono state raccolte oltre 4,5 ore di dati.

I dati dei partecipanti sono stati raccolti in una tabella MATLAB nel file "Bed_System_Database",i campi includono: ID partecipante, Genere, Età, Altezza_cm, Peso_kg, RawData, Condizione cardiaca ( vine echiesto se il partecipante ha mai ricevuto una diagnosi di anomalie cardiache o malattie come fibrillazione atriale, aritmia o altre condizioni cardiache) e Commenti.

![image](https://github.com/user-attachments/assets/fbe475b2-c45c-46b1-a6b2-47f82656df50)

L'acquisizione di tutti i dati è avvenuta tramite PC attraverso il sistema din acquisizione labVIEW.

Per ciascun partecipante, la struttura dati del campo RawData è stata configurata con venti campi per ciascun segnale acquisito :PPG, Resp, HR, ECG, Film0, Film1, Film2, Film3, LC_COP0, LC_BCG0, LC_COP1, LC_BCG1, LC_COP2, LC_BCG2, LC_COP3, LC_BCG3, reBAP, IBI, SV e dp_dt

![image](https://github.com/user-attachments/assets/4dc8065d-1c12-4b41-97c0-3b5b8391d797)


I segnali sono stati filtrati e sincronizzati per isolare i componenti cardiaci e ridurre il rumore: BCG (1-10 Hz), PPG e reBAP (passa-basso 10 Hz), ECG (1-40 Hz). I ritardi del Finometer sono stati corretti per una precisa analisi successiva, e i dati elaborati sono archiviati nella tabella "Preprocessed_Database".

![image](https://github.com/user-attachments/assets/c9b4bb30-9ac4-42a8-92c8-cb2dcd040a77)

**ARTICOLO ** 

L'articolo descrive un sistema di acquisizione basato sul letto per monitorare parametri cardiovascolari come pressione arteriosa e frequenza cardiaca, con una preelaborazione dei segnali BCG, ECG e PPG effettuata in MATLAB per ridurre il rumore e compensare i ritardi dei dispositivi di misura. L’analisi, condotta su circa 100 cicli cardiaci, include l’estrazione di parametri battito per battito come il picco J e metriche quali il volume sistolico e il massimo derivato della pressione. I modelli multivariati hanno evidenziato correlazioni più elevate nella stima della pressione sistolica e del volume sistolico, mostrando però variazioni tra i partecipanti. Il sistema è proposto come strumento per la ricerca cardiovascolare, permettendo lo sviluppo di algoritmi senza ulteriori investimenti in hardware.


## **DATASET2: Un set di dati di segni vitali del balistocardiogramma con segnali di sensori di riferimento in ambienti di sonno naturali**


Figshare DATASET: https://figshare.com/articles/dataset/A_ballistocardiogram_dataset_with_reference_sensor_signals_in_long-term_natural_sleep_environments/26013157?file=46976602 

ARTICOLO CORRELATO:https://www.nature.com/articles/s41597-024-03950-5#Tab1 

La raccolta dati è stata condotta nei locali della Beijing Sport University da novembre 2023 a gennaio 2024.
Questo dataset è stato progettato per supportare la ricerca avanzata nel monitoraggio discreto del sonno e nella valutazione della sua qualità. Questo dataset include dati ballistocardiografici (BCG) continui di 32 partecipanti sani ((16 maschi e 16 femmine) della Beijing Sport University, di età compresa tra 19 e 27 anni (media = 23,03, deviazione standard = 2,02).

I dati sono stati registrati utilizzando un sensore a pellicola piezoelettrica del modello H70030, prodotto da Beegor Ltd, posizionato sotto il materasso nella posizione del torace del partecipante, più due fasce a stretto contatto con la pelle che fungevano da sensori di riferimento per misurare la frequenza cardiaca e respiratoria. 

Sono state raccolti un totale di 212 notti di dati (6/7 notti consecutive per partecipante), per una media di circa 55 ore di registrazioni per ciascun partecipante.

Tutti i partecipanti hanno riferito di avere orari di sonno regolari, senza abitudini del sonno malsane come stare alzati fino a tardi o fare nottate intere e non soffrivano di gravi disturbi del sonno come l'insonnia cronica.

Un aspetto distintivo di questo dataset è che gli esperimenti sono stati condotti in scenari di vita quotidiana, piuttosto che in ambienti di laboratorio, permettendo quindi un monitoraggio prolungato e in condizioni di sonno naturale.

Inoltre, per validare l'accuratezza dei componenti cardiaci e respiratori estratti dai segnali BCG, sono stati registrati dati di riferimento della frequenza cardiaca e respiratoria tramite sensori specifici. 

![image](https://github.com/user-attachments/assets/eae4d273-91ff-42d1-8ef2-cd5cfa675499)

 Tutti i dati sono forniti in formato .csv 

 1) La cartella "data" contiene 32 sottocartelle, ciascuna corrispondente a un soggetto. Tutti i dati nelle sottocartelle "data" vengono salvati nel formato subjectID_date_datatype.csv, **subjectID** rappresenta 
    l'identificativo univoco del soggetto, **data**, formattata come "aaaaMMgg", specifica la data della raccolta dei dati, uniformemente assunta come la data in cui termina il periodo di sonno (ovvero l'ultimo 
    risveglio) **datatype** reppresenta il tipo di dati tra cui BCG o RR o resp. Al suo interno troviamo:
    
    - La cartella "BCG" che  contiene i dati BCG per il soggetto campionati a 140 Hz, ottenuti digitalizzando il segnale BCG grezzo utilizzando un convertitore analogico-digitale (ADC) a 16 bit integrato nel 
       sensore a pellicola piezoelettrica. Questi segnali BCG possono essere utilizzati per calcolare parametri fisiologici quali frequenza cardiaca e frequenza respiratoria;
     
    - La cartella "Reference" include i dati dai sensori di riferimento e comprende due sottocartelle: 
       
        + "RR" per i dati Inter-Beat Interval, registrano gli intervalli tra i battiti cardiaci raccolti da un sensore di frequenza cardiaca. Questo file non include una frequenza di campionamento. 
          La colonna A contiene il timestamp per ogni battito cardiaco, etichettato "Timestamp", con dati formattati come "yyyy/MM/dd H:mm:ss".
          La colonna B contiene la frequenza cardiaca calcolata per ogni battito  cardiaco, con l'intestazione di colonna "Heart Rate".
          La colonna C contiene la durata di ogni intervallo RR, etichettata "RR Interval in seconds", con unità in secondi (s).
      
        + "resp" contengono dati di forma d'onda respiratoria da un sensore capacitivo, registrati a una frequenza di campionamento di 20 Hz, con unità in picofarad (pF). I dati di forma d'onda respiratoria                  riflettono i cambiamenti di espansione e contrazione del torace durante la respirazione.


  2) La cartella “additional_info” include due sottofile che descrivono le informazioni personali di ciascun soggetto e i dettagli della raccolta dati, ovvero:

     - “subject_info.csv”, include le informazioni personali di base di ogni soggetto, con ogni riga corrispondente a un soggetto. Ciò include il loro ID (colonna A), sesso (colonna B), peso (colonna C), altezza          (colonna D) ed età (colonna E). L'età dei soggetti è determinata convertendo le loro date di nascita nella loro età effettiva al momento della registrazione dei dati.
   
     - “data_info.xlsx”,  fornisce dettagli sui record di dati di ciascun soggetto durante l'esperimento. Ogni colonna rappresenta quanto segue: ID soggetto (colonna A), data (colonna B) e presenza di dati BCG 
       (colonna C), RR (colonna D) e resp (colonna E) per la data corrispondente. I dati sono rappresentati in forma binaria, con "1" che indica la presenza di dati in una data specifica e "0" che indica nessun 
       dato registrato o perdita di dati in quella data. Le principali cause di perdita di dati includono malfunzionamento dell'apparecchiatura e funzionamento improprio.

  3) La cartella "code" contiene il codice con estensione .m  (scritto sul software MATLAB R2021b) utilizzato per il caricamento dei dati, l'imputazione dei dati mancanti, la sostituzione degli outlier e il rilevamento dei movimenti del corpo. Può essere utilizzato 
    specificando il percorso del file di configurazione, l'ID del soggetto, la data e il tipo di dati da visualizzare.


## **DATASET3: Apnea-ECG**

LINK: https://www.kaggle.com/datasets/paulopinheiro/the-apnea-ecg-database-v100/data
     https://physionet.org/content/apnea-ecg/1.0.0/
     
Pubblicato: 10 febbraio 2000. Versione: 1.0.0

I dati in questo elenco sono stati forniti dal Dr. Thomas Penzel della Phillips-University, Marburg, Germania. 

I dati comprendono 70 registrazioni, suddivise in un set di apprendimento (35 record) e un set di test (35 record), con durate tra 7 e 10 ore.

Ogni registrazione include segnali ECG continui, annotazioni di apnea basate sulla respirazione, e annotazioni QRS automatizzate. Otto registrazioni dispongono anche di segnali respiratori toracici e addominali, flusso d'aria oronasale e SpO2. I file associati includono dati ECG (.dat), intestazioni (.hea), annotazioni di apnea (.apn) per il set di apprendimento, e annotazioni QRS automatiche (.qrs).


Goldberger, A., Amaral, L., Glass, L., Hausdorff, J., Ivanov, P. C., Mark, R., ... & Stanley, H. E. (2000). PhysioBank, PhysioToolkit e PhysioNet: componenti di una nuova risorsa di ricerca per segnali fisiologici complessi. Circolazione [Online]. 101 (23), pp. e215-e220.

## **DATASET4: Rilevamento della frequenza cardiaca durante l'apnea notturna**

LINK: https://github.com/mo-gaafar/apnea-bcg-heartrate-detection

Il dataset raccoglie segnali ECG e BCG per monitorare la frequenza cardiaca, producendo grafici comparativi che evidenziano le differenze tra i due segnali e valutano l'accuratezza del segnale BCG nel rilevare la frequenza cardiaca, utile anche per l'identificazione dell'apnea notturna.
![image](https://github.com/user-attachments/assets/cb1731d4-47f0-4497-b231-5ea4d831efb4)


## **DATASET5:Ballistocardiografia con disturbi respiratori**

LINK: https://data.mendeley.com/datasets/9fmfn6kfn7/1

ARTICOLI CORRELATI: https://www.sciencedirect.com/science/article/abs/pii/S0020025520304849#preview-section-references , https://www.sciencedirect.com/science/article/abs/pii/S0950705119304009 

Pubblicato: 20 Marzo 2020

Versione 1
Questo lavoro è stato supportato dal Progetto di Ricerca Specifica della Facoltà di Informatica e Gestione dell'Università di Hradec Králové e dal progetto PERSONMED—Centro per lo Sviluppo della Medicina Personalizzata nelle Malattie legate all'Età.


In questo studio, è stato sviluppato un sistema di rilevamento assistito da computer per i disturbi respiratori. Il sistema ha utilizzato quattro sensori ballistocardiografici incorporati negli angoli di un letto di misurazione. La soluzione proposta si basa su nuove curvature ottimali di Cartan e su una normalizzazione dei dati basata su una stima esperta, che viene mantenuta costante per tutti i soggetti. Dopo l'elaborazione dei dati, è stato progettato un modello CNN profondo a 9 strati per riconoscere i problemi respiratori. L'accuratezza, la sensibilità e la specificità ottenute sono rispettivamente del 96,21%, 88,31% e 98,69%.

 Il dataset del sensore BCG è stato ottenuto da 20 soggetti testati, di cui 11 uomini di età compresa tra 23 e 33 anni e 9 donne di età compresa tra 24 e 65 anni, sdraiati su un letto con sensori posizionati ai piedi del letto, hanno effettuato sessioni di trattenuta del respiro di circa 30 secondi.
 I dettagli sui 20 soggetti e le loro preferenze sono riportati in figura:

![image](https://github.com/user-attachments/assets/7a8e2746-371d-41d6-ac1c-94eb06473e9f)

 Le misurazioni sono state programmate in due modalità (V1 e V2) che sono descritte in figura :
 
 ![image](https://github.com/user-attachments/assets/2e433bd9-7baf-48b0-9afc-ed08a9525b58)

Le misurazioni sono state eseguite con una pedana di forza composta da quattro tensometri, in grado di rilevare 12 segnali di forza nelle tre direzioni con una precisione di 0,1 N. ECG e forza sono stati registrati simultaneamente con un convertitore AD a 24 bit a 1 kHz, producendo 13 serie temporali. 

L'annotazione dei dati è effettuata manualmente sulla base delle osservazioni di misurazione.
Ogni misurazione è rappresentata da una matrice, in cui le righe corrispondono ai singoli campioni registrati ogni 1 ms e le 14 colonne contengono un valore di carico dei dati (0 per corretto, 1 per non corretto), dodici segnali di forza e il valore ECG.


Nel contesto di questo studio, le curvature di Cartan sono utilizzate per analizzare i segnali di ballistocardiografia (BCG) al fine di rilevare disturbi respiratori. Le curvature, derivate dalla geometria differenziale, amplificano le parti significative dei segnali BCG legate ai disturbi respiratori e filtrano i movimenti non rilevanti, come i movimenti collettivi del corpo. Poiché sono invariate rispetto ai movimenti del corpo, le curvature di Cartan permettono di eliminare l'influenza di cambiamenti di posizione, migliorando la precisione nella rilevazione dei disturbi respiratori senza l'uso simultaneo di segnali ECG.

Nel lavoro descritto, segnali BCG ed ECG vengono analizzati insieme da una rete neurale CNN per classificare il respiro come normale o disturbato. Tuttavia, l'obiettivo futuro è eliminare la necessità di ECG, utilizzando solo i dati BCG e le curvature di Cartan per calcolare un "trigger" che rilevi autonomamente i disturbi respiratori, consentendo così l'automazione del sistema e l'esplorazione di altri aspetti dell'emodinamica umana.
