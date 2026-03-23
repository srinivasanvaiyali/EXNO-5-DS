# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Generate sample data
np.random.seed(0)
cities = ['Delhi', 'Bangalore', 'Mumbai', 'Chennai']
data = pd.DataFrame({
    'id': range(1, 21),
    'City': np.random.choice(cities, size=20),
    'Category': np.random.choice(['A', 'B', 'C'], size=20),
    'Value': np.random.randint(10, 100, size=20),
    'Score': np.random.randn(20) * 10 + 50,
    'Target': np.random.choice([0, 1], size=20)
})
```
# 1. Pie Chart: City distribution:
```
plt.figure(figsize=(5, 5))
data['City'].value_counts().plot.pie(autopct='%1.1f%%', startangle=90)
plt.title('City Distribution (Pie Chart)')
plt.ylabel('')
plt.show()
```
<img width="617" height="520" alt="500345850-8f0829d9-d722-4af6-aba1-eccab7fa198d" src="https://github.com/user-attachments/assets/fd0550b0-d595-49fb-a0c3-9aba04bc896e" />


## 2. Bar Chart: Average Value per City:
```
plt.figure(figsize=(6, 4))
city_avg = data.groupby('City')['Value'].mean()
city_avg.plot(kind='bar', color='skyblue')
plt.title('Average Value per City (Bar Chart)')
plt.xlabel('City')
plt.ylabel('Average Value')
plt.show()
```
<img width="707" height="552" alt="500345908-5a67c065-da77-4eb2-becb-a82b8598d1a5" src="https://github.com/user-attachments/assets/ca1bd310-5609-4145-b83c-98c814859564" />


## 3. Line Graph: Value over id (mimicking time series) 
```
plt.figure(figsize=(6, 4))
plt.plot(data['id'], data['Value'], marker='o', linestyle='-')
plt.title('Value over id (Line Graph)')
plt.xlabel('id')
plt.ylabel('Value')
plt.show()
```
<img width="751" height="483" alt="500345988-eab6ee9b-33fe-4ff3-a32f-4dc2f8ee885e" src="https://github.com/user-attachments/assets/b4042956-3cf7-4205-9854-671b45f1e523" />



## 4. Scatter Plot: Value vs Score, colored by Target :
```
plt.figure(figsize=(6, 4))
sns.scatterplot(data=data, x='Value', y='Score', hue='Target', palette='Set1')
plt.title('Value vs Score (Scatter Plot)')
plt.show()
```
<img width="697" height="488" alt="500346096-9117b8f3-3bbf-400e-a47f-07b6178cd586" src="https://github.com/user-attachments/assets/5730487f-5a21-423a-bcde-fe71d240d553" />



## 5. Box Plot: Score distribution by City:
```
plt.figure(figsize=(6, 4))
sns.boxplot(data=data, x='City', y='Score')
plt.title('Score by City (Box Plot)')
plt.show()
```
<img width="743" height="492" alt="500346181-dd653fb2-793b-4d70-a3c1-ae37ac2a9e71" src="https://github.com/user-attachments/assets/e74eb305-1164-4fa3-a9a7-0313783b200f" />



##  6. Heatmap: Correlation between numeric columns :
```
plt.figure(figsize=(5, 4))
sns.heatmap(data[['Value', 'Score', 'Target']].corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
```
<img width="586" height="458" alt="500346276-4176498a-2e4d-4205-a28b-4e8abd7ff52b" src="https://github.com/user-attachments/assets/45d4e644-bbce-41f3-811e-29c6182a3aa8" />



## 7. Map: Plotting city locations (simple scatter, not a real map)
```
city_coords = {
    'Delhi': (28.6139, 77.2090),
    'Bangalore': (12.9716, 77.5946),
    'Mumbai': (19.0760, 72.8777),
    'Chennai': (13.0827, 80.2707)
}
city_df = pd.DataFrame(city_coords).T.reset_index()
city_df.columns = ['City', 'Latitude', 'Longitude']
city_counts = data['City'].value_counts().reset_index()
city_counts.columns = ['City', 'Count']
city_map = pd.merge(city_df, city_counts, on='City')

plt.figure(figsize=(7, 6))
plt.scatter(city_map['Longitude'], city_map['Latitude'], s=city_map['Count']*50, color='coral', alpha=0.7)
for _, row in city_map.iterrows():
    plt.text(row['Longitude']+0.2, row['Latitude']+0.2, row['City'], fontsize=12)
plt.title('City Locations (Bubble size = count)')
plt.xlabel('Longitude')
plt.ylabel('Latitude')
plt.grid(True)
plt.show()
```
<img width="747" height="610" alt="500346341-c07201f1-e7c7-4496-9038-a91c7c396634" src="https://github.com/user-attachments/assets/381476f6-2028-4e6f-908f-cdf4b7b019ca" />




# Result:
Thus, The implementation of data visualization using matplotlib has been successfully verified.
