# DBSCAN Clustering

This repository contains implementation of DBSCAN unsupervised machine learning algorithm.

## What is DBSCAN?

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is an unsupervised machine learning algorithm used for clustering. It groups together points that are closely packed in areas of high density, separating them from areas of low density[1].

## Key Concepts

- **Core Points**: Points that have at least `minPts` number of points within a distance `epsilon`.
- **Border Points**: Points that are within `epsilon` distance of a core point but don't have `minPts` neighbors themselves.
- **Noise Points**: Points that are neither core points nor border points.

## How DBSCAN Works

1. Select an arbitrary point from the dataset.
2. Find all points within `epsilon` distance of this point.
3. If the number of neighboring points is greater than or equal to `minPts`, mark it as a core point and start a new cluster.
4. Recursively add all directly reachable points to the cluster.
5. Move to the next unvisited point and repeat steps 2-4.
6. Continue until all points have been visited.

## Advantages of DBSCAN

- Can find arbitrarily shaped clusters
- Robust to outliers
- Does not require specifying the number of clusters beforehand
