# Item-Based-Collaborative-Recommendation-System-
The recommendation system Using the rating and similarity among the two users; the system recommends an item to the user for decision making. 
Then separate the movie data set into an unrated and rated sample set with the help of the KNN model.
It can recommend the movies to the unseen users via user registration information, and it can create new and not popular movie recommendations according to the film's history and score. The above representation depicts their effective way of approach for a collaborative filtering approach using KNN.
The Datasets which are used are movies and rating data for different users who experience different movies and rate them accordingly and the files can be viewed in this Repo
I used Google Colaboratory.
We can use anything for an IDE like VS, Jupyter if you know how to import the data its fine or use Google Colab using my code. Place the dataset in your Google-drive. Continue to code exactly and go through the Code to understand this explanation.
In the code, firstly we import different packages like NumPy and Pandas.
Then store the movies and rating dataset in 2 different variables respectively.
We must make a new dataset which is the union of 2 datasets that are interlinked by the pivot() method and also must consider the empty rows and fill them with 0 using the fillna() method to the dataset. Now, we perform the operations on variables in such a way that the redundant and useless data are filtered because a user cannot rate a movie twice, and also the user with less than 50 ratings is removed due to credibility and movies which are less than 10 user ratings are removed. Then we use reset_index() to make the dataset arrangement proper which a machine can identify.
For reducing time and space complexity now we use import csr_matrix methods from Scipy.sparse package to take in the KNN algorithm.
Now we import NearestNeighbors methods from sklearn.neighbors to use the KNN algorithm method for finding the nearest neighbors of the given movieId. KNN methods have 2 parameters which are similarity and their movieIds. zip(), and squezze(), lambda methods are also used to get a proper list. Sort using sorted and Remove the data which are noise and outliers from the nearest neighbors. print the remaining values in the list using a loop.
We automate the process by defining a method like get_movie_recommendations(movie_name), the movie_name is an input parameter. Now, we get our recommendations based on the given input and its respective movie similarities. 
