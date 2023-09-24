# Supervised Sentiment Analysis: Word2Vec as an input into Logistic Regression on IMDB Dataset

In this notebook, we will be training word embeddings over the IMDB Movie Review dataset, and averaging the word embeddings of each word over 1 review text blob to create an embedding representing each review. Then we will be feeding the embeddings we created as an input into a downstream Logistic Regression model that we will use to classify the prelabeled review sentiments as "Positive" or "Negative".

## Word2Vec and Word Embeddings

Word embeddings are a type of representation used in natural language processing (NLP) that allows words to be represented as dense vectors in a high-dimensional space. These vectors capture semantic and syntactic information about the words they represent, allowing NLP models to better understand the meaning of language.

Word2vec is a popular algorithm for training word embeddings. It works by analyzing the co-occurrence patterns of words in a large corpus of text and learning to predict which words are likely to appear near each other.

The Word2vec module is available directly in Python from the library "gensim". Notice that there are several parameters you can customize (size, window, min_count, sg). By default, size (defining the output vector dimensions) is set to 100, window to 5, min_count to 5, and sg to 0 (i.e. continuous bag of words). After developing our embeddings, we will use them as input into the downstream model – in this case, logistic regression. After that we will adjust the vector size of the embeddings between [25, 50, 100, 150] and window_size used to create embeddings between [2, 3, 5, 10], and assess how it affects our classifier algorithms performance by plotting Size vs. Accuracy graphs. 

Note that, since the dataset is too large it is not uploaded into this repository. However, you can find it on Kaggle through the link below:

https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews
