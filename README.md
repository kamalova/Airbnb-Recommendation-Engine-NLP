![](https://github.com/kamalova/Airbnb-Recommendation-Engine-NLP/blob/main/images/banner.png)
## **Airbnb Recommendation Engine for NYC through Sentiment Analysis**<p>
**Author: Nurgul Kurbanali kyzy**<p>
**Table of Contents**<p>
- [Overview and Business Statement]()
- [Data Understanding]()
- [Sentiment Analysis]()
- [Recommendation Engine]()
- [Limitations and Future Consideration]()
- [References]()
- [For More Information]() 


### **Overview and Business Statement**
**About Airbnb**: *You can host anything, anywhere, so guests can enjoy everything, everywhere.*<p>
Nowadays the demand for short and long-term temporary accommodation is increasing thanks to easing travel conditions. This demand positively affects the number of online platforms that allow you to make reservations before traveling. Airbnb is one such platform, which allows travelers to make accommodation reservations based on the fact that the host leases all or part of his or her home to the traveler.

Customer reviews play an important role in the customer’s decision to purchase a product or use a service. Customer preferences and opinions are affected by other customers’ reviews online, on blogs or over social networking platforms.
The main goal of this work is to combine both recommendation system with **Collaborative Filtering (CF)** and sentiment analysis in order to recommend the most accurate listings for users based on their preferences in New York City. Since both domains suffer from the lack of labeled data, to overcome that, this project detects the opinions polarity score using **NLTK VADER** (Valence Aware Dictionary and Sentiment Reasoner) Lexicon.

Overall, the project went through the following sections:

- Exploring available **AirBnb** listings in **NYC**
- Measuring polarity/sentiment scores along with vader_lexicon. This polarity measurement adapts to ***pos, neu, neg***, and ***compound***. By simply taking the compound from these values, a new feature was created on the data.
- Finally building a recommendation engine with **CF** to predict sentiment score for all reviewer-listing pairs and making personalised recommendations for each user based on their ranked preferences.

### **Data Understanding**
The dataset is obtained from [Inside Airbnb](http://insideairbnb.com/). It is is a mission driven project that provides data and advocacy about Airbnb's impact on residential communities. For the purpose of this project we downloaded the most recent quarterly datasets between December, 2021 - September, 2022 which includes information and metrics for ***listings and reviews*** in **NYC**. Datasets have been concatinated, preprosessed and some ***EDA*** techniques have been applied on.<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/nyc_map.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/amount_review.png)

### **Sentiment Analysis**
Prior to start my analysis I gave a brief information what is a **Sentiment Analysis(opinion mining)**. Further applied text pre-processing steps for each reviewer's comments (including language detection). Thanks to the NLTK's Vader lexicon I was able to calculate the compound polarity of each comment.<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/sent_type.png)<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/pos_review.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/neg_review.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/dist_polarity.png)
### **Recommendation Engine**
In this section I ended up building a recommendation engine with Collaborative Filtering to predict sentiment score for all reviewer-listing pairs and make personalised recommendations for each user based on their ranked preferences.<p>
**Grid Search Cross Validation** computed accuracy metrics for an algorithm on various combinations of parameters, over a cross-validation procedure **SVD Algorithm**<p> Accuracy on Test set- ***RMSE: 0.1629***<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/actual_vs_pred.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/result.png)

### **Limitations and Future Consideration**
Most of the existing approaches in sentiment-based recommender systems apply traditional recommendation techniques that lack of semantics information which lead to the major data sparsity and domain sensitivity problems. Hence, few have suggested the needs to consider domain sensitivity information in order to produce better sentiment accuracy and help to overcome data sparsity problem . However, the extent of how potential domain sensitivity information can improve the quality of recommendation still remains a question. Since most of the sentiments were positicve reviews we had an issue of the imbalanced data. To boost models performance we suggest to get more negative reviews as well and try anothoer common unsupervised learning algorithms.
### **References**
[Comprehensive Guide to build a Recommendation Engine from scratch (in Python)](https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-recommendation-engine-python/)<p>
[Sentiment Analysis: A Definitive Guide](https://monkeylearn.com/sentiment-analysis/)<p>
[Integrating contextual sentiment analysis in collaborative recommender systems](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0248695#:~:text=Sentiment%20analysis%20is%20relatively%20a,be%20processed%20by%20CF%20algorithm.)
### **For More Information**
You can review my full analysis in my **Jupyter Notebooks**: 
- [Listings Exploratory Data Analysis
](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/notebooks/Listings_EDA.ipynb),
- [Review Based Sentiment Analysis](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/notebooks/Sentiment_Analysis.ipynb)
- [Recommendation Engine](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/notebooks/Recommendation_Engine.ipynb) <p>
or Project  presentation.<p>

For any additional questions, please contact Nurgul Kurbanali kyzy at nurkamalova@gmail.com

**Repository Structure**
