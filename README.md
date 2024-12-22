# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

## NAME: KARTHIKEYAN S
## REG NO: 24900102

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
 ~~~
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
~~~
![image](https://github.com/user-attachments/assets/aaf30255-9261-4172-9a84-d1b40476bd8e)

~~~
df = sns.load_dataset("tips")
df
~~~
![image](https://github.com/user-attachments/assets/d17c16ac-b674-484c-b879-6468f4e39efe)

~~~
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
~~~

![image](https://github.com/user-attachments/assets/f6230965-c9e9-441f-a9c4-276d5ecc75b8)

~~~
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
~~~

![image](https://github.com/user-attachments/assets/519362d1-50e3-4fd1-ab2e-1489e7ac2a71)

~~~
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
~~~

![image](https://github.com/user-attachments/assets/d97bd382-3db8-43ee-a47e-21bb99aea1ad)

~~~
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
~~~

![image](https://github.com/user-attachments/assets/00fbba6e-cac0-452f-85e8-7f8e8a388060)

~~~
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
~~~

![image](https://github.com/user-attachments/assets/b2621378-db1a-4a51-9514-40d72da1eca4)

~~~
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
~~~

![image](https://github.com/user-attachments/assets/7d4c92fe-2411-4901-b30e-8de6ce3a6821)

~~~
tit=pd.read_csv("titanic_dataset.csv")
tit
~~~


![image](https://github.com/user-attachments/assets/d126d150-edca-4c44-9bf8-86f385afa40a)

~~~
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
~~~

![image](https://github.com/user-attachments/assets/098b7aa4-7687-407e-8f8d-d4881424f246)

~~~
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
~~~

![image](https://github.com/user-attachments/assets/6b95a3b9-befd-4c86-b729-c43b9af4c32f)

~~~
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
~~~

![image](https://github.com/user-attachments/assets/03608325-f8ce-4f05-af23-e783a05a014e)

~~~
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
~~~

![image](https://github.com/user-attachments/assets/88eaefa5-5d7f-452b-aac9-cace6c88b2c1)

~~~
sns.histplot(data = num_var, kde = True)
~~~

![image](https://github.com/user-attachments/assets/a14a4c93-651f-4660-a6a2-22e0a784cfa2)

~~~
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
~~~

![image](https://github.com/user-attachments/assets/1a326511-8230-497e-b336-6db927faeb99)

~~~
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
~~~

![image](https://github.com/user-attachments/assets/385a5dbf-c3ab-4386-b88a-94c371ad57c7)

~~~
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
~~~

![image](https://github.com/user-attachments/assets/6bee7c54-6c7c-41b7-8518-3dcb423bcb78)

~~~
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
~~~

![image](https://github.com/user-attachments/assets/8751acc0-9688-4276-a3d0-bf24b68631be)

~~~
mart=pd.read_csv("titanic_dataset.csv")
mart
~~~

![image](https://github.com/user-attachments/assets/2b31b33a-6e22-4125-8b0d-f5b2cff5c263)

~~~
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
~~~


![image](https://github.com/user-attachments/assets/3f0a3d8a-eaa0-4dd0-aecf-18994ea6f2a4)

~~~
sns.kdeplot(data=mart,x='PassengerId')
~~~

![image](https://github.com/user-attachments/assets/4d071e96-0844-4dc4-9d5e-4604f8c54f40)

~~~
sns.kdeplot(data=mart,x='Age')
~~~

![image](https://github.com/user-attachments/assets/f03f5052-e1d8-43b9-88f0-6962a5a29bf8)

~~~
sns.kdeplot(data=mart)
~~~

![image](https://github.com/user-attachments/assets/150dfcaf-b6e5-49f8-9a51-db9bd43c8612)

~~~
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
~~~

![image](https://github.com/user-attachments/assets/4bed611f-ef97-4ba7-8552-d7e350dffbb9)

~~~
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
~~~

![image](https://github.com/user-attachments/assets/9b83559f-a3a0-45f4-9562-9fd076ed483f)

~~~
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
~~~

![image](https://github.com/user-attachments/assets/688dea32-f930-4fa5-aecc-f49cf3bbd9bd)

~~~
hm=sns.heatmap(data=data)
~~~

![image](https://github.com/user-attachments/assets/dbeff466-47b3-4c06-86c9-392e6522b45c)


































# Result:
Thus, all the data visualization techniques of seaborn has been implemented.


