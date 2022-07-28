# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP
## Content
* Problem Statement
* EDA
* Preprocessing and Modeling
* Model Comparison
* Conclusion and Recommendations

## Problem Statement
---
There is an increase interest in Tolkien works recently due to the highly anticipated Lord of the Rings (LOTR) series coming up on September.
With that, LOTR fans are revisiting the two trilogy done by Peter Jackson: LOTR and The Hobbits. LOTR and Tolkien fans are discussing the works on Reddits and many other online discussion forums.
<br>

However, any Tolkien fans will know how extensive and in-depth Tolkien creation can be. Furthermore, characters can be in existence and involved through ages in Tolkien world.
<br>

Hence, the production team wants to help LOTR fans with differentiating the movies (LOTR and The Hobbits) online discussions. In that, LOTR fans will get the correct base knowledge required before the series is released.
<br>

_Note: Fans who only watched Percy Jackson movies are referred as LOTR fans in the statement above. While, hardcore Tolkien nerds who read the books are referred as Tolkien fans_

## EDA
---
Find the top common words in both dataset

<img src="./images/eda_bar_comparision.png" width="400"/>

Wordcloud

<img src="./images/wordcloud.png" width="400"/>

Putting my domain knowledge into practice, this word cloud is accurate. Characters like Aragon, Arwen and Elrond are very important in LOTR storyline.


## Preprocessing and Modeling
---
### Baseline model
LOTR = 0 has 0.508605 weightage in dataset
Hobbits = 1 has 0.491395 weightage in dataset

## Model and vectorizers
Piepeline and Grid search was used for modeling.
Two vectorizers are utilised: Count and TFID.
Four models for each vectorizers: Naive bayes, Logistics Regression, K Nearest Neighbours and Random Forest

| Vectorizer | Model         | Best score | Train score | Test Score | Accuracy | Specificity | Recall | Precision | F1 Score |
|------------|---------------|------------|-------------|------------|----------|-------------|--------|-----------|----------|
| NA         | Baseline      | 0.509      | 0.509       | 0.509      | 0.509    | 1.000       | 0.000  | 0.000     | 0.000    |
| Count      | Naive Bayes   | 0.701      | 0.798       | 0.703      | 0.703    | 0.758       | 0.647  | 0.721     | 0.682    |
| Count      | KNN           | 0.670      | 0.780       | 0.653      | 0.653    | 0.682       | 0.622  | 0.654     | 0.637    |
| Count      | Logistics Reg | 0.709      | 0.904       | 0.705      | 0.705    | 0.778       | 0.628  | 0.732     | 0.676    |
| Count      | Random Forest | 0.717      | 0.766       | 0.693      | 0.693    | 0.857       | 0.523  | 0.779     | 0.626    |
| TFID       | Naive Bayes   | 0.709      | 0.875       | **0.715**  | 0.715    | 0.746       | 0.683  | 0.722     | 0.702    |
| TFID       | KNN           | 0.585      | 0.730       | 0.607      | 0.607    | 0.685       | 0.526  | 0.617     | 0.568    |
| TFID       | Logistics Reg | **0.723**  | 0.868       | **0.714**  | 0.714    | 0.787       | 0.637  | 0.743     | 0.686    |
| TFID       | Random Forest | 0.714      | 0.769       | 0.693      | 0.693    | 0.857       | 0.523  | 0.779     | 0.626    |

**Observations from the table above:**
* The dataset has a balanced distribution between the 2 topic with ~51% belonging to LOTR and ~49% belonging to hobbit.
* Hence, accuracy score will be used mainly for determining the model performance instead of the F1 score.
* The best accuracy scores from the table above are models using **TFID vectorizer**.
* Naive Bayes and Logistics Regression model scored best with 0.715 and 0.714 respectively.
* Comparing the two models, **I've decided to chose Logistics Regression** instead of Naive Bayes. This is because the Best score for Logistics Regression is better than Naives Bayes (0.723 > 0.709)
* There is lesser of an overfit for Logistics Regression as well.
* The other models performing badly with accuracy under 0.70.


## Conclusion and Recommendation
---
**Conclusion**
<br>
Based on the results and findings, fans should use the TFID Vectorizer, Logistic Regression model to differentiate if the post is related to LOTR or The Hobbits. 
<br>
The main characters in the movie are important to differentiate between the movies. Dwarf characters such as Thorin, Bombur are prominent in The Hobbits movie as well as in the online discussions. 
<br>
While, LOTR discussions are mainly about the foes (black riders, eye, morgoth). 
<br>
Characters such as bilbo, gandalf are in existence in both movies. Hence, it is best for the production team to state that clearly during fans meet and greet session / conference to clear the confusion. 
<br>

**Recommendation**
<br>
Recommend the production team to work with YouTubers who specialize in recaps / Tolkien works. In order to provide bite sized videos on the background for LOTR fans before the upcoming series.
<br>
Also, recommend the production team to work with streaming platform (mainly Amazon Prime) to stream LOTR and the Hobbits trilogy. 
<br>
It would be recommended to have the uncut version on streaming platform. Then, the fans will get more details and clearer idea on the events.
<br>
Future work will recommend for the production team to use other online discussion forums to gather data.