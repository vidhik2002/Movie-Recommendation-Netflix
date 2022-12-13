# Movie-Recommendation-Netflix
Since the pandemic OTT Platforms like Netflix, Hulu, Amazon Prime have gained a lot of popularity when it comes to shows and Movies. 
Due to their immense usage, platforms like Netflix and Amazon Prime now make their own movies and shoes. To study the impact that these platforms have on people,
I wanted to analyze Netflix data including all its movies and shows, and come up with a recommending system to help users pick out movies and shows according to the 
content they already like!

### Datasets Used 
1. [Netflix Titles](https://github.com/vidhik2002/Movie-Recommendation-Netflix/blob/master/netflix_titles.csv)
2. [Ratings Small](https://github.com/vidhik2002/Movie-Recommendation-Netflix/blob/master/ratings_small.csv)

### Recommendation System
1. Content Based Filtering
2. Collaborative Filtering

#### Content Based Filtering
I used the Cosine Similarity to calculate a numeric quantity that denotes the similarity between two movies. Mathematically, it is defined as follows:

cosine(x,y) =   (x.y⊺) / (||x||.||y||)
            
On using TF-IDF Vectorizer, calculating the Dot Product will directly give  the Cosine Similarity Score. 
Therefore, sklearn's linear_kernel instead of cosine_similarities will give a much faster answer.

Our content-based engine has some serious drawbacks. It can only recommend movies/shows that are similar to a given movies/shows. In other words, it is unable to identify preferences and make recommendations across genres.

####  Collaborative Filtering
In order to anticipate how much I will enjoy a specific product or service that those people have tried or experienced but I have not, collaborative filtering is based on the notion that users who are similar to me can be used.
Instead of implementing Collaborative filtering from Scratch , I made the use of Singular Value Decomposition (SVD) using Surprise LIbrary of python.
The goal is to minimize the value of Root Mean Square Error (RMSE) to increase the accuracy of output.
