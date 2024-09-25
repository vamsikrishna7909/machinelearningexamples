# Clustering Analysis: K-Means and Hierarchical Clustering

## Overview of the Dataset
In this project, I have applied **K-Means Clustering** and **Hierarchical Clustering** on a Health Insurance dataset. The dataset contains two main columns used for clustering:
- **BMI** (Body Mass Index)
- **Insurance Charges**

These two features are used to group customers into distinct clusters to gain insights into customer behavior based on health metrics and insurance costs.

---

## 1. K-Means Clustering

### Introduction
**K-Means Clustering** is an unsupervised learning algorithm that groups unlabeled data into clusters. The algorithm assigns each data point to one of the **K** predefined clusters. The value of **K** (the number of clusters) needs to be specified in advance. 

- If **K=2**, the dataset will be split into 2 clusters.
- If **K=3**, the dataset will be split into 3 clusters, and so on.

### Finding the Optimal Number of Clusters

**Elbow Method**:  
To determine the optimal number of clusters, I used the **Elbow Method**. This method analyzes the **Within Cluster Sum of Squares (WCSS)** to find the optimal **K** value.

![Elbow Method](path/to/elbow-method-image.png)

- As shown in the figure above, the sharp bend or elbow in the plot represents the best value of **K**.  
- The bend appears at **K=3**, which indicates that 3 is the optimal number of clusters for this dataset.

### Visualizing the Clusters

Once the optimal number of clusters is determined using the Elbow Method, the clusters can be visualized.

![K-Means Clustering](path/to/k-means-cluster-visualization.png)

### Observation
The above visualization clearly shows three distinct clusters formed based on **BMI** and **Insurance Charges**.

- **Cluster 1 (Careless)**:  
  Customers with higher BMI values tend to pay higher insurance charges.  
- **Cluster 2 (Less Careless)**:  
  Customers with moderate BMI values pay lower insurance charges than those in Cluster 1.  
- **Cluster 3 (Careful)**:  
  Customers with the lowest BMI values pay the least in insurance charges compared to the other two clusters.

---

## 2. Hierarchical Clustering

### Introduction
**Hierarchical Clustering** is another unsupervised learning algorithm used to group unlabeled datasets into clusters. Unlike K-Means, it does not require specifying the number of clusters beforehand.

Hierarchical clustering builds a hierarchy of clusters in the form of a **dendrogram** (a tree-like structure). This method can be implemented in two ways:
- **Agglomerative Clustering** (bottom-up approach)
- **Divisive Clustering** (top-down approach)

### Approach Used
I applied the **Agglomerative Clustering** approach, which starts with each data point as a single cluster and merges them progressively until a single cluster is formed.

### Dendrogram for Optimal Number of Clusters

To determine the optimal number of clusters, I used a dendrogram. The **Y-axis** represents the Euclidean distance between the data points, and the **X-axis** represents the data points themselves.

![Dendrogram](path/to/dendrogram-image.png)

- From the dendrogram, we can observe a significant vertical line at **2 clusters**, which is the optimal number of clusters for Hierarchical Clustering.

### Visualizing the Clusters

After determining the optimal number of clusters, the clusters can be visualized as shown below:

![Hierarchical Clustering](path/to/hierarchical-cluster-visualization.png)

### Observation
By comparing the results from both K-Means and Hierarchical Clustering:
- **Cluster 1 (Careless)** and **Cluster 2 (Less Careless)** from K-Means correspond to **Cluster 1** in Hierarchical Clustering when the cluster value is 2.
- **Cluster 3 (Careful)** from K-Means corresponds to **Cluster 2** in Hierarchical Clustering.

Thus, customers categorized as "Careless" and "Less Careless" in K-Means are grouped together in **Cluster 1** in the Hierarchical Clustering, while those labeled as "Careful" form **Cluster 2**.

---

### Conclusion
Both **K-Means** and **Hierarchical Clustering** provide valuable insights into customer behavior based on BMI and insurance charges. The Elbow Method and Dendrogram helped to identify the optimal number of clusters, with K-Means suggesting 3 clusters and Hierarchical Clustering refining this to 2 broader categories.

### Tools Used:
- Python (Pandas, Matplotlib, Scikit-learn)
- K-Means Clustering
- Agglomerative Hierarchical Clustering
