# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
REG NO : 212224110037
NAME   : MANIKANDAN .T
```

```python
 import seaborn as sns
 
import matplotlib.pyplot as plt

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)
```
<img width="379" alt="SS 01" src="https://github.com/user-attachments/assets/d097f43f-31ce-4044-9afc-45b840778c32" />

```python
df=sns.load_dataset("tips")

df
```
<img width="398" alt="SS 02" src="https://github.com/user-attachments/assets/5fb1850d-0c94-4d32-ad18-07d49d2a6cb0" />

```python
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
<img width="499" alt="SS 03" src="https://github.com/user-attachments/assets/835d25e5-f08c-423b-a804-e0e15a8c23db" />

```python
x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title('Multi-Line plot')

plt.plot('X Label')

plt.plot('Y Label')
```

<img width="494" alt="SS 04" src="https://github.com/user-attachments/assets/c551221e-b810-46db-a008-ce9368ed1cd4" />

```python
import seaborn as sns

import matplotlib.pyplot as plt

tips=sns.load_dataset('tips')

avg_total_bill=tips.groupby('day')['total_bill'].mean()

avg_tip=tips.groupby('day')['tip'].mean()
```

<img width="919" alt="SS 05" src="https://github.com/user-attachments/assets/ef4d99cd-4657-49c8-b884-cadd864fbcbf" />

```python
plt.figure(figsize=(8,6))

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()
```

<img width="511" alt="SS 06" src="https://github.com/user-attachments/assets/a7738c24-f55e-4528-a2e3-a66025504a1a" />

```python
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)

plt.xlabel('Time of Day')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Time of Day')

plt.legend()
```

<img width="467" alt="SS 07" src="https://github.com/user-attachments/assets/095bd85f-a79d-44f2-a86e-f4fe052af606" />

```python
years=range(2000,2012)

apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]

oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896,]

plt.bar(years, apples)

plt.bar(years, oranges, bottom=apples)
```

<img width="437" alt="SS 08" src="https://github.com/user-attachments/assets/da227072-0d5a-4257-8430-6d82b988b8de" />

```python
import seaborn as sns

dt=sns.load_dataset('tips')

sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')

plt.xlabel('Day of the week')

plt.ylabel('Total Bill')

plt.title('Total Bill by Day and Gender')
```

<img width="457" alt="SS 09" src="https://github.com/user-attachments/assets/ebdf7f41-24c3-487d-bc8a-48dbac3b69e3" />

```python
import pandas as pd

tit=pd.read_csv("/content/titanic_dataset (2).csv")

tit

```

<img width="823" alt="SS 10" src="https://github.com/user-attachments/assets/a5270fc8-3929-42a9-9b8e-d814b957e91a" />

```python
plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")
```

<img width="839" alt="SS 11" src="https://github.com/user-attachments/assets/e0024357-f2bf-4f62-ae20-7cf134bc6524" />

```python
plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')

plt.title("Fare of Passenger by Embarked Town,Divided by Class")
```

<img width="521" alt="SS 12" src="https://github.com/user-attachments/assets/ce01945d-3579-4c5b-ac08-9f8214715b3f" />

```python
import seaborn as sns

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)

plt.xlabel('Total Bill')

plt.ylabel('Tip Amount')

plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

<img width="433" alt="SS 13" src="https://github.com/user-attachments/assets/19eea5ae-6c9a-4708-8193-cf595288404b" />

```python
import seaborn as sns

import numpy as np

import pandas as pd

np.random.seed(1)

num_var=np.random.randn(1000)

num_var=pd.Series(num_var,name="Numerical variable")

num_var
```

<img width="233" alt="SS 14" src="https://github.com/user-attachments/assets/164a03ca-906e-4b86-84c6-bfd99fd92703" />

```python
sns.histplot(data=num_var,kde=True)
```

<img width="467" alt="SS 15" src="https://github.com/user-attachments/assets/a8083ac2-31ef-40a0-adf2-da7c8f87627e" />

```python
df=pd.read_csv("/content/titanic_dataset (2).csv")

df
```

<img width="775" alt="SS 16" src="https://github.com/user-attachments/assets/d85b90a8-f4bd-44e4-86ae-29ba08c0bb52" />

```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="505" alt="SS 17" src="https://github.com/user-attachments/assets/eb494131-fa71-4c7f-a5de-61d8dde547de" />

```python
import seaborn as sns

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

np.random.seed(0)

marks=np.random.normal(loc=70,scale=10,size=100)

marks
```

<img width="476" alt="SS 18" src="https://github.com/user-attachments/assets/98495158-80fd-46ce-abeb-d7a0b68b6a9b" />

```python
import seaborn as sns

import pandas as pd

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```

<img width="430" alt="SS 19" src="https://github.com/user-attachments/assets/660621e1-627a-4f6e-87b8-e0ee79b1d7e9" />

```python
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"color":"lightblue","edgecolor":"darkblue"},

whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```

<img width="821" alt="SS 20" src="https://github.com/user-attachments/assets/31b6d222-4c70-4aa7-bfcc-e8e9b5559607" />

```python
sns.set(style='whitegrid')

tip=sns.load_dataset('tips')

sns.violinplot(x='day',y='tip',data=tip)
```

<img width="428" alt="SS 21" src="https://github.com/user-attachments/assets/bfe04b7b-e3c0-4f4e-a25e-4658bdb53cc6" />

```python
sns.set(style = 'whitegrid')

tip = sns.load_dataset('tips')

sns.violinplot(x=tip["total_bill"])
```

<img width="383" alt="SS 22" src="https://github.com/user-attachments/assets/d7d01793-56b9-43a8-a9fc-c9b268bfa528" />

```python
sns.set(style="whitegrid")

tips = sns.load_dataset("tips")

sns.violinplot(x="tip", y="day", data=tip)
```

<img width="554" alt="SS 23" src="https://github.com/user-attachments/assets/5c74d08d-5d27-4b0f-9f22-df287aeaf3c5" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="461" alt="SS 24" src="https://github.com/user-attachments/assets/a9628fe7-a484-4959-95bc-485fd08e4fa3" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="514" alt="SS 25" src="https://github.com/user-attachments/assets/6c49372a-e080-4c80-b764-8f03bcce7e1d" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="561" alt="SS 26" src="https://github.com/user-attachments/assets/5ea2e93d-880e-45bf-97e3-2cbb0fff96d0" />

```python
data=np.random.randint(low=1,high=100,size=(10,10))

print("The data to be plotted:\n")

print(data)
```

<img width="221" alt="SS 27" src="https://github.com/user-attachments/assets/dcb3e219-9e69-4131-bd1d-9dddaf872b81" />

```python
hm=sns.heatmap(data=data)
```

<img width="379" alt="SS 28" src="https://github.com/user-attachments/assets/27c5a0b8-b93f-47ff-a4ef-f5538e83ab01" />

```python
tips=sns.load_dataset('tips')

numeric_cols=tips.select_dtypes(include=np.number).columns

corr=tips[numeric_cols].corr()

sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```

<img width="401" alt="SS 29" src="https://github.com/user-attachments/assets/43006a3a-d02f-4133-bf24-806b6ea77e85" />



# Result:

      Thus the Data Visualization using seaborn python library has been implemented for the given datas.

