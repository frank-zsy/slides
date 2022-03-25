---
layout: cover
theme: default
background: ../assets/numbers-in-open-source/cover_bg.jpg
class: 'text-center'
---

# 数解开源

## 开源数据分析之旅

<br>
<br>
<br>
<br>

#### 赵生宇 @ 2022.3.26

---

# 关于我

### 赵生宇 Frank

<br>

- 2015 @ 微软：社区经理实习
- 2016 - 2018 @ 网易，游戏服务端研发
- 2018 - 2019 @ 阿里巴巴，开源办公室

<br>

- 2019 - 至今 @ 同济大学 & X-lab，计算机博士在读

<br>

- 2020.1 Wuhan2020
- 2020 InfoQ 中国十大开源杰出贡献人物
- 2020 SegmentFault 中国开源先锋 33 人
- 2020 开源社 开源之星

<div class="abs-tr mx-25 my-20 flex">
  <img src="/assets/ossummit19.jpg" class="h-80">
</div>

---

# 开源中的数据

- GitHub
  - 数千万仓库与开发者
  - 超 30 亿条开发者行为日志数据
    - 超 200 万条每天的增长速度
  - 开发者社交数据
- 开源组件制品库
  - Maven、npm、PyPI、Composer、Crates...
  - Docker、Helm
- StackOverflow
  - 数百万开发者技术问答内容

<div class="abs-tr mx-30 my-10 flex">
  <img src="/assets/github_data_size.png" class="h-50">
</div>

<div class="abs-tr mx-10 my-70 flex">
  <img src="/assets/data_status.png" class="h-55">
</div>

---

# 开源中的数据

<div class="abs-tl mx-15 my-10 flex">
  <img src="/assets/data_in_opensource.png" class="h-120">
</div>

---

# 在阿里的日子

### Open Source Summit 2019

<br>

- 开发者活跃度
  - 根据开发者的协作行为加权获得 —— 不同类型的活动具有相应的活跃权重
- 项目活跃度
  - 根据项目上的开发者活跃度加权获得 —— 开方使贡献人数作为因素掺入
- 项目协作关联度
  - 根据项目间的开发者活跃度调和平均获得 —— 同时在不同项目上活跃的开发者关联了这些项目

<div>
  <div class="abs-bl mx-10 my-10 flex">
    <img src="/assets/activity_table.png" class="h-35">
  </div>
  <div class="abs-br mx-10 my-10 flex">
    <img src="/assets/activity_example.png" class="h-35">
  </div>
</div>

---

# 统计度量的问题

<div grid="~ cols-2 gap-4">

<div>

- 统计度量很难横向比较，即 baseline 在哪里？
- 统计度量很多都是私有数据，无法全域规模化统计
- 无法规模化使用的度量很难达成共识

<br>

#### 度量三定律 - 观察者效应（Observer Effect）

- Goodhart's Law - 一个指标一旦变成既定目标，那么它就不再具有指示整体情况的作用
- Compell's Law - 当量化度量有重要后果后，会产生一些通过破坏过程以实现量化目标的行为，会完全违背监控完善过程的初衷
- Hawthorne Effect - 意识到自己正在被别人关注的个人会改变自己的行为，由于受到额外的关注可以导致绩效和工作态度的改善

</div>

<div class="text-center">
  <div class="abs-tr mx-15 my-40 flex">
    <img src="/assets/chaoss.png" class="h-80">
  </div>

  CHAOSS
</div>

</div>

---

# 价值网络——真实的世界

<div grid="~ cols-2 gap-4">

<div>
  <div class="abs-tl mx-10 my-30 flex">
    <img src="/assets/openrank_repo_actor.png" class="h-80">
  </div>
</div>

<div>

#### 网络为什么有意义

- 有多少活跃度重要，但是谁在活跃更重要
- 开发者之间的社交关系蕴含着丰富的信息
- 仓库之间的依赖关系隐含着使用价值的流动

<br>
<br>

#### 网络背后的价值观

- 更有价值的仓库会吸引到更有价值的开发者来贡献
- 更有价值的仓库会更容易被其他仓库所依赖
- 更有价值的开发者更易受到来自其他开发者的关注
- 开发者在更有价值的仓库上的贡献的收益更大

</div>

</div>

---

# 网络构建——一体两面

<div grid="~ cols-2 gap-4">

<div>
  <div class="abs-tl mx-10 my-30 flex">
    <img src="/assets/openrank_issue_actor.png" class="h-80">
  </div>
</div>

<div>
  <div class="abs-tr mx-10 my-20 flex">
    <img src="/assets/sourcecred.png" class="h-90">
  </div>
</div>

</div>

---

# OpenRank

<div grid="~ cols-2 gap-4">

<div>

#### 一种基于异质网络的价值评价算法

- 理
  - 需要数学严格保证算法收敛
  - $\boldsymbol{v}^{(k)} \\ =\boldsymbol{(AS)}^k\boldsymbol{v}^{(0)}+\sum_{t=0}^{k-1}{\boldsymbol{(AS)}^t}\boldsymbol{(E-A)v}^{(0)} \\ =(\boldsymbol{E}-\boldsymbol{AS})^{-1}(\boldsymbol{E}-\boldsymbol{A})\boldsymbol{v}^{(0)}$
- 工
  - 需要工程保证亿级数据点的同时评估
  - Node-centric Pregel
- 社
  - 需要对价值流形成共识
  - 价值终究是主观的共识
</div>

<div>

<div class="abs-tr mx-15 my-30 flex">
  <img src="/assets/complex_network.svg" class="h-80">
</div>

</div>

</div>

---

# 数据工具

OpenDigger, OpenLeaderboard, OpenGalaxy, Hypercrx. https://github.com/X-lab2017

<div>

<div class="abs-tl mx-30 my-30 flex">
  <img src="/assets/open_digger.png" class="h-50">
</div>

<div class="abs-tl mx-20 my-80 flex">
  <img src="/assets/open_leaderboard.jpg" class="h-50">
</div>

<div class="abs-tr mx-20 my-30 flex">
  <img src="/assets/open_galaxy_3d.gif" class="h-50">
</div>

<div class="abs-tr mx-40 my-80 flex">
  <img src="/assets/hypercrx.gif" class="h-50">
</div>

</div>

---
layout: center
class: text-center
---

# Thanks

[https://blog.frankzhao.cn/](https://blog.frankzhao.cn/)

<div>
  <center>
    <img src="/assets/wechat_qrcode.png" class="h-50">
  </center>
</div>
