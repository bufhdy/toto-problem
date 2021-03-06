# CCF NOIP 2014 Day 1

## 1. 生活大爆炸版石头剪刀布 rps

**问题描述**

石头剪刀布是常见的猜拳游戏：石头胜剪刀，剪刀胜布，布胜石头。如果两个人出拳一样，则不分胜负。在《生活大爆炸》第二季第 8 集中出现了一种石头剪刀布的升级版游戏。升级版游戏在传统的石头剪刀布游戏的基础上，增加了两个新手势：

斯波克：《星际迷航》主角之一。

蜥蜴人：《星际迷航》中的反面角色。

这五种手势的胜负关系如表一所示，表中列出的是甲对乙的游戏结果。

**表一 石头剪刀布升级版胜负关系**

<table>
<tr>
<th>甲对乙</th>
<th>剪刀</th>
<th>石头</th>
<th>布</th>
<th>蜥蜴人</th>
<th>斯波克</th>
</tr>
<tr>
<td>剪刀</td>
<td>平</td>
<td>输</td>
<td>赢</td>
<td>赢</td>
<td>输</td>
</tr>
<tr>
<td>石头</td>
<td>＼</td>
<td>平</td>
<td>输</td>
<td>赢</td>
<td>输</td>
</tr>
<tr>
<td>布</td>
<td>＼</td>
<td>＼</td>
<td>平</td>
<td>输</td>
<td>赢</td>
</tr>
<tr>
<td>蜥蜴人</td>
<td>＼</td>
<td>＼</td>
<td>＼</td>
<td>平</td>
<td>赢</td>
</tr>
<tr>
<td>斯波克</td>
<td>＼</td>
<td>＼</td>
<td>＼</td>
<td>＼</td>
<td>平</td>
</tr>
</table>

现在，小 A 和小 B 尝试玩这种升级版的猜拳游戏。已知他们的出拳都是有周期性规律的，但周期长度不一定相等。例如：如果小 A 以「石头－布－石头－剪刀－蜥蜴人－斯波克」长度为 6 的周期出拳，那么他的出拳序列就是「石头－布－石头－剪刀－蜥蜴人－斯波克－石头－布－石头－剪刀－蜥蜴人－斯波克－……」，而如果小 B 以「剪刀－石头－布－斯波克－蜥蜴人」长度为 5 的周期出拳，那么他出拳的序列就是「剪刀－石头－布－斯波克－蜥蜴人－剪刀－石头－布－斯波克－蜥蜴人－……」。

已知小 A 和小 B 一共进行 N 次猜拳。每一次赢的人得 1 分，输的得 0 分；平局两人都得 0 分。现请你统计 N 次猜拳结束之后两人的得分。

**输入**

第一行包含三个整数：N，NA，NB，分别表示共进行 N 次猜拳、小 A 出拳的周期长度，小 B 出拳的周期长度。数与数之间以一个空格分隔。

第二行包含 NA 个整数，表示小 A 出拳的规律，第三行包含 NB 个整数，表示小 B 出拳的规律。其中，0 表示「剪刀」，1 表示「石头」，2 表示「布」，3 表示「蜥蜴人」，4 表示「斯波克」。数与数之间以一个空格分隔。

**输出**

输出一行，包含两个整数，以一个空格分隔，分别表示小 A、小 B 的得分。

<table>
<tr>
<th>输入样例 1</th>
<th>输出样例 1</th>	
</tr>
<tr>
<td valign="top">
10 5 6<br />
0 1 2 3 4<br />
0 3 4 2 1 0<br />
</td>
<td valign="top">6 2</td>
</tr>
</table>

<table>
<tr>
<th>输入样例 2</th>
<th>输出样例 2</th>	
</tr>
<tr>
<td valign="top">
9 5 5<br />
0 1 2 3 4<br />
1 0 3 2 4<br />
</td>
<td valign="top">4 4</td>
</tr>
</table>

**数据规模与约定**

对于 100% 的数据，0 < N ≤ 200，0 < NA ≤ 200，0 < NB ≤ 200。

<br />

## 2. 联合权值 link

**问题描述**

无向连通图 G 有 n 个点，n - 1 条边。点从 1 到 n 依次编号，编号为 i 的点的权值为 W<sub>i</sub>，每条边的长度均为 1。图上两点 (u, v) 的距离定义为 u 点到 v 点的最短距离。对于图 G 上的点对(u, v)，若它们的距离为 2，则它们之间会产生 W<sub>u</sub> × W<sub>v</sub> 的联合权值。

请问图 G 上所有可产生联合权值的有序点对中，联合权值最大的是多少？所有联合权值之和是多少？

**输入**

接下来 n - 1 行，每行包含 2 个用空格隔开的正整数 u、v，表示编号为 u 和编号为 v 的点之间有边相连。

最后 1 行，包含 n 个正整数，每两个正整数之间用一个空格隔开，其中第 i 个整数表示图 G 上编号为 i 的点的权值为 W<sub>i</sub>。

**输出**

输出共 1 行，包含 2 个整数，之间用一个空格隔开，依次为图 G 上联合权值的最大值和所有联合权值之和。**由于所有联合权值之和可能很大，输出它时要对10007取余。**

