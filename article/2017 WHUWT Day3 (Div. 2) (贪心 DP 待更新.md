### 2017-02-15
### 题目链接 https://vjudge.net/contest/149930#problem



## A poj2376
区间覆盖
不用考虑到了某个奶牛 已经超过T再跳出去 消耗很少的没必要

典型阿QAQ写法照模版
以下是模版

    cow[N+1].first=0x7fffffff;
    int p=0,ans=0,tem=0;
    bool flag=false;
    for(int i=1;i<=N;i++){
        if(cow[i].first<=p+1){
            if(tem<cow[i].second) tem=cow[i].second,flag=true;
            if(cow[i+1].first>p+1&&flag) p=tem,ans++,flag=false;
        }
    }
    if(p<T) cout <<-1<<endl;
    else cout <<ans<<endl;
    
//todo



## B Codeforces 739 A
构造
题意...输入序列长度n 和所给参数组数m
每m行 第x-第y的位置上没有出现过的最小的自然数为该组mex(含0
输出可能的一个序列

//



## C Codeforces 762 B
only-usb only-ps/2 both的电脑共a b c台
m个鼠标 m行输入价值和类型
输出适配个数和最小cost
使用一个结构数组 记录种类价值按价值排序
WA 1 数组开的太小 RE( 一般+5
EXP 1 一个数组
EXP 2 想好条件怎么分

## D Codeforces 671 A
//todo



## E Codeforces 698 A
dp 
状态初始化 状态转移 
WA 1 数组开的小



## F Codeforces 756B
dp
EXP 1 想好条件怎么分


