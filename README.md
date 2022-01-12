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



Evaluation

During the research for our project we found out that the perceived motor competence isn't a good indicator as young children (below the age 8) aren't good in their self-perception (SOURCE). As other studies recommend and one of our results was that parental questionaire data might have a big impact on the motor skill development. Although these questionaires have to be handled with care as other studies say (SOURCE). That is why there might be other factors e.g. sport participation in sport clubs, which sports maybe have the biggest impact on the gross motor skill development. Another possible solution might be simplifying the motor skill quotient. 
<ul>
  <li>direction future work</li>
</ul>

Conclusions


NEEDS TO BE WRITTEN 
<ul>
  <li>discuss results</li>
  <ul>
    <li>show examples</li>
  </ul>
  <li>test outcomes (statistical significance)</li>
</ul>

Planning
In our project we decided to use an agile method for developing namely Scrum. But we changed it a bit so that we've got a project leader, a notes taker, developers and non-developers. The chart of done tasks can be seen Figure ?. (FIGURE ZAHL EINFÜGEN) 
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


<details>
  <summary>
    Domain Knowledge
  </summary>

Subject Field (UNFINISHED)
Motor skills in general are used in every day life and we practice those skills everyday by walking, bicycling, drawing or writing. But we differ motor skills into two major motor skills. First there is the fine motor skills which include skills like drawing, writing etc. so hand-eye coordination in general. Second there is the gross motor skills on which this study focuses. These include for example walking, running, jumping or bicycling. That's why motor skills are important for survival. 

Motor skills development begins right after birth (see verywellfamily.com) and is a never ending learning process (see study where it says staged process). These skills improve in school age and going to school helps improving them. Research has shown that motor skills have a greater impact than originally known. Motor skills have a great impact on their adolescent and adulthood as children with good motor skills tend to live a healthier life with a lower weight(SOURCE), lower risk of illnesses and overall have a better self-perception. Another important point is that they enjoy sports more. One major problem which research has shown is that children with good motor skills tend to improve their motor skills faster at some point than children with bad motor skills. The rift between children with bad motor skills and children with good motor skills broadens during the growing up. 

Our study takes self-perception into account but research shows that the self-perception isn't accurate until the age of eight. 

Another research states that not only the exercising part is important but also e.g. sleeping time. Thus there aren't only variables we can see directly in physical education or in exercising but also variables teachers/researchers can't see but have to ask the parents. 

Literature Research
<ul>
  <li>relevant research</li>
  <li>References & Bibliography</li>
</ul>

Terminology
Fine-motor skills = hand-eye coordination e.g. drawing
Gross-Motor skills = large muscle group coordination e.g. walking, running, jumping

AST-1 = Athletic Skill Test 1, Test from the research Hoeboer
AST-2 = Athletic Skill Test 2, Test from the research Hoeboer

MQ-Score = Motor Quotient score calculated by 
(percentile / AST-Time) *100 

MQ-category = classification of childs motor skill with the MQ-score

</details>  


<details>
  <summary>
      Data preprocessing
        
  </summary>

Data exploration
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

Data cleaning
<ul>
  <li>clean in good & sufficient way</li>
  <ul>
    <li>remove features with more than 20% missing values -> too many missing values for imputation</li>
    <li>adding MQ/BMI Score and MQ category</li>
     <li>merge data</li>
  </ul>
</ul>

Data preparation
<ul>
  <li>transform data (encode etc)</li>
  <li>removing outliers</li>
  <ul>
    <li>remove mean + std</li>
    <li>remove iqr method</li>
  </ul>
  <li>imputation</li>
  <ul>
    <li>Mean</li>
    <li>Median</li>
    <li>kNN Imputation</li> 
  </ul>
</ul>

Data explanation
<ul>
  <li>describe dataset</li>
</ul>

Data visualization (exploratory)
<ul>
  <li>visualize data for supporting models</li>
</ul>
</details>



<details>
  <summary>
    Communication
  </summary> 

Presentations
<ul>
  <li>more than two presentations</li>
</ul>
Writing paper
</details> 


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




<li>Alles over Sport. (n.d.). Start (V)aardig. Allesoversport.nl., from https://www.allesoversport.nl/startvaardig/ </li>
<li>https://www.verywellfamily.com/what-are-motor-skills-3107058</li>
</ul>
</details>

## Reflection and Evaluation
### STARR method
<details>
  <summary>Reflection on own contribution to the project</summary>
</details>

<details>
  <summary>Reflection on own learning objectives</summary>
</details>

<details>
  <summary>Evaluation on the group project as a whole</summary>
</details>

    

