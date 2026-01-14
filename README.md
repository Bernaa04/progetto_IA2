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

Il dataset utilizzato è il **Telco Customer Churn**, dataset creato da IBM trovato su Kaggle al seguente link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Esecuzione del codice e librerie utilizzate

Il progetto è stato sviluppato in Python 3 e per essere eseguito richiede le seguenti librerie:

* **Pandas**: Caricamento dati (da URL) e manipolazione dataframe.
* **NumPy**: Calcolo numerico e gestione array.
* **Matplotlib & Seaborn**: Visualizzazione dati (Heatmap, Boxplot, Scatterplot).
* **Scikit-learn**:
    * *Modelli*: LogisticRegression.
    * *Preprocessing*: MinMaxScaler, train_test_split.
    * *Valutazione*: confusion_matrix, classification_report, roc_auc_score, fbeta_score, cross_val_predict.
