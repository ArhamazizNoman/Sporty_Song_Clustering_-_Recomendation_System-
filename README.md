# Sporty_Song_Clustering_-_Recomendation_System-
This Project is a classic Data Science and Machine Learning project that combines Audio Analysis with Unsupervised Learning.




Overview

This section focuses on analyzing Spotify audio features to uncover musical “vibes” using K-Means clustering and building a two-method recommendation system based on centroid distance and K-Nearest Neighbors (KNN) similarity.

2.1 Feature Selection for the Vibe Model

Selected musical attributes that best represent a song’s overall vibe, such as:

danceability

energy

tempo

valence

loudness

Features were scaled/standardized to ensure equal contribution to clustering.

These features capture how listeners feel a track, making them suitable for grouping songs based on mood.

2.2 K-Means Clustering Analysis

Applied K-Means to the scaled vibe-based feature set.

Identified 4 distinct clusters, each representing a different musical mood or style.

Analyzed cluster structures by comparing:

average feature values,

representative songs closest to each cluster centroid,

differences in popularity across clusters.

Clusters showcased meaningful separation between high-energy tracks, calm/acoustic songs, upbeat pop, etc.

2.3 Clustering Evaluation

Evaluated clustering quality using:

Silhouette Score

t-SNE visualization

2D feature-space plots (e.g., Energy vs Loudness)

The four-cluster solution displayed:

well-separated structure,

good consistency,

interpretable mood-based grouping.

Demonstrated that selected features naturally form coherent vibe clusters.

2.4 Recommendation System (Centroid + KNN)

Two recommendation methods were implemented:

1. Centroid-Based Recommendations

Returns songs closest to the cluster centroid of the input track.

Produces stable, mood-consistent recommendations.

Reflects the general vibe of the cluster more than individual track details.

2. KNN-Based Recommendations

Computes similarity between the input song and its nearest neighbors in feature space.

Captures fine-grained similarity:

tempo

acousticness

energy

rhythm patterns

Often returns more personalized, track-specific recommendations.

Comparison

Centroid method → broad, vibe-focused suggestions.

KNN method → detailed, content-specific suggestions.

Combined, they provide both general mood accuracy and precision in similarity.

Example Demonstration

Generated top recommendations for “Oops!... I Did It Again” using both methods to show practical differences in output and behavior.
