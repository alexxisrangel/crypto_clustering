# Crypto Market Data Clustering 

## Table of Contents 
Prerequisites
Data Loading
Data Preprocessing
K-Means Clustering
Results

### Prerequisites

Before running the code, the following must be installed
- python (>=3.6)
- Jupyter Notebook
- pandas
- hvplot.pandas
- scikit-learn

#### Data Preprocessing 

The cryptocurrency market data is preprocessed to normalize the features using StandardScalar from scikit-learn. Scaling the data is necessary for K-means clustering![Screenshot 2023-09-28 at 12 43 10 PM]

(https://github.com/alexxisrangel/crypto_clustering/assets/129305054/0e5714fe-8f98-40d4-b8ee-0a4781951d09)

#### PCA Data 

PCA was used in order to see if better results may be obtained with less data. For PCA1 it explains that 37% of the total varience, meaning it represents the most significant patterns or information followed by PC2 at 34% and PC3at 17%. This helps us understand the relative importance of each principal component in reducing the dimensionality of our data. The more the data is reduced. We can use these principal components to decide how much we want to reduce our data. 
<img width="640" alt="Screenshot 2023-09-28 at 1 18 11 PM" src="https://github.com/alexxisrangel/crypto_clustering/assets/129305054/61bb48df-57e9-4a5a-8e27-a2f3b8069aea">


##### K-Means Clustering 

K-Means was preformed using both scaled data and the original data. It iterates through a range of k values (1-10) to determine teh optimal number of clusters (k) using the "elbow method". The Elbow Method helps identify the point at which inertia (within-cluster sum of squares) starts to level off. After the K-Means results, it was most optimal for the original data to have 4 clusters while the PCA data only required 3. 


![Screenshot 2023-09-28 at 12 52 17 PM](https://github.com/alexxisrangel/crypto_clustering/assets/129305054/0625429c-641e-4fec-9260-764cf4226021)



![Screenshot 2023-09-28 at 12 50 07 PM](https://github.com/alexxisrangel/crypto_clustering/assets/129305054/a1326d4c-1c2a-4a7c-83f0-99e2210f57f6)

![Screenshot 2023-09-28 at 12 50 24 PM](https://github.com/alexxisrangel/crypto_clustering/assets/129305054/40c28c34-2560-4bd6-9ae8-bd42d45314ff)


###### Results 

The impact of having fewer features to clusters resulte in less groups to identify the data by. Depedning on the project, this could be something we want or something to make us reconsider our approach. Having fewer clusters means less noise and potentially filtering out the data we dont need. However if too much is reduced, it can lead to less distinct or less accurate predictions. 

<img width="1379" alt="Screenshot 2023-09-28 at 1 19 38 PM" src="https://github.com/alexxisrangel/crypto_clustering/assets/129305054/221bb550-8e86-46c0-a4db-8b882cade2fd">



