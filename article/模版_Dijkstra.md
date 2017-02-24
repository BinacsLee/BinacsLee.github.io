    
    int n,m;//点 边
    int d[maxv];//存储最后的距离值
    int cost[maxv][maxv]
    bool used[maxv];
    void dijkstra(int s){
        d[s]=0;
        while(true){
            int v=-1;
            for(int u=0;u<n;u++)
                if(!used[u]&&(v==-1||d[u]<d[v])) v=u;
           if(v==-1) break;
            used[v]=true;
            for(int u=0;u<n;u++){
               d[u]=min(d[u],d[v]+cost[v][u]);
            }
       }
    }
    
    
*如果是无向图 输入的时候*
    
    cost[u][v]=cost[v][u]=w;
    
    
    
