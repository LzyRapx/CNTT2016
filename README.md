# IOI2017 中国国家集训队第一次作业
**注意：本页有关作业和分数构成的内容禁止集训队员更改。**
## 分数构成
今年的国家队选拔分数构成和去年相同，具体如下：

1. 集中训练：4天，每天组织一次考试，按标准分计12.5分，共50分。（标准分指将第一名成绩记为满分，其余同学成绩与考试成绩成正比）
1. 作业：一次，10分。
1. 冬令营考试：一次，按标准分计40分。

以上一共100分。冬令营后所有选手按总分排序，前15名成为国家队候选队员。

冬令营后，所有队员集中训练的成绩和冬令营的成绩将带入后续的选拔中，冬令营后的分数构成为：

1. 集中训练：由之前集中训练的成绩按50:15的比例折算成15分。
1. 冬令营考试：由之前冬令营考试的成绩按40:10的比例折算成10分。（请注意折算比率不同）
1. 候选队员命题互测：每人一次共15次，占5分。（本部分的成绩取决于选手参与命题以及考试的积极性）
1. 作业：一次，10分。
1. 论文答辩：10分。
1. CTSC考试：两次，每次按标准分计25分，共50分。

以上一共100分。CTSC中根据以上总分排序，前6名进入口试答辩环节。最后从中选出4名国家队队员。

## 第一次作业
**截止日期：第一部分 11 月 10 日，第二部分冬令营前 10 天。**

此次作业总分10分，其中8分为完成分，2分为拓展分。其中按时完成所有作业将获得全部的8分完成分，没有按时或完成不足将扣分；至多扣除全部的8分，不会出现负分。拓展分将在完成作业的过程中体现，与完成分独立计算。

### 第一部分：题解撰写
截止日期：11月10日。未能按时完成或纰漏过多的酌情扣除完成分，扣分上限为全部8分完成分。

作业内容为：每人负责一场 Topcoder SRM（Single Round Match） div1 中的三道题目，为题目撰写中文解题报告和参考程序，并放在这个工程中分享给大家。

每道题目的题解和程序需要放在`TC-SRM-编号-div1-分数`文件夹中。解题报告需要按照[样例](/TC-SRM-000-div1-1000/solution.md)中的要求书写，参考程序要求包含注释。在书写过程中，不限制参考官方题解和其他人的代码。所有的程序（包括泛做的程序）用`ID.cpp/java/py`或以ID命名的文件夹放在对应题目的文件夹中（如果有多个文件，例如一些笔记），其中请在[ID List](/id_list.md)中填写你的常用ID，并保持和每个文件夹中的ID一致。

在截止日期之后，所有队员可以帮助完善其他队员的题解，可以做的工作包括但不限于增加新方法、完善过程、疏通语句、修改错别字等。参与工作的同学可以酌情获得拓展分。除非纰漏过多或明显故意留给他人刷分，被完善题解的队员不扣分。

**注意：在截止日期前请不要修改他人的题解，禁止恶意修改他人的题解。**

具体如何使用这个工程可以在[后文中](#如何使用这个工程)找到。

每个人负责的比赛如下，其中548表示负责SRM548 div1中的三道题目（注意不是div2）。

|姓名|题目|姓名|题目|姓名|题目|姓名|题目
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|陈俊锟|548|刘子祯|572|孙耀峰|571|徐泽涛|576|
|陈通|556|陆宇暄|565|孙奕灿|584|闫书弈|579|
|承君阳|586|罗煜楚|583|汪乐平|562|杨家齐|580|
|丁力煌|566|罗哲正|551|王聿中|564|杨景钦|591|
|冯哲|555|吕欣|570|王子健|552|叶昊星|560|
|高杰|563|马龙|596|翁文涛|575|叶珈宁|578|
|高睿泉|550|毛啸|559|翁伊嘉|599|叶芃|585|
|辜俊儒|549|闵梓轩|577|谢兴宇|569|尤艺霖|589|
|何中天|592|穆皓远|568|邢健开|587|袁伟强|597|
|洪华敦|588|聂恺辰|581|熊云帆|590|袁宇韬|593|
|黄励新|573|欧阳思琦|574|徐海珂|598|赵晟宇|557|
|寇煜杭|594|权大磊|582|徐明宽|567|钟知闲|561|
|梁浩|595|沈睿|553|徐懿|554|周子鑫|558|

### 第二部分：试题泛做
截止日期：冬令营前10天。截止日期后的提交均不作数。截止时每有一道题目没有完成扣除完成分0.1分，直至8分全部扣完。

所有的队员需要完成全部的156道题目，并将代码（包含注释）放在每道题目的文件夹中，用前文提到的方式命名。过程中允许参考他人的工作，但不能照抄。

## 如何使用这个工程
这是一个gitbook工程，gitbook是使用markdown语法写书的工具。这个工程使用git做版本管理工具，大家对这个工程所做的所有改动将被可持久化地记录下来。这个工程托管在github上，github是一个管理、分享代码的~~同性交友~~网站，也即是大家的数据存储在这个网站上。

为了在这个工程中工作，你至少需要学会使用markdown的语法，并在[github.com](https://github.com/)和[gitbook.com](https://www.gitbook.com)网站上各注册一个账号，并把账号告诉陈许旻。此外，如果学习了git、node.js、gitbook等相关知识可能有助于你更方便地用得更顺手，但这些并不是必须的。

注意：这个工程本身跟Topcoder没有关系。如果你还不会使用Topcoder，你需要学习如何使用Topcoder做以往的题目。（在TC上做以往的题不需要参加任何一场比赛）

我们主要有两种方式编辑这个工程：

### 在线编辑
你可以在gitbook.com网站上编辑。当你成为这个工程的成员之后，你就可以在线进行编辑（这个比较好玩的是还可以多个人同时编辑同一个文档）。这是最简单的方式。

### 本地编辑
你可以使用git将[`https://github.com/Mulab11/cntt2016-hw1`](https://github.com/Mulab11/cntt2016-hw1)这个工程克隆（`git clone`）到本地，修改完成后推送（`git push`）回工程中。

为了用git维护和提交，你至少需要学会clone、add、commit、pull、push几种操作。

在本地，你可以直接把markdown当文本处理，也就是说可以用记事本等基本工具进行编辑。可以使用markdown的小工具预览或编辑（例如Windows、Mac下可以用Typora，注意不同工具的显示可能略有不同）。

此外，在本地你还可以把这这个项目部署成一个网站或是输出成一个PDF。具体需要先安装node.js、npm、gitbook，然后用`gitbook serve`就能部署。

注意gitbook这个工具和gitbook这个网站并不是相等的，前者是一套基于node.js的写书工具，后者是托管和展示由gitbook写成的书的网站。
