Overview

This repository contains a Smart Grid Monitoring System dataset along with a Google Colab notebook for data analysis and visualization. The dataset includes real-time electrical parameters such as Voltage, Current, Frequency, Power, Battery Storage, Renewable Energy Contribution, and Fault Detection.

Features
CSV Dataset: Contains 50+ entries recorded at different timestamps.

Google Colab Notebook: Used for data loading, processing, and visualization.
Visualization Graphs: Insights into power usage, renewable energy trends, voltage variations, and fault detection.

How to Use
1️⃣ Clone the Repository
git clone https://github.com/Kishore3148/Smart-Grid-Monitoring-System.git
cd smart-grid-monitoring

2️⃣ Upload CSV to Google Colab
Open Google Colab: Google Colab
Upload the Smart_Grid_monitoring_system.csv file.

3️⃣ Run the Colab Notebook
Open the Smart_Grid_monitoring_system.ipynb file in Google Colab.

Run the first cell to install dependencies:
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

Load the CSV file:
df = pd.read_csv('Smart_Grid_monitoring_system.csv')
df.head()

4️⃣ Visualize Data with Graphs
Voltage & Current Over Time
plt.figure(figsize=(10,5))
sns.lineplot(x=df['Timestamp'], y=df['Voltage (V)'], label='Voltage')
sns.lineplot(x=df['Timestamp'], y=df['Current (A)'], label='Current')
plt.xticks(rotation=45)
plt.title("Voltage & Current Over Time")
plt.legend()
plt.show()

Renewable Energy Contribution Trend
plt.figure(figsize=(10,5))
sns.barplot(x=df['Timestamp'], y=df['Renewable Energy (%)'])
plt.xticks(rotation=45)
plt.title("Renewable Energy Contribution Trend")
plt.show()

Fault Detection Analysis
fault_counts = df['Fault Detection'].value_counts()
fault_counts.plot(kind='bar', color=['green', 'red'])
plt.title("Fault Detection Frequency")
plt.xlabel("Fault Detected")
plt.ylabel("Count")
plt.show()

📌 Key Insights
Voltage and Current fluctuations are visualized using line charts.
Renewable energy trends are analyzed using bar plots.
Fault detection analysis helps identify grid anomalies.

🔗 Links
Dataset: Smart_Grid_monitoring_system.csv
Google Colab Notebook: Smart_Grid_monitoring_system.ipynb
GitHub Repository: https://github.com/Kishore3148/Smart-Grid-Monitoring-System

🤝 Contributing
Feel free to fork this repository, add new features, and submit a pull request!

📜 License
This project is licensed under the MIT License.
