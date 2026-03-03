# 🛍️ Ecommerce Sales Clustering
An end-to-end data science project that performs deep preprocessing, transformation, and K-Means clustering on e-commerce sales data to identify consumer patterns and operational insights.

This project automates the transition from raw, messy CSV data to structured machine learning clusters, handling challenges like mixed data types, outliers, and feature scaling.

## 📌 Project Overview
E-commerce datasets often contain missing values, inconsistent types, and extreme outliers that skew analysis. 

This project uses:
- **Pandas & NumPy** – for data profiling and deep cleaning
- **Scipy (Z-Score)** – for statistical outlier detection
- **Scikit-Learn** – for Min-Max scaling and K-Means clustering
- **Matplotlib & Seaborn** – for visual EDA and cluster interpretation

The pipeline processes thousands of transactions to segment sales into distinct, actionable groups.

## 🚀 Features
- **Data Profiling:** Detailed attribute analysis (Missing %, Unique Values, Dtypes).
- **Deep Cleaning:** Handles mixed-type columns, removes redundant tracking IDs, and performs Mean/Median/Mode imputation.
- **Outlier Treatment:** Dual-method detection using **Z-Score (±3)** and **IQR** with capping.
- **Feature Engineering:** Implements Min-Max scaling for `Amount` and Z-Score normalization for `Quantity`.
- **Categorical Encoding:** One-Hot Encoding for `Category`, `Fulfilment`, and `Sales Channel`.
- **Clustering:** Automated K-Means implementation with **Elbow Method** optimization.

## 📂 Project Structure
```text
Ecommerce-Sales-Clustering/
├── cluster.ipynb              # Main Jupyter Notebook (Code & Analysis)
├── Sales Report.csv      # Raw Dataset (Not tracked in Git)
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
└── .gitignore            # Excludes data and cache files

```

## ⚙️ Installation

1️⃣ **Clone the repository**

```bash
git clone [https://github.com/owaissaee/Ecommerce-Sales-Clustering.git](https://github.com/owaissaee/Ecommerce-Sales-Clustering.git)
cd Ecommerce-Sales-Clustering

```

2️⃣ **Create virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
# OR
venv\Scripts\activate     # Windows

```

3️⃣ **Install dependencies**

```bash
pip install -r requirements.txt

```

## ▶️ Usage

1. Ensure your `Sales Report.csv` is in the root folder.
2. Open the Jupyter Notebook:

```bash
jupyter notebook cluster.ipynb

```

3. Run all cells to execute the pipeline from data cleaning to clustering.

## 📊 Pipeline Output

The project generates several key visualizations and data structures:
| Stage | Description |
| :--- | :--- |
| **Profiling Table** | Summary of missing data and unique counts per column |
| **Outlier Plots** | Boxplots and Scatter plots before/after capping |
| **Elbow Plot** | Visual aid to determine the optimal number of clusters |
| **Cluster Map** | Scatter plot of segmented sales data based on Amount/Quantity |

## ⚠️ Notes

* The `Sales Report.csv` is ignored by Git due to its size; ensure you have the file locally.
* Large `DtypeWarnings` are handled automatically within the notebook.
* The K-Means `random_state` is set to 42 for reproducible results.

## 🧠 Future Improvements

* Integrate **PCA (Principal Component Analysis)** for better visualization of high-dimensional clusters.
* Add **Silhouette Score** for more precise cluster validation.
* Create an interactive dashboard using **Streamlit**.
* Automate the pipeline using **MLflow** for experiment tracking.

## 👤 Author

**Owais Saeed**
