
    
    
    const int MAXV=20050; //最大点数
    const int MAXE=2000050; //最大边数
    int father[MAXV],tot,n;//tot 边数
    char data[MAXV][10];
    struct Edge{
        int u,v,w;
    }edge[MAXE];
    
    bool cmp(Edge a,Edge b){
        return a.w<b.w;
    }
    int find(int x){
        if(father[x]==x) return x;
        return father[x]=find(father[x]);
    }
    void addedge(int u,int v,int w){
        edge[tot].u=u,edge[tot].v=v,edge[tot++].w=w;
    }
    int kruskal(int n){ //传入点数 返回最小生成树权值 -1表示不连通
        sort(edge,edge+tot,cmp);
        int cnt=0,ans=0; //cnt用来计算加入的边数
        for(int i=0;i<tot;i++){
            int u=edge[i].u,v=edge[i].v,w=edge[i].w;
            int t1=find(u),t2=find(v);
            if(t1!=t2){
                ans+=w;
                father[t1]=t2;
                cnt++;
            }
            if(cnt==n-1){
                break;
            }
        }
        if(cnt<n-1) return -1;
        else return ans;
    }
    
    
