# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file


# CODE

### DATA_SET.CSV FILE

```python
import pandas as pd
import numpy as np
df = pd.read_csv("/content/Data_set.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['show_name'] = df['show_name'].fillna(df['show_name']).mode()[0]
df['aired_on'] = df['aired_on'].fillna(df['aired_on']).mode()[0]
df['original_network'] = df['original_network'].fillna(df['original_network']).mode()[0]
#MEAN:
df['rating'] = df['rating'].fillna(df['rating']).mean()
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank']).mean()
#FORWARD METHOD:
df['watchers'] = df['watchers'].fillna(method='ffill')
#DUPLICATES:
df.duplicated()
df.info()
df.isnull().sum()
```

### LOAN_DATA.CSV

```python
import pandas as pd
import numpy as np
df = pd.read_csv("/content/Loan_data.csv")
df.head()
df.info()
df.isnull().sum()
#MODE:
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
#MEAN:
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
#VALUE METHOD:
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(value=360.0)
#BACKWARD METHOD:
df['Credit_History'] = df['Credit_History'].fillna(method='bfill')
#DUPLICATES:
df.duplicateed()
df.info()
df.isnull().sum()
```

# OUPUT

### First File

### Data_Set.csv FILE

![Screenshot 2023-05-29 212615](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/83d08586-cbfa-48d0-90b5-de060ff36cdd)


### INFO BEFORE CLEANING

![Screenshot 2023-05-29 212436](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/a39cd744-ed52-4c54-b33e-66aa5f176b1e)


### Isnull.().sum() before cleaning

![Screenshot 2023-05-29 212746](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/3e77f930-b20f-4612-8d68-0f6bb8b4f8a9)


### MODE

![Screenshot 2023-05-29 212800](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/dc39e114-7014-4134-ba00-0e1fdc885b65)


### MEAN

![Screenshot 2023-05-29 212805](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/0c8676ae-081c-4566-b04f-5fbced11645d)


### FORWARD METHOD

![Screenshot 2023-05-29 212811](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/b21e0779-c4fe-4be5-88ea-a99aa18e7dc0)


## DUPLICATES

![Screenshot 2023-05-29 212817](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/1e75e999-7c30-436e-a384-b2a62a4fbaba)


## INFO AFTER CLEANING

![Screenshot 2023-05-29 212824](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/6f65eee3-5021-4e40-94f3-bb6b08afb3cd)


## isnull().sum() after cleaning

![Screenshot 2023-05-29 212831](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/4a090f7c-3df2-4c35-ab72-3a01b2b03ca1)


### Second File

### Loan_Data.csv FILE

![output]![Screenshot 2023-05-29 212840](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/2798f1e4-02fb-45b1-9563-571b1ebbbc0d)


### INFO BEFORE CLEANING

![Screenshot 2023-05-29 212848](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/d3140955-abff-49b2-bf71-78014c6f9aca)


### Isnull.().sum() before cleaning

![Screenshot 2023-05-29 212855](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/a5757c95-4a1d-4986-a912-fe0f8f948a9d)


## MODE

![Screenshot 2023-05-29 212900](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/4131bdc6-502e-4ec9-b36b-3867f3b74a8e)


### MEDIAN

![Screenshot 2023-05-29 212905](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/6844e74b-4807-45c9-8068-bd1a988c1ab4)


### VALUE METHOD

![Screenshot 2023-05-29 212910](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/2b6e5f5e-7f6d-4022-b04e-ae2e977295ef)


### BACKWARD METHOD

![Screenshot 2023-05-29 212914](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/8b9717a2-922e-4ce8-9b30-68029d6d3140)


### DUPLICATES

![Screenshot 2023-05-29 212919](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/3b747bf6-faba-4cb2-8b83-d72cfc8c95e1)


### INFO AFTER CLEANING

![Screenshot 2023-05-29 212930](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/fe38cb97-eeef-488c-8f62-2764300bdc23)


### isnull().sum() after cleaning

![Screenshot 2023-05-29 212938](https://github.com/Nagul71/Ex-01-Data-Cleaning/assets/118661118/173a3c67-5c37-44b6-a800-3acd6c70401e)

### RESULT:
Thus the given data is read,cleansed and cleaned data is saved into the file.
