Measure of Dispersion

* Variance  
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

**Python Codes for Practice**  
import numpy as np  
**\#For population Variance**  
population \=\[1,2,3,4,5,6,7,8,9\]  
pop\_mean=sum(population)/len(population)  
pop\_deviation=\[(i-pop\_mean)\*\*2 for i in population\]  
pop\_variance=sum(pop\_deviation)/len(population)

**\#For Sample Variance**  
sample=np.arange(4,10,1)  
s\_mean=sum(sample)/len(sample)  
samp\_deviation=\[(i-s\_mean)\*\*2 for i in sample\]  
samp\_variance=sum(samp\_deviation)/len(sample)

**\#For Standard Deviation**  
import math  
std\_devin=math.sqrt(pop\_variance)  
print('Standard Deviation :{}'.format(round(std\_devin,2)))  
