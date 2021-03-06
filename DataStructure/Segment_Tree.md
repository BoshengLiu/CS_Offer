# 线段树

线段树是一种二叉树形结构，属于平衡树的一种。它将线段区间组织成树形的结构，并用每个节点来表示一条线段。一棵[1,10)的线段树的结构如下图所示： 

![][1]

可以看到，线段树的每个节点表示了一条前闭后开，即[a,b)的线段，这样表示的好处在于，有时候处理的区间并不是连续区间，可能是离散的点，如数组等。这样就可以用[a,a＋1)的节点来表示一个数组的元素a，做到连续与离散的统一。

线段树的根节点表示了所要处理的最大线段区间，而叶节点则表示了形如[a,a+1)的单位区间。对于每个非叶节点（包括根节点）所表示的区间[s,t)，令m = (s + t) / 2，则其左儿子节点表示区间[s,m)，右儿子节点表示区间[m,t)。这样建树的好处在于，对于每条要处理的线段，可以类似“二分”的进入线段树中处理，使得时间复杂度在O(logN)量级，这也是线段树之所以高效的原因。




参考：

[算法系列之二十三]线段树（Interval Tree）


[1]: https://cs-offer-1251736664.cos.ap-beijing.myqcloud.com/DataStructure_ST_1.jpg
 


