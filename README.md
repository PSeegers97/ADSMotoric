# Minor Applied Data Science
**Student:** Pascal Seegers <br>
**Student number:** 21132844 <br>
**Lecturer:** 
* Jeroen Vuurens
* Tony Andrioli
* Ruud Vermeij
<br>

**Period:** 2021/2022

<br>
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

  Our research project is a following study of the study "The Athletic Skills Track: Age- and gender -related normative values of a motor skills test for 4- to 12-year-old children" which was conducted by Hoeboer (Hoeboer, 2018). Our problem owner Pim Koolwijk is studying which biological or socio-demographic variables might have an impact on bad gross motor skills. So our goal was it to find patterns in children with bad gross motor skills and to eliminate these patterns in real world by improving relevant features or try to find spots for valuable variables for improvement which can be done by the government. Therefore our goal was to find similarities in children with bad motor skills as well as trying to predict with those similarities if a child will be lacking in motor skill development in the future in other words one year later. As this field of study is new there are only similar research projects which among each other use different model approaches. Thus one of our goals is to find the best prediction model for our study. 

<div>
    <h3>Research Question:</h3>
    <div align="center"><h4>
        <i>???How can data science be used to predict whether a child has a chance of developing a lack 
            in motor skills a year later????</i></h4>
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

---

<h3>Evaluation</h3>

During the research for our project we found out that the perceived motor competence isn't a good indicator as young children (below the age 8) aren't good in their self-perception (Morano, 2020). As other studies recommend and one of our results was that parental questionaire data might have a big impact on the motor skill development (Khodaverdi, 2013). Although these questionaires have to be handled with care as other studies say (Zysset, 2018). That is why there might be other factors e.g. sport participation in sport clubs, which sports maybe have the biggest impact on the gross motor skill development. Another possible solution might be simplifying the motor skill quotient.


<h3>Conclusions</h3>
During our study it has been discovered that research is right about the low self-perception of children in the age period from 4-year-olds to 6-year-olds as the perceived motor competence has no impact on our models and have been filtered out by our feature selection (Morano, 2020). As other studies show there might be some other variables which have a greater impact e.g. the sleeping time (Luft, 2005). Another solution might be to take more location specific data into account e.g. CBS data. One problem occured with the parental questionaire data as this had too many holes and therefore a full parental questionaire data might have better features (more important features) and might predict with a lower false-negative rate.

The model with the lowest false-negative rate was our bagging classifier with the binary MQ category. However as this isn't the only evaluation method we used it has been discovered that our k-nearest neighbor classifier worked best in form of precision, recall and accuracy although the false-negative rate is higher by 0,2%. But in general all models performed better (lower fN rate, higher accuracy, higher precision-recall) with our binary MQ category. 

Our overfitting could maybe be prevented if we split our dataset into two datasets one for children with bad motor skills and one for good motor skills as the research shows that children with good motor skills have a higher learning curve than children with bad motor skills and therefore the distance between good motor skills and bad motor skills gets higher. 

Research also shows that one year might be too short for predicting a lack in motor skills as the development in this age period (from 4-6) is slow and other research shows that significance occured after a longer period (Morano, 2020). 

The most interesting discovery is that our models did not rate the weight or BMI as valuable as other research shows. 

<details>
  <summary>Examples</summary>
<br>
<i><small>Table 1: Imputation methods compared with the binary classification kNN </small></i>


|  Imputation |  Accuracy Train set |  Accuracy Test set |  False-negative rate |
|---|---|---|---|
|  Mean |  92,3% |  64,9% |  35,1% |
|  Median |  100,0% |  64,9% |  35,1% |
|  kNN |  100,0% |  64,9% |  35,1% |
<br>

<i><small>Table 2: Model performances with t0 data mean outlier removal, mean imputation and binary classification</small></i>


| Model  |  Accuracy Train set | Accuracy Test set  |  False-negative rate |
|---|---|---|---|
|  Random Forest Classifier |  100,0% |  64,9% |  35,1% |
|  kNN Classifier |  92,3% |  64,9% |  35,1% |
|  Decision Tree Classifier |  100,0% |  64,9% | 35,1%  |
|  Gradient Boost Classifier |  50,0% |  38,8% |  35,1% |
|  Bagging Classifier |  98,0% |  65,2% |  34,9% |
<br>
<i><small>Table 3: Accuracy scores of models using multilabel classification</small></i>


