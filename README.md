# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
import numpy as np
import seaborn as sns
```

```
df=pd.read_csv("/content/Data_set (2).csv")
df
```
![Screenshot 2025-03-10 211726](https://github.com/user-attachments/assets/00b7d719-931d-4c3a-95dd-d61011f334b4)

```
df.info()

```

![Screenshot 2025-03-10 212018](https://github.com/user-attachments/assets/b3644d2b-a46f-4a2a-aeee-cbf0387be37b)

```
df.describe()
```

![Screenshot 2025-03-10 212331](https://github.com/user-attachments/assets/9b1575a0-f29b-47b6-a633-a044acdd3439)

```
df.head()
```

![Screenshot 2025-03-10 212443](https://github.com/user-attachments/assets/4621b498-0621-45ae-8ebd-bd0ea1d433bb)

```
df.tail()
```
![Screenshot 2025-03-10 212545](https://github.com/user-attachments/assets/94c02878-56f8-4692-85b9-2a5c6d91dfff)


```
df.tail(8)
```

![Screenshot 2025-03-10 212646](https://github.com/user-attachments/assets/0a8c7045-3081-454b-ab29-f1343f86b2f7)

```
df.isnull()

```
![Screenshot 2025-03-10 212959](https://github.com/user-attachments/assets/ef285c61-ce5d-4931-98c9-ae7060dd9f35)

```
df.notnull()
```
![Screenshot 2025-03-10 213146](https://github.com/user-attachments/assets/0190ee4b-b939-4d95-917c-17f1d1d0866d)

```
df.dropna(axis=0)
```


![Screenshot 2025-03-10 213328](https://github.com/user-attachments/assets/2c674249-6c85-4417-9cd8-a9b43883dc38)


```
df.dropna(axis=1)
```

![Screenshot 2025-03-10 213454](https://github.com/user-attachments/assets/8856dde5-7878-4c0e-bf35-18d24b23e424)

```
df[df['num_episodes']>20]
```
![image](https://github.com/user-attachments/assets/e08d6975-58c3-4728-b40d-9abfb3ca243d)

```
df.iloc[:3]
```


![Screenshot 2025-03-10 214039](https://github.com/user-attachments/assets/f2c78120-a52c-4b2f-b19e-c744d41d4c5f)

```
df.iloc[:3,3:]
```


![Screenshot 2025-03-10 214148](https://github.com/user-attachments/assets/66d1e6a9-94e7-4446-b200-6ea81e6734c4)

```
df.fillna(method='ffill')
```

![Screenshot 2025-03-10 214300](https://github.com/user-attachments/assets/0aa61a48-e582-4833-a3d3-71108275a53b)

```
df.fillna(method='bfill')
```

![Screenshot 2025-03-10 214357](https://github.com/user-attachments/assets/30ea24da-3f50-4a66-8f07-0aaff8aa785f)


```
df.iloc[[1,2,3],[1,3,5]]
```

![Screenshot 2025-03-10 214501](https://github.com/user-attachments/assets/2fc4b559-ea2f-409b-bea9-4d6d7ca09436)

```
df.fillna(df['rating'].mean())

```


![Screenshot 2025-03-10 214614](https://github.com/user-attachments/assets/f62fca43-41a9-4066-b841-219a42400c88)


```
df.isnull().any()

```

![Screenshot 2025-03-10 214702](https://github.com/user-attachments/assets/bf69ec82-af87-4444-b1b2-f7b0d4c41c8b)

```
df.notnull().any()
```

![Screenshot 2025-03-10 214834](https://github.com/user-attachments/assets/bb0e82ca-accc-43ac-8371-e1d31a9288ba)

```
df.isnull().sum()

```

![Screenshot 2025-03-10 214916](https://github.com/user-attachments/assets/bd67d172-b6cf-4251-8200-35f208882bce)

```

df.interpolate()

