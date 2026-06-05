# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Step 1: Read Dataset
df = pd.read_csv("bmi.csv")

# Display first five records
print(df.head())

# Convert categorical values into numeric values
df['Gender'] = df['Gender'].map({'Male':0,'Female':1})

# 1. Scatter Plot
sns.scatterplot(x='Height', y='Weight', data=df)
plt.title("Height vs Weight")
plt.show()

# 2. Histogram
sns.histplot(df['Height'], kde=True)
plt.title("Height Distribution")
plt.show()

# 3. Box Plot
sns.boxplot(x=df['Weight'])
plt.title("Box Plot of Weight")
plt.show()

# 4. Count Plot
sns.countplot(x='Index', data=df)
plt.title("Count Plot of BMI Index")
plt.show()

# 5. Pair Plot
sns.pairplot(df)
plt.show()

# 6. Correlation Heatmap
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title("Correlation Heatmap")
plt.show()
```
<img width="332" height="112" alt="image" src="https://github.com/user-attachments/assets/5cf947ee-b52e-4fce-9fc0-f042227cf157" />
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/7d495f50-32aa-4ef8-b146-4bbb5eb5dec2" />
<img width="563" height="453" alt="image" src="https://github.com/user-attachments/assets/1648df07-0757-4af7-891b-31eaf7912e0e" />
<img width="520" height="453" alt="image" src="https://github.com/user-attachments/assets/f031fb18-01da-43e6-be34-afca7573c498" />
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/45f36562-3b50-42c6-aa4a-e3c9fbaebffe" />

# Result:
Thus, the given dataset was successfully visualized using the Seaborn library. Various visualization techniques such as Scatter Plot, Histogram, Box Plot, Count Plot, Pair Plot, and Heatmap were generated to analyze patterns, distributions, and relationships within the dataset.
