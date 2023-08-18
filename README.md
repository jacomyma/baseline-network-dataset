# BaNeDa (baseline-network-dataset)
A dataset of networks (graphs) to test for a number of basic properties

*At the moment, this is just a draft.*

This dataset will have at least three sections:
* A. Different types of graphs: directed, with self-loops...
* B. Different topologies: stable and clique, lattice, scale-free...
* C. Different network sizes.
* D. Staples (optional).

Section A aims to allow testing whether a given library deals with different kinds of graphs appropriately. These networks will be quite small for convenience. It notably aims to help building consensus on how to compute graph metrics (betweenness centrality...) in different situations. Indeed, the reference literature is sometimes ambiguous about how to deal with things like self-loops, mixtures of directed and undirected edges, etc. Section B aims to help assessing how algorithms behave depending on the topology of a network. Indeed, some algorithms are efficient with a lattice but not with a scale-free network, or vice versa. Section C aims to allow benchmarking performance and focuses on networks of different sizes. The optional section D could contain staple networks such as C. Elegans, Karate Club etc.

## Similar works
[Netzschleuder: Network catalogue, repository and centrifuge.](https://networks.skewed.de/)
[SNAP: Stanford Large Network Dataset Collection](https://snap.stanford.edu/data/)
[OGB: Open Graph Benchmark](https://ogb.stanford.edu/)

## Roadmap
1. Draft specifications for section A
2. Generate a first iteration of the networks
3. Evaluate the project with other actors
4. ...

# Section A: Types of networks
## Properties covered
* Type: directed|undirected|mixed
* Self-loops allowed: true|false
* Parallel edges allowed: true|false
* Edges: true|false
* Edge weights: true|false
  * Edge weights are integer: true|false
  * Edge weigths are positive of null: true|false
  * Edge weigths do not exceed 1: true|false
* Dynamic: true|false (time dimension)
* Edge attributes: true|false (aside from weight)
  * Edge attribute type: boolean|integer|float|string|other
* Node attributes: true|false
  * Node attribute type: boolean|integer|float|string|other
* Connected: true|false (one or more connected components)
* Cyclic: true|false (false = acyclic graph; trees are typically connected acyclic undirected graphs)
* Modes: monopartite|bipartite|npartite Monopartite (resp. bipartite) graphs are sometimes called one-mode (resp. two modes). One can have n-partite networks with n>2.
