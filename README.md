研究系統是不是隨機推薦影片給使用者還是根據喜好 What is a recommendation system 1.1 Recommendation system tasks
The task of the recommendation system is to connect users and information, on the one hand, to help users find valuable information for themselves, and on the other hand to allow information to be displayed to users who are interested in it, to achieve a win-win situation for information consumers and information producers (as shown in Figure 1–1). (In the following part of this book, information will be collectively referred to as “items”, that is, things that can be consumed by users.)

1545116579930

Figure 1–1 The basic task of the recommendation system is to connect users and items and solve the problem of information overload

The recommendation system discovers user behavior and finds the user’s personalized needs, to accurately recommend long-tail products to users who need them, and help users find those products that they are interested in but difficult to find.

1.2 Recommendation system methods
Social recommendation (social recommendation)
Content-based recommendation (content_based filtering)
Based on collaborative filtering (collaborative filtering)
1.3 What is a recommendation system
The current recommendation system is a tool that automatically connects users and items. It can help users find information that interests them in an environment of information overload and can also push information to users who are interested in them.

2. Application of a personalized recommendation system
The application of recommendation systems can be seen in various websites on the Internet, and the main role of personalized recommendation systems in these websites is to provide different personalized page displays to different users by analyzing a large number of user behaviour logs, to improve the click-through rate and conversion rate of the website.

Although different websites use different recommendation system technologies, in general, almost all recommendation system applications are composed of three parts: the front-end display page, the back-end log system and the recommendation algorithm system.

E-commerce

Taking Amazon as an example, Amazon’s recommendation system is deeply integrated into its various products, among which the most important applications are personalized product recommendation lists and related product recommendation lists.

The personalized product recommendation list adopts an item-based recommendation algorithm (item-based method) and a friend-based personalized recommendation algorithm.

Movie and video websites

Taking Netflix and YouTube as examples, both mainly use item-based recommendation algorithms (2012 data)

Personalized music network radio

Pandora uses a content-based recommendation algorithm to feature songs and recommend similar songs based on the features;

Last.fm uses a user-based recommendation algorithm to recommend songs that other users with similar listening preferences like her.

Social networks

Personalized reading

Location-based services

Personalized emails

Personalized advertising

Personalized advertising has now become an independent discipline — computational advertising — but this discipline and recommendation systems are similar in many basic theories and methods, such as their purpose is to connect users and items, but in personalized advertising, the items are advertisements.

The difference between personalized advertising and narrow personalized recommendations is that personalized recommendations focus on helping users find items that may interest them, while advertising recommendations focus on helping advertisements find users who may be interested in them, that is, one is user-centric and the other is advertising-centric. There are currently three main types of personalized advertising technologies.

Contextual advertising By analyzing the content of the web page the user is browsing, ads related to the web page content are placed. The representative system is Google’s Adsense.
Search advertising By analyzing the user’s search history in the current session, the user’s search purpose is determined, and ads related to the user’s purpose are placed.
Personalized display advertising We often see a large number of display ads (those large banner images) on many websites. They are based on the user’s interests and different display ads are placed to different users. Yahoo is a representative of research in this area.
Necessary conditions for the successful application of personalized recommendations

The first is information overload, because if users can easily find the items they like from all the items, there is no need for personalized recommendations.

The second is that users do not have particularly clear needs most of the time, because if users have clear needs, they can directly find the items of interest through search engines.

3. Recommendation system evaluation
A complete recommendation system generally has three participants (as shown in Figure 1–22): users, item providers, and websites that provide recommendation systems.

1545120635995

Figure 1–22 Participants in the recommendation system

Prediction accuracy is an important indicator in the field of recommendation systems (no one else).

The advantage of this indicator is that it can be easily calculated offline, which makes it easier for researchers to quickly evaluate and select different recommendation algorithms. However, many studies have shown that accurate predictions do not mean good recommendations.

A good recommendation system can not only accurately predict user behavior, but also expand the user’s horizons and help users find things that they may be interested in but are not so easy to find. At the same time, the recommendation system should also be able to help merchants introduce good products buried in the long tail to users who may be interested in them.

To comprehensively evaluate the impact of the recommendation system on the interests of the three parties, this chapter will propose different indicators from different perspectives. These indicators include accuracy, coverage, novelty, surprise, trust, transparency, etc. Some of these indicators can be calculated offline, some can only be calculated online, and some can only be obtained through user questionnaires.

