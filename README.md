🌿 MAFDE-DN4 (Plant Disease Few-Shot Classification)

📌 Overview

MAFDE-DN4 is a few-shot learning model for plant disease classification based on Deep Nearest Neighbor Neural Network (DN4). It improves performance using attention and multi-scale feature fusion.

🧠 Key Idea

The model classifies plant diseases by comparing local image features between support and query images instead of learning a fixed classifier.

🔧 Improvements over DN4
BWFM: Multi-scale feature fusion for better disease representation
EA Module: Attention mechanism to focus on diseased regions
Improved Loss: Better class separation and stable training


🌱 Dataset

PlantVillage dataset (clean leaf images)
Converted into N-way K-shot episodic tasks
🎯 Few-Shot Setup
1-shot learning
5-shot learning
Each episode contains support + query images.

⚙️ Pipeline

CNN Backbone → BWFM → EA Attention → DN4 Matching → Classification

📊 Results

1-shot: ~57%
5-shot: ~81%

🚀 Usage

pip install -r requirements.txt
python train.py
python test.py

🌿 Goal

Efficient plant disease classification with very limited labeled data using few-shot learning.
