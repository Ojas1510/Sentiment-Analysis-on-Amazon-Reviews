# Sentiment Analysis on Amazon Fine Food Reviews
# Introduction
Sentiment analysis is a natural language processing (NLP) task that involves determining the sentiment or emotional tone expressed in a given piece of text. <br>
In this project, I performed sentiment analysis on the Amazon Fine Food Reviews dataset. <br>
The dataset was obtained from Kaggle and contains a large number of reviews for various food products available on Amazon. <br>

# Dataset
The dataset used in this project is the "Amazon Fine Food Reviews" dataset, which can be found on Kaggle at the following link: https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews. <br>
The dataset contains various attributes such as Id,	ProductId	,UserId	,ProfileName, HelpfulnessNumerator,	HelpfulnessDenominator,	Score	Time. <br>
# Data Preprocessing <br>
Before performing sentiment analysis, it's essential to preprocess the data to remove noise and irrelevant information. The preprocessing steps include: <br>
Handling the missing values in dataset. <br>
Removing HTML tags: Some reviews may contain HTML tags that are not relevant to sentiment analysis and need to be stripped. <br>
Removing special characters and punctuation: Non-alphanumeric characters are removed to clean the text and avoid unnecessary complications during analysis. <br>
Tokenization: The reviews are tokenized into individual words or phrases to facilitate further analysis. (This step was later done with hepl of Vader model). <br>

# Exploratory Data Analysis (EDA)
EDA involves examining the dataset's structure and performing basic statistical analysis to gain insights into the data. <br>
Here I analyzed the distribution of ratings and visualize trends in reviews over time. <br>
Additionally, I explored nature of dataset using bar-graph , and found out majority of reviews are 5 star ie. positive. <br>

# The VADER Model for Sentiment Analysis
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool specifically designed for social media text. <br>
It's a part of the Natural Language Toolkit (NLTK) and widely used for quick and effective sentiment analysis. <br>
It is a rule-based sentiment analyzer in which the terms are generally labeled as per their semantic orientation as either positive or negative. <br>
This uses a "bag of words" approach: <br>
         Stop words are removed <br>
         Each word is scored and combined to a total score. <br>
VADER works by scoring text based on a pre-built dictionary that maps words to their sentiment scores. <br>
The sentiment scores provided by VADER include: <br>

1. Positive sentiment score: A score representing the proportion of positive words in the text. <br>
2. Negative sentiment score: A score representing the proportion of negative words in the text. <br>
3. Neutral sentiment score: A score representing the proportion of neutral words in the text.   <br>
4. Compound sentiment score: A single value representing the overall sentiment, ranging from -1 (most negative) to 1 (most positive). <br>
5. VADER is particularly useful for social media text as it can handle the informal and colloquial language commonly found in platforms like Twitter and Facebook. <br>

# The Roberta Pretrained Model
Roberta is a variant of the BERT (Bidirectional Encoder Representations from Transformers) model, which is a highly effective transformer-based model for various NLP tasks. <br>
Roberta improves upon BERT by employing a larger dataset and longer pretraining duration, leading to better language representation capabilities. <br>
Roberta, like BERT, utilizes a transformer architecture, which enables bidirectional context understanding, making it more powerful in capturing complex patterns in text data. It can be fine-tuned for specific tasks like sentiment analysis with high accuracy due to its extensive pretraining on a diverse range of language data.

# Implementing Sentiment Analysis with Vader and Roberta
To perform sentiment analysis, first utilize VADER for scoring the sentiment of each review in the Amazon Fine Food Reviews dataset. The VADER scores are then plotted to visualize the distribution of sentiments in the dataset.<br>

Next,  the Roberta petrained model was used to score the sentiment of the same reviews. <br>
The pretrained Roberta model was downloaded from Hugging Face's model hub which was trained on the Twitter comments dataset , so in way it is kind of a transfer learning. <br>
Ran the sentiment analysis on our Amazon Fine Food Reviews dataset. <br>

# Combining Results from Vader and Roberta
The results from VADER and Roberta are combined into a single dataframe named "results," which contains the sentiment scores for each review from both models. This  will allow the comparison between the sentiment scores generated by VADER and Roberta side by side.

# Analyzing and Comparing the Results
The final step of the project involves analyzing and comparing the results obtained from both VADER and Roberta models. <br>
Created visualizations to understand how well each model performs in capturing the sentiments expressed in the reviews.  <br>
By reviewing specific examples where the models disagree, we gain insights into the strengths and weaknesses of each approach. <br>

# Conclusion
This project, explored sentiment analysis on the Amazon Fine Food Reviews dataset using both the VADER model and the fine-tuned Roberta model. Through data preprocessing, EDA, and sentiment scoring, valuable insights were gained into the sentiments expressed in the reviews. By comparing the results from VADER and Roberta, the effectiveness of each model was understood in the context of this specific dataset. <br>

Sentiment analysis is a crucial NLP task with widespread applications in understanding customer feedback, brand perception, and market trends. The combination of rule-based approaches like VADER and state-of-the-art transformer models like Roberta can provide a comprehensive understanding of the sentiments expressed in textual data. <br>

Please refer to the Jupyter Notebook or Python script in this repository for detailed code implementations and visualizations related to this project. <br> 

# Extra 
In the end transformer piplelines were aloso used for sentiment analysis. <br>
The pipelines are a great and easy way to use models for inference. These pipelines are objects that abstract most of the complex code from the library, offering a simple API dedicated to several tasks, including Named Entity Recognition, Masked Language Modeling, Sentiment Analysis, Feature Extraction and Question Answering. <br>
Transfor piplelines automatically uses most suitable model available. <br>


# References
Amazon Fine Food Reviews Dataset <br>
VADER Sentiment Analysis Tool <br>
Roberta: A Robustly Optimized BERT Pretraining Approach <br>