3.1 Experimental methods for recommendation systems
In recommendation systems, there are three main experimental methods for evaluating recommendation effects, namely offline experiments, user studies, and online experiments. The advantages and disadvantages of these three experimental methods are introduced below.

Offline experiments The offline experiment method generally consists of the following steps: (1) Obtain user behaviour data through the log system and generate a standard data set in a certain format; (2) Divide the data set into a training set and a test set according to certain rules; (3) Train the user interest model on the training set and make predictions on the test set; (4) Use pre-defined offline indicators to evaluate the prediction results of the algorithm on the test set.
Advantages Disadvantages
No need to have control over the actual system Unable to calculate indicators of commercial concern
No need for users to participate in the experiment There is a gap between the indicators of offline experiments and commercial indicators
Fast speed, can test a large number of algorithms

User survey

Reasons for user survey:

Note that there is a gap between the indicators of offline experiments and actual business indicators. For example, there is a big difference between prediction accuracy and user satisfaction. High prediction accuracy does not mean high user satisfaction. Therefore, if you want to accurately evaluate an algorithm, you need a relatively real environment. The best way is to test the algorithm directly online, but if you are not sure whether the algorithm will reduce user satisfaction, online testing has a higher risk, so a test called user survey is generally required before online testing.

User survey method:

User survey requires some real users to complete some tasks on the recommendation system to be tested. When they complete the task, we need to observe and record their behavior and ask them to answer some questions. Finally, we need to understand the performance of the test system by analyzing their behavior and answers.

Advantages and disadvantages of user surveys:

Advantages: Many indicators that reflect the user’s subjective feelings can be obtained, and the risk is very low compared to online experiments. It is easy to make up for errors;

Disadvantages: Recruiting test users is costly, and it is difficult to organize large-scale test users, so the statistical significance of the test results is insufficient; in many cases, it is very difficult to design double-blind experiments, and the behavior of users in the test environment may be different from that in the real environment, so the test indicators collected in the test environment may not be reproduced in the real environment.

Online experiments

After completing offline experiments and necessary user surveys, the recommendation system can be put online for AB testing and compared with the old algorithm.

AB testing method:

**AB testing is a very common experimental method for online evaluation algorithms. **It randomly divides users into several groups according to certain rules, and uses different algorithms for users in different groups, and then compares different algorithms by counting various evaluation indicators of users in different groups, such as counting the click-through rate of users in different groups, and comparing the performance of different algorithms by the click-through rate.

Advantages and disadvantages of AB testing:

The advantage of AB testing is that it can fairly obtain the performance indicators of different algorithms when they are actually online, including indicators of commercial concern. The main disadvantage of AB testing is that the cycle is relatively long, and long-term experiments must be conducted to obtain reliable results. Therefore, AB testing is generally not used to test all algorithms, but only to test those algorithms that perform well in offline experiments and user surveys.

**Secondly, the design of an AB testing system for a large website is also a complex project. **The architecture of a large website is divided into the front-end and the back-end. From the interface displayed to the user on the front end to the algorithm at the end, there are often many layers in the middle. These layers are often controlled by different teams, and they may all be AB tested. If AB testing systems are designed for different layers, different AB tests will often interfere with each other. For example, when we conduct an AB test of a background recommendation algorithm, and the web team is doing an AB test of the interface of the recommendation page, the final result is that you don’t know whether the test result is caused by changes in your own algorithm or changes in the recommendation interface.

Therefore, splitting traffic is the key in AB testing. Different layers and the teams that control these layers need to obtain their own AB test traffic from a unified place, and the traffic between different layers should be orthogonal.

AB testing system process:

Figure 1–23 is a simple AB testing system.

After the user enters the website, the traffic distribution system determines whether the user needs to be subjected to AB testing. If necessary, the traffic distribution system will label the user with the group he belongs to in the test.
**Then the user browses the web page, and the user’s behavior while browsing the web page will be sent back to the backend log database through the log system. **At this time, if the user has a test group label, the label will also be sent back to the backend database.
In the background, the work of the experimenter is first to configure the traffic distribution system to determine what kind of test the user who meets what conditions will participate in. Secondly, the experimenter needs to count the data in the log database, generate experimental reports for users in different groups through the evaluation system, and compare and evaluate the experimental results.
​ 1545129333858

Figure 1–23 AB test system

Generally speaking, a new recommendation algorithm is finally launched, and the three experiments mentioned above need to be completed.