```

![Screenshot 2025-03-10 215031](https://github.com/user-attachments/assets/68c44822-ccca-4712-94f9-167b104cb799)

```
df.shape
```

![Screenshot 2025-03-10 215136](https://github.com/user-attachments/assets/3b3df16a-106c-432e-b7f4-1432cd8c2c8f)

```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```

![image](https://github.com/user-attachments/assets/d12f5b60-5c6f-4b63-9d1c-5580e4c1a16c)

```
sns.heatmap(df.isnull(),yticklabels=False,annot=True)

```

![Screenshot 2025-03-10 215309](https://github.com/user-attachments/assets/69221d18-7116-4d30-850a-9b3745ae894d)

```
df.dropna(inplace=True)
```
```
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
```

![Screenshot 2025-03-10 215437](https://github.com/user-attachments/assets/524f632e-7877-4985-b479-b36334d49198)

```
import pandas as pd 
import seaborn as sns
import numpy as np

```
```

age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```

![Screenshot 2025-03-10 215529](https://github.com/user-attachments/assets/08a0c9d1-b5e9-4c47-b4f4-a221797c2afc)

```
sns.scatterplot(data=af)
```

![Screenshot 2025-03-10 215612](https://github.com/user-attachments/assets/b84d21d1-fbea-4144-afdf-f3726efae303)

```
q1=af.quantile(0.25)
q2=af.quantile(0.5)
q3=af.quantile(0.75)
iqr=q3-q1
iqr
```

![Screenshot 2025-03-10 215644](https://github.com/user-attachments/assets/477d1f9c-b4d7-412c-972e-588b98bfc6bf)

```
Q1=np.percentile(af,25)
Q3=np.percentile(af,75)
IQR=Q3-Q1
IQR
```

![Screenshot 2025-03-10 215729](https://github.com/user-attachments/assets/970e14bb-f667-496e-afdf-ca374b1183ed)

```
lower_bound=Q1-1.5*IQR
upper_bound=Q3+1.5*IQR

```
```
outliers=[x for x in age if x<lower_bound or x>upper_bound]
```
```
print("Q1: ",Q1)
print("Q3: ",Q3)
print("IQR: ",IQR)
print("Lower_bound: ",lower_bound)
print("Upper_bound: ",upper_bound)
print("Outliers: ",outliers)

```

![Screenshot 2025-03-10 215948](https://github.com/user-attachments/assets/9f884afd-46fe-4b60-9423-f59b35eea6f9)

```
sns.scatterplot(data=af)
```

![Screenshot 2025-03-10 220027](https://github.com/user-attachments/assets/d8ff85af-d0f4-454e-9a14-3b3d48b38a65)

```
import pandas as pd 
import numpy as np
import seaborn as sns
from scipy import stats

```
```
data={'weight':[12,15,18,21,24,27,30,33,36,39,42,45,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}
df=pd.DataFrame(data)
df

```
![image](https://github.com/user-attachments/assets/66b901a0-c771-4a73-adf4-529259bf0be0)

```
z=np.abs(stats.zscore(df))
z
```
![image](https://github.com/user-attachments/assets/beb8c785-a386-4b39-8428-3d0bcd37203a)

```
print(df[z['weight']>3])
```

![Screenshot 2025-03-10 220403](https://github.com/user-attachments/assets/1a0fffa3-bed0-4cca-a478-51052adbbe30)

```
import numpy as np
val=[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]
```
```
#zscore implementation without stats method
out=[]
def d_o(val):
    ts=3
    m=np.mean(val)
    sd=np.std(val)
    for i in val:
        z=(i-m)/sd
        if np.abs(z)>ts:
            out.append(i)
    return out 

```
```
op= d_o(val)

```

```
op
```

![Screenshot 2025-03-10 220558](https://github.com/user-attachments/assets/c8217ecc-1ac6-4a1f-a480-f08a85a61f22)

# Result
         Thus we have read and cleaned the data and also removed the outliers by detection using IQR and Z-score method.
