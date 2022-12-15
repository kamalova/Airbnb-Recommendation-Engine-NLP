![](https://github.com/kamalova/Airbnb-Recommendation-Engine-NLP/blob/main/images/banner.png)
## **Airbnb Recommendation Engine for NYC through Sentiment Analysis**<p>
**Author: Nurgul Kurbanali kyzy**<p>
**Table of Contents**<p>
- [Overview and Business Statement](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#overview-and-business-statement)
- [Data Understanding](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#data-understanding)
- [Sentiment Analysis](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#sentiment-analysis)
- [Recommendation Engine](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#recommendation-engine)
- [Limitations and Future Consideration](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#limitations-and-future-consideration)
- [References](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#references)
- [For More Information](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP#for-more-information) 


### **Overview and Business Statement**
**About Airbnb (Air Bed and Breakfast)**: *You can host anything, anywhere, so guests can enjoy everything, everywhere.*<p>
Nowadays the demand for short and long-term temporary accommodation is increasing thanks to easing travel conditions. This demand positively affects the number of online platforms that allow you to make reservations before traveling. Airbnb is one such platform, which allows travelers to make accommodation reservations based on the fact that the host leases all or part of his or her home to the traveler.

Customer reviews play an important role in the customer’s decision to purchase a product or use a service. Customer preferences and opinions are affected by other customers’ reviews online, on blogs or over social networking platforms.
The main goal of this work is to combine both recommendation system with **Collaborative Filtering (CF)** and sentiment analysis in order to recommend the most accurate listings for Airbnb users based on their preferences in New York City. Since both domains suffer from the lack of labeled data, to overcome that, this project detects the opinions polarity score using **NLTK VADER** (Valence Aware Dictionary and Sentiment Reasoner) Lexicon.

Overall, the project went through the following sections:

- Exploring available **AirBnb** listings in **NYC**
- Measuring polarity/sentiment scores with the help of  vader_lexicon. This polarity measurement adapts to ***pos, neu, neg***, and ***compound***. By simply taking the compound from these values, a new feature was created on the data.
- Finally building a recommendation engine with **CF** to predict sentiment score for all reviewer-listing pairs and making personalised recommendations for each user based on their ranked preferences.

### **Data Understanding**
The dataset is obtained from [Inside Airbnb](http://insideairbnb.com/). It is is a mission driven project that provides data and advocacy about Airbnb's impact on residential communities. For the purpose of this project we downloaded the most recent quarterly datasets between December, 2021 - September, 2022 which includes information and metrics for ***listings and reviews*** in **NYC**. Datasets have been concatinated, preprosessed and some ***EDA*** techniques have been applied on.<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/nyc_map.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/amount_review.png)

### **Sentiment Analysis**
Prior to start my analysis I gave a brief information what is a **Sentiment Analysis(opinion mining)**. Further applied text pre-processing steps for each reviewer's comments (including language detection). Thanks to the NLTK's Vader lexicon I was able to calculate the compound polarity score  of each comment. The compound score is the sum of positive, negative & neutral scores which is then normalized between **-1(most extreme negative)** and **+1 (most extreme positive)**. <p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/sent_type.png)<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/pos_review.png)
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/neg_review.png)
### **Recommendation Engine**
In this section I ended up building a recommendation engine with **Collaborative Filtering(CF)** to predict sentiment score for all reviewer-listing pairs and make personalised recommendations for each user based on their ranked preferences. The **CF** method focuses on collecting and analyzing data on user behavior, activities, and preferences, to predict what a person will like, based on their similarity to other users.To plot and calculate these similarities, collaborative filtering uses a matrix style formula. An advantage of collaborative filtering is that it doesn’t need to analyze or understand the content (products, films, books). It simply picks items to recommend based on what they know about the user.<p>
**Grid Search Cross Validation** computed absolute measure of fits for an algorithm on various combinations of parameters, over a cross-validation procedure **SVD Algorithm**<p> Accuracy on Test set- ***RMSE: 0.1680***<p>
![](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/images/reccommend.png)


### **Limitations and Future Consideration**
The results show that our model outperforms  in terms of the root  mean squared errors of the generated predictions. I would suggest to try using  models which involve regularization like: *Matrix factorization using Alternating ( optimization algorithms) least squares. Matrix factorization using Bayesian Personalized ranking.*
Balancing dataset with state-of-the-art oversampling or under sampling techniques such as *SMOTE* during pre-processing. Applying clustering techniques like K-means or  Self-Organizing Map (SOM) also can lead to  more accurate results. In addistion the time factor can play an important role in providing effective personalized recommendations and consequently improving the accuracy of predictions.
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
or project  [presentation](https://github.com/kamalova/NYC-Airbnb-Recommendation-Engine-NLP/blob/main/presentation.pdf).<p>

For any additional questions, please contact Nurgul Kurbanali kyzy at nurkamalova@gmail.com <p>





