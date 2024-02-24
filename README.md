## atcoder 刷题笔记

### at_abc_338
#### [C](https://www.luogu.com.cn/problem/AT_abc338_c)
枚举菜品A的数量从而计算出B的数量最后求max即可
#### [D](https://www.luogu.com.cn/problem/AT_abc338_d)
设断掉以点$i$与点$i+1$之间的路后走完路程的花费为$v_i$。对于从$x-y$，可以考虑走$x+1,x+2...y$也可以从$x-1,x-2,..,y$，假设第一种方式的路程为$d$，则断掉第一种方式的路$j$有$v_j + n-d$,对于第二种方案的则有$v_j + d$,利用差分或者DS方法优化即可
#### [E](https://www.luogu.com.cn/problem/AT_abc338_e)
考虑将圆拉直，若两个区间没有交点或者包含则弦不相交，考虑使用栈结构
#### [F](https://www.luogu.com.cn/problem/AT_abc338_f)
先用floyd求出任意两点之间的最小距离然后考虑状压dp，令$dp[i][j]$表示到过点的状态为$i$，目前在$j$的最小花费,转移为$dp[i|(1<<(k-1))][k] = \min{dp[i|1<<(k-1)][k],dp[i][j]+dis[j][k]}$
### at_abc_339
#### [C](https://www.luogu.com.cn/problem/AT_abc33_c)
求前缀和最小值，若最小值为$x<0$,则说明一开始至少有$-x$人,否则为$0$人
#### [D](https://www.luogu.com.cn/problem/AT_abc339_d)
把两个人当做一个人做bfs即可
#### [E](https://www.luogu.com.cn/problem/AT_abc339_e)
考虑dp，$dp[i] = \max_{j<i}^{(a[j]-a[i])<d}{f[j]}+1$。用线段树维护值域内每个数的dp值的最大值
