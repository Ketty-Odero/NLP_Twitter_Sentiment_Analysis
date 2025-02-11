This repository explores Natural Language processing by building a NLP Model to analyze twitter sentiments about Google Products.
## Introduction

## Data
Dataset was sourced from [data.world provided by CrowdFlower](https://data.world/crowdflower/brands-and-product-emotions) which contains 9,093 tweets about Apple and Google from the South by Southwest (SXSW) Conference. The tweet labels were crowdsourced and reflect which emotion they convey and what product/service/company this emotion is directed at based on the content.
## Methods

## Results
### Exploratory Data Analysis

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