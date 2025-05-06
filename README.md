
# 🛍️ Task 8: Mall Customer Segmentation - Clustering (K-Means & DBSCAN)

## 📌 Objective
Segment mall customers into meaningful groups using **K-Means** and **DBSCAN** clustering algorithms. Analyze customer behavior patterns based on features like **Gender**, **Age**, **Annual Income**, and **Spending Score**.

---

## 📂 Dataset
- **Source:** Mall Customer Segmentation Data
- **Features:**
  - `CustomerID`
  - `Gender` (Categorical)
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1-100)`

---

## 🔧 Preprocessing
- Converted `Gender` to numerical (`Male` → 1, `Female` → 0)
- Removed `CustomerID`
- Scaled all numerical features using `StandardScaler`

---

## 📊 Clustering Approaches

### 1️⃣ K-Means Clustering
- **Elbow Method:** Initially explored the optimal number of clusters
- **Silhouette Analysis:** Used to evaluate cluster cohesion
- **Optimal k:** Found to be **10** with the highest silhouette score (~0.42)
- **Cluster Summary:** Displayed mean values per cluster for feature interpretation
- **Visualization:** 2D scatter plot using PCA

### 2️⃣ DBSCAN Clustering
- **Density-based** clustering approach
- Identified outliers (labeled as `-1`)
- Performed poorly compared to K-Means on this dataset
- **Silhouette Score:** ~0.27
- **Visualization:** PCA-based cluster plot

---

## 📈 Evaluation

| Algorithm | Optimal Clusters | Silhouette Score | Notes |
|----------|------------------|------------------|-------|
| K-Means  | 10               | **0.42**         | Clear and compact clusters |
| DBSCAN   | 9 + outliers     | 0.27             | Struggled due to data distribution |

---

## 📌 Conclusion
- **K-Means** was more effective for this dataset due to well-separated, compact clusters.
- **DBSCAN** detected some outliers but struggled with the uniform distribution of points.
- Silhouette analysis was key in validating clustering quality.

---

## 📁 Files
- `task8_kmeans_dbscan.ipynb`: Jupyter notebook with full code and output
- `README.md`: Project summary and methodology
- Visual outputs: Cluster visualizations and silhouette plots
