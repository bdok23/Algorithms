#include \<fstream>
  
#include \<iostream>
  
#include \<vector>
  
using namespace std;

vector \<int> parent;


//Finds root of node x
```
int root(int n){
	while(parent[n] != n){
	  parent[n] = parent[parent[n]];
	  n = parent[n];
	}
	return n;
}
```

//Connects trees i and j
```
void connect(int i, int j, int rank[]){
	int rj = root(j); int ri = root(i);
    //cout << ri <<  " " << rj << "\n";
  if(ri != rj){
	  if(rank[ri] < rank[rj]){
	    parent[ri]=rj;
	    rank[rj]+=rank[ri];
	  }
	  else{
	    parent[rj]=ri;
	    rank[ri]+=rank[rj];
	  }
  }

}
```


```
int main() {
  ofstream fout ("output.out");
  ifstream fin ("input.in");
  //fout << "Number of nodes?: ";
  int numNodes; fin >> numNodes;
  int rank[numNodes];
  //Sets ranks to 1
  for(int i = 0; i < numNodes; i++){
    rank[i] = 1;
    parent.push_back(i);
  }
  
  for(int i = 0; i > -1; i++){
    int x; fin >> x; 
    if(x == -1){break;}
    int y; fin >> y;
    connect(x, y, rank);
  }
  ```

  //rest of the code is for output purposes only. The above code is the actual algorithm
  ```
  for(int i = 0; i < numNodes; i++){
    fout << root(i) << " ";
  }

  return 0;
}
```
