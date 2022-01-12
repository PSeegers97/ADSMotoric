# Minor Applied Data Science
This is the personal portfolio for the minor Applied Data Science at The Hague University made by Pascal Seegers.

## Datacamp
For basic understanding and getting to know machine learning there were assignments on Datacamp. As you can see I finished every course.
<br/><br/>
<details>
  <summary>Screenshot Datacamp Assignments</summary>
  <br/><br/>
  
<figure style="text-align: center">
<div style="text-align: center">
<!-- ![Datacamp assignments Pascal Seegers](/images/Datacamp_Screenshot.png) -->
<img src="/images/Datacamp_Screenshot.png" alt="Datacamp assignments Pascal Seegers" width="500">
<br/><br/>
<figcaption><i><small>Fig. 1: Datacamp assignments Pascal Seegers</small></i></figcaption>
</div>
</figure>
  
</details>
  
## Predicting motoric skill development in young children




<details>

  <summary>
    Research project
  </summary>

  <h3>Problem definition</h3>
  Our research project is a following study of the study "The Athletic Skills Track: Age- and gender -related normative values of a motor skills test for 4- to 12-year-old children" which was conducted by Hoeboer. Our problem owner Pim Koolwijk is studying which biological or socio-demographic variables might have an impact on bad gross motor skills. So our goal was it to find patterns in children with bad gross motor skills to eliminate these patterns or try to find spots for valuable variables for improvement which can be done by the government. Therefore our goal was to find similarities in children with bad motor skills as well as trying to predict with those similarities if a child will be lacking in motor skill development in the future in other words one year later. As this field of study is new there are only similar research projects which among each other use different model approaches. Thus one of our goals is to find the best prediction model for our study. 
    <div>
        *children lack in physical abilities if they won't develop gross motoric skills. Children with good gross motoric skills have a more active lifestyle in their adulthood.
    </div>
<div>
    <h3>Research Question:</h3>
    <div align="center"><h4>
        <i>“How can data science be used to predict whether a child has a chance of developing a lack 
            in motor skills a year later?”</i></h4>
    </div>
    <h4>Subquestions:</h4>
    <div >
        <ul style="text-align: center; list-style-position: inside">
            <h5>
            <li>Which biological and socio-demographic variables have an influence on the motoric skills development by children?</li>
            <br>
            <li>Which model has the lowest false negative rate? </li>
            <br>
<li>Which characteristics have the children with a lack motoric skills in common?  </li>
            </h5>       
</ul>
    </div>
</div>



<h3>Evaluation</h3>

During the research for our project we found out that the perceived motor competence isn't a good indicator as young children (below the age 8) aren't good in their self-perception (SOURCE). As other studies recommend and one of our results was that parental questionaire data might have a big impact on the motor skill development. Although these questionaires have to be handled with care as other studies say (SOURCE). That is why there might be other factors e.g. sport participation in sport clubs, which sports maybe have the biggest impact on the gross motor skill development. Another possible solution might be simplifying the motor skill quotient. 
<ul>
  <li>direction future work</li>
</ul>

<h3>Conclusions</h3>


NEEDS TO BE WRITTEN 
<ul>
  <li>discuss results</li>
  <ul>
    <li>show examples</li>
  </ul>
  <li>test outcomes (statistical significance)</li>
</ul>

<h3>Planning</h3>
In our project we decided to use an agile method for developing namely Scrum. But we changed it a bit so that we've got a project leader, a notes taker, developers and non-developers. The chart of done tasks can be seen Figure ?. (FIGURE ZAHL EINFÜGEN) 
<br/><br/>
<details>
<summary>Scrum chart board</summary>
  <br/><br/>
  
  <figure style="text-align: center">
    <img src="/images/Scrum_Charts.png" alt="Scrum board chart" width="500">
    <br/><br/>
    <figcaption><i><small>Fig. 2: Scrum board completed tasks</small></i></figcaption>
  </figure>
</details>
<ul>

  <li>Notes</li>
</ul>

</details>
---

<details>
  <summary>
    Domain Knowledge
  </summary>

<h3>Subject Field (UNFINISHED)</h3>

  <br/><br/>
Motor skills in general are used in every day life and we practice those skills everyday by walking, bicycling, drawing or writing. But we differ motor skills into two major motor skills. First there is the fine motor skills which include skills like drawing, writing etc. so hand-eye coordination in general. Second there is the gross motor skills on which this study focuses. These include for example walking, running, jumping or bicycling. That's why motor skills are important for survival. 

