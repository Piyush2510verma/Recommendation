# Recommendation


1. Data Loading and Preprocessing:
   - Two datasets are loaded, including `triplet_file` with user-song-listen_time data and `metadata_file` with song metadata.
   - The datasets are merged based on the 'song_id' column.
   - A new feature 'song' is created by combining the 'title' and 'artist_name' to represent each song.
   - The dataset is limited to the top 10,000 samples for faster processing.
   - The data is grouped by the 'song,' and the percentage of listen counts for each song is calculated.

2. Popularity Recommendation Engine:
   - The code uses the `Recommenders.popularity_recommender_py()` class to establish a popularity-based recommendation system.
   - This type of recommendation system suggests popular items to all users, regardless of their individual preferences.
   - The code recommends popular songs to specific users by calling the `recommend()` method of the popularity recommender. For instance, it provides recommendations for users with 'user_id' 5 and 100.

3. Item Similarity Recommendation Engine:
   - The `Recommenders.item_similarity_recommender_py()` class is utilized to create an item similarity-based recommendation system.
   - This recommendation system offers suggestions of items that are similar to those the user has interacted with previously.
   - Initially, the code retrieves the user's song history using the `get_user_items()` method and subsequently provides song recommendations to the user using the `recommend()` method.
   - Additionally, it can identify songs that are similar to a given set of songs using the `get_similar_items()` method. For example, it finds songs similar to 'Oliver James - Fleet Foxes' and 'The End - Pearl Jam'.


