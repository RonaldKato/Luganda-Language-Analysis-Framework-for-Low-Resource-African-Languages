# Luganda-Language-Analysis-Framework-for-Low-Resource-African-Languages
<img width="599" height="505" alt="Screenshot 2026-05-04 at 21 04 11" src="https://github.com/user-attachments/assets/35e3237a-c428-4a82-a0a7-6161febfcbbb" />

This repository implements a complete NLP pipeline for analyzing Luganda, a Bantu language spoken by over 16 million people in Uganda. The framework includes dataset loading, preprocessing, morphological analysis, topic modeling, and comprehensive visualizations based on ACTUAL dataset content.

**Execution Guide:**
# Step 1: Setup environment
conda create -n luganda-repro python=3.9
conda activate luganda-repro
pip install -r requirements.txt

# Step 2: Download datasets
# Place files in ./data/ directory

# Step 3: Run complete analysis
python train.py \
    --data_path ./data/ntvbbscbsbukedde_webcrawled.txt \
    --data_path ./data/mozillaCommonVoice_all_sentences.csv \
    --data_path ./data/Luganda_Bible_worldProject_Webcrawled.txt \
    --data_path ./data/Makerere_Luganda_Monolingual_Corpus.txt \
    --output_dir ./results \
    --generate_plots

# Step 4: Run evaluation
python eval.py \
    --model_path ./results \
    --test_data ./data/test_set.txt \
    --output_file evaluation_results.json

# Step 5: Generate result table
python scripts/generate_results_table.py --results_dir ./results


#Acknowledgments
Mbarara University of Science and Technology
Makerere University NLP Research

