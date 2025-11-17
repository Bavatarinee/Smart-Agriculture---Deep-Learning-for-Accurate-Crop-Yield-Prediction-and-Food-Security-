Drive Link : https://drive.google.com/drive/folders/1Ts1jLozW8ib9R5GuSHZ7WxVWLRpHJdMU?usp=sharing

# 🌾 FarmVision  
### Deep Learning–Based Crop Production Prediction System  
Smart Agriculture • Food Security • Yield Forecasting  

FarmVision is an AI-powered web application that predicts **crop production** using **real-world agricultural datasets** and an in-browser **Deep Learning model (TensorFlow.js)**.  
The system provides a user-friendly dashboard to visualize model accuracy, training metrics, prediction charts, and history — all in real time, with no backend required.

---

## 📌 **1. Project Overview**

Agricultural production in India depends on several complex factors such as crop type, season, area, state, and rainfall patterns. Manually estimating yield is challenging, especially for large-scale farming.

**FarmVision automates this process using a deep learning regression model** that learns from historical crop production data and predicts future production values.

The model runs **entirely inside the browser using TensorFlow.js**, providing real-time predictions without servers or Python environments.

---

## 🚀 **2. Key Features**

### 🔹 **✔ Real-time Deep Learning model (TF.js)**  
Runs a Multi-layer Neural Network directly in the browser.

### 🔹 **✔ CSV Upload**  
Users can upload any `Crop Production in India` dataset from Kaggle.

### 🔹 **✔ Automatic Preprocessing**  
- Category encoding (Crop, State, Season)  
- Normalization  
- Log transformation for stable learning  

### 🔹 **✔ Dashboard Metrics**
- R² Score  
- RMSE (Corrected using reverse log-scaling)  
- MAE  
- Training Loss Progress  

### 🔹 **✔ Prediction vs Actual Graph**
Canvas-based, no external chart libraries.

### 🔹 **✔ Quick Predict UI**
User inputs crop details → model predicts production instantly.

### 🔹 **✔ Local Storage History**
Stores latest predictions for user reference.

---

## 🧠 **3. Deep Learning Model**

FarmVision uses a **Fully Connected Neural Network (Dense Model)** designed for regression.

### **Model Architecture**
```

Input Layer → Dense(128, relu)
→ Dense(64, relu)
→ Dense(32, relu)
Output Layer → Dense(1)

```
 **Why Deep Learning?**
- Handles **non-linear relationships** better than classical ML  
- Learns pattern interactions: crop × state × season × area  
- Performs well even on noisy agricultural datasets  
- No need for manual feature engineering  

### **Log Transformation**
Crop production values vary drastically (from 100 to 50,000,000+).  
To stabilize training:

```

y = log(1 + Production)

```

Reverse transform for final output:

```

Production = exp(y_pred) - 1

````

This significantly improves accuracy.

---

## 📊 **4. Dataset Used**
**Crop Production in India (Kaggle)**  
Fields required:

- `State_Name`
- `Crop_Year`
- `Season`
- `Crop`
- `Area`
- `Production`

The system automatically extracts, cleans, and encodes these columns.

---

## 🖥 **5. Installation & Running the App**

### **Prerequisites**
- Node.js (v18+ recommended)
- npm enabled

---

### ▶️ **Step 1: Clone the repository**
```bash
git clone https://github.com/<your-username>/FarmVision.git
cd FarmVision
````

### ▶️ **Step 2: Install dependencies**

```bash
npm install
```

*(If PowerShell blocks npm, run:
`Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`)*

### ▶️ **Step 3: Start development server**

```bash
npm run dev
```

### ▶️ **Step 4: Open in browser**

```
http://localhost:5173/
```

---

## 📁 **6. Project Folder Structure**

```
FarmVision/
│
├── public/
│     └── crop_production_small.csv
│
├── src/
│     ├── App.jsx
│     ├── FarmVisionDashboard.jsx
│     ├── Dashboard.css
│     ├── components/
│     └── assets/
│
├── package.json
├── vite.config.js
└── README.md
```

---

## 📈 **7. Model Metrics (Example Output)**

| Metric   | Value   |
| -------- | ------- |
| **R²**   | 0.87    |
| **RMSE** | 544,493 |
| **MAE**  | 230,112 |

*(Values depend on data quality and number of crops selected.)*

---

## 🎨 **8. Dashboard UI Preview**

Add your screenshots here:

<img width="1884" height="824" alt="image" src="https://github.com/user-attachments/assets/ad884a8c-6fb3-4189-9d76-7cd9b9b0ea9f" />
<img width="854" height="526" alt="image" src="https://github.com/user-attachments/assets/1a63c939-0ef7-4126-b419-cfd2a0207b77" />

---

## 🔮 **9. Future Enhancements**

* Add rainfall, temperature, humidity data (NASA POWER API)
* Export prediction report as PDF
* Multiple model choices (LSTM, Random Forest, XGBoost)
* Support for multi-crop forecasting
* Map-based visualization


---

## 🙌 **Contributors**

* Dhanush C (24MDT1031)
* Bavatarinee T M (24MDT1081)
* Sree Sakthi N (24MDT1124)
  Department of Mathematics, VIT Chennai

---

# ⭐ If you like the project, don't forget to ⭐ the repository!

```


