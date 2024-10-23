# MovieLens Recommender System Comparison

## Overview

This project evaluates and compares the performance of different recommendation system algorithms using the **MovieLens 100K** dataset. The algorithms are evaluated based on key metrics such as RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), fit time, and test time.

The algorithms included in the comparison are:
- KNNBasic
- SVD (Singular Value Decomposition)
- NMF (Non-Negative Matrix Factorization)
- SlopeOne
- CoClustering

## Dataset

The dataset used in this project is the **MovieLens 100K** dataset, which consists of 100,000 ratings from 943 users on 1,682 movies. The dataset is provided by GroupLens and is commonly used for benchmarking recommendation algorithms.

For more details about the dataset, visit [MovieLens 100K](https://grouplens.org/datasets/movielens/100k/).

### Running the Code

To run the code, simply execute the provided script in your Python environment. The code evaluates each algorithm using 5-fold cross-validation and outputs the following metrics:
- **RMSE Mean**: The average RMSE across all folds.
- **RMSE Std**: The standard deviation of RMSE.
- **MAE Mean**: The average MAE across all folds.
- **MAE Std**: The standard deviation of MAE.
- **Fit Time Mean**: The average time taken to fit the model.
- **Test Time Mean**: The average time taken to make predictions.

### Example of the Output

The script will output a table that looks like this:

| Algorithm       | RMSE Mean | RMSE Std | MAE Mean | MAE Std | Fit Time Mean | Test Time Mean |
|-----------------|-----------|----------|----------|---------|---------------|----------------|
| SVD             | 0.936621  | 0.007199 | 0.738091 | 0.006104| 0.743771      | 0.115549       |
| NMF             | 0.963241  | 0.007117 | 0.757923 | 0.005815| 1.410286      | 0.115873       |
| Co Clustering   | 0.967707  | 0.008360 | 0.757615 | 0.005793| 1.252161      | 0.090510       |
| SlopeOne        | 0.944792  | 0.007117 | 0.742524 | 0.004487| 0.566474      | 1.904395       |
| KNNBasic        | 0.978599  | 0.002274 | 0.773216 | 0.001964| 0.264673      | 2.149462       |

Additionally, a bar plot comparing the RMSE means of all algorithms will be generated.

### Results Summary

From the output above, we can draw the following conclusions:
- **SVD** provides the best accuracy, with the lowest RMSE (0.936621) and MAE (0.738091) values.
- **NMF** and **CoClustering** have slightly higher RMSE values compared to SVD but are still competitive.
- **KNNBasic** has the highest RMSE (0.978599), indicating that it performs the worst in terms of prediction accuracy.
- In terms of computational efficiency, **KNNBasic** has the shortest fit time (0.264673), while **SlopeOne** and **KNNBasic** have the longest test times.

## Algorithms Used

1. **KNNBasic**: A basic k-nearest neighbors algorithm that calculates user or item similarities based on user ratings.
2. **SVD**: Singular Value Decomposition, a matrix factorization method widely used in collaborative filtering.
3. **NMF**: Non-Negative Matrix Factorization, a matrix factorization technique that ensures all elements in the factor matrices are non-negative.
4. **SlopeOne**: A simple and efficient algorithm for collaborative filtering.
5. **CoClustering**: An algorithm that performs co-clustering on users and items for recommendation.

## Results

Based on the RMSE, MAE, fit time, and test time metrics, **SVD** emerges as the most accurate algorithm for the MovieLens 100K dataset, with the lowest RMSE and MAE scores. However, depending on your requirements, algorithms like **NMF** or **CoClustering** might be better suited if you prefer faster fit times and are willing to trade a small amount of accuracy.

## License

This project is open-source and available under the MIT License. Feel free to modify and use it for your own projects.

## Acknowledgements

- Dataset provided by [GroupLens Research](https://grouplens.org/datasets/movielens/).
- Algorithms implemented using the [SURPRISE Library](http://surpriselib.com/).
