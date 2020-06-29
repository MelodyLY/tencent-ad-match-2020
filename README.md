# tencent-ad-match-2020
腾讯广告算法大赛2020参赛代码

运行环境：python3.5+, tensorflow2.0+

比赛链接：[https://algo.qq.com/index.html](https://algo.qq.com/index.html)

比赛说明：通过用户近90天广告点击信息预测用户性别和年龄，本质上可看作一个文本分类问题

最终成绩：1.418

备注：第一次参加文本分类相关的比赛，主要通过参与比赛对nlp相关知识有一定了解和实践，代码可供参考，还有待完善。

## 代码结构

- [data](./data)：用于存放数据
- [model](./model)：用于保存模型
- [result](./result)：用于输出提交结果
- 基于统计特征建模
  - [model_stat.ipynb](./model_stat.ipynb)：
- 基于文本特征建模
  - [user_seglist.ipynb](./user_seglist.ipynb)：基于文本特征建模的数据预处理部分，输出用户各个id的分词序列，格式为csv
  - [model_tfidf.ipynb](./model_tfidf.ipynb)：基于tf-idf进行建模
  - [model_w2v.ipynb](./model_w2v.ipynb)：基于word2vec进行建模，主要用于输出词向量
  - [model_nn_tf2.ipynb](./model_nn_tf2.ipynb)：基于深度学习模型进行建模，包含：dnn/textcnn/lstm/lstm+dnn/lstm+textcnn等模型，依赖[model_w2v.ipynb](./model_w2v.ipynb)训练出的词向量

## 数据说明

源数据由腾讯官方提供，备份数据以及word2vec训练结果可通过如下渠道获得，下载后解压至对应目录即可

[百度网盘资源链接-tecent_ad2020](https://pan.baidu.com/s/13Nu_pnza07U2gTejGDbY3Q)

**提取码：**scfi

## 参考资料

1. [赛题FAQ](https://docs.qq.com/doc/DSXJOZWNtaVRVR2t2)
2. [2020腾讯广告算法大赛：赛题理解与解题思路](https://zhuanlan.zhihu.com/p/141288029)
3. [2020腾讯广告算法大赛：如何突破分数瓶颈？](https://zhuanlan.zhihu.com/p/143185271)
4. [2020腾讯广告算法大赛：高分进阶](https://zhuanlan.zhihu.com/p/146419860)
5. [鹅厂大神上分思路，助你玩转初赛！](https://mp.weixin.qq.com/s?__biz=MzIzMzgzOTUxNA==&mid=2247484674&idx=2&sn=0f60b4e734f150d3141afd31270f745b&key=1ac6d7345b398eece99c91bc3acf5d7d713d8be5b55dd13559f7bbd221c21a74f2e26d1bec299f3564d132eda29eb250e08a6f74a38f6f5e99df7d7557ac625574ca993b3d3f7ca803375528f5ec2259&ascene=1&uin=Mjg0Mzg2ODg0MQ%3D%3D&devicetype=Windows+10+x64&version=62090523&lang=zh_CN&exportkey=AXaTAkr5LDHF9ejDGfGLIuc%3D&pass_ticket=%2FcjNDhEnlYRmSlfY1hZsRzD%2FiCV3T3qKDMTueuFbMFlx0oPPoZgEAcvM1d4NhcCA
   )
6. [初赛尾声将至，大神带你最后一搏！](https://mp.weixin.qq.com/s?__biz=MzIzMzgzOTUxNA==&mid=2247484720&idx=1&sn=e1e753b9a25671d6aa5247ee9cde6e8e&chksm=e8fecbc5df8942d315acfc726f7b2c06484a2507aa627e2e8bbefedb2b2d159ce1f0ef7037bb&mpshare=1&scene=1&srcid=&sharer_sharetime=1593413348200&sharer_shareid=20e95a37496b4afe75414f7e45d1d14a&key=9b180cabece10d14ded78dce7c0fa3f3b494f7cd14ace157102d35d43c6b7ac16cbb2411b67da5f14b77e59592df5f19e3c9c0d8b815b3aca6e29dedf961d49ba39eb571ddf3ee7d60458ddb00bedc0b&ascene=1&uin=Mjg0Mzg2ODg0MQ%3D%3D&devicetype=Windows+10+x64&version=62090523&lang=zh_CN&exportkey=AW%2BewCz13LPb4IQfLC%2FKrxs%3D&pass_ticket=%2FcjNDhEnlYRmSlfY1hZsRzD%2FiCV3T3qKDMTueuFbMFlx0oPPoZgEAcvM1d4NhcCA)
7. [零基础入门深度学习(5) - 循环神经网络](https://zybuluo.com/hanbingtao/note/541458?utm_source=wechat_session&utm_medium=social&utm_oi=696691015771230208)
8. [Example:text_classification_with_transformer](https://github.com/keras-team/keras-io/blob/master/examples/nlp/text_classification_with_transformer.py)

