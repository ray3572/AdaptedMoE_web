---
layout: archive
title: "整体方案示意图"
permalink: /how_adaptedmoe/
author_profile: true
redirect_from:
  - /resume
---
{% include base_path %}
# 数据集
## 数据集以轻微缺陷为主，包括布料、晶圆、金属板三大类39种具备重复性纹理的材料。训练集与测试集分离，测试集的光学方案、材料规格与训练集完全不同。
<center>
  <img src="\images\adaptedmoe\dataset.png">
</center> 


<center>
  <img src="\images\adaptedmoe\overview.png">
</center> 

# 整体方案
## 通过一个路由网络将测试数据路由至合适的专家网络，并通过测试时适配（TTA）将现有数据的表征分布与专家模型进行同步，最后通过专家网络进行异常检测。

<center>
  <img src="\images\adaptedmoe\MoE.png">
</center> 

# 路由网络的优势：
# 采用centerloss使得相同类型布料的表征相互聚集。专家模型可以用更小参数量习得分割超平面
# 将表征映射至超球面，通过限制表征分布空间使得不同类型的布料表征在特征空间分布更均匀，路由更准确

# 混合专家模型的优势：
## 将质检问题分治，减轻了不同类型布料之间的缺陷定义冲突带来的精度损失。
## 能够简化模型，在初始化之后只需要加载部分参数即可实现全部功能。
<center>
  <img src="\images\adaptedmoe\TTA.png">
</center> 

# TTA的优势：
## TTA模块能够对齐训练集与测试集表征分布上的差异，减少因光学方案、纹理差异等因素带来的精度损失。
## 线下训练数据与线上实测数据之间差异越大，该模块性能提升越明显。







