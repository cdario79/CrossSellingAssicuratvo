# 📊 Cross-Selling Assicurativo

**AssurePredict** è una compagnia di assicurazioni leader nel settore, specializzata nell'offrire soluzioni innovative per la gestione del rischio.  
Questo progetto mira a creare un **modello predittivo** in grado di individuare potenziali opportunità di *cross-selling* per clienti esistenti, identificando quelli che potrebbero essere interessati ad acquistare una **polizza aggiuntiva per il loro veicolo**.

---

## 🎯 Obiettivo del Progetto

Sviluppare un modello di **machine learning** che preveda se i clienti, attualmente in possesso di un’assicurazione sanitaria, potrebbero essere interessati a sottoscrivere una polizza assicurativa auto.

### ✅ Benefici per AssurePredict:
- **Aumento del tasso di conversione** nelle vendite di polizze auto.  
- **Ottimizzazione delle campagne di marketing**, indirizzando le offerte a clienti più propensi.  
- **Riduzione dei costi** legati a campagne inefficaci, grazie alla targettizzazione precisa.

---

## 📂 Dataset

Il dataset è disponibile al seguente link:  
[https://proai-datasets.s3.eu-west-3.amazonaws.com/insurance_cross_sell.csv](https://proai-datasets.s3.eu-west-3.amazonaws.com/insurance_cross_sell.csv)

### Variabili principali:
- `id`: identificativo cliente  
- `Gender`: sesso  
- `Age`: età  
- `Driving_License`: 1 se ha la patente, 0 altrimenti  
- `Region_Code`: codice della regione  
- `Previously_Insured`: 1 se ha già un veicolo assicurato  
- `Vehicle_Age`: età del veicolo  
- `Vehicle_Damage`: 1 se ha avuto danni  
- `Annual_Premium`: premio annuale pagato  
- `PolicySalesChannel`: canale di vendita  
- `Vintage`: giorni da cui è assicurato con AssurePredict  
- `Response`: **variabile target**, 1 se ha accettato il cross-sell, 0 altrimenti  

---

## 🧪 Attività Richieste

### 1. Esplorazione del Dataset
Analisi preliminare per:
- Comprendere la **distribuzione di `Response`** → classi sbilanciate?
- Studiare le **relazioni** tra:
  - `Annual_Premium`
  - `Vehicle_Age`
  - `Previously_Insured`
  - `Response`

> 💡 Un'esplorazione accurata permette di individuare pattern nascosti e criticità utili per il modello.

---

### 2. Gestione dello Sbilanciamento delle Classi

La variabile `Response` è potenzialmente sbilanciata. Possibili soluzioni:
- **Class Weights** (es. `class_weight='balanced'`)  
- **Oversampling** o **Undersampling**  
  - Vedi approfondimenti:
    - [Distribuzione delle classi](https://machinelearningmastery.com/tactics-to-combat-imbalanced-classes-in-your-machine-learning-dataset/)
    - [Oversampling e undersampling](https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/)

> ⚠️ Gestire lo sbilanciamento è cruciale per evitare modelli con molti **falsi negativi**.

---

### 3. Costruzione del Modello Predittivo

Addestrare un modello ML che predica la probabilità di risposta positiva al cross-sell.  
Algoritmi possibili:
- Logistic Regression
- Random Forest
- XGBoost  
- etc.

> ✅ Il modello aiuterà a **individuare i clienti più propensi**, migliorando ROI e targeting delle campagne.

---

## ✅ Conclusione

Questo progetto permetterà ad **AssurePredict** di sfruttare il machine learning per migliorare le strategie di **cross-selling**.  
Un approccio **data-driven** porterà a:
- Maggiori vendite
- Offerte più personalizzate
- Maggiore soddisfazione del cliente

---

## ⚠️ Punti di Attenzione

Controlla la **distribuzione delle classi**.  
Strategie consigliate:
- Penalizzazione della classe maggioritaria (`class_weight`)
- Tecniche di **oversampling** e **undersampling**

---

## 📎 Modalità di consegna

👉 Consegna finale: **Notebook Google Colab con link pubblico**
