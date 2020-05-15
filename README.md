# Goodreads-recommendation-engine



## Building a recommendation engine to recommend books in Spark

Using collaborative filtering to predict ratings of unread books on 'Goodreads'

The link to my blog published on TowardsDataScience detailing this project:-

https://towardsdatascience.com/building-a-recommendation-engine-to-recommend-books-in-spark-f09334d47d67?source=friends_link&sk=eb4e1f7c48660004224ccea0e6e8d19f

Warren Buffett was once asked about the key to success, he pointed to a stack of nearby books and said, "Read 500 pages like this every day. That's how knowledge works. It builds up, like compound interest. All of you can do it, but I guarantee not many of you will do it."
Books are the best resources for most of us to develop and gain perspectives. 

I myself love reading books. Once I like a book, I have a habit of going to good books or asking someone who has a similar taste to look for recommendations for the next series of books I might like. 
Artificial Intelligence has made our world so easy by recommending us books, movies, and products all based on the past data that saves our time and energy on analyzing different options. In fact, sometimes machines can recommend us better than what we think because they don't suffer from emotional biases.

**The intuition behind Alternating Least Square**

For someone who loves reading academic papers, here's the link to the paper: https://datajobs.com/data-science-repo/Recommender-Systems-%5BNetflix%5D.pdf.

The most important kind of recommender system is collaborative filtering based approach. Let's say you know a friend who has the same taste as you because you both love psychology, then you might like reading other books that your friend has read but you haven't. This is the sole concept behind collaborative filtering. Now let's talk specifically about Alternating least square method.


Collaborative filtering can be easily achieved by matrix factorization techniques like Singular Value decomposition where a user-rating matrix is decomposed into the user-concept matrix, concept-weights matrix, and rating-concept matrix. Concepts are basically latent or hidden factors that the matrix decomposition implicitly generates like in the case of the books, the different concepts can be psychology, data science, philosophy, etc.

Most of the matrix factorization techniques like Singular Value decomposition don't know how to deal with an incomplete/sparse matrix which means having empty values in the user-rating matrix(which is common as not every user would have read all the books). Traditionally, engineers have been imputing those values with the mean or median before performing matrix factorization to do collaborative filtering. This leads to overfitting since the books that have never been rated are being imputed by the mean or median which can skew the results towards them.

Recent methods like Alternating Least square don't suffer from these fallbacks. They suggest modeling directly the observed ratings while avoiding overfitting through a regularized mode.

##Dataset Details:

**1 million ratings rated by around 100,000 unique users**
**Rating lies from 0 to 5**

**Received RMSE score of approximately .9 using ALS**
