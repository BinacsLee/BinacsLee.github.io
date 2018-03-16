    
    
    const int INF=0x3f3f3f3f;
    int n,m;
    int d[105];
    struct edge{
        int from,to,cost;
    }es[10005];
    void bellman_ford(int s){
       d[s]=0;
       while(true){
            bool update=false;
           for(int i=0;i<m;i++){
                edge e;
                if(d[e.from]!=INF&&d[e.to]>d[e.from]+e.cost){
                    d[e.to]=d[e.from]+e.cost;
                    update=true;
                }
            }
            if(!update) break;
        }
    }
    
    
