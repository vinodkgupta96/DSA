# DSA
Data Structure and Algorithms
Collections of DSA concepts for interview preparation.

1. Graphs
	1. Given the adjacency list of a bidirectional graph. Your task is to return the adjacency list for each vertex.
	2. BFS of graph (connected)
		public ArrayList<Integer> bfsOfGraph(int V, ArrayList<ArrayList<Integer>> adj)
    {
        // Code here
        ArrayList<Integer> result = new ArrayList<>();
        boolean visited[] = new boolean [V];
        Queue<Integer> q = new LinkedList<Integer>();
        q.add(0);
        visited[0]=true;
        while(!q.isEmpty()){
            int curr = q.peek();
            q.remove();
            result.add(curr);
            for(Integer x : adj.get(curr)){
                if(!visited[x]){
                    q.add(x);
                    visited[x]=true;
                }
            }
        }
        return result;
    }
    3. DFS of graph (connected)

    public ArrayList<Integer> dfsOfGraph(int V, ArrayList<ArrayList<Integer>> adj)
    {
        // Code here
        boolean [] visited = new boolean[V];
        ArrayList<Integer> result = new ArrayList<>();
        result.add(0);
        visited[0] = true;
        dfsRec(result,visited,0,adj);
        return result;
        
    }
    
    
    public void dfsRec(ArrayList<Integer> result, boolean [] visited, int s, ArrayList<ArrayList<Integer>> adj){
        for(Integer x:adj.get(s)){
            if(!visited[x]){
                visited[x] = true;
                result.add(x);
                dfsRec(result,visited,x,adj); 
            }
        }
    }

    4. Find the number of islands 

    public int numIslands(char[][] grid)
    {
        // Code here
        int max_count = 0;
        int row = grid.length;
        int col = grid[0].length;
        for(int i = 0;i<row;i++){
            for(int j =0;j<col;j++){
                if(grid[i][j] == '1'){
                   grid[i][j] = 'A';
                   numIslandsRecurr(i , j, grid,row,col);
                   max_count++;
                }
            }
        }
        return max_count;
    }
    
    
    public void numIslandsRecurr(int i , int j, char[][] grid,int row, int col){
       
        int x, y;
        if(i+1<row && j+1<col && grid[i+1][j+1]=='1'){
            x= i+1;
            y=j+1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);
        }
        if(i+1<row && j-1>=0 && grid[i+1][j-1]=='1'){
            x= i+1;
            y= j-1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(i-1>=0 && j+1<col && grid[i-1][j+1]=='1'){
            x= i-1;
            y=j+1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(i-1>=0 && j-1>=0 && grid[i-1][j-1]=='1'){
            x= i-1;
            y=j-1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(j+1<col && grid[i][j+1]=='1'){
            x= i;
            y=j+1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(j-1>=0 && grid[i][j-1]=='1'){
            x= i;
            y=j-1;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(i+1<row  && grid[i+1][j]=='1'){
            x= i+1;
            y=j;
           grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
        if(i-1>=0  && grid[i-1][j]=='1'){
            x= i-1;
            y=j;
            grid[x][y] = 'A';
            numIslandsRecurr(x,y,grid,row,col);

        }
    }

