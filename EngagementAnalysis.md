# 📌 Pinterest Engagement Analysis  
*Analyzing user engagement trends on Pinterest using Kaggle data.*  

## 📖 Table of Contents  
1. [Project Overview](#project-overview)  
2. [Installation & Setup](#installation--setup)  
3. [Running the Script](#running-the-script)  
4. [Data Analysis & Insights](#data-analysis--insights)  
5. [File Structure](#file-structure)  
6. [Additional Resources](#additional-resources)  
7. [Contributing & Next Steps](#contributing--next-steps)  

## 📂 Project Overview  
This project explores **Pinterest user engagement** using the [Pinterest Snapshot of Popularity and Engagement](https://www.kaggle.com/datasets/oneliwickramasinghe/pinterest-snapshot-of-popularity-and-engagement) dataset from Kaggle. The analysis focuses on:  
✅ How users engage with Pinterest content (likes, repins, and comments).  
✅ What types of pins perform best based on engagement metrics.  
✅ Data-driven insights into content trends on Pinterest.  

## 📥 Installation & Setup  
### 1️⃣ Prerequisites  
Ensure you have the following installed:  
- **Python 3.7+**  
- **Jupyter Notebook** or **Google Colab**  
- **Required Python Libraries:** `kagglehub`, `kaggle`, `pandas`, `matplotlib`  

### 2️⃣ Install Required Libraries  
Run the following command to install dependencies:  
```bash
pip install kagglehub kaggle pandas matplotlib

3️⃣ Set Up Kaggle API Key
	1.	Go to Kaggle and sign in.
	2.	Click on your profile picture > Account > API > Create New API Token.
	3.	Download the kaggle.json file.
	4.	Move kaggle.json to the appropriate directory:

mkdir ~/.kaggle  
mv kaggle.json ~/.kaggle/  
chmod 600 ~/.kaggle/kaggle.json

For Google Colab, upload the kaggle.json file manually:

from google.colab import files  
files.upload()

🚀 Running the Script

To download, load, and analyze the dataset, run the following Python script:

# Install necessary libraries  
!pip install kagglehub kaggle pandas matplotlib  

# Import required libraries  
import os  
import kagglehub  
import pandas as pd  
import matplotlib.pyplot as plt  

# Set up Kaggle API credentials (Ensure kaggle.json is uploaded)  
os.environ['KAGGLE_CONFIG_DIR'] = "/content/"  # Change this path if needed  

# Download the dataset from Kaggle  
path = kagglehub.dataset_download("oneliwickramasinghe/pinterest-snapshot-of-popularity-and-engagement")  
print("Path to dataset files:", path)  

# Load the dataset (Update filename as necessary)  
dataset_path = os.path.join(path, "Pinterest Snapshots.csv")  # Adjust filename if needed  
df = pd.read_csv(dataset_path)  

# Display the first few rows  
print("Dataset Preview:")  
print(df.head())  

# Dataset summary  
print("\nDataset Info:")  
print(df.info())  

# Display basic statistics  
print("\nSummary Statistics:")  
print(df.describe())  

# Check column names  
print("\nColumn Names:")  
print(df.columns)  

# Visualize engagement trends - Like count distribution  
plt.figure(figsize=(8, 5))  
df['like_count'].hist(bins=30, color='skyblue', edgecolor='black')  
plt.xlabel("Like Count")  
plt.ylabel("Frequency")  
plt.title("Distribution of Likes on Pinterest Pins")  
plt.show()

📊 Data Analysis & Insights

📝 Key Research Questions
	1.	What types of Pinterest content receive the most engagement?
	2.	What is the relationship between likes, comments, and repins?
	3.	What trends emerge from Pinterest’s most popular posts?

📌 Expected Insights
	•	High engagement posts may have common themes, categories, or visual styles.
	•	Repins and comments may correlate with like count, helping predict virality.
	•	Analyzing trends can help content creators optimize their Pinterest strategy.

📁 File Structure

📂 pinterest-engagement-analysis  
│── 📄 README.md                # Project Documentation  
│── 📜 pinterest_analysis.ipynb  # Jupyter Notebook with Analysis  
│── 📊 visuals/                  # Folder for Graphs & Charts (Generated)  
│── 📂 dataset/                   # Downloaded Dataset  

🔗 Additional Resources
	•	📌 Pinterest Business Insights: help.pinterest.com
	•	📊 Kaggle Dataset: Pinterest Snapshot
	•	📖 Data Visualization in Python: Matplotlib Docs

👨‍💻 Contributing & Next Steps

✅ Future Enhancements:
	•	Apply machine learning to predict content virality.
	•	Conduct sentiment analysis on pin descriptions.
	•	Compare engagement across different social media platforms.
