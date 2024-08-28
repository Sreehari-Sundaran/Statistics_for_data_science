**Statistics Behind Plots**

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

