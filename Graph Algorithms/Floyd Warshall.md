### **Floyd Warshall Algorithm** 
*Floyd-Warshall Algorithm* - Shortest path from every vertex to every other vertex. Shortest path between all pairs of vertices, negative 
edges allowed. 

Keep a distance 2-d array initialized to the weights between each pair of vertices. Then if the condition 
dist[i][j] > dist[i][k] + dist[k][j] holds true, then update dist[i][j] as dist[i][k] + dist[k][j]. 

Time Complexity: **O(V^3)** 

Implementation:
```
let V = number of vertices in graph
let dist = V x V array of minimum distances
for each vertex v
  dist [v][v] <- 0
for each edge (u, v)
  dist[u][v] <- weight(u, v)
for k from 1 to V
  for i from 1 to V
    for j from 1 to V
      if dist[i][j] > dist[i][k] + dist[k][j]
        dist [i][j] <- dist[i][k] + dist[k][j]
      end if
```
 
