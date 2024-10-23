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

| Algorithm      | RMSE Mean | RMSE Std | MAE Mean | MAE Std | Fit Time Mean | Test Time Mean |
|----------------|-----------|----------|----------|---------|---------------|----------------|
| SVD            | 0.859966  | 0.001462 | 0.654187 | 0.001141 | 23.955620     | 0.814153       |
| NMF            | 0.849209  | 0.001781 | 0.653305 | 0.001397 | 13.608271     | 1.071799       |
| CoClustering   | 0.890069  | 0.003896 | 0.691604 | 0.002693 | 28.741858     | 0.768877       |
| SlopeOne       | 0.867366  | 0.002115 | 0.663711 | 0.001434 | 7.199376      | 16.545004      |
| KNNBasic       | 0.897160  | 0.000567 | 0.684796 | 0.000515 | 15.216415     | 79.488078      |

Additionally, a bar plot comparing the RMSE means of all algorithms will be generated.

## Algorithms Used

1. **KNNBasic**: A basic k-nearest neighbors algorithm that calculates user or item similarities based on user ratings.
2. **SVD**: Singular Value Decomposition, a matrix factorization method widely used in collaborative filtering.
3. **NMF**: Non-Negative Matrix Factorization, a matrix factorization technique that ensures all elements in the factor matrices are non-negative.
4. **SlopeOne**: A simple and efficient algorithm for collaborative filtering.
5. **CoClustering**: An algorithm that performs co-clustering on users and items for recommendation.

## Results

The RMSE values will help you decide which algorithm performs best in terms of prediction accuracy. Additionally, the fit time and test time provide insight into the computational efficiency of each algorithm.

## License

This project is open-source and available under the MIT License. Feel free to modify and use it for your own projects.

## Acknowledgements

- Dataset provided by [GroupLens Research](https://grouplens.org/datasets/movielens/).
- Algorithms implemented using the [SURPRISE Library](http://surpriselib.com/).
