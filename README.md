# Geographical Regionalization (Clustering)

Geographical regionalization is the process of dividing geographical areas into smaller regions based on shared characteristics. This repository demonstrates this process with regionalized map of Prague city as an example.

## Algorithm steps

- Initial clustering: K-means algorithm, assigns regions into clusters, regions of the same cluster can be disjoint on the actual map.

- Connected components creation: run of BFS on the geographical map that unifies regions of the same cluster in case they share a border on the map.
  At the end, each region is either a part of a connected component of regions with of the same cluster or has undefined cluster (in case it's connected component was not the largest one in the cluster).

- Undefined regions handling: K-Nearest-Neighbors algorithm that assigns a cluster to all undefined regions, based on the prevailing cluster of it's geographical neighbors.

## Optimal number of clusters

The optimal number of clusters was found by the Elbow rule, 4 clusters achieve the best dispersion, while keeping a number of clusters relatively low.
