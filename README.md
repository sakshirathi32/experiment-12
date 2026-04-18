Experiment 12: Create Dataset and Load Dataset
Aim:

To create a dataset using Python and pandas, save it as a CSV file, load it again, and perform basic inspection and analysis of the dataset.

Theory:

pd.DataFrame(data)
This function is used to convert a normal Python dictionary into a structured table called a DataFrame. The keys of the dictionary become the column names, while the list values form the rows of the dataset.

df.to_csv("filename.csv", index=False)
This command is used to save the DataFrame as a CSV file in storage. The index=False parameter is important because it avoids adding an extra unnecessary column for row index numbers.

pd.read_csv('path/to/file.csv')
This function is mainly used to load a CSV file into Python. It reads the file and converts it back into a DataFrame so that further operations can be performed.

df.info()
This provides complete information about the dataset structure. It shows the total number of rows, column names, data types of each column, and the number of non-null values present.

df.head() and df.tail()
These functions help in quickly viewing the dataset. head() displays the first five rows, while tail() shows the last five rows. They are useful for checking whether the data is loaded properly.

df.sample(n)
This function selects n random rows from the dataset. It helps in checking data quality from different sections without depending only on the beginning or end of the file.

df.columns
This returns the names of all columns in the DataFrame. It is helpful when exact column names are needed for calculations, filtering, or analysis.

df.describe()
This function gives statistical details of numerical columns such as count, mean, standard deviation, minimum value, maximum value, and quartile values (25%, 50%, and 75%).

df.isnull().sum()
This is useful for data cleaning. It identifies missing values (NaN) in each column and counts them so that incomplete data can be handled properly.

df.duplicated().sum()
This checks for duplicate rows that are exactly the same. It returns the total number of repeated rows that may need to be removed.

df.nunique()
This counts the number of unique values present in each column. It helps in understanding categorical data and relationships between different columns.

Conclusion:

This experiment explains the complete process of dataset handling, starting from data creation to loading and checking its structure. By using pd.DataFrame() and to_csv(), data is created and stored permanently. Functions like info(), describe(), and isnull() help in checking data quality by identifying missing values, duplicate rows, and statistical patterns. This organized approach makes the dataset reliable and ready for proper analysis and decision-making.
