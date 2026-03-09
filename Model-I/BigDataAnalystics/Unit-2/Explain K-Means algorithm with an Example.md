# 13.a) Explain K-Means Algorithm with an Example (20 Marks)

## Introduction

**K-Means Clustering** is an **unsupervised machine learning algorithm** used to group similar data points into clusters. It partitions a dataset into **K number of clusters**, where each cluster is represented by its **centroid (mean value of points)**. 

The algorithm iteratively assigns data points to clusters based on distance and recalculates cluster centroids until the clusters become stable.

---

## Definition

K-Means clustering is a **partition-based clustering technique** that divides a dataset into **K mutually exclusive clusters** based on similarity between data points. 

---

## K-Means Algorithm Steps

Given a dataset with **N data points** and **K clusters**, the algorithm works as follows:

1. **Choose K Centroids**

   * Randomly select K data points as initial centroids.

2. **Calculate Distance**

   * Compute the distance between each data point and the centroids using a distance metric (usually Euclidean distance).

3. **Assign Points to Clusters**

   * Assign each data point to the cluster whose centroid is closest.

4. **Recalculate Centroids**

   * Compute the mean of all points in each cluster to obtain new centroids.

5. **Repeat the Process**

   * Repeat steps 2–4 until centroids no longer change or clusters become stable.

At this stage, the clustering process stops. 

---

## Example of K-Means Clustering

Suppose we have the following **data points**:

| Point | Coordinates |
| ----- | ----------- |
| A1    | (2,10)      |
| A2    | (2,6)       |
| A3    | (11,11)     |
| A4    | (6,9)       |
| A5    | (6,4)       |

Assume **K = 2 clusters**.

### Step 1: Select Initial Centroids

Example:

C1 = (2,6)
C2 = (6,9)

---

### Step 2: Calculate Distance

Compute distance of each point from centroids.

Example:

Distance formula:

[
d = \sqrt{(x2-x1)^2 + (y2-y1)^2}
]

Each point is assigned to the nearest centroid.

---

### Step 3: Assign Clusters

After computing distances:

Cluster 1 → points near centroid C1
Cluster 2 → points near centroid C2

---

### Step 4: Recalculate Centroids

New centroid = Mean of all points in cluster.

Example:

Cluster1 points = (2,6), (6,4)

New centroid =

[
(2+6)/2 , (6+4)/2 = (4,5)
]

---

### Step 5: Repeat

Distances are recalculated and clusters updated until centroids stop changing.

---

## Applications of K-Means

According to the PDF, major applications include:

* Document classification
* Customer segmentation
* Image segmentation
* Fraud detection in banking
* Social media analysis 

---

## Advantages

* Easy to implement
* Works with large datasets
* Guaranteed convergence
* Can be applied to many domains 

---

## Disadvantages

* Need to decide number of clusters (K)
* Sensitive to outliers
* Depends on initial centroid selection
* Not effective for high dimensional data 

---

## Conclusion

K-Means clustering is a simple yet powerful unsupervised learning algorithm used to group similar data objects into clusters. It works iteratively by assigning data points to clusters and updating centroids until stable clusters are obtained.

---
