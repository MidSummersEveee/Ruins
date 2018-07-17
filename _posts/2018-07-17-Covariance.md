---
layout: post
title: Numpy Skill Stack - Covariance 协变性小记
excerpt: "对协变性的概念，计算方法和含义的总结"
modified: 01/07/2018, 21:14:5
tags: [DataStructure]
comments: true
category: blog
---

## 1.Meet Covariance

什么是Covariance?
> Covariance即是Co-vary，change together，是对两个变量之间的线性关系的方向性的直观反映。

**Covariance 的意味着，当一个变量的值有变化时，另一个变量是否变动，covariance的符号代表了这两个变量协变的方向。**
如果符号为正，称二者间存在Positive Linear Relationship，反之为Negative。

例如，根据两组变量的数据，算得covariance为负数，则说明随着A变量的值增加，B变量的值反而减少。


实际的例子比如SP 500指数和道琼斯指数的关系，二者都是对美国股票市场的总体性分析，虽然细节算法不同，但可以相见两者一定成正向线性关系。根据数据最终算得二者的covariance为165.9，这证实了我们的判断。

## 2. Found the Wrong Man
上例中还有一事需要说明，即165.9这个数字，除了符号之外，没有其他含义，不能证明两者间线性关系的强度。
**covariance只体现是否有关系，以及关系的方向，关系的紧密性，Strength，则由correlation来体现。**

## 3. Get Covariance
两种covariance各有解方法：
<img src="https://MidSummerseveee.github.io/images/formula.png" width="380" height="100" />
