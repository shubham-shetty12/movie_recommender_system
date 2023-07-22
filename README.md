# Movie Recommendation System using Collaborative Filtering
This Movie Recommendation System is based on collaborative filtering, specifically utilizing the item-item matrix approach. Collaborative filtering is a popular technique used in recommender systems to provide personalized recommendations to users based on the preferences and behaviors of similar users.

In this system, we will be using the item-item matrix to identify similarities between movies and make recommendations accordingly. The item-item matrix is constructed by calculating the similarity between each pair of movies based on user ratings. Once the item-item matrix is created, it can be used to find similar movies for a given movie and recommend them to users who have shown interest in the given movie.

### Requirements

To run this Movie Recommendation System, you will need the following:
- Python (>= 3.6)
- NumPy library
- Pandas library

### Installation

You can install the required libraries using pip

### Prepare Data

- Before using the recommendation system, you need to have a dataset containing user ratings for various movies. we have 2 csv files user and movie which has columns like item_id & title in movie and user_id,item_id,rating, timestamp. We can then merge both files using item_id coluimn.
- Timestamp can be used for splitting data, oldest timestamp data will be used for Train and latest timestamp data as Test. Timestamp should be sorted in descending.
- Load Data: Load the dataset into a Pandas DataFrame.
- Item-Item Matrix Calculation: Use the below code to calculate the item-item matrix based on the user ratings. The item-item matrix will represent the similarity between movies.
## sim_mat=data.pivot_table(index='user_id',columns='title',values='rating')
## sim_mat.head()

### Recommendation: 
Once the item-item matrix is calculated, you can use it to make movie recommendations for a given user. When a user requests movie recommendations, the system will look for the top-rated movies by similar users for the movies the user has already rated highly.

### Conclusion
This Movie Recommendation System utilizes collaborative filtering and the item-item matrix approach to provide personalized movie recommendations to users. By calculating the similarity between movies based on user ratings, the system can suggest relevant movies to users based on their past preferences. Feel free to experiment with different datasets and tuning parameters to optimize the performance of the recommendation system.

Happy recommending!
