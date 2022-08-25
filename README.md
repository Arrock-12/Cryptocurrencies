# Cryptocurrencies
## Overview
Using unsupervised machine learning algorithm, create a report on current cryptocurrencies trading in the market and classify them using Principal Component Analysis (PCA).

### Process

-	Preprocess data to prepare it for the unsupervised learning algorithm by cleaning up columns and eliminating null values, translating non-numeric columns into numeric using get_dummies function, and scaling the data
-	Using an elbow curve to determine the ideal number of centroids for a K-means algorithm
-	Clustering the data using the K-means algorithm
-	Using PCA to group the cryptocurrencies into 4 classes and visualize with hvplot

## Results

After cleaning the data, the rows were reduced from over 1,250 to 532. This step eliminated unmined cryptocurrencies and ensured that only cryptocurrencies that were actively being traded were grouped into classes.

![crypto_df_index_change](https://user-images.githubusercontent.com/101822948/186741767-76563a7d-b551-4e51-a683-0f493eed6d19.png)

The preprocessed data was then analyzed and plotted on an Elbow Curve to determine the ideal number of clusters to apply to the K-means algorithm. The Elbow Curve clearly indicated that four clusters were ideal.

![elbow_curve](https://user-images.githubusercontent.com/101822948/186741786-7bb25a2c-b5aa-4c8b-8cad-85bcdf72d6d8.png)

Using the results from the Elbow Curve, four clusters were fed into the K-means algorithm and PCA to determine three principal components: PC 1, PC 2, PC 3.

![principal components](https://user-images.githubusercontent.com/101822948/186741830-c3179b4a-5dc7-47a4-a821-59611df88a77.png)

The components were with plotted on a 3D scatterplot showing the four clusters of tradeable cryptocurrencies.

![3D_cluster](https://user-images.githubusercontent.com/101822948/186741845-3a2a3356-5c58-47dd-800f-c73793bde7ff.png)


Finally, the four classes of tradeable cryptocurrencies were plotted to show the Total Coins Mined vs the Total Coin Supply to provide to the client for their use. 

![hvplot_scatter](https://user-images.githubusercontent.com/101822948/186741869-880be57b-4d11-4a57-8bad-fa16a9e4c075.png)
