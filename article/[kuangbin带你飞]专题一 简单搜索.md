### 2017-3-9 ~ 2017-3-10
### 题目链接 https://vjudge.net/contest/65959
---------
## A POJ - 1321
简单dfs 注意回溯
---------
## B POJ - 2251
3维bfs 坐标写错MLE
---------
## D POJ - 3279
    
    /*状态压缩+对第一行暴搜
    二进制搜索 不会 要再做*/
     
    cout <<"to-do"<<endl;
    
    
---------
## E POJ - 1426
暴力dfs 粘的代码 有空再看 
---------
## F POJ - 3126
 bfs 
---------
## G POJ - 3087
 bfs  //see again
---------
## H POJ - 3414
    
    /*这种类型 bfs*/
    
     
    cout <<"to-do"<<endl;
    
    
---------
## I FZU - 2150
    
    /*总觉得有办法找到连通分量片里相距最远的俩点
    而多数题解使用的是暴搜 暴力枚举两个点的位置 再做*/
    
    cout <<"to-do"<<endl;
    
    
---------
## J UVA - 11624
    
    /* 对于bfs 
    如果判断结果的条件写在for内 显然节省入队再出队的时间 但是无法处理第一个入队的源节点即满足结果条件的情况；
    另外关于二维／三维 其struct结构应该如何使用已达到高效且节省空间的目的 此题int 17MB short 10(对于测试数据
    还是太大 (UVA好像没有MLE这个返回提示的  todo*/
    
    cout <<"to-do"<<endl;
    
    
---------
## K POJ - 3984
 简单bfs 
---------
## L HDU - 1241
 简单dfs 统计连通块数量 
---------
## M HDU - 1495
 dfs H的简单版 有空再做 另外有种解法十分简单
     
    //再看
    #include <cstdio>
    int gcd(int x, int y){
    return y ? gcd(y, x % y) : x;
    }
    int main(){
        int a, b, c;
        while (scanf("%i%i%i", &a, &b, &c), a + b + c) {
            (a /= gcd(b, c)) & 1 && ~puts("NO") || printf("%i\n", a - 1);
        }
        return 0;
    }
    
    
---------
## N HDU - 2612
2次bfs即可



