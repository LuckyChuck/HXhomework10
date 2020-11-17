# Thinking1	GCN/Graph Embedding 都有哪些应用场景 #
答：比如大规模交通路网速度预测，社交网络分析，生物网络，金融风控，商品推荐，聊天机器人中的语义分析及意图识别
# Thinking2	在交通流量预测中，如何使用Graph Embedding，请说明简要的思路 #
答:在构建图时，可以以每个路口或者地点作为顶点，车站之间联系作为边，以及t时刻各地点的交通客流量的矩阵。可以求出地点的相邻地点的邻接矩阵，以及度矩阵。然后根据3个矩阵进行神经网络搭建运算。  
文中的图卷积公式比较复杂，还没有看的很懂。不过大体思路还是了解的。应该是将原来的单一的特征矩阵化为2个矩阵了。没有经过实践，还不知道可行性。不过根据文中可得图卷积得效果比其他得效果要好。图卷积在挖掘特征关系方面具有独特得优势。还是要再接再厉得学习啊。



文章信息
https://blog.csdn.net/qq_33431368/article/details/98408489

《Predicting Station-Level Short-Term Passenger Flow in a Citywide Metro Network Using Spatiotemporal Graph Convolutional Neural Networks》。

2019年中国海洋大学的几位老师发在IISPRS International Journal of Geo-Information上的一篇文章（地学4区，IF:1.84）。
# Thinking3	在文本分类中，如何使用Graph Embedding，请说明简要的思路 #
答:可以将每个单词作为顶点，单词之间的先后联系作为边，去构建图。然后可以借鉴Deepwalk的思想，采用随机游走的方式随机选择起始点，设定游走次数和深度，从其邻居中随机采样节点作为下一个访问节点，重复此过程，产生词序。然后将将这些词序列作为训练样本输入word2vec，进行分类任务。
