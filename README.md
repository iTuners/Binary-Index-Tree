# Binary-Index-Tree
树状数组求查询区间最小值
不同于一般的树状数组求区间总和的用法，树状数组还可用于维护并查询区间最小（最大）值，具体实现如下：
设需要查询的数组为c[],用tree[x]表示以x为根的子叶中的最小值，维护树时用make（k,v）函数更新tree[k]和tree[k]的所有祖先节点的值不大于v，查询区间（a,b）的最小值时依次与tree[b],tree[b-lowbit(b)]....比较，注意在a之前要停止（即b-lowbit（b）>a）,再依次与与c[now],c[now]-1,....c[a]比较（设最后一次比较为tree[b]，则now=b-1）,得到的最小值为区间最小值。
例题：https://www.luogu.com.cn/problem/P1816
解答在code中给出。
