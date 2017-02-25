    
    struct node{
        int x;
        node *lchild,*rchild;
    };
    node *r=NULL;
    
    
    for(int i=0;i<n;i++){
        cin>>x;
        insert(x,r);   //包含创建
    }
    
    
    void insert(int x,node *&t){
        if(t==NULL){
            t=(node *)malloc(sizeof(node));
            t->x=x,t->lchild=t->rchild=NULL;
        }else{
           if(x<t->x) insert(x,t->lchild);
           else insert(x,t->rchild);
        }
    }
    
    void preorder(node *l){
       if(l==NULL) return;
       if(l!=r) printf(" ");
       printf("%d",l->x);
       preorder(l->lchild);
       preorder(l->rchild);
    }
    
    
    


    
    
    
    
    
    
    
    
    
    
    
    
    
