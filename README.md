# Book Recommendation System (Collaborative Filtering)

## Overview
This project implements an **item-based collaborative filtering** system to recommend books to users based on their past ratings. The system uses **Pearson similarity** to measure how similar books are based on overlapping user ratings.

Built using **Python, PySpark**, and Google Colab.

---

## Features
- Cleaned and preprocessed large book rating dataset
- Computed **item-item similarity** using Pearson correlation
- Generated top-N recommendations for any book
- Included metadata (title & author) in recommendations
- Visualized similarity distributions

---

## Project Structure

```
book-recommendation-cf/
│
├─ data/
│   ├─ book_similarity.csv          - Item-item similarity scores
│   └─ example_recommendations.csv  - Sample top-N recommendations
│
├─ notebooks/
│   └─ BookRecommendation.ipynb     - Main Colab notebook
└─ README.md                        - Project overview
```
---

## How to Run

1. Clone the repository:
```
https://github.com/AymanBerri/book-recommender-pearson.git
```
3. Open BookRecommendation.ipynb in Google Colab or Jupyter Notebook

4. Upload the **original book ratings dataset** (.csv) as instructed at the top of the notebook (the original dataset cant be uploaded
to github, so ill figure something out, for now the entire dataset for the item-item similarity scores is saved in data folder)

7. Run all cells sequentially

---

## Example Recommendations

Top 5 recommendations for a sample book:

| ISBN        | Title                   | Author         | Pearson Similarity |
|------------ |------------------------ |--------------- |----------------- |
| 044021145   | Book A                  | Author X       | 0.29            |
| 446310786   | Book B                  | Author Y       | 0.28            |
| ...         | ...                     | ...            | ...             |

---

## Key Learnings

- Data cleaning for large datasets
- Handling duplicates, invalid data, and missing values
- Computing **Pearson correlation** manually in Spark
- Building a **recommendation function** for real-world datasets
- Spark’s performance benefits over Pandas for large data

---

## Next Steps

- Implement **user-centric recommendations**
- Explore **other similarity metrics** (cosine, Jaccard)
- Integrate with a **web-based book recommendation UI**
