# Data Driven Customer Segmentation using RFM and Machine Learning

## 📌 Project Overview
This project focuses on segmenting customers based on their purchasing behavior using **RFM analysis** and **K-Means clustering**. The goal is to identify distinct customer groups to improve targeted marketing strategies and enhance customer retention.

## 📂 Dataset Description  

### 1️⃣ Customer Purchase Behavior 
**`purchase_behaviour.csv`** - Contains customer demographic details based on loyalty card usage.  

### 2️⃣ Transaction Data
- **`transaction_data.csv`** – Records all customer transactions, including products purchased and spending details.  

## 🛠️ Methodology  

### 1️⃣ Data Preprocessing  
- Converted date format from integer to datetime.  
- Removed anomalies (negative/zero values in `TOT_SALES` & `PROD_QTY`).  
- Dropped duplicates and standardized product names.  
- Merged transaction data with customer demographics.  

### 2️⃣ Exploratory Data Analysis (EDA)  
- Identified **top-selling** and **most profitable** products.  
- Analyzed customer spending patterns by **lifestyle & premium category**.  
- Visualized transaction trends using bar charts and heatmaps.  

### 3️⃣ RFM Segmentation  
- **Recency**: Days since last purchase.  
- **Frequency**: Total transactions per customer.  
- **Monetary**: Total spending per customer.  
- Identified **top loyal customers** based on RFM scores.  

### 4️⃣ Customer Clustering (K-Means)  
- Standardized RFM data for clustering.  
- Determined optimal clusters using **Elbow Method & Silhouette Score**.  
- Segmented customers into **3 behavior-based groups**.  
- Analyzed **lifestage & premium category** distribution in clusters.  

## 📊 Visualizations
- **Scatter Plot:** Customer segments based on total transactions & spending  
- **3D Plot:** RFM-based customer segmentation  
- **Bar Charts:** Spending analysis per cluster  
- **Heatmap:** Spending patterns by **LIFESTAGE** & **PREMIUM_CUSTOMER**  

## 🛠️ Tech Stack
- **Programming Language:** Python 🐍  
- **Libraries Used:**
  - `pandas` - Data manipulation  
  - `numpy` - Numerical computing  
  - `matplotlib` & `seaborn` - Data visualization  
  - `scikit-learn` - Machine learning (K-Means, StandardScaler)
 
## 📌 Usage

### 1️⃣ Run the Jupyter Notebook
To execute the analysis, open the Jupyter Notebook and run all cells:  
```sh
jupyter notebook customer_segmentation.ipynb
```

### 2️⃣ Follow the Workflow:  
- **Data Preprocessing:** Load and clean customer transaction data.  
- **Feature Engineering:** Compute **RFM** (Recency, Frequency, Monetary) values.  
- **Clustering:** Apply **K-Means** clustering to segment customers.  
- **Visualization:** Generate **2D & 3D cluster plots**.  
- **Analysis:** Interpret **cluster characteristics** and **spending behavior**.  

### 3️⃣ Understanding the Outputs:  

#### 🏷️ **Customer Segments:**  
- **Cluster 0** → Young Singles/Couples (**Low Spending, Low Transactions**)  
- **Cluster 1** → Older Families (**High Spending, High Transactions**)  
- **Cluster 2** → Older Singles/Couples (**Moderate Spending, Moderate Transactions**)  

#### 📊 **Visuals:**  
- **2D Scatter Plot:** **Transaction Frequency vs. Spending**  
- **3D RFM Segmentation:** **Recency, Frequency, Monetary**  
- **Heatmap:** **Spending by LIFESTAGE & PREMIUM_CUSTOMER**  

### 4️⃣ Modify & Experiment:  
- Adjust the **number of clusters** in K-Means (`n_clusters=3`).  
- Try **different clustering techniques** (Hierarchical, DBSCAN).  
- Tune **feature scaling** and analyze the impact.  
