# Movie-Recommendation
People spend a lot of time on their hobbies such as reading, writing, dancing, sports. Hobbies play an important role in shaping a person, to the extent that it can determine their likes and dislikes. The aim of this project is to build a movie recommendation system based on these hobbies and interests.

The ’Young People Survey’ dataset (1010 x 150) has been chosen from Kaggle. This data has been collected in a survey conducted on the youth of Slovakia. There are two csv files, responses.csv and columns.csv. The data set can be found in the folder titled dataset.
<br>Note:All program files are of .ipynb format. They can be run on jupyter notebook.

The first step was cleaning the data. This includes checking the outliers, checking missing values and replacing them with appropriate values and checking invalid entries. The code for this can be found in the 'Cleaning' branch.

Next, the data was visualised. This was done by using various visualisation techniques such as bar graphs, pie charts and correlograms.
These graphs were plotted on various attributes such as Age, Gender and BMI of the survey group. The code for this step can be found in the 'Visualisation' branch. 

The data has many attributes-almost too many to build a model on. When a model is built on many attributes, it can lead to overfitting. The model can instead be built on a few important attributes. These important attributes can be found out with the help of Principal Component analysis. The code for this can be found in the file titled 'PCA.ipynb'.

The first method employed for prediction was Linear Regression, where the rating for each genre was predicted with hobbies as features. The code for this can be found in 'Linear_Regression.ipynb'. The accuracy obtained by this method was very low. This lead us to look at various clustering algorithms.

Different clustering algorithms were implemented. Partitional K-means and K-modes was used to seperate the data into clusters. Code for this can be found in 'K-means.ipynb' and 'K-modes.ipynb' respectively. The disadvantage with this method was that there was no clear distinction between the clusters. Thus, agglomerative K-modes clustering was used. The number of clusters were gradually reduced until a minimum cost was obtained.The optimal number of clusters was found to be 8. Code for this can be found in 'Agglomerative_kmodes.ipynb'.

The ratings for a user were predicted based on collaborative filtering. The user was first classified into a cluster based on the euclidian distance with the centroid of each cluster. Cosine similarity between the new user and each user in the cluster was calculated. The ratings were predicted based on these calculations. The genres with top Three ratings were recommended. The code for this can be found in 'Recommendation.ipynb'.

The model was evaluated using 5-fold cross-validation. The accuracy was found to be 32.31%. Code for this can be found 'K-fold.ipynb'. Reasons for low accuracy could be other factors that influence preferences. Improvements include considering mood of a user while predicting.
