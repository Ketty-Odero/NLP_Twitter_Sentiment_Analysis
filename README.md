This repository explores Natural Language processing by building a NLP Model to analyze twitter sentiments about Google Products.

## Introduction
In today's hyper-connected world, social media is a critical tool for shaping brand perception and understanding public opinion. Millions of users share their thoughts on platforms like Twitter, making it a valuable resource for companies like Google to gather insights, adapt to trends, and make data-driven decisions.

As a hired Brand Strategist, I have been tasked with conducting a sentiment analysis of tweets from the SXSW Conference to provide actionable insights that will guide Google's brand positioning and product strategy

## Data
Dataset was sourced from [data.world provided by CrowdFlower](https://data.world/crowdflower/brands-and-product-emotions) which contains 9,093 tweets about Apple and Google from the South by Southwest (SXSW) Conference. The tweet labels were crowdsourced and reflect which emotion they convey and what product/service/company this emotion is directed at based on the content.
## Methods
We started with data cleaning and exploring the dataset to have a grasp of the features it contained.Data was cleaned(duplicates and missing values handled) and sentiments labels simplified to "Positive", "Neutral" and "Negative" before Exploratory Data Analysis (EDA).

In the EDA, we looked at tweets with positive and negative sentiments as a whole as well as on a company and product level. Wordclouds were generated for each analysis. To be able to produce these graphics the tweets were tokenized with nltk's TweetTokenizer since it has built-in functionality for tweets specifically, lemmatized with the WordNetLemmatizer and stop words were removed from these tokens. We customized stop words to get a better view of the content of the tweets for addressing the questions.

Modelling process was split in two: Binary Classification and Ternary Classification. For each type of classification, data was prepared and a baseline dummy classifier model was trained to serve as a baseline. For comparison we trained/tested Random Forest models and Logistic Regression models for Multiclass Classification while for Binary classification we explored Multinomial Naive Bayes and Logistic Regression.

Models were evaluated  and tuned hyperparameters with gridsearches that optimized for the recall macro scores, as we desired that the models correctly classify all classes. These steps were repeated with different parameters

## Results

### Binary Classification

### Ternary Classification

## Conclusions 

Our analysis of tweets from the SXSW Conference revealed the following key findings:

**1. How is Google perceived as a company during the SXSW Conference, and how does this compare to Apple?**
- 82% of all tweets related to Google were positive, slightly higher than Apple’s 81.1%.
- Negative sentiment for Google was 14.9%, lower than Apple’s 16.1%, suggesting Google had a slightly stronger overall brand perception during the event.
These results indicate that both Google and Apple are generally well-received during the SXSW Conference, with Google having a slight edge in positive sentiment and fewer negative mentions.

**2. How were Google and Apple's products and announcements perceived during the SXSW Conference? Are there specific pain points within Google's products that need attention?**

**Google - Positive Highlights:**

- Google’s party at Lustre Pearl created significant buzz, reinforcing Google’s ability to engage users beyond tech.
- Marissa Mayer's presence at SXSW generated positive discussions, indicating the influence of key executives on brand sentiment.
- Excitement around Google's new social network, "Circle," suggests strong anticipation for the product’s potential.
- Microsoft Bing was frequently mentioned in a negative light, reinforcing Google's dominance in search.

**Google - Areas for Improvement:**
- Android OS issues were widely discussed, with mentions of words like “buggy,” “replaced,” and “painful.” This indicates user dissatisfaction and potential areas for system optimization.
- Samsung was frequently mentioned in connection with Android, suggesting that some users might prefer Samsung’s Android experience over Google’s own offerings. Google may need to focus on differentiating its first-party Android devices.
- Meetup users reported compatibility problems on Android, highlighting the need for better third-party app support and system stability.

## Recommendations

- Enhance Android OS Stability & User Experience
- Strengthen Brand Differentiation from Competitors
- Capitalize on Social & Experiential Marketing
- Leverage Real-Time Sentiment Analysis for Competitive Edge**


## Limitations and Next Steps

**Dataset limitations**

- Subjectivity in Labeling: Sentiment classification is highly subjective, which may lead to potential mislabeling during crowdsourced labelling tasks
- Limited Data Size: The dataset contained only 9,093 tweets, and after removing neutral tweets, only ~3,000 were available for binary classification. 
- Class Imbalance: 61% Neutral, 33% Positive, 6% Negative as distribution for sentiments labels. Negative class was  very crucial for identifying areas of improvement but it was very underepresented.

**Next steps**
- Gather more data from Twitter & other sources to improve model generalization
-  Define clear criteria for sentiment classification to reduce labeling inconsistencies
- Improve model performance by exploring other sadvanced models and parameters and incorporating Neural Networks for better text classification


### Repository Structure

```
├── README.md               <- The top-level README for reviewers of this project.
├── index.ipynb             <- Narrative documentation of analysis in jupyter notebook
├── notebook.pdf            <- Narrative documentation of analysis in PDF
├── presentation.pdf        <- PDF version of project presentation
├── images                  <- Both sourced externally and generated from code
└── data                    <- Externally sourced data