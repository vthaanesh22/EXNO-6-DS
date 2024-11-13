# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
### NAME:THAANESH V
### REGNO:212223230228

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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/ac82e627-2826-41d1-80d0-c739f4a2b39a)


```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/4fac837b-1e15-4703-af09-cc950e9b2d97)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/5c1f2890-70e9-4725-a3ea-abee8cd7113b)
```
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
```
![image](https://github.com/user-attachments/assets/ba3ebd39-9c4e-4d32-a9ec-3ac7f4b89cd1)
```
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
```
![image](https://github.com/user-attachments/assets/4790b465-40ca-4cdd-b37d-c74089fa5a48)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/b9460255-5fb1-43f9-8abf-0138861b238d)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)

```
![image](https://github.com/user-attachments/assets/25f0eab0-d0db-4aad-8e8f-3306e698e8ea)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/b78dd4f3-ee21-44f2-9db4-1558a7bc426b)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/1052b40c-6f58-4fdd-b165-cd26778b85ea)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/c3c1407b-6370-490a-a4c0-81bcd698b03b)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/b385be57-4392-435b-b90e-07106aee48b7)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/0841f74e-ccbe-47b5-b34a-d8d88ce3a9ca)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/49152e24-2eec-4d78-bd8c-349cf1252cce)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/7277d38e-4a03-4e26-a077-54086e9f3697)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/40025ac0-4090-4b71-9681-288f2fce398b)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![image](https://github.com/user-attachments/assets/95019ffc-15c5-4cef-ba14-79c7202b3965)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![image](https://github.com/user-attachments/assets/1a687d24-bda2-4eef-afe4-7d90e8983c13)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/12933f81-26eb-459b-a80a-ca282c5f1c7a)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

![image](https://github.com/user-attachments/assets/ddc08603-4d22-4e76-a4aa-3b055edca8cb)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

![image](https://github.com/user-attachments/assets/e89ab100-359d-4fa6-9d96-e43d6eed89fc)
```
sns.kdeplot(data=mart,x='PassengerId')
```

![image](https://github.com/user-attachments/assets/13c0647b-0b25-4a9e-88d4-b1be4b46f9e7)

```

sns.kdeplot(data=mart,x='Age')
```

![image](https://github.com/user-attachments/assets/2164d956-0c94-44d0-ae61-341be1ca8704)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/0596cd5e-55a9-4297-bc09-888da081879f)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/0378fdf7-9f3e-4606-9fed-3da6fac5f13a)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/64a09f16-d0f1-4a87-8ab7-0c16297e52c8)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/35b2bacd-cad8-4479-8814-2a9974a45753)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/91a4e8f1-bb8b-4c6e-b2a6-93a98d0a25a1)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
