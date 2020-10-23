# CUSTOMIZATION

If you would like to implement a specific clustering algorithm, which is not being covered by 
Blanket Clusterer, it should be easy to do this, by simply creating a new Python class, then 
extend the `GenericClustering.py` class and implement the method `clusterize_cluster(cluster)`.

All other methods should remain the same, unless you 