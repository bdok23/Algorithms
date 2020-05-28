### **Prim's Minimum Spanning Tree**
*Prim's Algorithm* - Finds an MST. 

Goal:
1. Create a visited list containing all vertices already included in the MST and another set with the ones not yet included. 
2. The algorithm considers all pairs of edges between these two sets, and picks the minimum weight. 
3. Then, it moves the other endpoint into the visited list and keeps going until the non-visited set is empty. 

Algorithm:
1. Create a set mstSet keeping track of the vertices included in the MST.
2. Assign a key value to all the vertices in the input graph. Initialize all the key values to INF and 0 as the first (so that it is picked 
first). 
3. while (mstSet doesn't include all vertices): 
  - Pick a vertex u in the non-visited set with the minimum key
  - Include u to the mstSet
  - Update the key value of all adjacent vertices of u (not in mst) with the weights. To update, iterate through all the vertices. 
  Also if there is already a key value, then update only if it is less than that key value. 
  
  Prim's is better if their is a higher vert
