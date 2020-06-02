# Content Recommendation using Similarity metrics
Recommendation systems are a collection of algorithms used to recommend items to users based on information taken from the user. These systems have become ubiquitous can be commonly seen in online stores, movies databases and job finders. 

![x](https://github.com/pranavtumkur/Content-Recommendation-using-Similarity-metrics/blob/master/Datasfiles/Screenshot%20(237).png)

In this project, we explore 2 methodologies of designing a recommendation system:

• **Content based filtering** - This technique attempts to figure out what a user's favourite aspects of an item is, and then recommends items that present those aspects. In our case, we look at the genres of the movies the user has already rated. Depending on this rating, we find a cumulative genre-wise rating score. We then assign weights to the genre to a large movies dataset and suggest the most suitable movies to him in descending order.

• **Collaborative Filtering** (also known as User-User Filtering)- As hinted by its alternate name, this technique uses other users to recommend items to the input user. It attempts to find users that have similar preferences and opinions as the input and then recommends items that they have liked to the user. There are several methods of finding similar users (Even some making use of Machine Learning), and the one we will be using here is going to be based on the Pearson Correlation Function.

## The Data

The Dataset is acquired from [GroupLens](http://grouplens.org/datasets/movielens/), stored as an IBM Object Storage. It contains 22884377 ratings and 586994 tag applications across 34208 movies. The data is contained in four files, `links.csv`, `movies.csv`, `ratings.csv` and `tags.csv`. This and other GroupLens data sets are publicly available for download at http://grouplens.org/datasets/.

## The Process

The process varies between a content based and a collaborative approach
##### Collaborative Filtering
The general process flow for creating a User Based recommendation system is as follows :

- Select the movies the user has watched
- Based on his rating to movies, find the top X neighbours
- Get the watched movie record for each neighbour.
- Calculate a similarity score using some formula
- Recommend the items with the highest score
##### User-User Filtering
- Select the movies the user has watched
- Based on his rating to movies, find the top X criterion
- Apply that criterion to the movies data as a weight
- Recommend the items with the highest score

## Advantages and Disadvantages of Content-Based Filtering

##### Advantages
* Learns user's preferences
* Highly personalized for the user

##### Disadvantages
* Doesn't take into account what others think of the item, so low quality item recommendations might happen
* Extracting data is not always intuitive
* Determining what characteristics of the item the user dislikes or likes is not always obvious

## Advantages and Disadvantages of Collaborative Filtering

##### Advantages
* Takes other user's ratings into consideration
* Doesn't need to study or extract information from the recommended item
* Adapts to the user's interests which might change over time

##### Disadvantages
* Approximation function can be slow
* There might be a low of amount of users to approximate
* Privacy issues when trying to learn the user's preferences



