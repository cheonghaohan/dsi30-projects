
# Project 1: Standardized Test Analysis

### Problem Statement
The new format for the SAT was released in March 2016. As an employee of the College Board, my team tracks statewide participation and recommends where money is best spent to improve SAT participation rates. This project will be using the provided data and outside research to make recommendations about how the College Board might work to increase the participation rate in a state or states.

**Contents:**
* Background
* Research findings
* Findings from Datasets
* Conclusions
* Recommendations


### Background
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

Marks range for the respective tests:
* SAT marks range: 0 - 1600
* ACT marks range: 1 - 36


### Research findings:

**1. Best practices to increase SAT participation**
* SAT School Day
* Covering exam fees for students (partially or full)
* Creating a college is for all culture
<br>

<font size="4">**SAT School Day**</font>
SAT School Day is an initiative that allow students to take the SAT test during school day. In that, students with outside school commitments on weekends have a better chance to take the SAT. The availability of SAT School Day is determined by schools and districts. Some SAT School Day provides the SAT for free as well. 

<font size="4">**Covering exam fees for students**</font>
SAT provides fee waivers to low‐income students from the 11th and 12th grade in the U.S. The fee waivers includes registration fees, cancellation fees, change fees and regional fees. There are 2 free SAT tests and 2 changes to access answer services.
Sources from College Board.
[source](http://sat.collegeboard.org/register/sat‐fee‐waivers)
[source](http://sat.collegeboard.org/SAT/public/pdf/counselors‐guide‐to‐sat‐program‐fee‐waivers.pdf)

<font size="4">**Creating a college is for all culture**</font>
Students also indicated that the counselor is one of the most important influences for participating in the SAT tests. Having the school to adopt a culture that advocate attending college do help in increasing participation as well. 
<br>
**2. Sentiments towards college admissions**
The below are pointers taken from a report by CNBC on the college admissions process.([source](https://www.cnbc.com/2019/03/20/under-20percent-of-americans-think-the-college-admissions-process-is-fair.html))
According to a USA TODAY/Suffolk University Poll of 1,000 registered voters conducted:
* Fewer than one in five Americans believe the college admissions process is “generally fair.”
* About 67 percent of respondents said that the current college application and admissions process “favors the rich and powerful.”

Researchers have repeatedly found that wealthy students do enjoy significant advantages in the college admissions process.

Wealthy students are more likely to have access to tutors, more likely to have taken standardized test preparation classes and more likely to have taken standardized tests like the SAT more than once.
<br>


**3. Other reasons why states are switching from ACT to SAT**  ([source](https://www.coloradokids.org/wp-content/uploads/2016/01/ACTvsSAT_FINAL.pdf))

* New SAT format is aligned to the Common Core standards in English and Math.
* It also measures the skills and knowledge that is critical for college readiness.
* The College Board partnered with Khan Academy to provide free, personalized test prep for any student with computer access.

<br>

### Findings from Datasets

**Datasets used:** 

* sat_2017.csv 
* sat_2018.csv 
* sat_2019.csv
* act_2017.csv
* act_2018.csv 
* act_2019.csv

**Data dictionary**
|Feature|Type|Dataset|Description|
|---|---|---|---|
| state                              | object  | ACT/SAT  | The states of America
| suffix                             | String  | ACT/SAT  | Indicates the year: 2017, 2018, 2019
| sat_participation                  | float   | SAT      | The percentage of students in the state who have taken the SAT
| ebrw                               | int     | SAT      | evidence-based_reading_and_writing  average mark for the state (Marks range: 200 - 800)
| math                               | int     | SAT      | Math average mark for the state (Marks range: 200 - 800)                            
| total                              | int     | SAT      | This is the average total SAT mark for the state (Marks range: 400 - 1600)
| act_participation                  | int     | ACT      | The percentage of students in the state who have taken the ACT
| composite                          | float   | ACT      | This is the average total ACT mark for the state (Marks range: 1 - 36)

**Data Findings**

1) **State(s) with the lowest SAT and ACT participation rate**

_**2017 Data**_
State(s) with lowest SAT participation rate 2017 (at 2%):
(3 states)
* Iowa
* Mississippi
* North Dakota

State(s) with lowest ACT participation rate 2017 (at 8%):
(1 state)

* Maine

_**2018 Data**_
State(s) with lowest SAT participation rate 2018 (at 2%):
(1 state)

* Iowa
* Mississippi
* North Dakota

State(s) with lowest ACT participation rate 2018 (at 7%):
(1 state)

* Maine

_**2019 Data**_
State(s) with lowest SAT participation rate 2019 (at 2%):
(1 state)

* North Dakota
State(s) with lowest ACT participation rate 2019 (at 6%):
(1 state)

* Maine

**Findings for states with SAT ACT lowest participation rate**
Based on the result above, lowest SAT participation rate maintains at 2% from 2017 to 2019. While, lowest ACT participation rate drops from 8% in 2017 to 6% in 2019

The number of states with 2% SAT participation rate drops as well from 3 in 2017 to 1 in 2018 and 2019.

North Dakota and Maine are the consistent state with lowest participation rate for SAT and ACT respectively.
<br>
2. **State(s) with the highest SAT and ACT participation rate**

_**2017 Data**_
State(s) with highest SAT participation rate 2017 (at 100%):
(4 states)

* Delaware
* Michigan
* Connecticut
* District of Columbia

State(s) with highest ACT participation rate 2017 (at 100%):
(17 states)

* Alabama
* Utah
* Tennessee
* South Carolina
* Oklahoma
* North Carolina
* Nevada
* Montana
* Mississippi
* Wisconsin
* Minnesota
* Louisiana
* Kentucky
* Colorado
* Arkansas
* Missouri
* Wyoming

_**2018 Data**_
State(s) with highest SAT participation rate 2018 (at 100%):
(5 states)

* Delaware
* Michigan
* Connecticut
* ~~District of Columbia~~
* Colorado
*  Idaho

State(s) with highest ACT participation rate 2018 (at 100%):
(17 states)

* Alabama
* Utah
* Tennessee
* South Carolina
* Oklahoma
* North Carolina
* Nevada
* Montana
* Mississippi
* Wisconsin
* Minnesota
* Louisiana
* Kentucky
* Colorado
* Arkansas
* Missouri
* Wyoming
* Nebraska
* Ohio

_**2019 Data**_
State(s) with highest SAT participation rate 2019 (at 100%):
(8 states)

* Delaware
* Michigan
* Connecticut
* Colorado
* Idaho
* Rhode Island
* Florida
* Illinois

State(s) with highest ACT participation rate 2018 (at 100%):
(15 states)

* Alabama
* Utah
* Tennessee
* South Carolina
* Oklahoma
* North Carolina
* Nevada
* Montana
* Mississippi
* Wisconsin
* Louisiana
* Kentucky
* Arkansas
* Missouri
* Wyoming
* Nebraska
* Ohio

**Findings for states with SAT ACT highest participation rate**
Based on the result above, both highest SAT and ACT participation rates are 100% from 2017 to 2019.
The number of states with 100% SAT participation rate increases from 4 in 2017 to 8 in 2019.
The number of states with 100% ACT participation rate decreases from 17 in 2017 to 15 in 2019.

_Interesting finding:_
In 2018, Colorado changed from 100% ACT participation rate to 100% SAT participation rate.
<br>

3. **States with lowest and highest SAT total mean**

States with the lowest mean total scores for the 2017, 2018 and 2019 SAT respectively:
* District of Columbia
* District of Columbia
* West Virginia
<br>

States with the highest mean total scores for the 2017, 2018 and 2019 SAT :
* Minnesota

**Findings for states with highest SAT total mean**
Based on the result above, the state with the highest SAT total mean from 2017 to 2019 is Minnesota
While, the state with the lowest SAT total mean is District of Columbia from 2017 to 2018. In 2019, West Virginia beats District of Columbia to be the state with lowest SAT total mean.

_Interesting finding:_
In 2017, District of Columbia has a 100% SAT participation rate and lowest SAT total mean.
In 2019, District of Columbia does not have a 100% SAT participation rate and lowest SAT total mean.
<br>

4. **State(s) with the lowest and highest ACT composite mean**

State with the lowest mean composite scores for the 2017, 2018 and 2019 ACT :
* Nevada

States with the highest mean composite scores for the 2017, 2018 and 2019 ACT respectively:
* New Hampshire
* Connecticut
* Connecticut

**Findings for states with highest and lowest ACT composite mean**
Based on the result above, the state with the lowest ACT composite mean from 2017 to 2019 is Nevada
While, the state with the highest ACT composite mean is New Hampshire in 2017. In 2018, Connecticut beats New Hampshire to be the state with highest ACT composite mean and stays till 2019.

_Interesting findings:_
Nevada has a 100% ACT participation rate and lowest ACT composite mean from 2017 to 2019.
Connecticut has a 100% SAT participation rate and highest ACT composite composite mean from 2018 to 2019.


State(s) with highest SAT participation rate in 2017

Connecticut, Delaware and Michigan have a 100% SAT participation rate from 2017 till 2019. Thus, there is 0 yoy rate growth for these 3 years.
District of Columbia has a 100% SAT participation rate in 2017 and drop to 92% in 2018 before rising to 94% in 2019.
<br>

5. **Growth rate YOY for states with 100% SAT participation rate** 

* State(s) with highest SAT participation rate in 2019
* Connecticut, Delaware and Michigan have a 100% SAT participation rate from 2017 till 2019. Thus, there is 0 yoy rate growth for these 3 years.
* Illinois has the highest yoy growth rate (1000%) from 2017 to 2018, followed by Colorado (809%).
<br>

6. **State(s) with >50% participation on both tests from 2017 to 2019**

* Florida and Hawaii have more than 50% for SAT and ACT participation rate from 2017 t0 2019.
* Georgia have more than 50% for SAT and ACT participation rate from 2017 to 2018.
* North Carolina and South Carolina have more than 50% for SAT and ACT participation rate from 2018 to 2019.
<br>

7. **Interpretation from graphs plotted using the datasets**

**Findings from the Heatmap:**
* The correlation for SAT participation and ACT participation is negative correlated (-0.79 to -0.87)
* The correlation for SAT participation in one year to another year is positively correlated (0.84 to 0.95)
* The correlation for ACT participation in one year to another year is positively correlated (0.9 to 0.99)
* The correlation for SAT participation to the SAT total is negatively correlated (-0.79 to -0.87)
* The correlation for ACT participation to the ACT composite is negatively correlated (-0.86 to -0.87)

**Findings from the Scatter Plot:**
* The correlation for SAT participation and ACT participation is a strong negative correlation
* There are a number of outliers with high SAT and ACT participation rate from 2017 to 2019

**Findings from the Box Plot:**
* The boxplot for SAT and ACT participation is getting longer as the year passes
* The median participation for SAT and ACT gets closer as the year passes
* In 2017 and 2018, ACT has a higher median participation than SAT. However, in 2019, SAT median participation closes up to ACT.

**Findings from the Line Plot:**
* The SAT average participation is increasing as the year passes
* The SAT participation growth rate from 2018 to 2019 slowed down compared to the growth rate from 2017 to 2018.

**Findings from the Histogram:**
* There is an obvious increase in the number of states having 80% to 100% SAT participation rate from 2017 to 2019
* Likewise, an obvious drop in the number of states having 0% to 10% SAT participation rate from 2017 to 2019
* The median has been steadily increasing over the 3 years and passes the mean in 2019
<br>
### Conclusions and Recommendations
Based on your exploration of the data, what are you key takeaways and recommendations? Make sure to answer your question of interest or address your problem statement here.

**Conclusion**
Based on the data and graphs plotted above, the SAT participation rate has been growing since the redesigned SAT format was released in 2016. However, the growth from 2018 to 2019 slowed down compared to the growth from 2017 to 2018. 

There is a strong negative correlation between SAT participation and ACT participation. Hence, for most of the states, if the SAT participation is high, the ACT participation will be low. 

The participation for one year to the next is a strong positive correlation. Therefore, there is a good chance of having states sticking with their preferred tests if there is one. One significant case where the state switched from 100% ACT participation to 100% SAT participation is Colorado. Using Colorado as the use case for researching on the cause for switch, it is found that the redesigned SAT format is aligned to the Common Core standards in English and Math. It also measures the skills and knowledge that is critical for college readiness. 

Costs of the tests are also great influence to the test participation rates. With SAT offering fee waivers to low income students, and collaborating with states / schools for SAT School Day, the participation rates for SAT increases greatly.
<br>
**Recommendations**
There are 3 approaches to increase SAT participation rate. The 3 approaches are arranged in order of priority with the highest as the first approach stated below:

1. **Target poorer states with “No fees and All free” slogan**
Poorer states such as New Mexico, Kansas and Iowa will appeal more towards the low cost benefits. 
The easiest target among the three will be New Mexico. The state is the poorest of the three and have the lowest ACT participation rate of 63% with the SAT participation rate stands at 18%. <br>
It will be strongly recommended for College Board to target these 3 states, mainly New Mexico. The approach to increase the SAT participation rate will be to working with the states on having SAT School Day that provides fee waivers for those eligible. To promote the preparation for SAT tests, the College board can also advertise on their free prep course by Khan Academy. Having lower opportunity costs and actual costs to taking SAT, the 3 states will be inclined to advocate SAT more than ACT.
<br>

2. **Target states without 100% participation rates for either of the tests**
The 5 states are Hawaii, North Carolina, South Carolina, South Dakota and Missouri. South Dakota does not have ACT requirement or having ACT offered for free in their state. <br>
The other 4 have ACT requirements but the participation rate is not 100%. This speaks volume in the trust the states or even the students have in ACT tests as the standard. In that, College Board can take this opportunity and pitch the redesigned format to the states on how it aligned with the Common Core standards in English and Math. Addtionally, the Board can also pitch new format also measures the skills and knowledge that is critical for college readiness. 
<br>

3. **Replicate Colorado strategy**
This will be the hardest states to tackle compared to the states recommended earlier. The 3 states here are Oklahoma, Ohio and Nevada. The ACT tests requirement is compulsory in the Ohio and Nevada, while, it is not for Oklahoma. <br>
The sliver lining in these states is that the SAT participation rate is also high at around 20% compared with other states with 100% ACT participation rate. With the 2016 newly revised SAT format bringing SAT and ACT tests format even closer, students can now easily prepare for both tests since the differences are at its minimal. Adopt the same pitch that was done to switch Colorado over to SAT and place it on these 3 states. Other states that have followed Colorado are: Connecticut, Michigan, Oregon and Illinois.
<br>

In summary, with the postive outlook from the 2016 redesigned format of SAT. Putting the 3 recommendations above in place will help College Board to further established itself in USA as the most taken tests for college admission.

[Source on states with compulsory ACT and SAT](https://testive.com/state-sat-act/)
[Source on Illinois switching to SAT](https://www.chicagotribune.com/news/ct-illinois-chooses-sat-met-20160211-story.html)
[Source on Michigan switching to SAT](https://www.freep.com/story/news/local/michigan/2015/01/07/michigan-replaces-act-sat/21385299/)
[Source on Connecticut switching to SAT](https://www.nytimes.com/2015/08/07/nyregion/connecticut-to-require-all-11th-graders-to-take-the-sat.html)
[Source on states outlook](https://www.richstatespoorstates.org/)
[Source on states outlook](https://www.thebalance.com/which-states-have-the-best-economies-3980690)