Motor skills development begins right after birth (see verywellfamily.com) and is a never ending learning process (see study where it says staged process). These skills improve in school age and going to school helps improving them. Research has shown that motor skills have a greater impact than originally known. Motor skills have a great impact on their adolescent and adulthood as children with good motor skills tend to live a healthier life with a lower weight(SOURCE), lower risk of illnesses and overall have a better self-perception. Another important point is that they enjoy sports more. One major problem which research has shown is that children with good motor skills tend to improve their motor skills faster at some point than children with bad motor skills. The rift between children with bad motor skills and children with good motor skills broadens during the growing up. 

Our study takes self-perception into account but research shows that the self-perception isn't accurate until the age of eight. 

Another research states that not only the exercising part is important but also e.g. sleeping time. Thus there aren't only variables we can see directly in physical education or in exercising but also variables teachers/researchers can't see but have to ask the parents. 

<h3>Literature Research</h3>

  <br/><br/>
<ul>
  <li>relevant research</li>
  <li>References & Bibliography</li>
</ul>

<h3>Terminology</h3>
  <br/><br/>
Fine-motor skills = hand-eye coordination e.g. drawing
Gross-Motor skills = large muscle group coordination e.g. walking, running, jumping

AST-1 = Athletic Skill Test 1, Test from the research Hoeboer
AST-2 = Athletic Skill Test 2, Test from the research Hoeboer

MQ-Score = Motor Quotient score calculated by 
(percentile / AST-Time) *100 

MQ-category = classification of childs motor skill with the MQ-score

</details>  
---

<details>
  <summary>
      Data preprocessing
        
  </summary>

<h3>Data exploration</h3>
  <br/><br/>

First of all the used/inspected datasets are t0 data, school postcodes from Rotterdam, Den Haag and Groningen, parental questionaire data, t1 data which is separated in data from The Hague University of Applied Sciences and Eindhoven and cbs data for gender and age, for migration background, income and core numbers. 

<h4>Data loading</h4>
The t0 data is a csv file which has been loaded in form of a pandas dataframe with the function "read_csv" for the t0 data the separator has to be specified as a ; has been used as the separator. The same applies to the cbs data, postcode data and t1 data. Only the questionaires are an excel file which has been loaded with the pandas function "read_excel". After running the insights function it clearly showed that the dataframes have been loaded correctly. 

<h4>Visualizations</h4>
For a first understanding of the t0 data there were different ways to properly understand the data. The first step is to visualize the data. Which has been done in form of scatter plots as well as histograms, as t-SNEs and zipcode related plots. It was clearly visible in the scatter plots that there are outliers as you can see in fig (FIGURE EINFÜGEN). In these scatter plots no correlation between features has been found. 



Insights</h4>
Another step to understand the t0 data was to print all summaries in the notebook. The pandas functions info(), head(), shape, size, describe() and the sum of nan values for columns have been used. The info function shows clearly that there are columns which have holes or how big these holes are and also that some columns which should be numbers are objects. In further research it has been found out that the perceived motor competence scores are objects instead of numeric values. This is because these columns also contain strings that might be because of errors in testing. E.g. in the column "1. Rennen" there was a "x" in one row which might be because this child doesn't want to answer this question. There is another example the columns "Opmerkingen", "Opmerkingen.1" and "Unnamed: 33" can be dropped as they have more than 1000 empty rows. With the describe function it has been found that a few columns don't have that much variety e.g. the column "IC" has a min of 1 and a max of 1 which is understandable as this feature only states the consent on data acquiration (NOT A GOOD SENTENCE). 

|  Dataframe |  Size |  Shape |
|---|---|---|
|  t0 |  1708 rows, 34 columns |  58072 |
|  parental questionaires |  1102 rows, 92 columns |  101384 |
|  t1 THUAS |  733 rows, 36 columns |  26388 |
|  t1 Eindhoven |  2649 rows, 51 columns |  135099 |
|  CBS core numbers |  17341 rows, 118 columns |  2046238 |
|  CBS gender age |  513576 rows, 7 columns |  3595032 |
|  CBS income |  25032 rows, 22 columns |  55074 |
|  CBS migration background |  512576 rows, 7 columns |  3595032 |

<ul>
  <li>examine data</li>
  <li>visualize data</li>
  <ul>
    <li>scatter plots</li>
    <li>missingno plots</li>
    <figure style="text-align: center">
      <img src="/images/Visualizations/T0_data_msno.pdf" alt="Missing values in raw dataset" width="500">
      <br/><br/>
    <figcaption><i><small>Fig. 2: Missingno plot of raw T0 data</small></i></figcaption>
  </figure>
    <li>histogram plots</li>
    <li>t-SNE</li>
    
  </ul>
  <li>distributions</li>
  
  <li>outliers</li>
  <ul>
    <li>missingno</li>  
  </ul>
  
  <li>correlation</li>
  <ul>
    <li>hypothesis</li>
  </ul>
