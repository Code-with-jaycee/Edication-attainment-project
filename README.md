# Edication-attainment-project

<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
  <div id="badges">
  <a href="https://www.linkedin.com/in/josphat-rono-61a075232/">
    <img src="https://img.shields.io/badge/-Jaycee-0e76a8?style=flat&labelColor=0e76a8&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="mailto:jayceecoder@gmail.com">
    <img src="https://img.shields.io/badge/-jayceecoder-c0392b?style=flat&labelColor=c0392b&logo=gmail&logoColor=white)]" alt="Youtube Badge"/>
  </a>
  <a href="https://twitter.com/CodeJaycee">
    <img src="https://img.shields.io/badge/-@CodeJaycee-1ca0f1?style=flat&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/CodeJaycee" alt="Twitter Badge"/>
  </a>
  <a href="https://www.youtube.com/channel/UCyH8q1BeRAPtaVm_iwsiHpw">
    <img src="https://img.shields.io/badge/-Code_with_Jaycee-e74c3c?style=flat&labelColor=e74c3c&logo=youtube&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="https://www.instagram.com/programmer_jaycee/">
    <img src="https://img.shields.io/badge/-@programmer_jaycee-e84393?style=flat&labelColor=e84393&logo=instagram&logoColor=white" alt="Youtube Badge"/>
  </a>
  
  
</div>
<img src="https://komarev.com/ghpvc/?username=Code-with-jaycee&style=flat-square&color=blue" alt=""/>

<h1>
Hi I'm Josphat 

<h4>Consider the Education_attainment.csv data-set. Column descriptions for this data are as follows:</h4>

◦ Year: The year this row represents. Note there may be more than one row for the same year to show the percent breakdowns by sex.<br>
◦ Sex: The sex of the students this row pertains to, one of "F" for female, "M" for male, or"A" for all students.<br><br>

◦ Min degree: The degree this row pertains to. One of "high school", "associate's","bachelor's", or "master's".<br><br>
◦ Total: The total percent of students of the specified gender to reach at least the minimum level of educational attainment in this year.<br><br>


◦ White / Black / Hispanic / Asian / Pacific Islander / American Indian or Alaska Native / Two or more races: The percent of students of this race and the specified gender to reach at least the minimum level of educational attainment in this year.<br><br>



<h5><b>a. Read this data into Python Pandas.</b></h5>
<br>

```
#imports
import pandas as pd
```
```
Education_data = pd.read_csv("Education_attainment.csv")
Education_data
```

b. Determine the percentages for women vs. men having earned a Bachelor's Degree in 1980.
<br><br>

```
Women = len(Education_data[
        (Education_data["Sex"] == "F" ) &
        (Education_data["Year"] == 1980) 
       
        ]
)
Men = len(Education_data[
    (Education_data["Sex"] == "M") &
    (Education_data["Year"] == 1980) 
    
])
Percentage = Women/(Women + Men) * 100

print(f"Percentages for Women vs Men = {Percentage}%")
```
<h2>Output</h2>

```
Percentages for Women vs Men = 50.0%
```
c. Analyze the data for the two most commonly awarded levels of educational attainment awarded between 2000-2010 (inclusive).<br><br>

d. Compare the difference between total percent of bachelor's degrees received in 2000 to those in 2010.<br><br>

e. Derive descriptive statistics for this data-set.<br><br>
f. Using the Seaborn library :<br><br>



i. Plot the total percentages of all people of bachelor's degree as minimal completion with a line chart over years.<br><br>

ii. Plot the total percentages of women, men, and total people with a minimum education of high school degrees in the year 2009. Label the x-axis "Sex", the yaxis "Percentage", and title the plot "Percentage Completed High School by Sex".<br><br>