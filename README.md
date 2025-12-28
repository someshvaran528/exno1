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
            <<include your coding and its corressponding output screen shots here>>
df=pd.read_csv("data_set.csv")
df
# OUTPUT 
<img width="1216" height="456" alt="image" src="https://github.com/user-attachments/assets/45dfa15d-5217-4bcd-8c3c-a3f676766a77" />

# CODING
df.isnull()

# OUTPUT
<img width="714" height="525" alt="image" src="https://github.com/user-attachments/assets/d0ba2039-1804-4745-81a5-2608407ebef0" />

# CODING
df.isnull().sum()

# OUTPUT
<img width="375" height="197" alt="image" src="https://github.com/user-attachments/assets/d7d10a35-83c3-4c4b-908a-876e1f3e9d53" />

# CODING
df.notnull()

# OUTPUT
<img width="1062" height="467" alt="image" src="https://github.com/user-attachments/assets/37e22cae-cfaf-45f7-99f2-53f85d80880e" />

# CODING
print(df.dropna(axis=0))

# OUTPUT
<img width="564" height="619" alt="image" src="https://github.com/user-attachments/assets/385757f6-e574-41e4-95c2-4787f7275c41" />

# CODING
print(df.dropna(axis=1))

# OUTPUT
<img width="448" height="227" alt="image" src="https://github.com/user-attachments/assets/b217b757-2cc5-49c9-8d1c-07819af81901" />

# CODING
dfs=df[df['num_episodes']>20]
dts

# OUTPUT
<img width="1013" height="650" alt="image" src="https://github.com/user-attachments/assets/77896ffd-30d1-4a2e-ab71-7c649e488e5c" />

# CODING
dfs=sd[sd['country'].str.startswith(('C'))&(df['num_values']>15)]
dfs

# OUTPUT
<img width="1006" height="670" alt="image" src="https://github.com/user-attachments/assets/4c92e3a9-6a29-4887-876d-21969ea8b13e" />

# CODING
df.iloc[:4]

# OUTPUT
<img width="990" height="150" alt="image" src="https://github.com/user-attachments/assets/fc4af1e0-68a3-432c-906c-8b900a854157" />

# CODING
df.iloc[[1,3,5],[1,3]]

# OUTPUT
<img width="296" height="127" alt="image" src="https://github.com/user-attachments/assets/d70bceb6-8754-4081-a73d-b0c500f47cf7" />

# CODING
df.iloc[0:4,1:4]

# OUTPUT
<img width="377" height="154" alt="image" src="https://github.com/user-attachments/assets/0b3b7781-0046-4c86-b17b-5e47cadd19d3" />

# CODING
dff=df.fillna(0)
dff

# OUTPUT
<img width="984" height="375" alt="image" src="https://github.com/user-attachments/assets/2972e637-7f7c-4834-bd0e-a16521afc15b" />

# CODING
df.fillna(method='ffill')

# OUTPUT
<img width="993" height="383" alt="image" src="https://github.com/user-attachments/assets/922fdef5-5dd3-4305-8a3c-288abbf073ee" />

# CODING
df.fillna(method='bfill')

# OUTPUT
<img width="970" height="429" alt="image" src="https://github.com/user-attachments/assets/85af6e79-e4d7-41a2-a529-f749703e7f07" />

# CODING
df['num_episodes'].fillna(value=df['num_episodes'].mean())

# OUTPUT
<img width="355" height="207" alt="image" src="https://github.com/user-attachments/assets/b12661be-5cf7-47bb-9657-8267e0611d6b" />

# CODING
df['num_episodes'].fillna(value=df['num_episodes'].mean(),inplace=False)

# OUTPUT
<img width="356" height="201" alt="image" src="https://github.com/user-attachments/assets/4f778ad1-fc58-49f2-8ed0-ef2495e61d88" />

# CODING
Import matplotlib.pyplot as plt plt.bar(df["country"],df["num_episodes"])
plt.show()

# OUTPUT
<img width="592" height="389" alt="image" src="https://github.com/user-attachments/assets/e742d775-c805-4b23-9c8d-239db9cd7184" />

# CODING
plt.barh(df["country"],df["num_episodes"])
plt.show()

# OUTPUT
<img width="701" height="384" alt="image" src="https://github.com/user-attachments/assets/2e1c7994-fa78-4ac2-bda3-cd791fb84d36" />

# CODING
plt.plot(df["country"],df["num_episodes"])
plt.show()

# OUTPUT
<img width="628" height="390" alt="image" src="https://github.com/user-attachments/assets/c10fd2de-11a1-4f71-8be4-8ed6690122d8" />

# CODING
plt.scatter(df["country"],df["num_episodes"])
plt.show()

# OUTPUT
<img width="619" height="380" alt="image" src="https://github.com/user-attachments/assets/9f5c1c18-cf9e-4d73-8ec2-297dfad682ed" />

# Result
          <<include your Result here>>
The Data cleaning process is completed successfuly
  <<include your coding and its corressponding output screen shots here>>
The Data cleaning process is completed successfuly <>