</ul>

<h3>Data preparation & cleaning </h3>


The dataframes are from now on mentioned as their dataframe name.

<h4>Cleaning</h4>
  <br/><br/>
One part of data preparation is the data cleaning where outliers are removed and categorical data gets encoded. 

As the visualizations and the insights showed us t0 has a few outliers which have to be removed. E.g. one outlier is a child with a BMI of 7113 which isn't possible as a human. Therefore the two approaches mean and standard deviation method and the iqr method are compared. 

But the IQR method isn't appropriate for this study as there are features with a low variance and thus the IQR method removes valuable children (SHOW IQR OUTPUT) with a bad motor skill. That happens because the lower quartile has too high values. The IQR method wasn't pursued after discovering this. 



| Dataframe  |  Shape |  Size |
|---|---|---|
|  t0 | 1271 rows, 32 columns  |  40672 |
|  t0 after outlier removal and imputation |  1697 rows, 32 columns |  54304 |
|  t0 with postcodes after imputation |  1271 rows, 34 columns |  43214 |


For encoding of the categorical features the LabelEncoder has been used. 

<h4>Feature selection</h4>
  <br/><br/>
Features with a no variance have been dropped as they won't have an impact on the model and would lead to overfitting. In this study two different approaches were done one was done with a RandomForestClassififer and the other one was done by using the function SelectKBest from Sklearn.feature_selection. I did the SelectKBest version with chi^2 and selected the 5 best features. 


<h4>Merging</h4>
  <br/><br/>
In t0 and t1/t1 eindhoven there were no MQ score, MQ category and BMI category. These columns must be calculated and added to their dataframe. It has been done by the formula (REFERENCE TO DOMAIN KNOWLEDGE). 

For geographical insights the school postcode numbers and postcode letters from postcodes dh rot and postcodes gro have been added to t0. Not to t1 as t1 is only used for prediction. 

There was also an approach to add the questionaire data to t0 but after dropping all nan values the dataframe had only 37 rows which is too few for machine learning. t0 and questionaire data combined had too many holes therefore this approach has been stopped and dropped. 

Another approach was to merge cbs data into t0 on the zipcodes. The problem is cbs data is very complex and the zipcodes in t0 have a one-to-one relationship while the zipcodes in cbs have a one-to-many relationship. For merging a dictionary containing a zipcode as a key and their dataframe as their value has been created. But there wasn't a solution to flatten these dataframes into a one-to-one relationship. It could have been done by hand but there wasn't enough time for this approach. So this approach has been dropped. 

In the end there are 11 different dataframes:
<ul>
<li>t0</li>
<li>t0 outlier removed by mean and using mean imputation</li>
<li>t0 outlier removed by mean and using median imputation</li>
<li>t0 outlier removed by mean and using knn imputation</li>
<li>t0 mean imputed</li>
<li>t0 median imputed</li>
<li>t0 knn imputed</li>
<li>t0 with zipcodes  after dropna</li>
<li>t0 with zipcodes with mean imputation</li>
<li>t0 with zipcodes with median imputation</li>
<li>t0 with zipcodes with knn imputation</li>
</ul>

After merging the NaN values had to be dropped because models can't calculate with a NaN value. That led t0 to 1271 rows and 32 columns. 


<h4>Imputation</h4>
  <br/><br/>
The missing values in the dataframes have been treated with different approaches. First of all if a feature has less than 80% data the feature has been dropped as the imputation methods might create "big" patterns in the dataframes which has to be avoided to answer the research question adequate and to be valid. 

One approach is the imputation using the mean of the features, another one is using the median of the features and the last one is done via the kNNImputer from sklearn.impute. 


For overfitting prevention there are also two different "tasks". The first one is a binary classification problem (ADD MQ BINARY TO MERGING) and the second one is a multilabel classification problem this has been done by converting the multiclass column MQ category into a multilabel column using the LabelBinarizer from Sklearn.preprocessing. 


<h3>Data explanation</h3>
  <br/><br/>
In the data preparation part it has been discovered that the data is not perfect for machine learning as there is not much variety in it as well as too much veracity in a few dataframes e.g. questionaire data. The questionaire data also has not much volume as this dataframe ends up after merging with t0 and dropping nan values with 37 rows. 

<h3>Data visualization (exploratory)</h3>
  <br/><br/>
