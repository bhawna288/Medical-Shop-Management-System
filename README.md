#Movie-Recommender-System
Building A Recommender System on User-User Collaborative Filtering We can use many similarity models for this purpose like the Pearson, Cosine etc and we will be using to the Eucledian Distance model for this one. This is the popular MovieLens dataset.It has 100,000 ratings from 1000 users on 1700 movies. Released 4/1998.It has multiple CSV files zipped into a folder. We shall be working with these files

u.data: -- The full u data set, 100000 ratings by 943 users on 1682 items. Each user has rated at least 20 movies. Users and items are numbered consecutively from 1. The data is randomly ordered. This is a tab separated list of user id | item id | rating | timestamp. The time stamps are unix seconds since 1/1/1970 UTC
u.item -- Information about the items (movies); this is a tab separated list of movie id | movie title | release date | video release date | IMDb URL | unknown | Action | Adventure | Animation | Children's | Comedy | Crime | Documentary | Drama | Fantasy | Film-Noir | Horror | Musical | Mystery | Romance | Sci-Fi | Thriller | War | Western | The last 19 fields are the genres, a 1 indicates the movie is of that genre, a 0 indicates it is not; movies can be in several genres at once. The movie ids are the ones used in the u.data data set.
u.user -- Demographic information about the users; this is a tab separated list of user id | age | gender | occupation | zip code The user ids are the ones used in the u.data data set.

#Requirements
1.Numpy
2.Pandas
3.Scipy
4.Matplotlib
Collaborative Filtering is based on the similarity in preferences, tastes and choices of two users. It analyses how similar the tastes of one user is to another and makes recommendations on the basis of that.

Recommender System Based on User-Based Collaborative Filtering We used only two of the three data files in this one; u.data and u.item. We used Eucledian Distance as a measure of similarity between users. In case two users have less than 4 movies in common they were automatically assigned a high EucledianScore. Otherwise EuclediaScore was calculated as the square root of the sum of squares of the difference in ratings of the movies that the users have in common.
