### 2017-02-13
### 题目链接 https://vjudge.net/contest/149928


## A poj1979
从@点开始 最多能走多少个'.'

dfs

WA 1 自己第一次写的时候忘记加 tiles[new_h][new_w]=='.'

EXP 1 main内部注意不能再次定义全局变量( w h

EXP 2 这种上下左右移动的可以定义全局数组 int dir[4][2]={{1,0},{-1,0},{0,1},{0,-1}};方便操作。



## B poj3009
从S移动到G 通过移动后碰撞墙壁可以使墙壁消失(更新地图 PS紧挨墙壁无法向墙壁移动故不能往那边走啦QAQ

问最少操作次数 dfs (bfs的时候因为碰撞更新并发会相互影响???

EXP 1 注意回溯的写法= =
EXP 2 坐标边界判断的一点经验


    
    px+=dir[i][0],py+=dir[i][1];if(px<=0||px>h||py<=0||py>w) break; //这里
    
    
    
    


          
## C poj3669
bfs

流星撞地球 M个在Ti撞击到(Xi,Yi) (撞击点有范围故人物不在撞击点范围内亦可但必须第一象限 撞击后撞击点及相邻四个点均不能走
人物初始位置在原点 单位时间只能上下左右走一步 不能对角移动


## D poj3718
next_permutation



## E poj3187
类似斐波那契数列的应用 同时结合next_permutation

## F poj3050
简单dfs

