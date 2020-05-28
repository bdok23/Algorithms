### **Dijkstra Shortest Path Algorithm**
*Dijkstra* - Given a graph and a source vertex of the graph, it finds the shortest path from that node to all other nodes in the graph. 

This method obviously accounts for the weights in a graph. 

- You start with the source node. You add it to the sptSet, which is initialized to {0, INF, INF, ...}. 
- Then you look at adjacent nodes, and find the one with the smallest distance/weight and add it to the sptSet. 
- And then you look at the node with the smallest distance from source node that is not on sptSet, add it to the set, and keep going until you get a 
*Shortest Path Tree*. 

Time Complexity: **O(V^2)** or **O(E * Log v)**

Applications: Finding the shortest path between two nodes

 
 
