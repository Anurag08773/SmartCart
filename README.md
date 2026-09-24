# 🛒 SmartCart – Customer Segmentation

SmartCart is a machine learning project that analyzes customer data and groups customers based on their **demographics, income, and spending behavior**.

The main goal of this project is to understand different types of customers using **unsupervised machine learning**. The project uses data preprocessing, feature engineering, PCA, and clustering algorithms to find meaningful customer segments.

## 📌 About the Project

Customer data can contain many different features, which can make it difficult to understand customer behavior directly. In this project, the data is cleaned and transformed into useful features such as **Age, Customer Tenure, Total Spending, and Total Children**.

After preprocessing the data, **PCA (Principal Component Analysis)** is used to reduce the number of dimensions. The reduced data is then used for customer clustering using **K-Means** and **Agglomerative Clustering**.

The clusters are finally analyzed using income and spending patterns to understand how the customers differ from each other.

## 🔍 What This Project Does

* Loads and explores the customer dataset
* Handles missing income values
* Creates new features from the existing data
* Converts customer joining dates into customer tenure
* Calculates total customer spending
* Groups education and marital status into simpler categories
* Removes unnecessary columns
* Detects and removes some outliers
* Performs correlation analysis
* Converts categorical data using One-Hot Encoding
* Scales the features using StandardScaler
* Reduces the dimensions using PCA
* Finds a suitable number of clusters using the Elbow Method and Silhouette Score
* Applies K-Means Clustering
* Applies Agglomerative Clustering
* Visualizes the customer clusters
* Compares customer income and spending across clusters

## 🧠 Machine Learning Techniques Used

### 1. PCA

Principal Component Analysis is used to reduce the dimensionality of the dataset while keeping the important information.

In this project, PCA is reduced to **3 components**, which also makes it easier to visualize the data in 3D.

### 2. K-Means Clustering

K-Means is used to divide customers into different groups based on similarities in their features.

The project uses **4 clusters** for the final K-Means model.

### 3. Agglomerative Clustering

Agglomerative Clustering is another unsupervised learning method used in the project to group similar customers.

The project uses **4 clusters** for the Agglomerative Clustering model as well.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Kneed
* Jupyter Notebook

## 📊 Dataset Processing

The project performs several preprocessing steps before applying clustering.

### Missing Values

Missing values in the `Income` column are filled using the **median income**.

### Feature Engineering

Some new features are created to make the customer data more useful:

* **Age** – calculated from the customer's birth year
* **Customer Tenure** – number of days since the customer joined
* **Total Spending** – total spending across different product categories
* **Total Children** – combination of children and teenagers in the household

### Data Simplification

Some categories are grouped together to make the data easier to analyze.

For example:

* Basic and 2n Cycle → Undergraduate
* Graduation → Graduate
* Master and PhD → Postgraduate

Similarly, marital status is converted into two broader categories:

* Partner
* Alone

### Outlier Removal

Some extreme values are removed from the dataset, including customers with:

* Age of 90 or above
* Income of 600,000 or above

This helps reduce the effect of extreme values during clustering.

## 🔄 Project Workflow

```text
Customer Dataset
       ↓
Data Exploration
       ↓
Missing Value Handling
       ↓
Feature Engineering
       ↓
Data Cleaning
       ↓
Outlier Removal
       ↓
One-Hot Encoding
       ↓
Feature Scaling
       ↓
PCA
       ↓
Finding Suitable Number of Clusters
       ↓
K-Means & Agglomerative Clustering
       ↓
Cluster Visualization
       ↓
Customer Analysis
```

## 📈 Visualizations

The notebook includes several visualizations to understand the dataset and clustering results, including:

* Pair plots
* Correlation heatmap
* PCA 3D projection
* Elbow curve
* Silhouette score plot
* K-Means cluster visualization
* Agglomerative clustering visualization
* Customer count by cluster
* Income vs Total Spending by cluster

## 📂 Project Structure

```text
SmartCart/
│
├── smartcart.ipynb
├── smartcart_customers.csv
└── README.md
```

### `smartcart.ipynb`

The main Jupyter Notebook containing the complete data analysis, preprocessing, visualization, and clustering process.

### `smartcart_customers.csv`

The customer dataset used for the analysis.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/SmartCart.git
```

### 2. Open the project folder

```bash
cd SmartCart
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kneed
```

### 4. Open the notebook

```bash
jupyter notebook
```

Then open:

```text
smartcart.ipynb
```

Make sure `smartcart_customers.csv` is kept in the same folder as the notebook.

## 🎯 Project Objective

The main objective of SmartCart is to use customer data to discover different customer groups based on their characteristics and purchasing behavior.

This type of segmentation can be useful for understanding customers and can provide a starting point for things such as targeted marketing, customer analysis, and personalized offers.

## 🔮 Future Improvements

Some possible improvements for the project are:

* Add more clustering algorithms for comparison
* Create an interactive dashboard for the clusters
* Provide detailed profiles for each customer segment
* Build a system that can assign new customers to an existing segment
* Explore customer purchasing patterns in more detail
* Use the clusters for personalized marketing or recommendation systems

## 👨‍💻 Project

**SmartCart – Customer Segmentation Using Machine Learning**

Built using Python and popular data science and machine learning libraries.
