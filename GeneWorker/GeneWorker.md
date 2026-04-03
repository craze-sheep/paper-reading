

## 专业术语
meta-learning 元学习
surpervise监督学习
Transformer
generato 生成器
worker network
MDP


## 收获
1.参数固定，就好比我们的功能固定了，但是我们人在做一些工作时，调用的功能是不同的，比如看电视主要用视觉方面的理解，而不会用鼻子和嘴巴有关的神经功能
方法一：训练大量智能体：算力不够 任务分工不好明确
方法二：感觉像加了一个间接层，就是根据输入来派人干活（大卫：计算机科学中的所有问题都可以通过增加一个间接层来解决，当然，间接层太多的问题除外。）
2.核心思想：模拟人脑（这个确实好，我都思维固化了想当然,认为这些可以训练出来）
3.解决办法：增加间接层，在这里也算是一种分治思想吧（我的直观感受就是原来要训练100个参数的网络，现在变成训练2个网络：30(决策)+70(动作)，根据分治思想感觉后者处理起来是更加容易地）


## 个人idea
1.it is also difficult to unambiguously determine which network is suitable for processing the current input information
投票选举
2. 


## 疑问
1. training a set of networks is quite computationally inefficient
我对这个说法不是很理解，感觉这个不能成为比较的原因（我天，竟然有引用，那我得去看看这篇论文了），我的理解：虽然老师训练的是一个能干各种活大智能体，但是训练一系列小智能体——功能的总和等于大智能体，自我感觉分治处理不是更容易也更省资源吗？而且通过比较我们发现后者其实是少训练了各个模块之间的配合的参数，所以总体上来我感觉专业化分开训练是比整合训练更加容易的，而不是computationally inefficient(这算是我个人的直觉吧,就算是错的感觉也可以拿出来说说，还是等看了那个论文在说吧)