# HOW IT WORKS

If you fancy getting into the project, this page _might_ be useful for you.

## Architecture

The Python module is build upon already existing clustering algorithms, courtesy of 
[scikit-learn](https://scikit-learn.org/stable/) and [NLTK](https://www.nltk.org/).

The currently supported algorithms are K-Means, Agglomerative, BIRCH and DBSCAN, with more to come
in the future.

The implementation of the algorithms were divided into as many classes as there are algorithms, 
and all classes extend a main parent class `GenericClustering.py` which contains methods that are static
and used by all other clustering algorithms.

![Module Structure](../_images/implementation/Blanket_Clusterer_Structure.png)

## Clustering

The methods have certain explanation in the code itself, so covering them here, is redundant.

The only method that needs a better explanation is the `clusterize_cluster(cluster)` method, which
is implemented in every clustering class.

```python
def clusterize_cluster(self, this_cluster):
        """
        Function used to clusterize a cluster
        Implement it for each clustering algorithm
        :param this_cluster:
            Cluster needed to be clusterized
        :return:
            Dictionary of new clusters
        """
        return None
```

TODO: Continue