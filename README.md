# Part 2: Clustering Using K-Means & Recommendation System

## Overview
This section focuses on analyzing Spotify audio features to uncover musical “vibes” using **K-Means clustering** and building a two-method recommendation system based on **centroid distance** and **K-Nearest Neighbors (KNN)** similarity.

---

## 2.1 Feature Selection for the Vibe Model
- Selected audio attributes representing a song’s vibe:
  - `danceability`, `energy`, `tempo`, `valence`, `loudness`.
- Features were **scaled** to ensure equal contribution.
- These features emphasize how listeners *experience* a track.

---

## 2.2 K-Means Clustering Analysis
- Applied **K-Means** on the standardized vibe features.
- Identified **4 distinct clusters**, each aligned with a different musical mood.
- Analyzed clusters by:
  - Average feature values
  - Songs closest to each centroid
  - Popularity differences across clusters
- Clusters reflected clear separation between energetic, calm, acoustic, and upbeat songs.

---

## 2.3 Clustering Evaluation
- Evaluated clustering quality using:
  - **Silhouette Score**
  - **t-SNE visualization**
  - **Energy vs Loudness** plots
- Four-cluster configuration showed:
  - Good cohesion
  - Strong separation
  - Stable mood-based grouping

---

## 2.4 Recommendation System (Centroid + KNN)
Two recommendation approaches were implemented:

### Centroid-Based Recommendations
- Finds songs closest to a cluster's **centroid**.
- Produces **stable, consistent mood-based** recommendations.
- Represents general vibe of the cluster.

### KNN-Based Recommendations
- Finds **nearest neighbors** to the input song.
- Captures fine-grained similarity in:
  - Tempo
  - Energy
  - Acousticness
  - Other musical patterns
- More **song-specific** than centroid method.

### Comparison
- **Centroid** → Broad vibe similarity.
- **KNN** → Precise audio similarity.
- Both combined provide balanced recommendation quality.

### Example Output
- Recommendations were generated for **"Oops!... I Did It Again"** using both methods to illustrate their behavioral differences.

---

## Short Summary
This module applies K-Means clustering to group songs by mood using audio features, then provides recommendations using both centroid-based and KNN-based similarity. The system captures both overall vibe and detailed audio characteristics for improved music recommendation.
