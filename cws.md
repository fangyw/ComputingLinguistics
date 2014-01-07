Chinese Word Segmentation
========

英语中也存在分词，通常叫做tokenization，主要是对一些标点做一些处理。

词是由语素构成的、能够独立运用的最小的语言单位。

##基本方法

* 基于词表的方法
  - 最大匹配法
  - 全切分+路径选择
* 字序列标记方法

##自动切分的评价

准确率P=切分结果中正确分词数/切分结果中所有分词数  
召回率R=切分结果中正确分词数/标准答案中所有分词数  
F-measure=2PR/(P+R)

##关键问题

* 歧义（交集型、组合型、混合型）
* 未登录词识别

##TODO
基于ME、CRF、MM、WFST 分词方法的实现
