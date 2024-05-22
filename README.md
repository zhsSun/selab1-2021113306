# 软件工程实验一
## 要求一
编写一个Java程序，首先让用户选择或输入文本文件的位置和文件名,其中包含用英文书写的文本数据。要求如下：

    文本分为多行，你的程序应默认将换行/回车符当作空格
    文本中的任何标点符号，也应当作空格处理
    文本中的非字母(A-Z, a-z)字符应被忽略

程序读入文本数据，进行分析，将其转化为有向图：有向图的节点为文本中包含的某个单词，不区分大小写，两个节点A,B之间存在一条边A到B，意味着在文本中至少有一处位置A和B相邻出现（即A和B之间有且仅有1或多个空格），并且A到B的边权重是文本中A和B相邻出现的次数。

## 要求二
打印该图

## 要求三
在生成有向图之后，用户输入任意两个英文单词word1、word2，程序从图中查询它们的“桥接词”。word1、word2的桥接词word3：图中存在两条边word1到word3和word3到word2。要求如下：

    输入的word1或word2如果不在图中出现，则输出“No word1 or word2 in the graph!”
    如果不存在桥接词，则输出“No bridge words from word1 to word2!”
    如果存在一个或多个桥接词，则输出“The bridge words from word1 to word2 are: xxx, xxx, and xxx.”

## 要求四
用户输入一行新文本，程序根据之前输入文件生成的图，计算该新文本中两两相邻的单词的bridge word，将bridge word插入新文本的两个单词之间，输出到屏幕上展示。如果两个单词无bridge word，则保持不变，不插入任何单词：如果两个单词之间存在多个bridge words，则随机从中选择一个插入进去形成新文本。
例如：

    用户输入：Seek to explore new and exciting synergies
    输出结果：Seek to explore strange new life and exciting synergies

## 要求五
用户输入两个单词，程序计算它们之间在图中的最短路径（路径上所有边权值之和最小），以某种突出的方式将路径标注在原图并展示在屏幕上，同时展示路径的长度（所有边权值之和）。

## 要求六
随机游走。进入该功能时，程序随机的从图中选择一个节点，以此为起点沿出边进行随机遍历，记录经过的所有节点和边，直到出现第一条重复的边为止，或者进入的某个节点不存在出边为止。在遍历过程中，用户也可随时停止遍历。

##感谢wuooo同学和SunSeeker同学的研发贡献，加star

##在B1分支上进行修改，此段文字为测试内容