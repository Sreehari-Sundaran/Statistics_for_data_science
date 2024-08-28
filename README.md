# Statistics for Data Science

## CONTENTS📝

- [Basics (Introduction to Advanced Mathematics)](#basics-introduction-to-advanced-mathematics)
- [Measure of Dispersion](#measure-of-dispersion)
- [Python Codes for Practice](#python-codes-for-practice)

## Basics (Introduction to Advanced Mathematics)

* **Statistics**\-Analyzing data Obtained from a Sample  
* **Sample**\-Part of Whole Population  
* **M**\=Successes in Population  
* **N**\=Total Population  
* **x**\=Successes in Sample  
* **n**\=Total Sample from Population  
* **Mean(Measure of Central Tendency)**  
  * Average of components  
  * Value of components/No of components  
  *  Μ symbol (pronounced "mew")=Mean of Population  
  * x bar (x̄) symbol=Mean of Sample  
  * Outliers Effect Result  
    * Eg : 1,2,3,**100,150**,4,5  
    * The highlighted terms are outliers which will effect the result of mean,So we have median and mode  
* **Median**  
  * Number present at the centre of data set  
  * If there are Odd number of terms-Simply take the middle term  
    * Eg. 1,2,**3**,4,5  
  * If there are even number of terms,simply add the even number of terms and divide it by 2  
    * Eg 1,2,**3,4**,5,6  
    * Median \=(4+3)/2=3.5  
* **Mode**  
  * The number that occurs most often  
    * Eg: 3,3,3,3,6,9  
      * Here the Mode is 3  
    * Eg:3,3,6,6,9  
      * Here the mode is 3 and 6  
  * If all Values are equal,then mode will be zero
 
##  Measure of Dispersion

* **Variance**  
  * Observes the spread of values from mean of the data  
  * It gives an idea on **how is data spread around mean?**  
  * symbol for population variance is **σ2,** which is read as **"sigma squared".**  
  * sample variance is usually denoted by **s2(“s squared)**  
* **Standard Deviation**  
  * It is the square root of variance  
  * Variance which is a squared value gives extra weight to outliers  
  * Inorder to eliminate these outliers we need standard deviation  
  * Standard deviation is directly proportional to the spread  
  * **σ  is the standard deviation of population**  
  * **S is the standard deviation of sample**

## **Python Codes for Practice**  
```python
import numpy as np 
#For population Variance 
population=[1,2,3,4,5,6,7,8,9]
pop_mean=sum(population)/len(population)
pop_deviation=[(i-pop_mean)**2 for i in population]
pop_variance=sum(pop_deviation)/len(population)

#For Sample Variance
sample=np.arange(4,10,1)
s_mean=sum(sample)/len(sample)
samp_deviation=[(i-s_mean)**2 for i in sample] 
samp_variance=sum(samp_deviation)/len(sample)

#For Standard Deviation
import math  
std_devin=math.sqrt(pop_variance)

#Output
print('Population Mean :{}'.format(pop_mean))
print('Population Deviation :{}'.format(pop_deviation))
print('Population Variance :{}'.format(round(pop_variance,2)))
print('Sample Mean :{}'.format(s_mean))
print('Sample Deviation :{}'.format(samp_deviation))
print('Sample Variance :{}'.format(round(samp_variance,2)))
print('Standard Deviation :{}'.format(round(std_devin,2))) 
```