<table>
<tr>
<th>输入样例</th>
<th>输出样例</th>	
</tr>
<tr>
<td valign="top">
5<br />
1 2<br />
2 3<br />
3 4<br />
4 5<br />
1 5 2 3 10<br />
</td>
<td valign="top">20 74</td>
</tr>
</table>

**样例说明**

本例输入的图如上所示，距离为 2 的有序点对有 (1,3)、(2,4)、(3,1)、(3,5)、(4,2)、(5,3)。其联合权值分别为 2、15、2、20、15、20。其中最大的是 20，总和为 74。

**数据规模与约定**

对于 30% 的数据，1 < n ≤ 100；

对于 60% 的数据，1 < n ≤ 2000；

对于 100% 的数据，1 < n < 200,000，0 < W<sub>i</sub> ≤ 10,000。

<br />

## 3. 飞扬的小鸟 bird

**问题描述**

Flappy Bird 是一款风靡一时的休闲手机游戏。玩家需要不断控制点击手机屏幕的频率来调节小鸟的飞行高度，让小鸟顺利通过画面右方的管道缝隙。如果小鸟一不小心撞到了水管或者掉在地上的话，便宣告失败。

为了简化问题，我们对游戏规则进行了简化和改编：

1. 游戏界面是一个长为 n，高为 m 的二维平面，其中有 k 个管道（忽略管道的宽度）。

2. 小鸟始终在游戏界面内移动。小鸟从游戏界面最左边任意整数高度位置出发，到达游戏界面最右边时，游戏完成。

3. 小鸟每个单位时间沿横坐标方向右移的距离为 1，竖直移动的距离由玩家控制。如果点击屏幕，小鸟就会上升一定高度 X，每个单位时间可以点击多次，效果叠加；如果不点击屏幕，小鸟就会下降一定高度 Y。小鸟位于横坐标方向不同位置时，上升的高度X和下降的高度 Y可能互不相同。

4. 小鸟高度等于 0 或者小鸟碰到管道时，游戏失败。小鸟高度为 m 时，无法再上升。

现在，请你判断是否可以完成游戏。如果可以，输出最少点击屏幕数；否则，输出小鸟最多可以通过多少个管道缝隙。

**输入**

第 1 行有 3 个整数 n，m，k，分别表示游戏界面的长度，高度和水管的数量，每两个整数之间用一个空格隔开；

接下来的 n 行，每行 2 个用一个空格隔开的整数 X 和 Y，依次表示在横坐标位置 0－n - 1 上玩家点击屏幕后，小鸟在下一位置上升的高度 X，以及在这个位置上玩家不点击屏幕时，小鸟在下一位置下降的高度 Y。

接下来 k 行，每行 3 个整数 P，L，H，每两个整数之间用一个空格隔开。每行表示一个管道，其中 P表示管道的横坐标，L 表示此管道缝隙的下边沿高度为 L，H 表示管道缝隙上边沿的高度（输入数据保证 P 各不相同，但不保证按照大小顺序给出）。

**输出**

共两行。

第一行，包含一个整数，如果可以成功完成游戏，则输出 1，否则输出 0。

第二行，包含一个整数，如果第一行为 1，则输出成功完成游戏需要最少点击屏幕数，否则，输出小鸟最多可以通过多少个管道缝隙。

<table>
<tr>
<th>输入样例 1</th>
<th>输出样例 1</th>	
</tr>
<tr>
<td valign="top">
3 9<br />
9 9<br />
1 2<br />
1 3<br />
1 2<br />
1 1<br />
2 1<br />
2 1<br />
1 6<br />
2 2<br />
1 2 7<br />
5 1 5<br />
6 3 5<br />
7 5 8<br />
8 7 9<br />
9 1 3<br />
</td>
<td valign="top">
1<br />
6<br />
</td>
</tr>
</table>

<table>
<tr>
<th>输入样例 2</th>
<th>输出样例 2</th>	
</tr>
<tr>
<td valign="top">
10 10 4<br />
1 2<br />
3 1<br />
2 2<br />
1 8<br />
1 8<br />
3 2<br />
2 1<br />
2 1<br />
2 2<br />
1 2<br />
1 0 2<br />
6 7 9<br />
9 1 4<br />
3 8 10<br />
</td>
<td valign="top">
0<br />
3<br />
</td>
</tr>
</table>

**样例说明**

如下图所示，蓝色直线表示小鸟的飞行轨迹，红色直线表示管道。

**数据规模与约定**

对于 30% 的数据：5 ≤ n ≤ 10，5 ≤ m ≤ 10，k = 0，保证存在一组最优解使得同一单位时间最多
点击屏幕 3 次；

对于 50% 的数据：5 ≤ n ≤ 20，5 ≤ m ≤ 10，保证存在一组最优解使得同一单位时间最多点击屏
幕 3 次；

对于 70% 的数据：5 ≤ n ≤ 1000，5 ≤ m ≤ 100；

对于 100% 的数据：5 ≤ n ≤ 10000，5 ≤ m ≤ 1000，0 ≤ k < n，0 < X < m，0 < Y < m，0 < P < n，0 ≤ L < H ≤ m，L + 1 < H。

