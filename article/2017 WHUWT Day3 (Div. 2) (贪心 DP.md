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
构造<br>
题意...输入序列长度n 和所给参数组数m<br>
每m行 第x-第y的位置上没有出现过的最小的自然数为该组mex(含0<br>
输出可能的一个序列<br>

//



## C Codeforces 762 B
only-usb only-ps/2 both的电脑共a b c台<br>
m个鼠标 m行输入价值和类型<br>
输出适配个数和最小cost<br>
使用一个结构数组 记录种类价值按价值排序<br>
WA 1 数组开的太小 RE( 一般+5<br>
EXP 1 一个数组<br>
EXP 2 想好条件怎么分<br>

## D Codeforces 671 A
如果一个人去捡了某个瓶子那么他之后肯定会走到箱子的位置上去<br>
然后再去捡的话就是箱子到某个瓶子的距离 那么我们可以分这样三种情况考虑<br>
1.人物A一个人捡完了所有的瓶子<br>
2.人物B一个人捡完了所有瓶子<br>
3.人物A捡了某个瓶子 人物B捡了某个瓶子<br>
对于3 这两个瓶子肯定不一样 那么当他们都回到箱子的时候无论谁去捡剩下的瓶子其距离都是固定的<br>
那么我们可以先计算出所有瓶子到箱子的距离然后加上得到结果sum 然后如果人物A去捡了一个第i个瓶子那么 sum+dis(A,i)-dis(箱子,i) <br>
依次去算剩下的两种情况 然后三者中取一个最小值<br>



## E Codeforces 698 A
dp <br>
状态初始化 状态转移 <br>
WA 1 数组开的小<br>



## F Codeforces 756B
dp<br>
EXP 1 想好条件怎么分<br>


