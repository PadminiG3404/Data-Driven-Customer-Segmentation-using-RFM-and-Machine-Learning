# Data Driven Customer Segmentation using RFM and Machine Learning

## 📌 Project Overview
This project focuses on segmenting customers based on their purchasing behavior using **RFM analysis** and **K-Means clustering**. The goal is to identify the most profitable products and the characteristics of the most loyal customers. The insights derived will help the marketing team optimize targeting strategies, enhance product positioning, and maximize profitability.  

### **Key Objectives**  
- Identify the **top 3 most profitable products** based on revenue.  
- Analyze **customer loyalty** based on purchasing behavior.  
- Understand **lifestage and spending patterns** of the most loyal customers.  
- Provide data-driven recommendations for **marketing and sales strategies**.  

### **Key Findings**  
- **Top Selling Products:**  
  1. Dorito Corn Chip Supreme  
  2. Smiths Crinkle Chips (Original)  
  3. Smiths Crinkle Chips (Salt & Vinegar)  
- **Most Loyal Customers:**  
  - Older Singles/Couples & Older Families  
  - Primarily in the **Mainstream & Budget** segments  
- **Spending Patterns:**  
  - Older families in the budget segment are the highest spenders.  
  - Younger singles spend the least.  

### **Next Steps**
- Implement **personalized marketing campaigns** for high-value customer segments.  
- Introduce **bundling strategies** for best-selling products.  
- Expand **customer loyalty programs** to encourage repeat purchases.

---

## 📂 Dataset Description  

### 1️⃣ Customer Purchase Behavior 
**`purchase_behaviour.csv`**[Uploading purchase_behaviour.csv…]()
 - Contains customer demographic details based on loyalty card usage.  

### 2️⃣ Transaction Data
**`transaction_data.csv`** – Records all customer transactions, including products purchased and spending details.  

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
