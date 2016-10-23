# DrawingPointsDivOne

作者：叶昊星

## 关键词

前缀和，最大范围的预测与证明，二分法

## 题目描述

定义一次操作为将平面上所有由存在的点为顶点组成的$$1*1$$的正方形的中心点标出，并将原来的点抹去。

现在给你一个经过$$k$$次操作后平面上所有$$n$$个点的坐标，问$$k$$的最大值，输出这个最大值或无界输出$$-1$$。

## 数据范围

$$n<=50, |x_{i}|,|y_{i}|\leq 70, |x_{i}|,|y_{i}|\leq 70$$

## 定义

定义逆操作为将所有存在的点标记以当前点为中心的$$1*1$$的正方形的$$4$$个顶点，并擦去原来的点。（注意一个操作不一定对应一个逆操作。）

定义$$k*k$$指定矩阵为一个范围为$$k*k$$同时包含一些点的矩阵。若$$k$$为奇数，则点阵中的点集为范围内所有横纵坐标均不为整数的点的集合。若$$k$$为偶数，则点阵中的点集为范围内所有横纵坐标均为整数的点的集合。特别的，当$$k=0$$时指定矩阵为一个点。易知指定矩阵为$$k*k$$范围中点数最多的矩阵。且对于一个点，$$k$$次操作后该点l可扩展出$$k*k$$指定矩阵。

定义左边界为一个点集最左边的点的$$x$$坐标，右边界为最右边的点的$$x$$坐标，最大差值为右边界减去左边界。

定义行$$k$$为点集中满足$$y$$坐标为$$k$$的点组成的点集。

定义连续为在一行上相邻两个点的距离不超过$$1$$。

定义点集的相邻为两个没有相同点的点集，存在一种方法，使得在两个点集中各取一个点，其曼哈顿距离为$$1$$。

## 引理

### (1) 对于点集$$S$$和$$S$$做$$1$$次逆操作后再做$$1$$次操作后产生的点集$$S’$$,$$S\subseteq S'$$。

证明：如果一个点$$\in S$$且$$\notin S'$$，说明在$$1$$次逆操作之后该点为中心的$$1*1$$正方形的$$4$$个顶点不全有点，与定义矛盾。

### (2) 如果每一行所有的点都是连续的且每一列所有的点都是连续的（设此条件为$$cond$$），则进行$$k$$次逆操作再进行$$k$$次操作后点集不变。

证明：易知若一个点集满足$$cond$$，那么此点集经上述变换后的点集亦满足$$cond$$。

设行$$a$$的最大差值为$$s$$，原点集为$$S$$，变换后的点集为$$S'$$

显然行$$a-1$$和行$$a+1$$的左边界不可能同时比行$$a$$的左边界小，右边界不可能同时更大，否则与定义矛盾。

那么经过一次逆操作后行$$a-0.5$$和行$$a+0.5$$的左边界最大值不小于行$$a$$的左边界，右边界的最小值不大于行$$a$$的右边界。

所以行$$a+0.5$$与行$$a-0.5$$的最大差值不超过$$s+1$$，从而再经过一次操作后新的行$$a$$的最大差值不超过$$s$$。

由操作前每行点是连续的得到$$S'\subseteq S$$，根据引理(1)得到$$S\subseteq S'$$，所以$$S=S'$$

由等号的传递性易推广到$$k$$次逆操作及$$k$$次操作的情况。

### (3) 如果点阵不满足$$cond$$，则在原点集中存在两个点扩展出的两个$$k*k$$的指定矩阵不相交或相邻。

证明：设该点阵行$$a$$不连续（列不连续同理），则该行可以被分成几个极长连续段。

取其中两段，易知这两段x属于不同的两个$$k*k$$指定矩阵，且任意一段的左右边界为所对应的指定矩阵的左右边界。所以两段是否相交或相邻与两个对应的指定矩阵是否相交或相邻等价。

### (4) 当$$k\geq 139$$时，点阵一定满足$$cond$$。

证明：根据定义，一个点可扩展出$$k*k$$的指定矩阵，由引理(3)得必有两个点扩展出的$$k*k$$点阵不相交或相邻。

设这两个点阵的中心点为$$(x1,y1),(x2,y2)$$，则$$x2-x1\geq k+2$$或$$y2-y1\geq k+2$$，由数据范围得到矛盾。

## 解法1

由于点的坐标范围较小，我们猜测所有$$k$$有界情况时$$k$$的最大值不会很大。

大胆猜测这个值不会超过138，即不存在一种情况使得$$k=a>138$$时满足要求且$$k>a$$时不满足要求。

由引理2和4可得出上述结论。所以我们只需将k从1到138依次判断，如果均合法则无界。此处可用二分优化。

事实上，在$$k*k$$的范围内指定点阵为点数最多的点阵。所以判断一个点是否在k此操作后存在等价于判断该点为中心的$$k*k$$的范围内是否有$$(k+1)*(k+1)$$个点。这个可以用二维前缀和解决

于是，每一次判定为将每一个点扩展出一个指定点阵，做一遍二维前缀和，再对$$[-70,70] [-70,70]$$的范围的整点依次判断该点周围是否有$$k*k$$的指定点阵。

这就做完了本题。

### 时空复杂度

$$O(x_{max}^{2} * log k_{max}) = O(x_{max}^{2} * log x_{max})-O(x_{max}^{2})$$

（注：参考程序给出的是未加二分的版本，事实上不加二分复杂度为$$O(x_{max}^{3})$$，也可以通过测试数据。）