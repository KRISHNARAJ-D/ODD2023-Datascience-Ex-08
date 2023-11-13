# Ex-08-Data-Visualization-
# AIM

To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
- STEP 1:
 Read the given Data
- STEP 2:
 Clean the Data Set using Data Cleaning Process
- STEP 3:
 Apply Feature generation and selection techniques to all the features of the data set
- STEP 4:
 Apply data visualization techniques to identify the patterns of the data.

# PROGRAM:
```
Developed By: KRISHNARAJ D  
Reg No: 212222230070
```
### READING THE GIVEN FILES
```python
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
### DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
- <B>_LINE PLOT:_</B>
```python
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
![280221142-ebf5d018-c31c-4610-b26e-6395daeb5448](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/37675db6-570a-441f-aab9-79aefa10193a)
![280221177-f50bd4c8-8840-4d61-afa9-f090d98716d2](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/4e77110a-466e-48cc-b876-7fc8e6adc23b)

![280221197-dddc0ce1-5d37-463d-af9d-d9a39cf33def](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/1fcc416b-f6f5-4e8b-acf0-91344f349d93)

- <B>_SCATTERPLOT:_</B>
```python
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221332-23b30b9e-cb60-4dd5-a7a7-be941b7e291d](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/0f4ef7af-a50e-4a26-b043-041f93f2e1f6)
![280221367-e422342a-4fff-487e-9780-aa92e2db6b19](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/08b7d64e-ea1f-48ac-92af-3d094ecdb230)
![280221405-8f9e780a-bcdd-47e0-a21e-25e8dca37cab](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/70c21362-8327-400b-8674-5af7bbe9dcf4)

- <B>_BOXPLOT:_</B>
```python
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
![280221591-68af3f52-c256-452b-b987-afc6767d09ac](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/d1507a94-712c-4baa-84fc-925302f8e82d)
![280221620-27f1e245-2725-436d-a68b-df3b3c5c1660](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/d0bdd19d-7772-4cdf-a0b1-1c07ec86ae02)


- <B>_VIOLIN PLOT:_</B>
```python
sns.violinplot(x="Profit",data=df)
```
![280221737-19b590d7-641d-47ed-af0f-40e52df39587](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/d133765c-5e00-454b-9814-d7c8a811690f)


- <B>_BARPLOT_</B>
```python
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221836-16ece634-b224-42df-82be-c4a731f908af](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/1ac00b48-eada-43a6-8e82-23b87a48dc65)
![280221914-32fcf2ae-85be-4bfa-bacb-0839304efe5b](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/3e4ab63a-6478-460f-82d2-5a678adfd0d9)


- <B>_POINTPLOT_</B>
```python
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
![280222052-cc5c01fb-bc88-4f6e-8f53-08e45f679e08](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/f5d2cae8-82bd-415e-83da-96423381afc0)


- <B>_COUNT PLOT_</B>
```python
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
![280222076-b6e8298d-0a6c-4a58-85b6-6a0e5c53508f](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/75369dea-0426-4aee-bd91-3edf6ba1b8b2)
![280222076-b6e8298d-0a6c-4a58-85b6-6a0e5c53508f](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/3619240c-9187-49f3-88d8-a7cdf6fde707)


- <B>_HISTOGRAM_</B>
```python
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
![280222156-6e5a4fab-1cfd-4415-9a76-6e398571742b](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/dccccd2a-034a-41e3-b0ba-3364c5c30b5b)

- <B>_KDE PLOT_</B>
```python
sns.kdeplot(x="Profit", data = df,hue='Category')
```
![280222235-2129a043-381c-4b04-a0da-5b6745ba0adf](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/da2d6acd-ac15-4f42-add6-aa7560ec2991)


### DATA VISUALIZATION USING MATPLOTLIB :
- <B>_PLOT_</B>
```python
plt.plot(df['Category'], df['Sales'])
plt.show()
```
![280224173-5f621aad-c520-4e01-96cf-1701acefa1e7](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/32581e64-aea3-4091-b56a-8c4c400fd751)


- <B>_HEATMAP:_</B>
```python
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
![280224277-d133809e-1704-4f91-8332-0041d7ca3e33](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/a16a6eee-0f32-454f-8e65-5414c2e10752)


- <B>_PIECHART:_</B>
```python
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
![280224381-09b81541-1b03-4017-bd64-e20c6894898b](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/9d3292ff-64d6-4080-acd5-dcb8c71c56ff)
![280224408-76eb96a0-0bec-4d40-af21-f906b45b9c16](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/c4b98f83-7916-44b0-9123-019f83a886e3)


- <B>_HISTOGRAM:_</B>
```python
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
![280224500-5d549a00-18a3-4126-af87-1652098f826d](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/5231b3ee-9d3f-44be-a9a2-7a8cfabe9f23)


- <B>_BARGRAPH:_</B> 
```python
plt.bar(df.index,df['Category'])
plt.show()
```
![280224538-bee209ed-e0f9-4968-94c7-babc9140edfb](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/06e2838f-0ed3-4ec8-b1ae-9f8728558719)


- <B>_SCATTERPLOT:_</B>
```python
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
![280224583-82653e8a-3f2a-4a58-ae41-0631925cd402](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/8b0ffcab-3741-49a3-9315-bb98e9ec7a89)


- <B>_BOXPLOT:_</B>
```python
plt.boxplot(x="Sales",data=df)
plt.show()
```
![280224625-9515bcd2-15ba-453a-a02e-e3e6e3ea875c](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex-08/assets/119559695/ce7fe0d4-c468-469a-8896-6c8007d04117)

# RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
