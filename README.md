# Item-to-Item Collaborative Filtering Recommendation System 🛒🎯

A machine learning recommendation engine designed to suggest products to users based on their historical purchasing behavior, using Item-to-Item Collaborative Filtering.

## 🚀 Project Overview

In modern e-commerce, personalized recommendations drive a massive percentage of sales. Unlike Content-Based filtering (which relies on product descriptions), **Collaborative Filtering** relies entirely on user behavior. 

Specifically, this project implements an **Item-to-Item** approach (popularized by Amazon). Instead of finding similar users, the algorithm calculates similarities directly between items based on how often they are purchased together. This approach scales much better and provides highly relevant recommendations.

## ⚙️ Methodology

1. **Data Preprocessing**: 
   - Loaded the massive Online Retail Dataset.
   - Cleaned the data by removing canceled orders, handling missing Customer IDs, and standardizing product descriptions.
2. **User-Item Matrix Creation**:
   - Pivoted the dataset to create a vast User-Item interaction matrix, where rows represent unique customers and columns represent unique products. The values indicate purchase frequency or binary interaction.
3. **Similarity Calculation**:
   - Utilized `sklearn.metrics.pairwise.cosine_similarity` to compute the cosine distance between the columns (items).
   - This generated an Item-Item similarity matrix, revealing exactly which products are most frequently bought together.
4. **Recommendation Generation**:
   - Built a function that accepts a user's shopping cart (a list of item IDs) and queries the similarity matrix to return the top $N$ recommended items that complement their current cart.

## 📊 Dataset

The model utilizes the **Online Retail Data Set** from the UCI Machine Learning Repository, containing over 500,000 transactions occurring between 2010 and 2011 for a UK-based registered non-store online retail.

## 🛠️ Tech Stack & Libraries Used

- **Data Manipulation:** Pandas, NumPy
- **Machine Learning Algorithms:** Scikit-learn (`cosine_similarity`)

## 📈 Key Outcomes

- Built a highly scalable recommendation pipeline capable of suggesting cross-sell items in milliseconds.
- Demonstrated advanced matrix manipulation and sparse data handling techniques.

---
*This repository is part of my AI Engineer / Data Scientist Portfolio.*
