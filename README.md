# Music-Recommendation-System-using-Machine-Learning

**Abstract**

This project presents a content-based music recommendation system that leverages natural language processing (NLP) techniques to suggest similar songs based on user input. The dataset is preprocessed by handling missing values, removing duplicates, and standardizing textual data. Key features such as singer/artist names, genres, album/movie titles, and user ratings are combined into a unified text field (tags) for each song. This composite field is then vectorized using the Bag-of-Words approach via CountVectorizer, and cosine similarity is computed to measure the textual closeness between songs. A recommendation function identifies and returns the top five most similar songs for any given input track. The model and similarity matrix are serialized using pickle for future use. Visualizations including genre distribution, user rating histograms, and artist frequency charts are also incorporated to provide insight into the dataset’s composition. This system demonstrates a scalable approach to building lightweight, explainable music recommenders without relying on complex deep learning models or user-specific behavior.

**Steps**

1.	Data Loading & Cleaning
   
	•	Removed null values and duplicates.
	•	Extracted user rating substring (i[1:3]), which assumes the rating is in a consistent format like '★4.5'.

2.	Data Visualization
   
	•	Visualized distributions of genres, user ratings, artists, and albums.
	•	Generated a correlation heatmap (though it likely has limited numerical data).

3.	Text Processing
   
	•	Created a tags column by concatenating cleaned fields (Singer/Artists, Genre, Album/Movie, User-Rating).
	•	Transformed text to lowercase and tokenized it using CountVectorizer.

4.	Similarity Calculation
   
	•	Used cosine_similarity on the CountVectorizer output.
	•	Implemented a recommend() function that returns the top 5 similar songs based on the tags.

5.	Model Serialization
    
	•	Pickled new_df and similarity matrix for later use.
