import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns



# Load the CSV files
owid_covid_data = 'C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/owid-covid-data (1).csv'
World_Happiness_Index_2013 = 'C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/WorldHappinessIndex2013-2023.csv'

df1 = pd.read_csv(f'C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/owid-covid-data (1).csv')
df2 = pd.read_csv(f'C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/WorldHappinessIndex2013-2023.csv')

# Display the first few rows of each DataFrame
print("C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/owid-covid-data (1).csv")
print(df1.head())

print("\n'C:/Users/georg/git repositories/project 1 group 16/project_1group_16_/WorldHappinessIndex2013-2023.csv':")
print(df2.head())



# Check for missing values
print("Missing Values in df1:")
print(df1.isnull().sum())

# Drop rows with missing values
df1_cleaned = df1.dropna()

# Drop duplicates
df1_cleaned = df1_cleaned.drop_duplicates()

# Reset index after cleaning
df1_cleaned.reset_index(drop=True, inplace=True)

#df2

# Check for missing values
print("Missing Values in df2:")
print(df2.isnull().sum())

# Drop rows with missing values
df2_cleaned = df2.dropna()

# Drop duplicates
df2_cleaned = df2_cleaned.drop_duplicates()

# Reset index after cleaning
df2_cleaned.reset_index(drop=True, inplace=True)

#merge
merged_df = pd.merge(df1_cleaned, df2_cleaned, on=['Country', 'Year'], how='inner')
