# Modular descomposition

Implementation of the algorithms exposed in *A survey of the algorithmic aspects of modular decomposition* by Michel Habib and Christophe Paul, 2010.

### Installation and Dependencies

They require Python 3.7 or higher. They have the following dependencies:

- [NetworkX](https://networkx.org/)
- [Matplotlib](https://matplotlib.org/)

### Usage

The function `ModularPartition` require a NetworkX `Graph` and a list with one partition of its vertices set as input.

## Modular partition

Given a graph G and a partition P of its vertices set, this function give as an output the coarsest modular partition of G with respect to P.

```
Gtest = nx.complete_bipartite_graph(2,8)
Ptest = [[5],[0,7,8],[1,6,9,2,3,4]]
print(ModularPartition(Ptest,Gtest))
```


