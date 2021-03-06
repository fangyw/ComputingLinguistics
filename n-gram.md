Language Modeling
-----------------

历史信息越多（阶的大小），选择限制越强，模型越准确。

由于训练样本不足而导致所估计的分布不可靠的问题，称为数据稀疏问题。

##Zipf law
---
Zipf law 描述了词频以及词在词频表中位置的关系。  
语言中只有很少的常用词，大部分都是低频词（不常用的词）。  
对于语言中的大多数词，他们在语料库中的出现是稀疏的。

由于数据稀疏的存在，MLE不是一种很好的参数估计方法。解决方法，采用平滑技术，把在训练样本中出现过的事件适当较小，把减小得到的概率密度分配给训练语料中没有出现的事件。

##平滑技术
---
Add-one、留存、Good-Turing、Jelinek-Mercer平滑、Katz平滑

Add-one的缺点：未出现n元数组数量太多。平滑后，所有未出现的n元组占据了整个分布的很大比例。
也就是说，Add-one给训练语言中没有出现的语料分配了太多的概率空间。

思考：认为所有未出现的n元组概率相等，出现的n元组增加同样的频度值，是否合理？

双向交叉验证也称作删除估计

Good-Turing平滑的思想：利用高频率的n元组调整低频的n元组的概率。

Back-off model的基本思想：在高阶模型可靠时，尽量使用高阶模型；必要时，使用低阶模型。