|  Model | Accuracy Train set  |  Accuracy Test set | 
|---|---|---|
|  Random Forest Classifier |  100,0% |  8,6% |  
|  kNN Classifier |  62,5% |  0,3% |   
|  Decision Tree Classifier |  100,0% |  20,2% |

<br>
<i><small>Table 4: 10-Fold cross-validation with accuracy as scoring method</small></i>


| N-Fold  |  1 |  2 |  3 | 4  |  5 |  6 | 7  |  8 |  9 |  10 |
|---|---|---|---|---|---|---|---|---|---|---|
| Accuracy  |  90,0% |  85,6% |  93,1% |  89,9% |  88,1% |  91,8% |  92,5% |  91,2% |  90,6% |  88,1% |

<br>

<i><small>Table 5: Mean and standard deviation of cross-validation</small></i>


|  kNN-binary model |  Accuracy |
|---|---|
|  Mean |  90,1% |
|  Standard deviation |  2,2% |


<br>
</details>

<h3>Planning</h3>
In our project we decided to use an agile method for developing namely Scrum. But we changed it a bit so that we've got a project leader, a notes taker, developers and non-developers. The chart of done tasks can be seen Figure 2. 
We used Github as a version control tool and pushed everyday in the evening our process to the repository.
<br/><br/>
<details>
<summary>Scrum chart board</summary>
  <br/>
  
  <figure style="text-align: center">
    <img src="/images/Scrum_Charts.png" alt="Scrum board chart" width="500">
    <br/>
    <figcaption><i><small>Fig. 2: Scrum board completed tasks</small></i></figcaption>
  </figure>

  [Link to Microsoft Planner (Scrum board)](https://tasks.office.com/DeHaagseHogeschool.onmicrosoft.com/Home/PlanViews/9Jb-xUUDp0Gu_F2YlVNn2ZYAAPLf?Type=PlanLink&Channel=Link&CreatedTime=637776783096820000)


</details>
<hr>
</details>


<details>
  <summary>
    Domain Knowledge
  </summary>

<h3>Subject Field</h3>

  <br/>
Motor skills in general are used in every day life and we practice those skills everyday by walking, bicycling, drawing or writing. But we differ motor skills into two major motor skills. First there is the fine motor skills which include skills like drawing, writing etc. so hand-eye coordination in general. Second there is the gross motor skills on which this study focuses. These include for example walking, running, jumping or bicycling. That's why motor skills are important for survival (Fine and Gross Motor Skills in Children, 2021). 

Motor skills development begins right after birth (Fine and Gross Motor Skills in Children, 2021) and is a never ending learning process (Luft, 2005). These skills improve in school age and going to school helps improving them. Research has shown that motor skills have a greater impact on adulthood life than originally known (Piek, 2006). Motor skills have a great impact on their adolescent and adulthood as children with good motor skills tend to live a healthier life with a lower weight (Robinson, 2015), lower risk of illnesses and overall have a better self-perception (Haga, 2009 and Morano, 2020). Another important point is that they enjoy sports more (Morano, 2020). One major problem which research has shown is that children with good motor skills tend to improve their motor skills faster at some point than children with bad motor skills. The rift between children with bad motor skills and children with good motor skills broadens during the growing up (Luft, 2005). 

One major point research shows is that obese children perform very low in motor competence tests compared to healthy-weight children (Gentier, 2013).  

Our study takes self-perception into account but research shows that the self-perception isn't accurate until the age of eight (Morano, 2020). 

<br>

#### Terminology

**Fine-motor skills**: hand-eye coordination e.g. drawing <br>
**Gross-Motor skills**: large muscle group coordination e.g. walking, running, jumping

**AST-1**: Athletic Skill Test 1, Test from the research Hoeboer <br>
**AST-2**: Athletic Skill Test 2, Test from the research Hoeboer

**MQ-Score**: Motor Quotient score calculated by: 
(percentile / AST-Time) *100 <br> (the percentile can be found in Hoeboer, 2018)
<br>

**MQ-category**: classification of childs motor skill with the MQ-score
<br>

**MQ-category binary**: simplified classification of childs motor skill with the MQ-category &#8594; MQ-category below 3 is classified as bad all above as good

<hr>
</details>  




<details>
  <summary>
      Data preprocessing
        
  </summary>

<h3>Data exploration</h3>
  <br/>

First of all the used/inspected datasets are t0 data, school postcodes from Rotterdam, Den Haag and Groningen, parental questionaire data, t1 data which is separated in data from The Hague University of Applied Sciences and Eindhoven and cbs data for gender and age, for migration background, income and core numbers. 

<h4>Data loading</h4>
The t0 data is a csv file which has been loaded in form of a pandas dataframe with the function "read_csv" for the t0 data the separator has to be specified as a ; has been used as the separator. The same applies to the cbs data, postcode data and t1 data. Only the questionaires are an excel file which has been loaded with the pandas function "read_excel". After running the insights function it clearly showed that the dataframes have been loaded correctly. 

<h4>Visualizations</h4>
For a first understanding of the t0 data there were different ways to properly understand the data. The first step is to visualize the data. Which has been done in form of scatter plots as well as histograms, as t-SNEs and zipcode related plots. It was clearly visible in the scatter plots that there are outliers as you can see in fig 3. In these scatter plots no correlation between features has been found. 

[The visualization notebooks can be found here.](Notebooks/Visualizations)


<div>
<img src="images/Visualizations/Age-Bmi.jpg" alt="Scatter plot of t0 with x: age and y: bmi" width="500">
<br>
<figcaption><i><small>Fig. 3: Scatter plot of t0 with outliers (x-axis:age, y-axis:BMI)</small></i></figcaption>
</div>
<br>
<div style="text-align: center">
<img src="images/Visualizations/ASt-Age.jpg" alt="Scatter plot of t0 with x: age and y: AST-Time" width="500">
<br>
<figcaption><i><small>Fig. 4: Scatter plot of t0 with outliers (x-axis: age, y-axis: AST-Time)</small></i></figcaption>
</div>
<br>


In figure 4 it can be seen that there is a correlation between these two feature. This can be ignored as the MQ-score gets calculated by these two features. 


<h4>Insights</h4>
Another step to understand the t0 data was to print all summaries in the notebook. The pandas functions info(), head(), shape, size, describe() and the sum of nan values for columns have been used. The info function shows clearly that there are columns which have holes or how big these holes are and also that some columns which should be numbers are objects. In further research it has been found out that the perceived motor competence scores are objects instead of numeric values. This is because these columns also contain strings that might be because of errors in testing. E.g. in the column "1. Rennen" there was a "x" in one row which might be because this child doesn't want to answer this question. There is another example the columns "Opmerkingen", "Opmerkingen.1" and "Unnamed: 33" can be dropped as they have more than 1000 empty rows. With the describe function it has been discovered that a few columns don't have that much variety e.g. the column "IC" has a min of 1 and a max of 1 which makes sense as this feature only states the consent on data acquiration.



[The Insights can be found here.](Notebooks/Data-Preprocessing/Data_Preprocessing.ipynb)

<i><small>Table 6: Small insights in all collected data</small></i>

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


<br>
  <figure style="text-align: center">
      <img src="/images/Visualizations/MSNO/t0_msno.jpg" alt="Missing values in raw dataset (t0)" width="500">
      <br/><br/>
    <figcaption><i><small>Fig. 5: Missingno plot of raw T0 data</small></i></figcaption>
  </figure>

<br>
<h3>Data preparation & cleaning </h3>


[The data preprocessing notebook can be found here.](Notebooks/Data-Preprocessing/Data_Preprocessing.ipynb)
The dataframes are from now on mentioned as their dataframe name.



<h4>Cleaning</h4>
  <br/>
One part of data preparation is the data cleaning where outliers are removed and categorical data gets encoded. 

As the visualizations and the insights showed us t0 has a few outliers which have to be removed. E.g. one outlier is a child with a BMI of 7113 which isn't possible as a human. Therefore the two approaches mean and standard deviation method and the iqr method are compared. 

But the IQR method isn't appropriate for this study as there are features with a low variance and thus the IQR method removes valuable children (SHOW IQR OUTPUT) with a bad motor skill. That happens because the lower quartile has too high values. The IQR method wasn't pursued after discovering this. 

<i><small>Table 7: t0 shapes and sizes after outlier removal and imputation</small></i>

| Dataframe  |  Shape |  Size |
|---|---|---|
|  t0 | 1271 rows, 32 columns  |  40672 |
|  t0 after outlier removal and imputation |  1697 rows, 32 columns |  54304 |
|  t0 with postcodes after imputation |  1271 rows, 34 columns |  43214 |


For encoding of the categorical features the LabelEncoder has been used. 

<h4>Feature selection</h4>
  <br/>
Features with a no variance have been dropped as they won't have an impact on the model and would lead to overfitting. In this study two different approaches were done one was done with a RandomForestClassififer and the other one was done by using the function SelectKBest from Sklearn.feature_selection. I did the SelectKBest version with chi^2 and selected the 5 best features. I choose the 5 best as after experimenting with a higher `k` we got a bigger overfitting problem. We can't use less than 5 features as the feature selection would only select the features which are needed to calculate the MQ-Category.


<h4>Merging</h4>
  <br/>
In t0 and t1/t1 eindhoven there were no MQ score, MQ category, MQ score binary and BMI category. These columns must be calculated and added to their dataframe.  

It has been done by [the formula](###Terminology). 
The MQ category and BMI category has been calculated using [this logic](Logic/Syntax%20in%20word%20for%20students.docx)

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
  <br/>
The missing values in the dataframes have been treated with different approaches. First of all if a feature has less than 80% data the feature has been dropped as the imputation methods might create "big" patterns in the dataframes which has to be avoided to answer the research question adequate and to be valid. 

One approach is the imputation using the mean of the features, another one is using the median of the features and the last one is done via the kNNImputer from sklearn.impute.
After experimenting a bit with the kNNImputer I decided to set the `nearest_neighbors` to 6 as other values don't improve much in our model. 


For overfitting prevention there are also two different "tasks". The first one is a binary classification problem and the second one is a multilabel classification problem this has been done by converting the multiclass column MQ category into a multilabel column using the LabelBinarizer from Sklearn.preprocessing. 


<h3>Data explanation</h3>
  <br/>
In the data preparation part it has been discovered that the data is not perfect for machine learning as there is not much variety in it as well as too much veracity in a few dataframes e.g. questionaire data. The questionaire data also has not much volume as this dataframe ends up after merging with t0 and dropping nan values with 37 rows. 

A special case is the t1 Eindhoven data as this has 2649 rows and 51 columns. After running the function `printDataframeInsights` it has been discovered that in this dataset is the t0 and t1 data in one file. There are features in this dataset which are only for t0 that also explains why there are compared to t0 too many features. But with the column **Perioden** the t1 data can be filtered and extracted into another dataframe.

<h3>Data visualization (exploratory)</h3>
  <br/>
To find some similarities in the t0 dataset dimensionality reduction using the t-SNE has been plotted. 

[Here are the plots with different t-SNE parameters.](/Notebooks/Visualizations/t-SNE_visualizations.ipynb) 

After viewing them it has been discovered that there is no real cluster in the t-SNE therefore no pattern has been discovered (figure 6).
<br>
  <figure style="text-align: center">
      <img src="/images/Visualizations/tsne-age.png" alt="t-SNE plot of t0 data with dots colored based on age" width="500">
      <br/><br/>
    <figcaption><i><small>Fig. 6: t-SNE plot of t0 data with dots colored based on age</small></i></figcaption>
  </figure>





<hr>
</details>



<details>
  <summary>
    Communication
  </summary> 

<h3>Presentations</h3>
I participated in a few presentations and prepared the presentations with the other group members. I presented the second external presentation as well as the internal presentation 6 and the learning lab.

[The learning lab notebook can be found here.](Notebooks/T-SNE_learning_lab.ipynb)

[The presentations can be found here.](Presentations)

<h3>Writing paper</h3>
We decided as a group that everybody works on the paper and therefore I wrote together with Joost van Viegen the result part as well as the conclusion and together as a group we wrote the abstract. Everybody (myself included) reread the paper and corrected it.

<h3>Notes</h3>
For better communication and better understanding of our progress I was the one who took notes from our stand ups and topics we needed to talk about. 

[Link to Folder with Notes as pdfs](/Notes/)
<hr>
</details> 


<details>
  <summary>
    Bibliography
  </summary>

* Robinson LE, Stodden DF, Barnett LM, Lopes VP, Logan SW, Rodrigues LP, D'Hondt E. Motor Competence and its Effect on Positive Developmental Trajectories of Health. Sports Med. 2015 Sep;45(9):1273-1284. doi: 10.1007/s40279-015-0351-6. PMID: 26201678.
* Monika Haga, Physical Fitness in Children With High Motor Competence Is Different From That in Children With Low Motor Competence, Physical Therapy, Volume 89, Issue 10, 1 October 2009, Pages 1089???1097, https://doi.org/10.2522/ptj.20090052


* Khodaverdi, Z., Bahram, A., Khalaji, H., & Kazemnejad, A. (2013). Motor Skill Competence and Perceived Motor Competence: Which Best Predicts Physical Activity among Girls?. Iranian journal of public health, 42(10), 1145???1150.
* Morano, M., Bortoli, L., Ruiz, M. C., Campanozzi, A., & Robazza, C. (2020). Actual and perceived motor competence: Are children accurate in their perceptions?. PloS one, 15(5), e0233190. https://doi.org/10.1371/journal.pone.0233190
* Hoeboer, J., Ongena, G., Krijger-Hombergen, M., Stolk, E., Savelsbergh, G., & de Vries, S. I. (2018). The Athletic Skills Track: Age- and gender-related normative values of a motor skills test for 4- to 12-year-old children. Journal of science and medicine in sport, 21(9), 975???979.
* Luft, A.R., Buitrago, M.M. Stages of motor skill learning. Mol Neurobiol 32, 205???216 (2005). https://doi.org/10.1385/MN:32:3:205
* Jan P. Piek, Grant B. Baynam, Nicholas C. Barrett,
The relationship between fine and gross motor ability, self-perceptions and self-worth in children and adolescents,
Human Movement Science, Volume 25, Issue 1, 2006, Pages 65-75, ISSN 0167-9457, https://doi.org/10.1016/j.humov.2005.10.011
* Ilse Gentier, Eva D???Hondt, Sarah Shultz, Benedicte Deforche, Mireille Augustijn, Sofie Hoorne, Katja Verlaecke, Ilse De Bourdeaudhuij, Matthieu Lenoir,
Fine and gross motor skills differ between healthy-weight and obese children, Research in Developmental Disabilities, Volume 34, Issue 11, 2013, Pages 4043-4051, ISSN 0891-4222, https://doi.org/10.1016/j.ridd.2013.08.040
* Zysset, A. E., Kakebeeke, T. H., Messerli-B??rgy, N., Meyer, A. H., St??lb, K., Leeger-Aschmann, C. S., Schmutz, E. A., Arhab, A., Ferrazzini, V., Kriemler, S., Munsch, S., Puder, J. J., & Jenni, O. G. (2018). The validity of parental reports on motor skills performance level in preschool children: a comparison with a standardized motor test. European journal of pediatrics, 177(5), 715???722. https://doi.org/10.1007/s00431-017-3078-6
* Aurlien Geron. 2017. Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems (1st. ed.). O'Reilly Media, Inc.




* Alles over Sport. (n.d.).???Start (V)aardig. Allesoversport.nl., from https://www.allesoversport.nl/startvaardig/

* Fine and Gross Moto Skills in Children: https://www.verywellfamily.com/what-are-motor-skills-3107058

</details>

## Reflection and Evaluation

<details>
  <summary>Reflection on own contribution to the project</summary>
  <br/>
In our group project we didn't have any specific roles. But we decided to do a stand up every weekday in the morning. In these meetings my role was to take notes on our tasks, goals, etc and also to inform the members which couldn't attend the meetings. Therefore we all knew what our goals were and knew where what our progress is at that moment. I learned to communicate more clearly and describe goals, tasks and so on more clearly. 
One major problem was our t0 dataset. The first data preparation team tried to merge every data in one single file. So in one datafile there should be t0 data, questionaire data from the parents and cbs data. As nobody tested the dataset or took a deeper look into it we worked with this dataset for one to two months. After this time I discovered that there was information missing and also not consistent information. During merging cbs data with our t0 data there was data from the cbs data dropped. That happened because cbs data is more complex. We tried to merge the cbs data on the zipcodes but the zipcodes in our t0 dataset has a one-to-one relationship while the zipcodes in the cbs data has a one-to-many relationship. After I discovered that I tried to go back to the beginning so to data preparation but there wasn't much time left so I decided to drop the cbs data and focus on other things and take a look into it if we still have time. Since then I learned to test more and more and not assume that everything works perfectly. 

Another role for me was after we discovered that our dataset was corrupted during cleaning to take a look into the cleaning again. As well as get a very good overview on the data in general. My task was to prepare the data therefore I tried to make a few different versions with different outlier handling and imputation methods. Our goal was to make a working prototype for our problem owner which can be used in the future. Therefore I tried to cover every single case for t0 data as well as t1 data. (Mehr informationen n??tig).
As we discovered the mistakes in our dataset very late (begin/middle of december) I needed time. Because of my thinking "What if" the cleaning took too long and I tried to pursue a too perfectionist approach as I tried to make one single pipeline for t0 and t1 data which wasn't really possible as there were a few different columns in the t1 data. The data preparation was finished after two weeks because of many errors in the dataset as well as my perfectionism. But this time was precious and at that point we lost too much time with our preparation as we had to hand in our project three to four weeks later. However during this I learned that I should follow a simpler strategy (which I did after one week) and also to not pursue perfectionism but a working example. 
<hr>
</details>

<details>
  <summary>Reflection on own learning objectives</summary>
  <br/>
  In this study I wanted to get to know to machine learning and learn the basics in machine learning. As well as see if this might be a direction of work for me in the future. In the beginning there was very much information and an information overload for me which made it hard for me to understand how machine learning works. That's why I choose to read the book "Hands-on Machine Learning with Scikit-Learn, Keras, and Tensorflow: Concepts, Tools, and Techniques to Build Intelligent Systems". At the beginning it didn't help much as there was still a information overload. But after trying some things in our group project I understood more and more. Adding to this I asked a friend of mine who already worked with machine learning which helped a lot. The outcome of this all was that I understood machine learning more and more which lead to an ever changing project code and approach. In the end it all clicked and makes sense. I understand the basics of machine learning now when to do which steps and why doing these steps is important. The information overload was very hard for me in the beginning but as I absorbed more and more information through different sources I learned to use these sources and how to use them. 

Another learning objective for me was the project planning. As I never had an interdisciplinary study/course with people not from programming in general I never knew how to work in a "work environment" and how to explain functions to not developers. Therefore one of my tasks was to explain functions or developing in general more clearly to not developers. I did this and asked the person afterwards what they think I meant. Also what they think the outcome will look like and compared this to my thoughts/results from these questions. If they aligned I could assume that they understood what I meant. Sometimes the developers understood my points but the non developers didn't and they looked confused after my explanations. After this I noticed that my thoughts are very specific and that it was hard to explain things easy and short. That's how I learned to express myself more precise and simpler. As well as trying to understand the thinking process of other non developers more. I learned also that I sometimes assume things which shouldn't be assumed and that I needed to ask myself and the other members more questions. 
<hr>
</details>

<details>
  <summary>Evaluation on the group project as a whole</summary>
  <br/>
  The group in general was a good group although we weren't all developers. That led to the fact that we sometimes got stuck. One problem was that we had to explain in detail what our steps were and what some code snippet does. Another point is that non-developers tried to do very hard tasks e.g. data preparation which led to a "wrong" dataset as this wasn't tested neither by other group members nor by me. So after we discovered that there were mistakes we had to begin at the start again. Now I know that I should test more and that cross-testing is mandatory for hard tasks. Also that clear and precise communication is the key to a good group project. (not finished)

All in all was it a good group project as we had a good problem management and discussed many things in our group. When somebody had a problem we asked each other if somebody has a solution or could help and pair program. Therefore we could solve almost all problems and if it took too much time we did it separately and tried to absorb as much information as possible. In the end somebody always had a solution for our problem. 
During this I learned that pair programming sometimes leads to good solutions and aren't a time waste as I always thought. Also I learned that the easiest way in my mind isn't always the easiest way. Some times my thinking process was too complicated.
And I also learned that my thinking is way to me focused as I sometimes assumed other people understand developing very well because it is "easier" for me. Which led me to be a calmer person as well as managing with other opinions better. I improved in the sense that I don't take many things for granted and that a interdisciplinary group opens my mind more as I notice that people from other studies give arguments I never thought of but are after they said it very strong arguments which make sense and help me understand problems/topics more.
</details>


    