To find some similarities in the t0 dataset a t-SNE has been plotted. Here (LINK ZUM FOLDER) are the plots with different t-SNE parameters. After viewing them it has been discovered that there is no real cluster in the t-SNE therefore no pattern has been discovered.
</details>

---

<details>
  <summary>
    Communication
  </summary> 

<h3>Presentations</h3>
  <br/><br/>
I participated in a few presentations and prepared the presentations with the other group members. I presented the second external presentation as well as the internal presentation 5 and the learning lab. 

<h3>Writing paper</h3>
  <br/><br/>
We decided as a group that everybody works on the paper and therefore I wrote together with Joost van Viegen the result part as well as the conclusion and together as a group we wrote the abstract. Everybody (myself included) reread the paper and corrected it. 

</details> 

---
<details>
  <summary>
    Bibliography
  </summary>
  <ul>
<li>Robinson LE, Stodden DF, Barnett LM, Lopes VP, Logan SW, Rodrigues LP, D'Hondt E. Motor Competence and its Effect on Positive Developmental Trajectories of Health. Sports Med. 2015 Sep;45(9):1273-1284. doi: 10.1007/s40279-015-0351-6. PMID: 26201678.</li>
<li>Monika Haga, Physical Fitness in Children With High Motor Competence Is Different From That in Children With Low Motor Competence, Physical Therapy, Volume 89, Issue 10, 1 October 2009, Pages 1089–1097, https://doi.org/10.2522/ptj.20090052</li>
<li>Khodaverdi, Z., Bahram, A., Khalaji, H., & Kazemnejad, A. (2013). Motor Skill Competence and Perceived Motor Competence: Which Best Predicts Physical Activity among Girls?. Iranian journal of public health, 42(10), 1145–1150.</li>
<li>Morano, M., Bortoli, L., Ruiz, M. C., Campanozzi, A., & Robazza, C. (2020). Actual and perceived motor competence: Are children accurate in their perceptions?. PloS one, 15(5), e0233190. https://doi.org/10.1371/journal.pone.0233190</li>
<li>Hoeboer, J., Ongena, G., Krijger-Hombergen, M., Stolk, E., Savelsbergh, G., & de Vries, S. I. (2018). The Athletic Skills Track: Age- and gender-related normative values of a motor skills test for 4- to 12-year-old children. Journal of science and medicine in sport, 21(9), 975–979.</li>
<li>Luft, A.R., Buitrago, M.M. Stages of motor skill learning. Mol Neurobiol 32, 205–216 (2005). https://doi.org/10.1385/MN:32:3:205</li>
<li>Jan P. Piek, Grant B. Baynam, Nicholas C. Barrett,
The relationship between fine and gross motor ability, self-perceptions and self-worth in children and adolescents,
Human Movement Science, Volume 25, Issue 1, 2006, Pages 65-75, ISSN 0167-9457, https://doi.org/10.1016/j.humov.2005.10.011</li>
<li>Ilse Gentier, Eva D’Hondt, Sarah Shultz, Benedicte Deforche, Mireille Augustijn, Sofie Hoorne, Katja Verlaecke, Ilse De Bourdeaudhuij, Matthieu Lenoir,
Fine and gross motor skills differ between healthy-weight and obese children, Research in Developmental Disabilities, Volume 34, Issue 11, 2013, Pages 4043-4051, ISSN 0891-4222, https://doi.org/10.1016/j.ridd.2013.08.040</li>
<li>Aurlien Gron. 2017. Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems (1st. ed.). O'Reilly Media, Inc.</li>




<li>Alles over Sport. (n.d.). Start (V)aardig. Allesoversport.nl., from https://www.allesoversport.nl/startvaardig/ </li>
<li>https://www.verywellfamily.com/what-are-motor-skills-3107058</li>
</ul>
</details>

## Reflection and Evaluation

<details>
  <summary>Reflection on own contribution to the project</summary>
  In our group project we didn't have any specific roles. But we decided to do a stand up every weekday in the morning. In these meetings my role was to take notes on our tasks, goals, etc and also to inform the members which couldn't attend the meetings. Therefore we all knew what our goals were and knew where what our progress is at that moment. I learned to communicate more clearly and describe goals, tasks and so on more clearly. 
