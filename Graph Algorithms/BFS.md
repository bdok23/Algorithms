### Breadth First Search
*Graph Traversal* - Visiting every vertex and edge exactly once in a well-defined order.

*BFS* - A traversing algorithm where you start from the source node and traverse the graph layerwise, exploring the neighbor nodes. 

You go through every vertex and you traverse the neighbor nodes and mark them as visited (to keep track). 

Time Complexity: **O(V+E)** - V = Number of nodes, E = Number of edges

Applications: Finding the level of a node in a given tree. Checking if a node exists in a tree. 


Implementation:

```
   vector <int> v[10] ;   //Vector for maintaining adjacency list explained above
    int level[10]; //To determine the level of each node
    bool vis[10]; //Mark the node if visited 
    void bfs(int s) {
        queue <int> q;
        q.push(s);
        level[ s ] = 0 ;  //Setting the level of the source node as 0
        vis[ s ] = true;
        while(!q.empty())
        {
            int p = q.front();
            q.pop();
            for(int i = 0;i < v[ p ].size() ; i++)
            {
                if(vis[ v[ p ][ i ] ] == false)
                {
            //Setting the level of each node with an increment in the level of parent node
                    level[ v[ p ][ i ] ] = level[ p ]+1;                 
                     q.push(v[ p ][ i ]);
                     vis[ v[ p ][ i ] ] = true;
      }
            }
        }
    }
    
