# Ex-04-Multivariate-Analysis
AIM:

To apply multivariant analysis on the given data set.

ALGORITHM:

1.start

2.read the dta from the file

3.clean the data a)remove outliers b)fill the null value or drop the column

4.perform multivariate analysis a)scatter plot b)box plot c)heat map

CODE:

ISNULL.SUM():

![image](https://user-images.githubusercontent.com/95408668/192772748-39be029b-361d-4f64-8991-b3ec937a539a.png)

DTTYPES:

 ![image](https://user-images.githubusercontent.com/95408668/192774808-ef42604c-e5e0-444b-adc4-82d70797387c.png)

KURTOSIS:

![image](https://user-images.githubusercontent.com/95408668/192774866-203f3bfb-e494-4048-8c37-4dafc1dc8d4a.png)

BOX PLOT:

![image](https://user-images.githubusercontent.com/95408668/192774973-9dce762e-cc2e-4101-8cc6-e075feb3b61a.png)

BARPLOT:

 ![image](https://user-images.githubusercontent.com/95408668/192775064-1828556e-11e2-4235-bea3-787c2f2a3fad.png)

 BOXPLOT:
 
import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

states=df.loc[:,["Postal Code","Sales"]]

states=states.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Postal Code")

plt.ylabel=("Sales")

plt.show()

![image](https://user-images.githubusercontent.com/95408668/192775131-968fbba1-d84d-4c28-9499-a0f582f875a8.png)

CODE:

import pandas as pd

import seaborn as sns 

import matplotlib.pyplot as plt

states=df.loc[:,["State","Postal Code"]]

states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Sales")

plt.ylabel=("Postal Code")

plt.show()

![image](https://user-images.githubusercontent.com/95408668/192775258-befdb180-7d0f-4322-aa9f-6aec9c606db5.png)

KURTOSIS:

![image](https://user-images.githubusercontent.com/95408668/192775370-1a972199-5cfc-4213-b45b-b2660d882825.png)

CODE:

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/SuperStore.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

![image](https://user-images.githubusercontent.com/95408668/192775456-ed2ae855-df24-4632-9a88-2635775f3613.png)

