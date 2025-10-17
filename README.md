Name : B Harshala Reddy

Reg no. : 212224040050
 
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
import seaborn as sns
import matplotlib.pyplot as plt
df = sns.load_dataset("tips")
df
```
<img width="1353" height="615" alt="1" src="https://github.com/user-attachments/assets/a8bff1d7-2d02-4208-aa3a-084476987067" />

```
sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto", palette="Set1")
```
<img width="1394" height="643" alt="2" src="https://github.com/user-attachments/assets/1925fde7-e8b6-4953-8d29-8f2be5346264" />

```
x = [1,2,3,4,5]
y1 = [3,5,2,6,1]
y2 = [1,6,4,3,8]
y3 = [5,2,7,1,4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
```
<img width="1253" height="770" alt="3" src="https://github.com/user-attachments/assets/6b0ed751-2ea3-487b-85bd-948f3381fd43" />

```
tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip = tips.groupby("day")["tip"].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index, avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index, avg_tip,bottom=avg_total_bill, label='Tip')
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```
<img width="1074" height="770" alt="4" src="https://github.com/user-attachments/assets/e72b235c-1883-45c8-9dee-21fabe8e728b" />

```
avg_total_bill = tips.groupby("time")["total_bill"].mean()
avg_tip = tips.groupby("time")["tip"].mean()
p1=plt.bar(avg_total_bill.index, avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index, avg_tip,bottom=avg_total_bill, label='Tip',width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```
<img width="949" height="648" alt="5" src="https://github.com/user-attachments/assets/e29e52b1-a0aa-4784-81a4-41f65c8ae28b" />

```
import seaborn as sns
df = sns.load_dataset("tips")
sns.barplot(x="day", y="total_bill", hue="sex",data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
<img width="962" height="626" alt="6" src="https://github.com/user-attachments/assets/67358930-1e93-4bfe-a222-1fe46f72ba5c" />

```
import seaborn as sns
df = sns.load_dataset("tips")
sns.scatterplot(x="total_bill", y="tip", hue="sex",data=df,palette='Set1')
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```
<img width="931" height="627" alt="7" src="https://github.com/user-attachments/assets/810474a6-04d8-427f-b785-b2c8ed57aaba" />

```
sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette='Set1')
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
<img width="967" height="591" alt="8" src="https://github.com/user-attachments/assets/0c396500-edd9-494c-a11d-bbceaab68d10" />

```
import seaborn as sns
import pandas as pd
df = sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill',hue='sex',data=df, palette='Set2')
```
<img width="1055" height="629" alt="9" src="https://github.com/user-attachments/assets/2994501b-d9b4-4b59-a432-454d02d7806d" />

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette="Set1")
```
<img width="1280" height="640" alt="10" src="https://github.com/user-attachments/assets/f148f777-b66d-45fc-adcb-b368679150a4" />

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set1",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
<img width="1100" height="648" alt="11" src="https://github.com/user-attachments/assets/e922525e-bc1e-47aa-a528-e12d3a86b5b6" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="day", y="tip", data=tip, palette="Set2")
```
<img width="1010" height="647" alt="12" src="https://github.com/user-attachments/assets/656a16a4-3977-4d00-b220-a698642d59a3" />


```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x=tip["total_bill"],palette="Set1")
```
<img width="1234" height="709" alt="13" src="https://github.com/user-attachments/assets/9927c6bd-3754-412b-9859-f9aae9b255db" />
```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")
```
<img width="1125" height="699" alt="14" src="https://github.com/user-attachments/assets/b057c0d0-d590-478f-9566-d2d9da42dd76" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
```
<img width="1278" height="658" alt="15" src="https://github.com/user-attachments/assets/415869df-a871-4383-9db4-a7d484f042b9" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="stack",linewidth=3,palette="Set3",alpha=0.8)
```
<img width="1291" height="656" alt="16" src="https://github.com/user-attachments/assets/b108ce30-fc51-4f98-aae0-418a2485c767" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="fill",linewidth=3,palette="Set1",alpha=0.8)
```
<img width="1271" height="657" alt="17" src="https://github.com/user-attachments/assets/5e9621bf-99cb-4010-b59c-f2ec181f61c0" />

```
import seaborn as sns
tip = sns.load_dataset("tips")
num = tips.select_dtypes(include=['float64','int64']).columns
corr = tips[num].corr()
sns.heatmap(corr,annot=True,cmap='YlGnBu')
```
<img width="1032" height="703" alt="18" src="https://github.com/user-attachments/assets/fcc41451-244a-4565-9bff-be29bb0ba79e" />


```
sns.heatmap(corr,cmap='YlGnBu')
```
<img width="1083" height="633" alt="19" src="https://github.com/user-attachments/assets/1e77b134-7687-4de2-9053-5458f5039d3c" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data executed successfully.

