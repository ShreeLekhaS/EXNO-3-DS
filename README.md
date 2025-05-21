# EXNO-3-DS

# AIM:
To read the given data and perform Feature Encoding and Transformation process and save the data to a file.

# ALGORITHM:
STEP 1:Read the given Data.
STEP 2:Clean the Data Set using Data Cleaning Process.
STEP 3:Apply Feature Encoding for the feature in the data set.
STEP 4:Apply Feature Transformation for the feature in the data set.
STEP 5:Save the data to the file.

# FEATURE ENCODING:
1. Ordinal Encoding
An ordinal encoding involves mapping each unique label to an integer value. This type of encoding is really only appropriate if there is a known relationship between the categories. This relationship does exist for some of the variables in our dataset, and ideally, this should be harnessed when preparing the data.
2. Label Encoding
Label encoding is a simple and straight forward approach. This converts each value in a categorical column into a numerical value. Each value in a categorical column is called Label.
3. Binary Encoding
Binary encoding converts a category into binary digits. Each binary digit creates one feature column. If there are n unique categories, then binary encoding results in the only log(base 2)ⁿ features.
4. One Hot Encoding
We use this categorical data encoding technique when the features are nominal(do not have any order). In one hot encoding, for each level of a categorical feature, we create a new variable. Each category is mapped with a binary variable containing either 0 or 1. Here, 0 represents the absence, and 1 represents the presence of that category.

## Methods Used for Data Transformation:
  ## 1. FUNCTION TRANSFORMATION
• Log Transformation
• Reciprocal Transformation
• Square Root Transformation
• Square Transformation
  ## 2. POWER TRANSFORMATION
• Boxcox method
• Yeojohnson method

## CODING AND OUTPUT:
```
import pandas as pd
import numpy as np

df=pd.read_csv('data.csv',usecols=['Ord_1','Ord_2'])
df.head()
```
![image](https://github.com/user-attachments/assets/a6baeda4-a87f-432f-9f5d-76b1bcec8aa0)

```
df.shape
```
![image](https://github.com/user-attachments/assets/5106abde-3c6c-4b8a-a551-0612fcfceaf8)

```
pd.get_dummies(df).shape
```
![image](https://github.com/user-attachments/assets/47a70f2b-67dd-4146-959c-71b2a10d1575)

```
len(df['Ord_1'].unique())
```
![image](https://github.com/user-attachments/assets/606606dc-41fd-444a-beb2-24fbf52d8779)

```
len(df['Ord_2'].unique())
```
![image](https://github.com/user-attachments/assets/a5aebdbb-f14d-4a17-a06a-c1142e0b7b17)
```
for col in df.columns[0:]:
    print(col,':',len(df[col].unique()),'labels')
```
![image](https://github.com/user-attachments/assets/9cb4b753-8804-45c2-8462-4d511532083c)

```
df.Ord_2.value_counts().to_dict()
```
![image](https://github.com/user-attachments/assets/3c52caea-0e19-4a35-a8af-1fcbf1df73b0)

```
df_frequency_map=df.Ord_2.value_counts().to_dict()

df.Ord_2=df.Ord_2.map(df_frequency_map)
df.head()
```
![image](https://github.com/user-attachments/assets/3785259d-d230-4316-9843-fa6df41729fa)

# RESULT:
       Thus the given data and performing Feature Encoding and Transformation process was executed successfully

       
