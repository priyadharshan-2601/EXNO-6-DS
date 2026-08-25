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

import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt 
df=pd.read_csv("titanic_dataset.csv") 
df.head()
<img width="1271" height="212" alt="image" src="https://github.com/user-attachments/assets/6fcb128f-356d-43f9-913b-4d92cf9e98c2" />

x=[1,2,3,4,5] 
y=[3,6,2,7,1] 
sns.lineplot(x=x,y=y) 
plt.title('Line Plot')
<img width="665" height="540" alt="image" src="https://github.com/user-attachments/assets/07b62d15-1df6-45bf-8ca3-5335a06ebd06" />

x=[1,2,3,4,5] 
y1=[3,5,2,6,1] 
y2=[1,6,4,3,8] 
y3=[5,2,7,1,4] 
sns.lineplot(x=x,y=y1) 
sns.lineplot(x=x,y=y2) 
sns.lineplot(x=x,y=y3) 
plt.title('Multi Line Plot')
<img width="662" height="542" alt="image" src="https://github.com/user-attachments/assets/d0bd187c-dea0-4f3c-b6ba-2ac02bb52023" />

plt.figure(figsize=(8,5)) 
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') 
plt.title("Fare Of Passenger By Embarked Town")
<img width="847" height="577" alt="image" src="https://github.com/user-attachments/assets/70ca7c0a-317a-4449-ac72-22eada751ba2" />

sns.scatterplot(x="Age", y="Fare", data=df) 
plt.title('Scatterplot of Age vs Fare') 
plt.show()
<img width="711" height="566" alt="image" src="https://github.com/user-attachments/assets/b475a201-c5c4-45d0-ba1f-d3e5ea229ff6" />

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200)) 
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') 
plt.show()
<img width="716" height="557" alt="image" src="https://github.com/user-attachments/assets/ce47d5de-ac0b-459a-8e53-8e93021935ed" />

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="707" height="537" alt="image" src="https://github.com/user-attachments/assets/e808fe20-1be2-4325-b3c6-be8de46b67fa" />

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') 
plt.title("Age By Passenger Class")
<img width="701" height="567" alt="image" src="https://github.com/user-attachments/assets/42546b3d-4e76-4c20-8f48-30e3279c6b52" />

sns.violinplot(x="Pclass", y="Fare", data=df) 
plt.title('Violin Plot of Fare by Passenger Class') 
plt.show()
<img width="705" height="567" alt="image" src="https://github.com/user-attachments/assets/c49ad767-d2ab-43e9-a894-6b4bcf4578fe" />

sns.kdeplot(data=df['Age'], shade=True) 
plt.title('Density Plot of Passenger Ages')
plt.show()
<img width="725" height="565" alt="image" src="https://github.com/user-attachments/assets/3c047b3b-6bf0-4edd-ba78-d3f7b88c9ffb" />

numeric_df = df.select_dtypes(include=['float64', 'int64']) 
corr_matrix = numeric_df.corr() 
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') 
plt.title('Heatmap of Titanic Dataset') 
plt.show()
<img width="742" height="620" alt="image" src="https://github.com/user-attachments/assets/5af732c0-c21f-4203-8db9-ff6de789ab97" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
