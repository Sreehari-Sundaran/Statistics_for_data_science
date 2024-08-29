# Statistics for Data Science

**<li>Check out my Portfolio**:<a href="https://github.com/lionheartsss1997"> Sreehari's Portfolio</a><br></li>

## CONTENTS📝

- [Basics (Introduction to Advanced Mathematics)](#basics-introduction-to-advanced-mathematics)
- [Measure of Dispersion](#measure-of-dispersion)
- [Python Codes for Practice](#python-codes-for-practice)
- [Statistics Behind Plots](#statistics-behind-plots)

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
## Statistics Behind Plots

When visualizing data, it's important to understand the underlying statistics that inform the plots. Below are some key statistical concepts:

| Plot Type      | Key Statistic(s)                      |Type | Description                                                                                  |
|----------------|---------------------------------------|-----|-----------------------------------------------------------------------------------------|
| Histogram      | **Frequency Distribution**            |Univariate |Shows the distribution of data by counting the number of observations in each bin.           |
| Box Plot       | **Quartiles, Median, IQR**            | Univariate |Visualizes the spread and skewness of data using quartiles, highlighting outliers.           |
| Scatter Plot   | **Correlation Coefficient**           |Bivariate | Displays the relationship between two variables, often with a regression line.               |
| Bar Chart      | **Mean, Proportions**                 |Bivariate | Compares categorical data by showing the mean or proportion of each category.                |
| Line Plot      | **Trends, Moving Average**            |Bivariate | Depicts trends over time, highlighting patterns, cycles, or fluctuations in data.            |

Understanding these statistics helps in choosing the right plot for your data and interpreting the results accurately.

* **Univariate Plots-** Refers to analysis of one variable or related to distribution of single variable  
  **Types**  
1. **Histogram**(used for general distribution to identify outliers)  
   1. represent numerical data in form of graphs  
   2. It has only one axis  
   3. X axis \- bin ranges ; Y axis \- information about the frequency of data (Bin-Seperation between bars)

Histogram using Seaborn(library for making statistical graphics in Python)  
```python
import seaborn as sns  
penguins \= sns.load\_dataset("penguins")  
sns.displot(penguins, x="flipper\_length\_mm")  
```
![image](https://github.com/user-attachments/assets/d865bfcd-2de4-453a-b52f-fd9840c1949f)

2. **Box Plot**  
   1. Identifies how well the data is distributed in the dataset  
   2. Divided the data into three quartiles  
   3. Helps to recognise effect of outliers on data set and useful in comparing the distribution of data  
   4. A box plot consist of 5 things.  
      1. Minimum  
      2. First Quartile or 25%  
      3. Median (Second Quartile) or 50%  
      4. Third Quartile or 75%  
      5. Maximum

BoxPlot using Seaborn  
```python
import seaborn as sns  
tips \= sns.load\_dataset('tips')  
sns.set\_style("whitegrid")  
sns.boxplot(x \= 'day', y \= 'total\_bill', data \= tips)
```
![image](https://github.com/user-attachments/assets/ab8827c1-d93c-4261-8d9c-81a200d60133)

| Observations<br>1. Bottom black horizontal line of blue box plot is minimum value<br>2. First black horizontal line of rectangle shape of blue box plot is First quartile or 25%<br>3. Second black horizontal line of the rectangle shape of the blue box plot is Second quartile or 50% or median.<br>4. Third black horizontal line of rectangle shape of blue box plot is third quartile or 75% Top black horizontal line of the rectangle shape of the blue box plot is maximum value.<br>5. Circle shape of blue box plot is outlier data |
| :---- |

3. **Pie Chart**  
   1. Represent part of whole  
   2. Used to show percentage  
   3. Often used to represent sample data

Piechart using matplotlib  
```python
import matplotlib.pyplot as plt  
import numpy as np  
y \= np.array(\[35, 25, 25, 15\])  
mylabels \= \["Apples", "Bananas", "Cherries", "Dates"\]  
plt.pie(y, labels \= mylabels)  
plt.show()
```
![image](https://github.com/user-attachments/assets/99759855-1d69-4ea8-ad68-ede16d42e260)

* **Bivariate Plots-** two variables are observed  
  * One variable is dependent while other is independent<br>
  Types
1. **Bar Plot**\-aggregating numerical and categorical data according to some methods

BarPlot using seaborn  
```python
import seaborn as sns  
sns.set\_theme(style="whitegrid")  
tips \= sns.load\_dataset("tips")  
ax \= sns.barplot(x="day", y="total\_bill", data=tips)  
```
![image](https://github.com/user-attachments/assets/36f00713-e0d3-484a-8490-d3bbdef454ad)

2. **ScatterPlot**  
   1. It shows relationship between different Variables  
   2. It is used to determine whether there are patterns or correlations between the two variables  
   3. Avoid ScatterPlot  
      1. When you have large data set  
      2. When your data is not at all related

ScatterPlot using seaborn  
```python
import seaborn as sns  
sns.set(style='whitegrid')  
fmri \=sns.load\_dataset("fmri")  
sns.scatterplot(x="timepoint",y="signal",data=fmri)  
```
![image](https://github.com/user-attachments/assets/0c7c20b1-b56f-4d90-9386-f57d0abdcd45)


3. **Line Chart**  
   1. Points connected from left to right to demonstrate changes in values

LinePlot using seaborn & matplotlib  
```python
import seaborn as sns  
import matplotlib.pyplot as plt  
data \= sns.load\_dataset("tips")  
sns.lineplot(x="total\_bill", y="size", hue="sex", style="sex",data=data)  
plt.show()
```
![image](https://github.com/user-attachments/assets/85e5e1a0-fc21-4f18-ae95-9cc69d4a2961)

