# transforming-healthcare-with-AI-powered-disease-predicition-based-on-paitent-data-project
import pandas as pd

file_path = '/content/patient_data_heart_and_diabetes final.xlsx'
df = pd.read_excel(file_path, sheet_name='Sheet1')
print(df.shape)
print(df.dtypes)
print(df.describe(include='all'))
print(df.isnull().sum())
print(df.duplicated().sum())
import matplotlib.pyplot as plt
import seaborn as sns

# Age distribution
sns.histplot(df['Age'], kde=True)
plt.title("Age Distribution")
plt.show()

# Gender distribution
sns.countplot(x='Gender', data=df)
plt.title("Gender Distribution")
plt.show()

# Billing Amount by Disease
sns.boxplot(x='Disease_Name', y='Billing_Amount', data=df)
plt.title("Billing Amount by Disease")
plt.xticks(rotation=15)
plt.show()
target = df['Disease_Name']
features = df.drop(columns=[
    'Patient_ID', 'Name', 'Disease_Name', 'Doctor_Name',
    'Hospital_Name', 'Date_of_Admission', 'Discharge_Date', 'Room_Number'
])
print(features.head())
print(target.value_counts())
