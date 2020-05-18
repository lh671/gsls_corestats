# GSLS Core Stats Training - May2020

## Set-up

### Create a version repository    
Create new repository on GitHub. Open in R studio using version control - gsls_corestats

### Opening new data sets    
fishlengthDF<- read.csv(file = 'CS1-onesample.csv', header=T      
oystercatcher<-read.csv(file.choose(),header=T)     

### Set working directory     
'setwd("~/gsls_corestats/CS2 - Single Categorical Data")'

## Library used:   
tidyverse    
tidytex   
cars   

## Workflow
1. Summarise and visualise the data
  + ggnorm, ggline, boxplot, summary
2. Run appropriate test with assumptions
3. Check assumptions
  + normality - shapiro.test
  + variance - bartletts.test, leveneTest

## Statistical Tests


Sample Size   | Normal Distribution | Abnormal Distribution 
------------- | ------------------- | --------------------- 
Small         | Parametric          | Non-parametric                      
Big           | Parametric          | Parametric            

__Parametric tests:__

Paired?       | Equal Variation     | Unequal variation
------------- | ------------------- | --------------------- 
Yes           | Paired t-test       | Paired t-test        
No            | Student's t-test    | Welch's t-test

__Non-parametric tests:__

Paired?       | Equal Variation           | Unequal variation
------------- | ------------------------- | ------------------------- 
Yes           | Wilcoxon signed-rank test | Wilcoxon signed-rank test      
No            | Mann-Whitney U test       | *Resampling required*

Test for normality    
- graphical:     
  + ggnorm/ggline()    
  + boxplot()    
- shapiro-wilks test    
  + shapiro.test()      
  
Test for variance:
Normal distribution - yes 
+ bartletts.test
Normal distribution - no
+ leveneTest

