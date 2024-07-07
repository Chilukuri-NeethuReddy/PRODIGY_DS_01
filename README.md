# PRODIGY_DS_01
## ProdigyInfoTech_TASK1

## Task 1: Data Visualization - Literacy Rates by Gender and Distribution
This project demonstrates how to visualize the distribution of a categorical variable (gender) and a continuous variable (literacy rate) using a literacy rates dataset. The visualizations are created using pandas, matplotlib, and seaborn.

## Dataset:
The dataset used in this project is the Literacy Rates dataset ,which can be found on Kaggle.
https://www.kaggle.com/datasets/thedevastator/youth-adult-literacy-rates-in-2019

## Visualizations:

1.**Average Literacy Rate by Gender**: A bar chart that shows the average literacy rate for each gender in the dataset.

2.**Literacy Rate Distribution**: A histogram that shows the distribution of literacy rates in the dataset.

## How to Run:

1.Clone the repository.

2.Ensure you have the necessary libraries installed (pandas, matplotlib, seaborn).

3.Place the dataset (Literacy_rates.csv) in the same directory as the script.

4.Run the script to generate the visualizations.

## Code:

```python

import pandas as pd

import matplotlib.pyplot as plt

import seaborn as sns

# Load the dataset
data = pd.read_csv('Literacy_rates.csv')

# Display the first few rows of the dataset

print(data.head())
```

![Screenshot 2024-07-06 220725](https://github.com/Chilukuri-NeethuReddy/PRODIGY_DS_01/assets/174725064/2b464ee7-ce20-4a05-98f7-a4321ac689b3)


```python
# Set the style of the visualization

sns.set(style="whitegrid")

# Define the color palette

palette_colors = ['orange', 'blue', 'lightgreen']

# Create the bar plot for average literacy rate by gender

plt.figure(figsize=(12, 6))

sns.barplot(x='Gender', y='Literacy rate', data=data, palette=palette_colors)

plt.title('Average Literacy Rate by Gender in Literacy Rates Dataset')

plt.xlabel('Gender')

plt.ylabel('Average Literacy Rate')

plt.show()
```

### Bar Chart for Average Literacy Rate by Gender
![Screenshot 2024-07-06 215923](https://github.com/Chilukuri-NeethuReddy/PRODIGY_DS_01/assets/174725064/a2ff570f-3143-49ea-8e68-94628e81fab6)


```python
# Create the histogram for literacy rate distribution

plt.figure(figsize=(12, 6))

sns.histplot(data['Literacy rate'], bins=30, kde=True)

plt.title('Literacy Rate Distribution in Literacy Rates Dataset')

plt.xlabel('Literacy Rate')

plt.ylabel('Frequency')

plt.show()
```

### Histogram for Literacy Rate Distribution
![Screenshot 2024-07-06 220244](https://github.com/Chilukuri-NeethuReddy/PRODIGY_DS_01/assets/174725064/47d5585a-056b-4a50-a500-23fc16e2b974)

