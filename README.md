# Toxic Comment Classification Challenge

Our main focus is to explore the Deep Learning models to classify the comments into different toxicity labels such as ‘toxic’, ‘severe_toxic’, ‘obscene’, ‘threat’, ‘insult’ and ‘identity_hate’.

# Kaggle Challenge

The Kaggle competition for toxic comment classification available at https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge is about detection of different types of toxic comments by classifying them into one or more labels from ‘toxic’, ‘severe_toxic’, ‘obscene’, ‘threat’, ‘insult’ and ‘identity_hate’.
The objective is to develop pre-defined models and improve their accuracy as compared to the outputs provided by Perspective API.

# Data

Originally, the train and test datasets are in csv format which were converted to json format later on.
The reason for attempting to read data from MongoDB was its ability to define secondary indexes to read any slice with millisecond latency into our processing jobs.

# Approach

Our project is focused on developing a series of neural network models to compete in toxic comment classification Challenge on Kaggle. 
The goal is to build a model which can predict the probability of each category of toxic classification, of Twitter comments. 
Three different models tested against this challange were:
1. A Recurrent Neural Network (RNN) with Long-Short term Memory and word embedding 
2. A Convolutional Neural Network (CNN) with word embedding
3. A Convolutional Neural Network (CNN) with character embedding


# Results

Analysis of all the 3 model performances are as shown below:

Model | Embeddings | AUC | LOSS | Epoch
--- | --- | --- | --- | ---
RNN | Word | 0.98488 | 0.0616 | 1
CNN | Word | 0.98603 | 0.0314 | 2
CNN | Character | 0.95649 | 0.0875 | 1

# Conclusion

By working with different types of Neural Network models with word embedding initializations, we could conclude which models may be better suited for the task of toxic comment classification. We found that the best model in our case was the CNN model with word embeddings. Although its performance accuracy is marginally better than the LSTM model, it could gain a better categorization of toxic comment accuracy. 

# Run notebook

Download all the files in a folder.

Download train.csv and test.csv data from https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data

Download fast text embeddings from https://tinyurl.com/wordtovec.

Run the notebooks RNN, CNN with word emebedding and CNN with character embedding.

You will need some time to train a model. It takes ~3-4 hours on jupyter notebook. 
Once finished, files submission1,submission2 and submission3 will be generated for respective models.




