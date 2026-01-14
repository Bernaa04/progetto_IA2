# Analisi Telco Customer Churn Dataset

## Descrizione del progetto

Con questo progetto il nostro obiettivo è quello di indagare le dinamiche del Customer Churn grazie all'analisi del dataset "Telco Customer Churn". 
Attraverso l'implementazione di modelli di classificazione statistica la nostra ricerca mira a sviluppare un sistema predittivo che possa individuare i clienti a rischio abbandono.
L'analisi è condotta con un approccio **"business-oriented"**, dove la priorità è la minimizzazione dei falsi negativi (clienti che abbandonano non rilevati).

Dopo aver svolto le attività di preprocessing e feature engneering (MinMaxScaler, One-hot encoding, normalizzazione, eliminazione di colonne multicollineari) abbiamo implementato la Logistic Regression ottimizzando il modello in base all'obiettivo preposto e ai risultati ottenuti:

- **Modello base**, LR standard
- **Gestione dello sbilanciamento**, utilizzo di pesi di classe (class_weight = "balanced")
- **Ottimizzazione della Threshold (F2-Score)**, affinamento della soglia decisionale basato sulla metrica F2 per migliorare Recall a discapito della Precision

Abbiamo infine analizzato modelli tematici, addestrando modelli classificatori specifici su sottinsiemi di feature (Gruppo finanziario, Gruppo tecnico, Gruppo demografico).

## Dataset

Il dataset utilizzato è il **Telco Customer Churn**, dataset creato da IBM trovato su Kaggle al seguente link: 
