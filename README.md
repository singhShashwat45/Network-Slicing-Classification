# 📡 Network Slicing Classification

This project demonstrates **Network Slicing Classification** using machine learning techniques on a dataset containing LTE/5G features.  
The goal is to classify data into three types of network slices:  

- **eMBB (Enhanced Mobile Broadband)**  
- **URLLC (Ultra-Reliable Low-Latency Communication)**  
- **mMTC (Massive Machine Type Communication)**  

---

## 📂 Dataset

The dataset consists of LTE/5G features such as:

- LTE/5G Category  
- Time  
- Packet Loss Rate  
- Packet Delay  
- IoT / Healthcare / Smart City / Smartphone indicators  
- Target label: **Slice Type (1 = eMBB, 2 = URLLC, 3 = mMTC)**  

**Files used:**
- `train_dataset.csv` → Training data  
- `test_dataset.csv` → Testing data  

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Loaded dataset from Google Drive  
- Applied memory optimization (`reduce_mem_usage`) to reduce memory by ~86%  
- Selected key features for training:  

### 2. Train-Test Split
- **70% training**, **30% testing**  
- `train_test_split` with random state 12  

### 3. Model Training
- Used **K-Nearest Neighbors (KNN)** Classifier  
- Hyperparameter tuning: Tested `n_neighbors` from 2 → 8  
- Evaluated metrics:  
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Execution time  

### 4. Results
- Best performance at **n_neighbors = 3**  
- **Test Accuracy: ~93%**  
- Confusion Matrix plotted for classification distribution  

### 5. Predictions
- Random samples from `test_dataset.csv` were predicted  
- Mapped predicted slice type labels to names:  
- `1 → eMBB`  
- `2 → URLLC`  
- `3 → mMTC`  
- Displayed results in both tabular printout and a matplotlib **custom table visualization**  

---

## 📊 Visualization

- Performance metrics plotted across neighbors (Accuracy, Precision, Recall, F1)  
- Confusion Matrix for best model (`n_neighbors=3`)  
- Randomly selected test rows with **Predicted Slicing Type** shown in a structured table  

---

## 🚀 How to Run

1. Clone the repository:
 ```bash
 git clone https://github.com/singhShashwat45/Network-Slicing-Classification.git
 cd Network-Slicing-Classification
