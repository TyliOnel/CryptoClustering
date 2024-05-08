# Crypto Clustering

![image](https://github.com/TyliOnel/CryptoClustering/assets/153153538/5d4c2372-ef3f-45cb-948c-22bb5112eb61)


## Introduction
The Crypto Clustering project seeks to utilize unsupervised learning techniques, particularly K-means clustering, to determine if cryptocurrencies are impacted by 24-hour or 7-day price changes. Additionally, the project explores how Principal Component Analysis (PCA) affects clustering performance.

## Steps
1. **Data Loading and Preprocessing**: Load cryptocurrency market data and prepare it for analysis.
2. **Data Scaling**: Standardize the data using StandardScaler for consistency.
3. **Determining Optimal K**: Apply the elbow method to find the best number of clusters.
4. **Clustering**: Perform K-means clustering on the original scaled data to group cryptocurrencies.
5. **Principal Component Analysis (PCA)**: Conduct PCA to reduce feature dimensions to three principal components.
6. **Determining Optimal K (PCA Data)**: Use the elbow method on PCA-transformed data to find the best number of clusters.
7. **Clustering (PCA Data)**: Employ K-means clustering on PCA-transformed data to cluster cryptocurrencies.
8. **Visualization and Comparison**: Visualize clustering results using hvPlot and compare outcomes between the original and PCA-transformed data.

Through these steps, the project aims to gain insights into cryptocurrency behavior and evaluate the impact of dimensionality reduction techniques on clustering accuracy.

## Dependencies
- Python
- pandas
- NumPy
- scikit-learn
- hvPlot

## Results
### Elbow Graphs

![image](https://github.com/TyliOnel/CryptoClustering/assets/153153538/32e552bb-2cbb-4c0f-af68-dc5a933e0c52)

![image](https://github.com/TyliOnel/CryptoClustering/assets/153153538/c65195c0-549d-40ef-9662-13a17e695c19)

The PCA data's elbow curve (elbow curve 2) exhibits a decreased inertia value compared to the original data's elbow curve (elbow curve 1). This suggests that utilizing fewer features led to a diminution in the sum of squared distances within clusters. A reduced inertia value indicates enhanced clustering performance and tighter cohesion of data points within each cluster.

### Cluster Graphs

![image](https://github.com/TyliOnel/CryptoClustering/assets/153153538/90ba9c38-7a8a-4941-8bc5-8d2532f17bfd)
Cluster Graph 1 (utilizing original data): The clusters exhibit overlap without clear separation or distinctiveness. This implies that employing the original dataset, with its numerous features, might not adequately capture the inherent patterns or structure essential for clustering.

![image](https://github.com/TyliOnel/CryptoClustering/assets/153153538/3999f454-b69f-4b01-b9d5-ada72c71148d)
Cluster Graph 2 (utilizing PCA data): In this graph, clusters are non-overlapping, displaying clear separation and well-defined groupings. Four distinct clusters are identifiable. This suggests that employing fewer features via PCA may have mitigated noise, thereby unveiling more discernible patterns within the data, resulting in more meaningful and distinguishable clusters.

## Conclusion
After visually analyzing the cluster analysis results, it's clear that reducing the number of features for data clustering using K-Means made a significant difference. Originally, the elbow curve suggested 4 clusters, but two contained only one data point each, and the others weren't well separated. Implementing PCA with an optimal K value of 2 resulted in a more accurate clustering plot.

