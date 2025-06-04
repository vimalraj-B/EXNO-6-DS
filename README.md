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
import seaborn as sns import matplotlib.pyplot as plt
df=sns.load_dataset("tips")
df
```
![435431965-47b224dc-8448-43b0-89ce-40530ccf1e8d](https://github.com/user-attachments/assets/50b4db0b-93c1-4f3b-98ac-ad991c17bbb3)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex", linestyle="solid", legend="auto", palette="Set1")
```

![435431978-769feaaa-b476-448f-a77e-f69fb5d8a50f](https://github.com/user-attachments/assets/edbda7be-588c-4d18-84c8-e3c14f0eeb57)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day") ["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
```
![435432001-a9846818-111b-431d-a245-8ebaf0ea8d87](https://github.com/user-attachments/assets/21248a6d-2152-4f6f-b623-a2fe5e38c988)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill, label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```

![435432025-dfef54a0-93ee-4849-b9bc-f655c03b35c9](https://github.com/user-attachments/assets/c8745450-776c-4df9-b78b-f9a863e2e90f)

```
avg_total_bill=tips.groupby('time') ['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
```
![435432036-0d383df5-5e0d-41f3-87fa-62f0970721a9](https://github.com/user-attachments/assets/239a4528-61ad-4771-aae7-d7403c148790)

```
p1=plt.bar(avg_total_bill.index,avg_total_bill, label="Total Bill",width=0.4)
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip", width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```
![435432042-dc095d56-c476-483a-8429-15ca71c1d852](https://github.com/user-attachments/assets/803fa9bb-ea41-4218-9da5-5445c9a4cd7e)

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill", hue="sex", data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
![435432050-1d358f73-5f2e-419c-852e-69ddb287ff5b](https://github.com/user-attachments/assets/95c4e259-0ac3-4569-9e0d-97af662d6f3b)

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip", hue="sex", data=df, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```
![435432066-525cb59d-a824-4fcd-aa90-4caba71d3c7f](https://github.com/user-attachments/assets/fae20e07-9b95-4059-89ff-4386201aec4b)

```
sns.histplot(data=df,x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
![435432084-0375a63e-6aa7-4134-b495-5f9d4288ee84](https://github.com/user-attachments/assets/b1795f0e-231a-4857-acf2-0d96ed3f09e2)

```
import seaborn as sns
import pandas as pd
df=sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')
```
![435432096-ba02e77d-9caa-467e-9874-465349c58863](https://github.com/user-attachments/assets/10837351-121e-4093-bb1a-c0d0447c8c80)

```
sns.boxplot (x="day",y="total_bill", hue="smoker",
        data=df, linewidth=2,width=0.6,
        
        fliersize=7, flierprops={"marker":"o", "markerfacecolor":"grey"},
        
        boxprops={"facecolor":"red", "edgecolor":"black"}, 
        
        whiskerprops={"color":"darkblue", "linestyle":"--", "linewidth":2},
        
        capprops={"color":"darkblue","linestyle":"-","linewidth": 2},palette="Set1")
```
![435432109-7a3053d2-25be-493d-9f20-855aca23c166](https://github.com/user-attachments/assets/588066e7-883d-42d5-874a-2069d53b5c0e)

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette='Set1',inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![435432128-dea564ac-0e5e-4d26-b5a9-c57032fbd147](https://github.com/user-attachments/assets/65f3f07c-aceb-4fc1-a983-f520f8d1d4ba)

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset('tips')
sns.violinplot(x = 'day', y = 'tip', data = tip, palette="Set2")
```
![435432135-355430c4-6efd-4629-ba8a-cfd2330fcf81](https://github.com/user-attachments/assets/8510ab05-418c-44a0-8983-0f3dc97c7386)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"], palette="Set1")
```
![435432146-1f8ad803-117c-42e3-9f18-92ab4dc5ba73](https://github.com/user-attachments/assets/5174df59-f11f-47f7-948d-cd55acf8b471)

```
import seaborn as sns
sns.set(style="whitegrid")
tips = sns.load_dataset("tips")
sns.violinplot(x="tip", y="day", data=tip, palette="rainbow")
```
![435432160-f866a5dc-2420-4a6c-a82c-49a38dc44265](https://github.com/user-attachments/assets/b8dd0053-7629-4848-bc69-028933fce201)

```
sns.kdeplot(data=tips,x='total_bill', hue='time', multiple="layer", linewidth=3, palette='Set2', alpha=0.8)
```
![435432169-43f7c984-8098-4e28-b090-01eb19916ce7](https://github.com/user-attachments/assets/78028b05-0eeb-4123-8dbc-71e010efbefc)

```
sns.kdeplot(data=tips,x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set3',alpha=0.8)
```
![435432189-49f722d9-1782-4b8b-a090-1bd2a7913e56](https://github.com/user-attachments/assets/b7a3a05d-8eaa-4961-bab8-3c541f418116)

```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=3, palette='Set1', alpha=0.8)
```
![435432213-90bd8375-2d21-4ca3-9e9d-82587b27f456](https://github.com/user-attachments/assets/65465c9f-4824-4354-b0a3-61643e56c18b)

```
import seaborn as sns
tip = sns.load_dataset('tips')
num=tips.select_dtypes (include=['float64', 'int64']).columns
corr=tips[num].corr()
sns.heatmap (corr, annot=True, cmap="YlGnBu")
```
![435432229-0f6ce553-b7f8-47bb-948d-30c680052bcd](https://github.com/user-attachments/assets/475eecfb-4751-4f5b-91af-c9b4c20788cc)

```
sns.heatmap(corr,cmap="YlGnBu")
```
![435432243-ce3d9e25-0708-4083-a23d-826461c1e15a](https://github.com/user-attachments/assets/bc53041d-00ca-44bc-985a-50664bbbebd4)

# Result:
```
Thus the data visualization techniques of seaborn has been implemented.
```
