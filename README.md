# Unsupervised Machine Learning / Clustering on cryptocurrency dataset
Cleaning of a cryptocurrency dataset to perform and visualize clustering using Principal Component Analysis, K-means

## Resources
- Data: crypto_data.csv from CryptoCompare https://min-api.cryptocompare.com/data/all/coinlist
- Software: Jupyter Notebook 6.3.0, scikit-learn, Plotly, hvplot and Pandas libraries

## Overview
Creating a grouping / classification system for all the available cryptocurrencies using unsupervised ML with the scikit PCA and K-means libraries.

Dataset was initially cleaned to exclude currencies that are not traded and not currently mined. Final, cleaned dataset includes 532 currencies.

Data for string columns ('Algorithm' and 'ProofType') was then transformed and scaled using `get_dummies()` and `StandardScaler()`

<img width="500" alt="Screen Shot 2022-02-22 at 00 14 28" src="https://user-images.githubusercontent.com/90064437/155073665-ba15498f-2eda-4b37-9005-013535804ad9.png">


Next, scikit's PCA library was used to reduce the scaled data to three components:

<img width="500" alt="Screen Shot 2022-02-22 at 00 16 31" src="https://user-images.githubusercontent.com/90064437/155073897-9bcbc7b8-16ce-4366-ae5c-c463e77e800a.png">


Clustering using scikit's `KMeans()` resulted in an elbow curve suggesting four clusters:

<img width="500" alt="Screen Shot 2022-02-22 at 00 17 09" src="https://user-images.githubusercontent.com/90064437/155074199-4c10093d-0042-4e2c-8d7a-22261900c17b.png">


Combining the original dataset and the PCA dataset, setting the KMeans predictions as 'Class':

<img width="500" alt="Screen Shot 2022-02-22 at 00 20 14" src="https://user-images.githubusercontent.com/90064437/155074380-04526159-f76a-47b4-a5e7-408d9db13e48.png">

<br>
Visualizing combined dataset using Plotly Express Scatter 3D:

<img width="500" alt="Screen Shot 2022-02-22 at 00 22 00" src="https://user-images.githubusercontent.com/90064437/155074630-b25da16d-1032-4497-ae8d-0a728a6b173d.png">


Transforming the 'Total Coins Mined' and 'Total Coins Supply' columns using scikit's `MinMaxScaler()`:

<img width="500" alt="Screen Shot 2022-02-22 at 00 24 49" src="https://user-images.githubusercontent.com/90064437/155074865-8645b7a6-5c72-47b3-b522-1699bf9fc1f9.png">


Finally, visualizing the scaled dataset to show class distribution using hvplot's scatter function:

<img width="500" alt="Screen Shot 2022-02-22 at 00 25 26" src="https://user-images.githubusercontent.com/90064437/155074984-7d8213d8-d91e-486e-b9ad-91386b16949e.png">