First, it is necessary to prove through offline experiments that it is better than the existing algorithms in many offline indicators.
Then, it is necessary to determine through user surveys that its user satisfaction is not lower than that of the existing algorithms.
Finally, it is determined through online AB testing that it is better than the existing algorithms in the indicators we care about.
3.2 Evaluation Indicators
3.2.1 User Satisfaction
User satisfaction cannot be calculated offline and can only be obtained through user surveys or online experiments.

In online systems, user satisfaction is mainly obtained through some statistics on user behavior. For example, in e-commerce websites, if users buy recommended products, it means that they are satisfied to a certain extent. Therefore, we can use the purchase rate to measure user satisfaction. In addition, some websites collect user satisfaction by designing some user feedback interfaces. More generally, we can use indicators such as click-through rate, user dwell time and conversion rate to measure user satisfaction.

3.2.2 Prediction Accuracy
Prediction accuracy measures the ability of a recommendation system or recommendation algorithm to predict user behavior. This indicator is the most important offline evaluation indicator for recommendation systems.

Prediction Accuracy Process:

When calculating this indicator, an offline data set is required, which contains the user’s historical behavior records. Then, the data set is divided into a training set and a test set by time. Finally, the user’s behavior and interest model is established on the training set to predict the user’s behavior on the test set, and the overlap between the predicted behavior and the actual behavior on the test set is calculated as the prediction accuracy.

Rating prediction:

Many websites that provide recommendation services have a function that allows users to rate items. Then, if we know the user’s historical ratings of items, we can learn the user’s interest model from it and predict how much the user will rate an item in the future when he sees an item he has not rated. The behavior of predicting the user’s rating of an item is called rating prediction.

The prediction accuracy of rating prediction is generally calculated by root mean square error (RMSE) and mean absolute error (MAE). For a user u and item i in the test set, let
be the actual rating of item i by user u, and $\hat{r}{ui}$ be the predicted rating given by the recommendation algorithm, then RMSE is defined as: $$ RMSE = \frac{\sqrt{\sum{u,i \in T}{(r_{ui} — \hat{r}_{ui})²}}}{|T|} $$ MAE uses absolute value to calculate prediction error, and its definition is:

Regarding the advantages and disadvantages of the two indicators RMSE and MAE, Netflix believes that RMSE increases the penalty for inaccurately predicted user item ratings (punishment of square terms), and thus is more demanding in the evaluation of the system. Studies have shown that if the rating system is based on integers (that is, the ratings given by users are all integers), then rounding the prediction results will reduce the error of MAE.

TopN recommendation:

When providing recommendation services, websites generally give users a personalized recommendation list, which is called TopN recommendation. The prediction accuracy of TopN recommendation is generally measured by precision/recall. Let R(u) be the recommendation list given to the user based on the user’s behavior in the training set, and T(u) be the user’s behavior list in the test set. Then, the recall of the recommendation result is defined as: $$ Recall = \frac{\sum_{u\in U}|R(u) \and T(u)|}{\sum_{u \in U} |T(u)|} $$ The accuracy of the recommendation result is defined as: $$ Recall = \frac{\sum_{u\in U}|R(u) \and T(u)|}{\sum_{u \in U} |R(u)|} $$ Sometimes, in order to comprehensively evaluate the accuracy and recall of TopN recommendations, different recommendation list lengths N are generally selected, a set of accuracy/recall rates are calculated, and then the accuracy/recall curve is drawn.

Discussion on review prediction and TopN recommendation:

In this regard, Greg Linden, a former Amazon scientist, pointed out that the purpose of movie recommendation is to find the movies that users are most likely to be interested in, rather than predicting what kind of rating users will give to movies after watching them. Therefore, TopN recommendation is more in line with actual application needs. There may be a movie that users will give a high score after watching, but the possibility of users watching it is very small. Therefore, predicting whether a user will watch a movie should be more important than predicting what rating the user will give it after watching the movie. Therefore, this book mainly discusses TopN recommendation.

