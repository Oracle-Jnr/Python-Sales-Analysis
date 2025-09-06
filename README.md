
=======
```markdown
Python sales Analysis
This project explores patterns in sales using Sales dataset. it covers cleaning, exploratory analysis and visualization using Python

Project Structure 
notebooks: Jupyter notebook for EDA
data/: Dataset


Tools Used
Python (pandas, Matplotlib, Seaborn)
Git/GitHub

Comprehensive Documentation: Sales Data Analysis
Step 1: Library Import
Imported the required libraries:
 pandas for data manipulation and analysis
 numpy for numerical computations
 Matplotlib and seaborn for data visualization
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
Step 2: Data Import
Imported the dataset using pd.read_excel
 Loaded the sales data from an Excel file into a pandas DataFrame
sd= pd.read_excel('sales_data.xlsx')
Step 3: Data Exploration
Explored the dataset to get familiar with its structure and content:
 Checked the first few rows of the dataset using head()
 Checked the data types of each column using dtypes
print(sd.head())
print(sd.dtypes)
Step 4: Data Cleaning
Dropped the first row as it's blank and used the second row as column header:
 Used header parameter to specify the second row as the column header
Dropped the first column as it was blank using dropna:
 Used dropna function to remove columns with all NaN values
df = pd.read_excel('sales_data.xlsx', header=1)
df = df.dropna(axis=1, how='all')
Step 5: Missing Value Identification
Identified missing values in the dataset:
 Used isnull function to check for missing values
 Found no other missing values in the dataset besides the ones already removed
print(sd.isnull().sum())
Step 6: Dataset Size Check- Checked the size of the dataset using .shape:
 Verified the number of rows and columns in the dataset
print(sd.shape)
Step 7: Duplicate Check
Checked for duplicates in the dataset:
 Used duplicated function to check for duplicate rows
 Found no duplicates in the dataset
print(sd.duplicated().sum())
Step 8: String Cleaning
Removed extra spaces for all strings:
Used str.strip function to remove leading and trailing spaces from string columns
sd['column_name'] = sd['column_name'].str.strip()
Step 9: Data Type Conversion
Converted columns to appropriate data types:
Used astype function to convert columns to integer, float, and datetime data types
sd['Order ID'] = sd['Order ID'].astype(int)
sd['Price'] = sd['Price'].astype(float)
sd['Quantity'] = sd['Quantity'].astype(float)
sd['Date'] = pd.to_datetime(sd['Date'])
Step 10: Data Type Verification
Checked the data type using .dtypes to ensure the changes were effected:
 Verified that the data types of each column were correctly converted
print(sd.dtypes)
Step 11: Summary Statistics
Used .describe to get the summary statistics of the sales dataset:
Calculated mean, median, mode, and standard deviation for numerical columns
sd .describe().T
Step 12: Business Questions
Used the cleaned dataset to answer business questions:


Author Oracle Jnr
>>>>>>> a4fd864 (Initial commit: Upload dataset, readme, and EDA notebook)
