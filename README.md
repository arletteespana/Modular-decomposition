# Modular decomposition

Implementation of the algorithms exposed in *A survey of the algorithmic aspects of modular decomposition* by Michel Habib and Christophe Paul, 2010.

### Installation and Dependencies

They require Python 3.7 or higher. They have the following dependencies:

- [NetworkX](https://networkx.org/)
- [Matplotlib](https://matplotlib.org/)

### Usage

The functions `ModularPartition`, `FactPerm`, `FractureTree`, and `ModularDecomposition` require a NetworkX `Graph`, a list with one partition of its vertices set, a vertex, and one list as input.

## Modular partition

Given a graph G and a partition P of its vertices set, this function give as an output the coarsest modular partition of G with respect to P.

```
Gtest = nx.complete_bipartite_graph(2,8)
Ptest = [[5],[0,7,8],[1,6,9,2,3,4]]
print(ModularPartition(Ptest,Gtest))
```
## Factoring permutation

Given a graph G and vertex v, this function give as an output the factoring permutation of G.

```
Gtest = nx.Graph()
Gtest.add_edges_from([(1,2),(1,3),(1,4),(2,4),(2,5),(2,6),(2,7),(3,4),(3,5),(3,6),(3,7),(4,5),(4,6),(4,7),(5,6),(5,7),(6,8),(6,9),(6,10),(6,11),(7,8),(7,9),(7,10),(7,11),(8,9),(8,10),(8,11),(9,10),(9,11)])
print(FactPerm(Gtest, 1))
```

## Fracture tree

Given the factoring permutation of a graph G, this functions give as an output the fracture tree, that is actually a good estimation of the Modular decomposition of G.

```
Gtest = nx.Graph()
Gtest.add_edges_from([(1,2),(1,3),(1,4),(2,4),(2,5),(2,6),(2,7),(3,4),(3,5),(3,6),(3,7),(4,5),(4,6),(4,7),(5,6),(5,7),(6,8),(6,9),(6,10),(6,11),(7,8),(7,9),(7,10),(7,11),(8,9),(8,10),(8,11),(9,10),(9,11)])
H = nx.Graph(Gtest)
H.to_undirected()
FractureTree(1,H)
```

## Modular decomposition

Given a graph G, this functions give as an output a good estimation of the Modular decomposition of G.

```
Gtest = nx.Graph()
H = nx.Graph(Gtest)
H.to_undirected()
ModularDecomposition(H)
```

## References

Habib M., Paul C. A survey of the algorithmic aspects of modular decomposition, Comp. Sci. Rev., 4 (2010), pp. 41-59.
