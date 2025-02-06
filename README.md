# Data-Driven-Customer-Segmentation-using-RFM-and-Machine-Learning

## 📌 Project Overview
This project focuses on segmenting customers based on their purchasing behavior using **RFM analysis** and **K-Means clustering**. The goal is to identify distinct customer groups to improve targeted marketing strategies and enhance customer retention.

## 📂 Dataset Description  

### 1️⃣ Customer Purchase Behavior (`purchase_behaviour`)  
Contains customer demographic details based on loyalty card usage.  

#### 🔹 Columns:  
- **`LYLTY_CARD_NBR`** → Unique customer ID  
- **`LIFESTAGE`** → Customer life stage (e.g., Young Singles/Couples, Older Families)  
- **`PREMIUM_CUSTOMER`** → Customer category (Budget, Mainstream, Premium)  

### 2️⃣ Transaction Data (`transaction_data`)  
Records all customer transactions, including products purchased and spending details.  

#### 🔹 Columns:  
- **`DATE`** → Purchase date (integer format)  
- **`STORE_NBR`** → Store number where the transaction occurred  
- **`LYLTY_CARD_NBR`** → Customer ID (matches `purchase_behaviour`)  
- **`TXN_ID`** → Unique transaction ID  
- **`PROD_NBR`** → Product ID  
- **`PROD_NAME`** → Product name (e.g., "Natural Chip Company Sea Salt 175g")  
- **`PROD_QTY`** → Quantity of product purchased  
- **`TOT_SALES`** → Total transaction amount (in $)  

## 🚀 Methodology
1. **Data Preprocessing**  
   - Clean missing values  
   - Convert categorical variables  
   - Scale numerical features using `StandardScaler`  

2. **RFM Analysis**  
   - Compute **Recency, Frequency, and Monetary (RFM)** scores  
   - Standardize RFM values  

3. **K-Means Clustering**  
   - Determine optimal number of clusters using the **Elbow Method**  
   - Apply **K-Means clustering** to segment customers  

4. **Cluster Visualization & Analysis**  
   - 2D scatter plots for transaction-based clustering  
   - 3D visualization of RFM-based clusters  
   - Spending behavior analysis per segment  

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
## 📌 Workflow  

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
