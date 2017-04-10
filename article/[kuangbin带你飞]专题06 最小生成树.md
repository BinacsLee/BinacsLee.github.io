## 2017-3-19~2017-3-20
## 题目链接 https://vjudge.net/contest/66965

### A	POJ 1251/M HDU 1301
两题一样 简单最小生成树 但是hduG++会WA C++AC //有空看编译器
A CE一次对于cmp函数 cmp(edge a,edge b) //not 'egge &a'

### B	POJ 1287 
RE一次 数组开小了

### C	POJ 2031
简单kruskal
### D	POJ 2421
RE一次 数组开小了
### E	ZOJ 1586
编译器选错CE一次 数组开小RE(Segmentation Fault)一次
### F POJ 1789 
做过 模版题
### G POJ 2349 
CE数组开小 WA一次
    
    if(cnt<p-s) return -1; //right p为点数
    if(cnt<n-s) return -1; //wrong n为case数..
    
    
### H	POJ 1751 
Special Judge</br>
     
     //以下为wrong
     for(int i=1;i<=n;i++){
        for(int j=i+1;j<=n;j++){
            double len=dis(i,j);
            addedge(i,j,len);addedge(j,i,len);
        }
    }
    //以下为正确的写法
    for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
            double len=dis(i,j);
            addedge(i+1,j+1,len);addedge(j+1,i+1,len);
        }
    }
    //唉智障贡献了一WA 写下标注意吧
     
### I	POJ 1258 
做过 模版题
### J	POJ 3026  MARK
bfs+最小生成树(有个很坑的地方是测试数据输入行列后面还跟着空格...gets解之..</br>
MLE好几次.. 问题出在bfs 经验教训是:
    
    // 1
    for(i=0;i<4;i++) {int xx=...... q.push(ee);}
    vis[ee.x][e.yy]=true;   //在for结束再后写不对 这样多算的太多了
    //2
    for...
    vis[e.x][e.y]=true;    //mdzz....
    //3
    vis[e.x][e.y]=true;
    for...                 //function same with 1....
    

这个题蛮好的 mark住闲着无聊回头看
### K	POJ 1679 
//??次小生成树? 专题八第一题就是 放那了
### L	HDU 1233
简单模版题
### M HDU 1301 见A
### N	HDU 1875
模版题


</br>


 1. Pro.A CE 边edge类型的cmp函数不用写&
 2. Pro.B,D,E RE es数组开太小了
 3. Pro.H 数组下标写错WA
 4. Pro.J "Borg Maze POJ - 3026" 值得记忆 bfs部分node e,ee定义在while循环内MLE 定义在前面就AC
 
 
 不知道为啥M G++WA C++AC</br>
 另外 K放在生成树专题
 
 
