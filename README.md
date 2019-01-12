# 面向交通数据的张量计算技术

  - 作者：何兆成（中山大学）
  
  > 评述：我们的手册实际上是要提出一种面向交通数据分析与计算的范式，架构包括数据组织-特征计算-分析应用三个层次。第一部分数据组织讲清楚交通数据的多维性、随机性、稀疏性、物理性的特点，通过数据例子呈现这些特性，引出张量结构的优势以及要解决的问题；第二部分是特征计算，这一部分要承前启后，引入满足交通数据特性下的特征计算的各类方法；第三部分是应用分析，给出交通数据分析应用的标准问题：修复问题、聚类问题、预测问题（以后结合图谱还有推理问题），这部分结合案例进行介绍。(何兆成，2018.12.14)
  
## 第一章  总论（Introduction）

第一节  交通数据特性

【主要介绍交通数据本身具有高维度、随机性、稀疏性以及检测器带来的不完备性，通过列举实例生动展现这些特性】

第二节  张量简介

【主要介绍张量的定义及其数据表达的优势，简单引入张量分解的一些思想】

第三节  张量与交通数据

【主要介绍用张量组织交通数据后具有的优势，一是结构优势—交通数据本身的多维性；二是模型优势-如隐特征发现、可以处理多种数据类型等】
【简单介绍目前张量在交通数据分析方面的研究进展，后面章节详细讲解】

第四节  本书的组织结构

【第一章、第二章、第三章为张量计算基础；第四章为特征计算方法；第五章、第六章为交通应用分析】

第五节  本章参考文献

- Zheyi Pan, Yuxuan Liang, Junbo Zhang, Xiuwen Yi, Yong Yu, Yu Zheng, 2018. [*HyperST-Net: hypernetworks for spatio-temporal forecasting*](https://arxiv.org/pdf/1809.10889.pdf). arXiv.

  - Truc Viet Le, Richard Oentaryo, Siyuan Liu, Hoong Chuin Lau, 2017. [*Local Gaussian processes for efficient fine-grained traffic speed prediction*](https://arxiv.org/pdf/1708.08079.pdf). arXiv.

  - Yaguang Li, Cyrus Shahabi, 2018. [*A brief overview of machine learning methods for short-term traffic forecasting and future directions*](https://doi.org/10.1145/3231541.3231544). ACM SIGSPATIAL, 10(1): 3-9.

  - Bing Yu, Haoteng Yin, Zhanxing Zhu, 2017. [*Spatio-temporal graph convolutional networks: a deep learning framework for traffic forecasting*](https://arxiv.org/pdf/1709.04875.pdf). arXiv. ([appear in IJCAI 2018](https://www.ijcai.org/proceedings/2018/0505.pdf))

  - Feras A. Saad, Vikash K. Mansinghka, 2018. [*Temporally-reweighted Chinese Restaurant Process mixtures for clustering, imputing, and forecasting multivariate time series*](http://proceedings.mlr.press/v84/saad18a/saad18a.pdf). Proceedings of the 21st International Conference on Artificial Intelligence and Statistics (*AISTATS 2018*), Lanzarote, Spain. PMLR: Volume 84.

  - Zhengping Che, Sanjay Purushotham, Kyunghyun Cho, David Sontag, Yan Liu, 2018. [*Recurrent neural networks for multivariate time series with missing values*](https://doi.org/10.1038/s41598-018-24271-9). Scientific Reports, 8(6085).

## 第二章  张量计算的数学基础

第一节  张量的代数结构

【主要介绍张量与矩阵、向量的不同符号表示；介绍张量的纤、切片（通过三阶张量例子说明，有水平切片、前切片和侧切片）】

第二节  范数

【从矩阵的Frobenius范数和迹范数引入张量的范数和迹范数（范数的主要作用是度量元素间的距离，范数实际上是一个映射】

第三节  内积与外积

【主要介绍张量内积公式以及其与范数的关系；向量的外积与秩一张量】

第四节  矩阵的Kronecker积、Khatri-Rao积和Hadamard积

【主要介绍三种矩阵积的运算公式以及关于三种矩阵积常用的一些变换公式】

第五节  张量与矩阵的n-模积

【关于张量与矩阵的一种特殊乘积运算，其结果仍是一个张量】

第六节  张量的矩阵化和向量化

【通过实例展现向量化运算以及不同维度的矩阵化运算】

第七节  本章参考文献

## 第三章  统计学习基础

第一节  最大似然估计

第二节  最大后验估计

第三节  共轭分布

第四节  随机过程

  - 介绍高斯过程、中餐馆过程等。

第五节  MCMC算法

第六节  变分推断

第七节  案例：贝叶斯线性回归

第八节  本章参考文献

## 第四章  矩阵分解

第一节  特征值分解

第二节  奇异值分解

第三节  UV分解

第四节  概率矩阵分解

第五节  贝叶斯矩阵分解

第六节  本章参考文献

## 第五章  主成分分析与压缩感知

第一节  主成分分析

第二节  概率主成分分析

第三节  贝叶斯主成分分析

第四节  压缩感知

第五节  低秩矩阵复原

第六节  本章参考文献

## 第六章  张量分解

第一节  Tucker分解

第二节  CP分解

第三节  本章参考文献

## 第七章  低秩张量复原

第一节  核范数最小化

第二节  增强拉格朗日算子

第三节  本章参考文献

## 第八章  贝叶斯张量分解

第一节  高斯张量分解

第二节  贝叶斯高斯张量分解

第三节  泊松张量分解

第四节  贝叶斯时序张量分解

第五节  本章参考文献

## 第九章  深度张量分解

第一节  贝叶斯神经网络

  - 基本的神经网络

    - 介绍标准的神经网络，并指出现有模型的弊端。

  - 用贝叶斯推断求解神经网络

    - 主要介绍变分推断在神经网络中的应用。

第二节  案例：非线性回归

  - 具体介绍如何实现贝叶斯神经网络。

第三节  将逼近问题转换为回归问题

  - 讨论现有的深度张量分解模型，论述交替条件更新的可行性，探究贝叶斯深度张量分解模型的结构。
  
第四节  本章参考文献

## 第十章  张量与交通数据修复

第一节  缺失交通数据修复

  - 城市路网车速数据集

  - 矩阵计算技术

  - 张量计算技术

第二节  交通模式挖掘

  - 隐性特征发现

  - 显性特征提取
  
第三节  本章参考文献

## 第十一章  张量分解与交通预测

第一节  以相似性为基础的交通预测模型

第二节  以时序特征为基础的交通预测模型

第三节  案例：个体出行预测

  - 协同群体的出行模式

  - 个体出行重构
  
第四节  本章参考文献
