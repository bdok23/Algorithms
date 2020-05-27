### **Kruskal's Minimum Spanning Tree Algorithm**
*Spanning Tree* - Given a connected and undirected graph, the spanning tree is a subgraph that is a tree that connects all the vertices
 together. 
 
*Minimum Spanning Tree (MST)* - A spanning tree with the least weight among the other spanning trees. 

An MST has V-1 edges, where the original graph has V vertices. 

MST is useful for network design, approximation for NP problems, cluster analysis, ...

*Kruskal's Algorithm* - Finds an MST. 

1. Sort all the edges in non-decreasing order of their weight.
2. Pick the smallest edge. Check if it forms a cycle with the spanning tree formed so far. If cycle is not formed, include this edge. Else, discard it.
3. Repeat step#2 until there are (V-1) edges in the spanning tree.

Use union-find to detect a cycle. 
