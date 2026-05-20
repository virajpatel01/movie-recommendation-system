# Movie Recommendation System using Collaborative Filtering

This project implements and compares collaborative filtering approaches for predicting user ratings in a movie recommendation system using the MovieLens 100K dataset.

## Project Overview

The goal of this project is to estimate how strongly a user may like a target movie by predicting a rating. The project compares baseline methods, user-based collaborative filtering, item-based collaborative filtering, and a hybrid recommender system.

## Dataset

The project uses the MovieLens 100K dataset, which contains:

- 100,000 movie ratings
- 943 users
- 1,682 movies
- User, movie, genre, and train/test split files

The included `u1` to `u5` train/test files support cross-validation style evaluation, while `ua` and `ub` provide additional predefined evaluation splits.

## Methods Implemented

| Method | Description |
|---|---|
| User Average | Predicts ratings using each user's average rating |
| Item Average | Predicts ratings using each movie's average rating |
| User-KNN | Predicts ratings using ratings from similar users |
| Item-KNN | Predicts ratings using ratings from similar movies |
| Hybrid KNN | Combines user-based and item-based collaborative filtering |

## Results

| Method | MAE | RMSE |
|---|---:|---:|
| User Average | 0.8259 | 1.0311 |
| Item Average | 0.7961 | 1.0013 |
| User-KNN | 0.8247 | 1.0431 |
| Item-KNN | 0.7570 | 0.9845 |
| Hybrid KNN | **0.7329** | **0.9362** |

The hybrid collaborative filtering method achieved the best overall performance, showing that combining user-based and item-based perspectives can improve prediction accuracy.

## Key Skills Demonstrated

- Recommendation systems
- Collaborative filtering
- User-based KNN
- Item-based KNN
- Hybrid modelling
- Cosine similarity
- Model evaluation using MAE and RMSE
- Python-based data analysis

## Repository Structure

```text
movie-recommendation-system/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── recommender_system.ipynb
│
├── data/
│   ├── README_MovieLens_Assignment.txt
│   └── raw/
│       ├── u.data
│       ├── u.item
│       ├── u.user
│       ├── u.genre
│       ├── u.occupation
│       ├── u.info
│       └── train/test split files
│
├── scripts/
│   ├── allbut.pl
│   └── mku.sh
│
├── reports/
│   └── presentation.pptx
│
└── src/
```

## How to Run

1. Clone this repository.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook notebooks/recommender_system.ipynb
```

4. Run all cells in order.

## Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Collaborative Filtering
- K-Nearest Neighbours

## Future Improvements

- Tune the number of neighbours (`k`) for KNN methods
- Tune the hybrid weighting parameter
- Add matrix factorization methods such as SVD
- Build a simple movie recommendation interface
- Add top-N recommendation output for selected users

## Author

Viraj Patel  
GitHub: [virajpatel01](https://github.com/virajpatel01)  
LinkedIn: [virajpatel02](https://www.linkedin.com/in/virajpatel02)