One major problem was our t0 dataset. The first data preparation team tried to merge every data in one single file. So in one datafile there should be t0 data, questionaire data from the parents and cbs data. As nobody tested the dataset or took a deeper look into it we worked with this dataset for one to two months. After this time I discovered that there was information missing and also not consistent information. During merging cbs data with our t0 data there was data from the cbs data dropped. That happened because cbs data is more complex. We tried to merge the cbs data on the zipcodes but the zipcodes in our t0 dataset has a one-to-one relationship while the zipcodes in the cbs data has a one-to-many relationship. After I discovered that I tried to go back to the beginning so to data preparation but there wasn't much time left so I decided to drop the cbs data and focus on other things and take a look into it if we still have time. Since then I learned to test more and more and not assume that everything works perfectly. 

Another role for me was after we discovered that our dataset was corrupted during cleaning to take a look into the cleaning again. As well as get a very good overview on the data in general. My task was to prepare the data therefore I tried to make a few different versions with different outlier handling and imputation methods. Our goal was to make a working prototype for our problem owner which can be used in the future. Therefore I tried to cover every single case for t0 data as well as t1 data. (Mehr informationen nötig).
As we discovered the mistakes in our dataset very late (begin/middle of december) I needed time. Because of my thinking "What if" the cleaning took too long and I tried to pursue a too perfectionist approach as I tried to make one single pipeline for t0 and t1 data which wasn't really possible as there were a few different columns in the t1 data. The data preparation was finished after two weeks because of many errors in the dataset as well as my perfectionism. But this time was precious and at that point we lost too much time with our preparation as we had to hand in our project three to four weeks later. However during this I learned that I should follow a simpler strategy (which I did after one week) and also to not pursue perfectionism but a working example. 
</details>

<details>
  <summary>Reflection on own learning objectives</summary>
  In this study I wanted to get to know to machine learning and learn the basics in machine learning. As well as see if this might be a direction of work for me in the future. In the beginning there was very much information and an information overload for me which made it hard for me to understand how machine learning works. That's why I choose to read the book "Hands-on Machine Learning with Scikit-Learn, Keras, and Tensorflow: Concepts, Tools, and Techniques to Build Intelligent Systems". At the beginning it didn't help much as there was still a information overload. But after trying some things in our group project I understood more and more. Adding to this I asked a friend of mine who already worked with machine learning which helped a lot. The outcome of this all was that I understood machine learning more and more which lead to an ever changing project code and approach. In the end it all clicked and makes sense. I understand the basics of machine learning now when to do which steps and why doing these steps is important. The information overload was very hard for me in the beginning but as I absorbed more and more information through different sources I learned to use these sources and how to use these sources. 

Another learning objective for me was the project planning. As I never had an interdisciplinary study/course with people not from programming in general I never knew how to work in a "work environment" and how to explain functions to not developers. Therefore one of my tasks was to explain functions or developing in general more clearly to not developers. I did this and asked the person afterwards what they think I meant. Also what they think the outcome will look like and compared this to my thoughts/results from these questions. If they aligned I could assume that they understood what I meant. Sometimes the developers understood my points but the non developers didn't and they looked confused after my explanations. After this I noticed that my thoughts are very specific and that it was hard to explain things easy and short. That's how I learned to express myself more precise and simpler. As well as trying to understand the thinking process of other non developers more. I learned also that I sometimes assume things which shouldn't be assumed and that I needed to ask myself and the other members more questions. 
</details>

<details>
  <summary>Evaluation on the group project as a whole (NEEDS IMPROVEMENT)</summary>
  The group in general was a good group although we weren't all developers. That led to the fact that we sometimes got stuck. One problem was that we had to explain in detail what our steps were and what some code snippet does. Another point is that non-developers tried to do very hard tasks e.g. data preparation which led to a "wrong" dataset as this wasn't tested neither by other group members nor by me. So after we discovered that there were mistakes we had to begin at the start again. Now I know that I should test more and that cross-testing is mandatory for hard tasks. Also that clear and precise communication is the key to a good group project. (not finished)

All in all was it a good group project as we had a good problem management and discussed many things in our group. When somebody had a problem we asked each other if somebody has a solution or could help and pair program. Therefore we could solve almost all problems and if it took too much time we did it separately and tried to absorb as much information as possible. In the end somebody always had a solution for our problem. 
During this I learned that pair programming sometimes leads to good solutions and aren't a time waste as I always thought. Also I learned that the easiest way in my mind isn't always the easiest way. Some times I thought too difficult (Ist das ein Satz?)
And I also learned that my thinking is way to me focused as I sometimes assumed other people understand developing very well because it is "easier" for me. Which led me to be a calmer person as well as managing with other opinions better. I improved in the sense that I don't take many things for granted and that a interdisciplinary group opens my mind more as I notice that people from other studies give arguments I never thought of but are after they said it very strong arguments which make sense and help me understand problems/topics more.
</details>


    

