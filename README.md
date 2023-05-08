# EX-05-Feature-Generation


# AIM :

To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation :

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM :

## STEP 1 :

Read the given Data

## STEP 2 :

Clean the Data Set using Data Cleaning Process

## STEP 3 :

Apply Feature Generation techniques to all the feature of the data set

## STEP 4 :

Save the data to the file


# CODE :

## DEVELOPED BY : ABRIN NISHA A
## REG NO : 212222230005

## Encoding Data.csv :

```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```


## data.csv :

```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```

## titanic_dataset.csv :

```
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```

# OUTPUT :

## Encoding Data.csv :

## df.head() :

![Screenshot 2023-05-08 105026](https://user-images.githubusercontent.com/118889454/236740396-8f9b2b9e-c34d-48ed-8342-a70ac341128f.png)

## Ordinal encoder :

![Screenshot 2023-05-08 105131](https://user-images.githubusercontent.com/118889454/236740498-38e22002-ab28-4add-ba42-4edb7bf586e8.png)

## Label encoder :

![Screenshot 2023-05-08 105217](https://user-images.githubusercontent.com/118889454/236740594-ef963106-c9b0-4426-a212-4b9a9ca1dcf9.png)

## Binary encoder :

![Screenshot 2023-05-08 105306](https://user-images.githubusercontent.com/118889454/236740787-1e8a6496-32be-44b0-a665-ae37b7ed5228.png)

![Screenshot 2023-05-08 105428](https://user-images.githubusercontent.com/118889454/236740884-b32fafe7-2c1a-4863-a4a4-2a3917ff2449.png)

## data.csv :

## df.head() :

![Screenshot 2023-05-08 105642](https://user-images.githubusercontent.com/118889454/236741182-88427b84-6689-44ba-972f-5696b44750d8.png)

## Ordinal encoder :

![Screenshot 2023-05-08 105752](https://user-images.githubusercontent.com/118889454/236741371-6d5fdb87-f5de-4db4-bde6-26fb4da7c754.png)

![Screenshot 2023-05-08 105802](https://user-images.githubusercontent.com/118889454/236741396-4f6f6d0d-db55-4981-bc3b-a51cfaa93928.png)

## Label encoder :

![Screenshot 2023-05-08 105948](https://user-images.githubusercontent.com/118889454/236741577-b2839b62-0608-4bc6-96d0-2bfb821dbfaf.png)

## Binary encoder :

![Screenshot 2023-05-08 110207](https://user-images.githubusercontent.com/118889454/236741869-85a5dfe3-58f1-4f19-809e-54a4b13e8dc1.png)

![Screenshot 2023-05-08 110403](https://user-images.githubusercontent.com/118889454/236742079-40566a92-9011-4e9c-a50d-6bf7b6b4be65.png)


## titanic_dataset.csv :

## df.head() :

![Screenshot 2023-05-08 110603](https://user-images.githubusercontent.com/118889454/236742323-756daa19-c5bd-4a5c-9265-c23688dc981e.png)

## Binary encoder :

![Screenshot 2023-05-08 110731](https://user-images.githubusercontent.com/118889454/236742466-b37ca9b0-f28b-4867-b9c0-21bdf9e487a7.png)

# RESULT:

The Feature Generation process was performed and saved the data to a file.
 



