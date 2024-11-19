## AHC

In this assignment, I implemented Agglomerative Hierarchical Clustering (AHC) using Object Oriented Programming (OOP) principles from scratch. The goal was to create a fully functional AHC model without relying on pre-existing libraries or implementations, except for random and matplotlib. This process not only involved programming the clustering logic but also included designing the AHC tree and visualizing the results.

# Key Implementation steps
1. I generated 100 random observations in 3D space (R3), with coordinated uniformly distributed between -50 and 50. A fixed random seed, based on hypothetical birthday ensured reproducibility.
2. A function was developed to calculate the Euclidean distance any two points in R3, forming the basis for clustering decisions.
3. The core of the AHC algorithm, a Node class was implemented. Each node in the AHC tree represents a cluster and has attributes for;
-  Cluster: A list of points in the cluster.
-  Height: Height of the node in the tree.
-  LeftChild/RightChild: Links to child nodes, representing merged clusters.
4. Multiple linkage methods were implemented to compute distance between clusters:
-  Single Linkage: Minimum distance between any two points in the clusters.
-  Complete Linkage: Maximum distance between any two points in the clusters.
-  Average Linkage: Average distance between all points in the clusters.
-  Centroid Linkage: Distance between the centroids of the clusters.
5. A function was implemented to determine which clusters should merge at each step based on the chosen linkage method. The output was a new node representing the merged cluster.
6. The complete AHC algorithm was developed to iteratively merge clusters until all points formed a single cluster. The algorithm relied on the previously implemented Node class and linkage functions.
7. A cutTree function was created to segment the tree into a specified number of clusters (k). This allowed for flexible cluster analysis and comparison.
8. Using matplotlib, I plotted the 3D observations, coloring points based on their clusters for k = 5. Visualizations were generated for each linkage method, providing insight into effects on clustering.
