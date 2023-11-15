# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE
```
Developed By: DIVYA.K
Reg No: 212222230035
```
READING THE GIVEN FILES
```
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
DATA VISUALIZATION USING SEABORN:
```
import seaborn as sns
from matplotlib import pyplot as plt
```
LINE PLOT:
```
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```




![280221142-ebf5d018-c31c-4610-b26e-6395daeb5448](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/dace3322-a1d0-42d2-9e6c-f2bdb1373e7b)





![280221197-dddc0ce1-5d37-463d-af9d-d9a39cf33def](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/6c548d4d-147b-4fc9-9e55-ddc44e5108a4)

SCATTERPLOT
```
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```



![280221332-23b30b9e-cb60-4dd5-a7a7-be941b7e291d](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/704f41c6-9e87-49a5-b6c8-2cf28858f12f)



![280221367-e422342a-4fff-487e-9780-aa92e2db6b19](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/971a4945-c661-4eb6-b402-d620d754dca6)



![280221405-8f9e780a-bcdd-47e0-a21e-25e8dca37cab](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/e25c95e0-1f96-481a-99cc-cf805fcda379)


BOXPLOT:
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```


![280221591-68af3f52-c256-452b-b987-afc6767d09ac](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/5429ba3e-5958-48eb-b5ef-0ab6e897bb92)


![280221620-27f1e245-2725-436d-a68b-df3b3c5c1660](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/d0809678-25a2-437e-82cc-586968b37a81)

VIOLIN PLOT:
```
sns.violinplot(x="Profit",data=df)
```

![280221737-19b590d7-641d-47ed-af0f-40e52df39587](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/e9d4dc2f-190c-4ba3-a340-8d3704b38482)

BARPLOT:
```
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```



![280221836-16ece634-b224-42df-82be-c4a731f908af](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/4706b119-0475-46d9-8891-7d0d9d7a1daa)



![280221914-32fcf2ae-85be-4bfa-bacb-0839304efe5b](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/33a071f1-03ef-4e12-8dad-95d939350946)


POINTPLOT
```
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```




![280222052-cc5c01fb-bc88-4f6e-8f53-08e45f679e08](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/bd39871b-879f-4088-b0df-1a6494ed9e7f)

COUNT PLOT:
```
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```



![280222076-b6e8298d-0a6c-4a58-85b6-6a0e5c53508f](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/87d3fec3-fcd8-4d6b-9f5e-867c17b73228)

![280222110-a9e07021-4889-490c-8451-69864bf6f778](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/f49fcf87-e033-42bf-8b37-a8d8c397a8c8)

HISTOGRAM:
```

sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
```


![280222156-6e5a4fab-1cfd-4415-9a76-6e398571742b](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/d8542732-4e7e-4c02-828b-18ef0cddd3a7)


KDE PLOT:
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```

![280222235-2129a043-381c-4b04-a0da-5b6745ba0adf](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/b4a98962-2fa8-4590-9aae-aac256bf80a2)

### DATA VISUALIZATION USING MATPLOTLIB:

PLOT
```
plt.plot(df['Category'], df['Sales'])
plt.show()
```
![280224173-5f621aad-c520-4e01-96cf-1701acefa1e7](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/1678eca5-73ac-4467-be9e-d7b9882346d1)

HEATMAP:
```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```

![280224277-d133809e-1704-4f91-8332-0041d7ca3e33](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/9cf0d58f-fc61-4d2e-9d24-2859df7f56ba)

PIECHART:
```
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```


![280224381-09b81541-1b03-4017-bd64-e20c6894898b](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/f3fb8197-b825-46c6-99d5-7bb4e7534d1a)






![280224408-76eb96a0-0bec-4d40-af21-f906b45b9c16](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/138bca70-1f59-446e-93a5-c1194459e183)


HISTOGRAM:
```
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```

![280224500-5d549a00-18a3-4126-af87-1652098f826d](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/5bdd57cd-1bef-475b-829b-13a4417319e2)


BARGRAPH:
```
plt.bar(df.index,df['Category'])
plt.show()
```



![280224538-bee209ed-e0f9-4968-94c7-babc9140edfb](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/87f79802-2fe5-4e0e-88f9-f55199436d7f)

SCATTERPLOT:
```

plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show()
```


![280224583-82653e8a-3f2a-4a58-ae41-0631925cd402](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/89506c40-bb6f-4b29-bb4a-f10c83590796)


BOXPLOT:
```
plt.boxplot(x="Sales",data=df)
plt.show()
```


![280224625-9515bcd2-15ba-453a-a02e-e3e6e3ea875c](https://github.com/divyakumars/ODD2023-Datascience-Ex-08/assets/119393621/b1a35116-458c-48f3-8ed0-482bc02af10b)


### RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.




