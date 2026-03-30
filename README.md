K-Means-Clustering-of-Dense-Network-Topology-with-Energy-Analysis-
K-Means clustering lab exploring node grouping and energy visualization using Python.

1. Introduction

This lab focuses on the implementation and analysis of the K-Means clustering algorithm using Python. The objective is to group a set of nodes based on their spatial positions and to examine how changes in the number of clusters affect the results. Additionally, the lab explores the distribution of energy values across clusters through visualization techniques.


2. Methodology

A dataset of 600 nodes was generated, where each node is assigned:

* An X-coordinate
* A Y-coordinate
* A randomly generated energy value

The K-Means clustering algorithm was applied to group the nodes based on their spatial coordinates (X and Y). The energy values were not used in the clustering process but were analyzed separately.

The experiment was conducted using two different values of *k*:

k = 7 (initial clustering)
k = 3 (modified clustering)

3. Tools and Technologies

The following Python libraries were used:

* NumPy
* Pandas
* Matplotlib
* NetworkX
* Scikit-learn
* SciPy

4. Results and Observations

4.1 Effect of Changing k

When the number of clusters was reduced from 7 to 3:

* Clusters became larger and less specific
* More nodes were grouped together
* The level of detail in clustering decreased

With k = 7:

* Clusters were smaller and more refined
* Node grouping was more precise
* Separation between clusters was clearer

4.2 Cluster Distribution

The distribution of nodes across clusters was not equal. One cluster contained significantly more nodes than the others, indicating that K-Means does not enforce equal cluster sizes. Instead, it groups nodes based on proximity to centroids.

4.3 Energy Analysis

Energy values were randomly assigned and not considered during clustering. As a result:

* Each cluster contained a mix of high and low energy nodes
* No cluster was inherently more energy-efficient than others
* Energy distribution varied independently of cluster boundaries


4.4 Visualization Insights

Three types of visualizations were generated:

1. Network Graph
   Displays nodes and their connections. Due to the density of the network, individual clusters are difficult to distinguish clearly.

2. 3D Scatter Plot
   Shows clustering results with different colors representing different clusters and centroids marked clearly.

3. 3D Surface Plot
   Represents energy distribution across the node space. Steep gradients indicate rapid changes in energy values.

5. Limitations of K-Means

* Requires the number of clusters (k) to be specified in advance
* Sensitive to initial centroid placement
* Does not consider additional attributes such as energy
* May produce imbalanced cluster sizes
* Performs poorly when clusters overlap

6. Conclusion

This lab demonstrates how K-Means clustering groups data based on spatial proximity rather than additional attributes like energy. The results highlight the importance of selecting an appropriate value for k, as it significantly impacts cluster size and accuracy. While K-Means is effective for partitioning data, its limitations must be considered when interpreting results.

7. How to Run the Project

1. Install the required libraries:
   pip install numpy pandas matplotlib networkx scikit-learn scipt

2. Run the script:
   python kmeans.py
   

8. Files Included

* `kmeans.py` – Implementation of the clustering algorithm
* Output screenshots – Visualizations generated from the program
