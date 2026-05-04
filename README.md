# Luganda-Language-Analysis-Framework-for-Low-Resource-African-Languages
<img width="599" height="505" alt="Screenshot 2026-05-04 at 21 04 11" src="https://github.com/user-attachments/assets/35e3237a-c428-4a82-a0a7-6161febfcbbb" />

This repository implements a complete NLP pipeline for analyzing Luganda, a Bantu language spoken by over 16 million people in Uganda. The framework includes dataset loading, preprocessing, morphological analysis, topic modeling, and comprehensive visualizations based on ACTUAL dataset content.

**Steps to Run the Luganda NLP Project**
**Step 1:** Download Files
bash
git clone https://github.com/YOUR_USERNAME/luganda-nlp-visualization.git
cd luganda-nlp-visualization

**Step 2: ** Install Packages
bash
pip install matplotlib numpy pandas scipy seaborn networkx wordcloud scikit-learn

**Step 3:** Add Your Data
bash
# Create data folder and add your .txt or .csv files
mkdir data
# Copy your Luganda dataset files into the 'data' folder

**Step 4:** Create & Run Script
Save this as run.py:

python
from src.analyzer import LugandaDatasetAnalyzer
import os

# Load all files from data folder
paths = {f: os.path.join("data", f) for f in os.listdir("data") if f.endswith(('.txt','.csv'))}

# Run analysis
analyzer = LugandaDatasetAnalyzer(paths)
analyzer.run_complete_analysis()
analyzer.create_all_visualizations()
print("Done! Check for PNG files.")
Run it:
bash
python run.py

**Step 5:** Check the Results
bash
# Open the generated PNG files
open enhanced_luganda_analysis_1.png   # Mac
start enhanced_luganda_analysis_1.png  # Windows
xdg-open enhanced_luganda_analysis_1.png # Linux

#Acknowledgments
Mbarara University of Science and Technology
Makerere University NLP Research