3.2.3 Coverage
**Coverage describes the ability of a recommendation system to discover the long tail of items. **Coverage can be defined in different ways. The simplest definition is the proportion of items that the recommendation system can recommend to the total set of items. Assuming that the user set of the system is U, the recommendation system recommends a list of items R(u) of length N to each user. Then the coverage of the recommendation system can be calculated by the following formula: $$ Converage = \frac{|U_{u \in U} R(u)|}{I} $$ From the above definition, we can see that coverage is an indicator that content providers care about. Taking book recommendations as an example, publishers may be very concerned about whether their books are recommended to users. A recommendation system with a coverage rate of 100% can recommend each item to at least one user. In addition, from the above definition, we can see that the recommendation coverage rate of the popular list is very low. It will only recommend popular items, which account for a small proportion of the total items. A good recommendation system needs to have not only high user satisfaction, but also high coverage.

However, the above definition is too rough. A system with a coverage rate of 100% can have countless item popularity distributions. In order to describe the ability of the recommendation system to explore the long tail in more detail, it is necessary to count the distribution of the number of times different items appear in the recommendation list. If all items appear in the recommendation list and the number of times they appear is similar, then the recommendation system has a good ability to explore the long tail. Therefore, the ability of the recommendation system to explore the long tail can be described by studying the distribution of the number of times items appear in the recommendation list. If this distribution is relatively flat, it means that the recommendation system has a high coverage rate, and if this distribution is steep, it means that the recommendation system has a low coverage rate. There are two well-known indicators in information theory and economics that can be used to define coverage. The first is information entropy: $$ H = -\sum_{i=1}^{n}p(i)log\ p(i) $$ Here p(i) is the popularity of item i divided by the sum of the popularity of all items. The second indicator is the Gini Index: $$ G = \frac{1}{n-1}\sum_{j=1}^{n}(2j-n-1)p(i_j) $$ Here, $i_j$ is the jth item in the list of items sorted from small to large according to the popularity p() of the items.

1545135485983

There is a famous Matthew effect in the field of sociology, that is, the so-called effect that the strong become stronger and the weak become weaker. If a system increases the popularity gap between popular items and non-popular items, making popular items more popular and non-popular items less popular, then this system has the Matthew effect.

So, does the recommendation system have the Matthew effect? ​​The original intention of the recommendation system is to eliminate the Matthew effect so that various items can be displayed to a certain group of people who are interested in them. However, many studies have shown that the current mainstream recommendation algorithms (such as collaborative filtering algorithms) have the Matthew effect. **A simple way to evaluate whether a recommendation system has the Matthew effect is to use the Gini coefficient. **If G1 is the Gini coefficient of item popularity calculated from the initial user behavior, and G2 is the Gini coefficient of item popularity calculated from the recommendation list, then if G2 > G1, it means that the recommendation algorithm has the Matthew effect.

3.2.4 Diversity
In order to meet the wide range of user interests, the recommendation list needs to be able to cover different areas of interest of users, that is, the recommendation results need to be diverse.

Diversity describes the dissimilarity between items in the recommendation list. Therefore, diversity and similarity correspond to each other. Assume that
the similarity between items i and j is defined, then the diversity of user u’s recommendation list R(u) is defined as follows: $$ Diversity(R(u)) = 1 — \frac{\sum_{i,j \in R(u), i \neq j }s(i,j)}{\frac{1}{2}|R(u)|(|R(u)| -1)} $$ The overall diversity of the recommendation system can be defined as the average of the diversity of all user recommendation lists: $$ Diversity = \frac{1}{|U|} \sum_{u \in U} Diversity(R(u)) $$ From the above definition, we can see that different item similarity measurement functions
can define different diversities. If we use content similarity to describe the similarity between items, we can get the content diversity function. If we use the collaborative filtering similarity function to describe the similarity between items, we can get the collaborative filtering diversity function.

3.2.5 Novelty
Novel recommendations refer to recommending items to users that they have not heard of before. The simplest way to achieve novelty on a website is to filter out items from the recommendation list that users have previously acted on on the website.

O’scar Celma studied the evaluation of novelty in his doctoral thesis “Music Recommendation and Discovery in the Long Tail”. The simplest way to evaluate novelty is to use the average popularity of the recommended results, because the less popular items are more likely to be considered novel by users. Therefore, if the average popularity of the items in the recommended results is low, then the recommended results may have a relatively high novelty.

Using the average popularity of the recommended results to measure novelty is relatively rough, because different users do not know different things. Therefore, to accurately count novelty, user surveys are required.

3.2.6 Serendipity
Surendipity is the hottest topic in the field of recommendation systems in recent years.

Serendipity VS Novelty

If the recommended results are not similar to the user’s historical interests, but make the user feel satisfied, then it can be
