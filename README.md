# Sentiments-Analysis
# Sentiment Analysis of Customer Tweets: Gaining Competitive Insights for Google and Apple Products

## Business Undersstanding
### Background
Ensemble Africa is an independent consultancy firm that has been contacted by Google to carry out an analysis on customers' sentiments expressed in tweets by one of its major product competitor. Google, a leading technology company, aims to gain insights into their competitor, Apple, by analyzing customers' sentiments expressed in tweets.

The goal of this project is to develop a sentiment analysis model that accurately rates the sentiments of tweets about Apple products. By understanding the sentiments of customers' experiences, Google intends to gain a competitive advantage by identifying areas where they can improve their products or services, thereby enhancing customer satisfaction and loyalty.

The project has taken cognizance the adoption of exploratory data analysis. From the available data, we have undertaken to cleaning and using descriptive analysis we intend to provide resourceful explanatory analytics that Google can use to gain competitive advantage over Apple inc.

## Objectives
To build a specialized sentiment analysis model that can analyze twitter sentiments of google and apple products
To establish if there is any differences in twitter sentiments between apple and google product
To find out the inclusive sentiment view towards apple an google products from twitter
To investigate the recurring topics of interest associated with negative or positive sentiments as seen by google and apple brands

## Stakeholders
Our stakeholder is a marketting agency seeking to understand client product needs based on their twitter sentiments. The client's aim is to also offer consumer insights with regards to the positive and negative mentions of the Google and Apple products.

## Hypothesis
Null Hypothesis (H0): Our model's ability to accurately classify tweet sentiments between Google and Apple products is not significantly different from random chance.

Alternative Hypothesis (Ha): Our model's ability to accurately classify tweet sentiments between Google and Apple products is significantly better than random chance.

## Data Understanding
The dataset used in this project,sourced from https://data.world/crowdflower/brands-and-product-emotions, consists of 3 columns and 9093 rows. The columns include;

## The following observations were made;

The dataset contains a total of 9093 rows and 3 columns.

The columns are labeled 'tweet_text', 'emotion_in_tweet_is_directed_at', and 'is_there_an_emotion_directed_at_a_brand_or_product'.

The 'is_there_an_emotion_directed_at_a_brand_or_product' column has four unique values: 'No emotion toward brand or product', 'Positive emotion', 'Negative emotion', and "I can't tell".

The 'emotion_in_tweet_is_directed_at' column has nine unique values.

Null values are present in the 'tweet_text' and 'emotion_in_tweet_is_directed_at' columns. The 'tweet_text' column has one null value, and the 'emotion_in_tweet_is_directed_at' column has 5802 null values.

## Data Cleaning and Preparation
Column names were changed to enhance the dataset's readability, clarity, and user-friendliness. It contributes to smoother data analysis and facilitates sharing insights, as the new names accurately represent the content of the columns. There were a total of 46 duplicates that were erased. The following is the breakdown of the null values that were also erased; tweets (1), brand (5,786). We decided to drop the 'I can't tell' because we wanted to classify the sentiments in 'positive' , 'negative' and 'no emotion' as this will help us enhance the quality of our analysis.

## EDA

### Univariate
![image](https://github.com/kithinji007/Sentiments-Analysis/assets/128479803/0790ea1e-c914-465d-88d7-8b9215e2950f)
The distribution of the texts seem to be left skewed From above histogram, the tweets are comprised of around 29-160 characters

![image](https://github.com/kithinji007/Sentiments-Analysis/assets/128479803/72563985-0fba-48f6-9629-f02da7fa4f9e)

## Bivariate Analysis
Sentiment vs. Product To analyze how sentiment (positive, negative, neutral) varies across different products (Apple, Google) mentioned in the tweets. This can help you understand how customers perceive each company's products.

![image](https://github.com/kithinji007/Sentiments-Analysis/assets/128479803/5d6b68fe-dbaf-4e14-a7b1-a4fa9a38aebe)

From the visualiatin above, the product that recieved most tweets is google. The common trend is that most customers don't hold any emotion towards the product.

![image](https://github.com/kithinji007/Sentiments-Analysis/assets/128479803/5fc91610-eacc-4a63-9bc2-d06192177293)
From the box plots, we notice that most of the tweets whose lengths are longer hold negative sentiments. Also, the margine between the three sentiments is not too far apart. Therefore, it is safe to say that the length of the tweets is not enough to conclude on the customers' sentiments

## Pre-processing for NLP
### Tokenization, Stemmer, and Stopwords Objects
Here, we will preprocesses textual data by cleaning and tokenizing it, perform sentiment-based word frequency analysis, and presents the results using bar plots and word clouds. These visualizations help gain insights into the most common words associated with different sentiments in the tweets.

The pre-processing steps include:-

Converting it to lowercase, removing URLs, specific words ("mention," "link," "2," "rt"), punctuation, and filtering out common words(stopwords) that don't contribute much to the analysis.

![image](https://github.com/kithinji007/Sentiments-Analysis/assets/128479803/305d37a3-7f2d-41da-a167-a659139c8955)

## Modelling
In our sentiment analysis project, we explored the effectiveness of various machine learning models in categorizing text-based data into sentiment classes. We employed a range of models to capture the nuances of sentiment expressed in textual content. These models included:

### Naives Bayes
It's particularly suited for text classification tasks due to its simplicity and efficiency. Despite its "naive" assumption of independence between features, Naive Bayes can perform remarkably well on sentiment analysis tasks by capturing word occurrence patterns.

### Random Forest
This ensemble lesrning technique offers robustness against overfitting and the ability to capture complex interactions in the data. Also it is really good in handling both numerical and categorical features, making them suitable for text-based sentiment analysis.

### Support Vector Machine (SVM)
This powerful classification method that aims to find the optimal hyperplane that best separates data points of different classes. This will be great in text classification tasks like sentiment analysis to find the most discriminating features.

### Neural Networks
In sentiment analysis, neural networks have demonstrated their ability to capture contextual information and long-range dependencies in text. This will help automatically learn complex patterns and hierarchical representations from data.
Each of these models brings unique strengths to the task of sentiment analysis.

In order to start modeling we split the data into training and testing sets and vectorize our textual data into a format that machine learning algorithms can process.
