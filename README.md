# IMDB Movie Analysis Project

This project performs a comprehensive data analysis of IMDB movie metadata using R. The goal is to predict movie success (measured by IMDB scores and Gross revenue) and to group movies using various clustering techniques.

## Project Overview

The analysis includes:
- **Data Preprocessing**: Handling missing values and feature selection.
- **Predictive Modeling**:
  - Linear Regression and ANOVA.
  - Machine Learning: Random Forest, Gradient Boosting (GBM), and Neural Networks.
  - Deep Learning: Multi-layer neural networks using the `h2o` framework.
- **Clustering**: K-Means, Hierarchical Clustering (Ward's method), and Model-based clustering.

## Prerequisites

To run the script, you will need R installed along with the following libraries:
- `ggplot2`: Data visualization.
- `readr`: Fast CSV reading.
- `caret`: Data partitioning and model training.
- `randomForest`: Random Forest algorithm.
- `gbm`: Generalized Boosted Regression Models.
- `neuralnet` / `nnet`: Neural network implementations.
- `h2o`: Deep learning and high-performance machine learning.
- `dplyr`: Data manipulation (filtering/selection).
- `pvclust`: Hierarchical clustering with p-values.
- `mclust`: Model-based clustering.
- `fpc` / `cluster`: Clustering visualization.

## Datasets

The script expects the following CSV files in the project directory:
1. `movie_metadata.csv`: Initial raw dataset.
2. `movie_data_final.csv`: Refined dataset with additional calculated scores (genres, directors, and actors).

## Methodology

### 1. Data Cleaning
The script handles missing values by imputing them with the mean of the respective columns. It focuses on numerical predictors such as budget, duration, and social media likes.

### 2. Regression & Inference
- **IMDB Score Prediction**: Uses multiple linear regression to identify significant predictors of movie ratings.
- **Gross Revenue Prediction**: Specifically filters for "USA" movies to predict financial outcomes.
- **ANOVA**: Analyzes interactions between director scores, actor scores, and budget.

### 3. Machine Learning
- **Random Forest**: Evaluates feature importance and prediction accuracy (MSE).
- **Boosting**: Uses a Gaussian distribution with 5000 trees for refined prediction.
- **Neural Networks**: Explores both categorical classification (1-10 labels) and continuous regression.

### 4. Deep Learning
Uses the `h2o` platform to build a 5-layer deep neural network (100 nodes each) for score prediction.

### 5. Clustering
- **K-Means**: Determined optimal cluster count using the "Elbow" method (Within groups sum of squares).
- **Dendrograms**: Visualizes relationships using Ward's Hierarchical Clustering.
- **Cluster Plots**: Visualizes clusters against principal components.

## How to Run

1. Place `movie_metadata.csv` and `movie_data_final.csv` in the same directory as the script.
2. Open `IMDB Movie_Final.R` in RStudio or your preferred R environment.
3. Install missing packages using `install.packages()`.
4. Run the script. *Note: The H2O section requires a local cluster initialization.*

---
*Created as part of QMST 4373 - Spring 2017.*
