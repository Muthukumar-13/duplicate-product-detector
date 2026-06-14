# Duplicate Product Record Detector

## Problem
Large product catalogs accumulate duplicate records from multiple 
suppliers with inconsistent naming conventions and formats.
This ML pipeline automatically detects these duplicates.

## Pipeline
1. Load product data from CSV
2. Simulate real world dirty data with noise
3. Normalize text for fair comparison
4. Blocking - reduce comparisons by 81%
5. Compute 7 fuzzy similarity features per pair
6. Train Random Forest classifier
7. Evaluate with precision, recall, F1 score

## Results
- 81% reduction in comparisons via blocking
- 100% recall - caught every real duplicate
- Discovered and fixed ground truth labeling bug during evaluation

## Libraries Used
- pandas - data manipulation
- scikit-learn - ML model training and evaluation
- thefuzz - fuzzy string similarity scoring
- matplotlib - visualizations

## How to Run
1. Clone this repository
2. Install dependencies: pip install -r requirements.txt
3. Open duplicate_product_detector.ipynb in Jupyter
4. Run all cells top to bottom

## Domain Context
Built on Master Data Management (MDM) domain knowledge -
blocking strategy mirrors how MDM systems use golden record
attributes to scope deduplication.
