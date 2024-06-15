# Enhancing-Music-Clustering-and-Recommendation-with-Advanced-Machine-Learning

## Overview
This project aims to enhance music clustering and recommendation systems using advanced machine learning techniques. By leveraging a comprehensive dataset of over 300,000 Spotify tracks, we employ methods such as Principal Component Analysis (PCA), autoencoders, KMeans, and DBSCAN clustering to develop a robust system for categorizing and recommending music tracks.

## Features
- Data Preprocessing: Removal of duplicates, irrelevant features, and application of SMOTE to balance genre distribution.
- Feature Scaling: Standardization of features to have zero mean and unit variance.
- Dimensionality Reduction: Utilization of PCA and Linear Discriminant Analysis (LDA) for feature reduction and visualization.
- Clustering Algorithms: Implementation of KMeans, DBSCAN, and autoencoders for clustering.
- Performance Evaluation: Use of metrics like Silhouette Score and Davies-Bouldin Score to evaluate clustering performance.
- Interpretability: Application of SHapley Additive exPlanations (SHAP) values to understand feature importance.
- Recommendation System: Development of a system to recommend the nearest songs within the same category and from different categories.

## Dataset
The dataset used in this project is sourced from Kaggle and contains over 300,000 Spotify tracks, each annotated with detailed audio features. These features include:
- Track Metadata: Track name, artist, genre.
- Audio Features: Tempo, energy, danceability, loudness, valence, speechiness, acousticness, instrumentalness, liveness, duration, etc.

## Methodology

### Data Preprocessing
- Duplicate Removal: Eliminate duplicate entries based on unique track identifiers.
- Feature Selection: Remove irrelevant features to reduce noise.
- Class Imbalance Handling: Apply SMOTE to generate synthetic samples for minority classes.

### Feature Scaling
- StandardScaler: Standardize features to have zero mean and unit variance.
- Dimensionality Reduction
- PCA: Reduce feature space while retaining significant variance.
- LDA: Further reduce dimensions for visualization purposes.

### Clustering Algorithms
- KMeans: Applied on original scaled data and PCA-reduced data. Elbow method used to determine the optimal number of clusters.
- DBSCAN: Applied on PCA-reduced data with optimal parameters determined using the k-distance graph.
- Autoencoders: Train an autoencoder to learn compressed representations of data, followed by KMeans clustering in the encoded space.

### Performance Evaluation
- Silhouette Score: Measures cohesion and separation of clusters.
- Davies-Bouldin Score: Evaluates cluster similarity and separation.

### Interpretability
- SHAP Values: Compute SHAP values to understand the importance of different features.

### Recommendation System
- Recommend the 11 nearest songs from the same cluster.
- Recommend the 3 nearest songs from each different cluster.

## Results
- Clustering Performance: The autoencoder-based KMeans clustering showed superior performance in terms of Silhouette and Davies-Bouldin Scores.
- Feature Importance: Features like liveness, time signature, valence, danceability, and energy significantly influenced clustering.
- Recommendation System: Successfully developed to provide relevant and diverse music recommendations based on clustering results.

## Conclusion
This project demonstrates the effective use of advanced machine learning techniques for music clustering and recommendation. By combining data preprocessing, feature selection, clustering, and interpretability methods, we developed a robust framework that enhances the accuracy and relevance of music recommendations.

## Acknowledgments
This project was developed for the course "Advanced Machine Learning" as part of the MSc program "Artificial Intelligence" at the Department of Informatics, Aristotle University of Thessaloniki.
