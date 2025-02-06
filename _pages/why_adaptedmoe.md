---
layout: archive
title: "要解决的问题：训练集测试集数据不一致"
permalink: /why_adaptedmoe/
author_profile: true
redirect_from:
  - /resume
---

### AOI设备交付的过程中，经常会遇到训练集和测试集数据不一致的问题  
### 比如训练过程中只能收集到ABC三种布料，而测试时出现了DE两种布料，这种情况下模型的性能往往会大幅下降。
### 针对这类问题，我们提出了一种基于混合专家模型外加测试时自适应的方法，在不增加额外计算量的情况下，显著提升了模型性能
{% include base_path %}
<center>
  <img src="\images\/adaptedmoe\/issue_define.png">
</center> 










