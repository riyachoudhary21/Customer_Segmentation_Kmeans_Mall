# Mall Customer Segmentation Using K-Means Clustering

## Overview
This repository implements **K-Means Clustering** for customer segmentation using the popular **Mall Customers** dataset. It demonstrates the complete unsupervised learning pipeline, including exploratory analysis, optimal cluster identification, and multi-dimensional visualization techniques.


## Objectives
- Perform unsupervised clustering on mall customers using income, age, and spending behavior.
- Identify optimal number of clusters using the **Elbow Method**.
- Visualize customer segments in **2D and 3D**.
- Evaluate clustering performance using the **Silhouette Score**.
- Use **PCA** for dimensionality reduction and decision boundary visualization.


## Tools & Technologies
**Language:** Python  
**Environment:** Google Colab / Jupyter Notebook  

### Key Libraries:
- `pandas`, `numpy` – Data handling  
- `matplotlib`, `seaborn` – Visualization  
- `scikit-learn` – ML modeling (`KMeans`, `StandardScaler`, `PCA`, `silhouette_score`)  
- `mpl_toolkits` – 3D plotting  


## Workflow & Highlights

### Data Exploration

- **Dataset:** 200 mall customers with features like Age, Annual Income (k$), and Spending Score (1-100)  
- **No missing values** or null entries found  
- Used selected features for clustering:
  - **2D:** Annual Income, Spending Score  
  - **3D:** Age, Annual Income, Spending Score  

### Data Preprocessing

- Standardized selected features using StandardScaler  
- Converted data into suitable format for clustering  


## Model Building & Optimization

### Elbow Method (WCSS)
- Plotted **Within-Cluster Sum of Squares (WCSS)** for K = 1 to 10  
- Identified **optimal K = 5 (2D)** and **K = 6 (3D)** based on the elbow

### K-Means Clustering
- Used KMeans with init='k-means++' for faster convergence  
- Fitted models on scaled features  
- Assigned cluster labels  


## Evaluation Metrics

| Feature Set               | Optimal K | Silhouette Score |
|---------------------------|-----------|------------------|
| 2D (Income, Score)        | 5         | 0.553            |
| 3D (Age, Income, Score)   | 6         | 0.585            |  


## 🖼️ Visual Outputs

- Elbow plots (**2D & 3D**)  
- Cluster visualizations with centroids  
- PCA-based scatter plot of segments  
- Clear segmentation visible for high, low, and average spenders  


## Key Insights

- Five main customer groups were found based on income and spending habits  
- PCA-based visualization confirms well-separated clusters  
- Spending Score was highly influential in cluster separation  
- 3D clustering gave slightly better silhouette score, showing benefit of multi-feature analysis  


## Learning Outcomes

- Practical implementation of K-Means clustering.  
- Experience using Elbow Method and Silhouette Score for evaluation.  
- Applied 3D and PCA visualizations for interpretability.  
- Learned customer segmentation techniques used in marketing and business intelligence.
