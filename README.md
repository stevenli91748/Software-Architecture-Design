# Software-Architecture-Design
软件架构设计的流程，从项目立项--》项目需求--》项目设计--》项目开发

# [软件系统架构面试](https://github.com/stevenli91748/Software-Architecture-Design/tree/master/Interview)

目录
---
<a href="https://ibb.co/X20SnLf"><img src="https://i.ibb.co/4mvPbtw/2.png" alt="2" border="0"></a>

软件架构设计为什麽难？因为它是跨越现实世界（问题领域）到计算机领域（解决方案）之间的一座桥，需求分析是明确“问题领域”，将要解决的问题以
"功能 + 质量 + 约束"的形式定义下来，但需求不管做得再细，也没有打破“系统是黑盒子”这一点，软件架构设计就是完成从面向问题领域到面向解决方案的转换
（进入系统黑盒子）

**架构设计3个原则：**

1. 看透需求

   需求要全(**功能需求 质量需求【性能 可用性 伸缩性 可展性，安全性】  约束需求**)，需求间的矛盾关系要清楚(例如 性能最重要 可用性折衷)。
   
2. 架构大方向正确

   设计好概念架构，这是决定系统成败的关健。

3. 设计好架构的各个方面

   运用多视图设计方法设计系统的不同方面
   
   为了满足**系统功能**等方面的**功能性需求**，必须运用**逻辑架构视图**制定分层 分层细化 功能模块 细化功能模块，通用模块 通用框架的设计决策
   
   为了满足**性能，可用性**等方面的**质量性需求**，必须运用**运行架构视图**制定相应的并行 分时 排队 缓存的设计决策。
   
   为了满足**可展性，可重用性**等方面的**质量性需求**，必须运用**开发架构视图**深入研究软件系统开发期间的代码文件组织和框架使用，制定相应的设计决策。
   
   为了满足**约束**等方面的**约束需求**, 必须运用**物理架构视图**制定物理拓朴的设计决策。
   




# 需求工程

需求工程要明确**功能 质量 约束**这三方面的需求
 
## [软件需求规划](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/软件需求规划/README.md)
  ![Imgur](https://farm8.staticflickr.com/7876/32567759858_2e4ec05b05_o.jpg)
  ![Imgur](https://farm8.staticflickr.com/7904/45527345245_21539d7bb5_o.jpg)

   * 业务研究
   * 应用建模
   * 系统规划
   * 分析计算
   * 报告编制
   * 规划评审

## [软件需求开发](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/软件需求开发/README.md)
  
  ![Imgur](https://farm8.staticflickr.com/7853/31500635057_a8341723a5_o.jpg)
  ![Imgur](https://farm8.staticflickr.com/7851/46440126601_b521848ce2_o.jpg)

   * 需求获取
   * 需求分析
   * 需求编写
   * 需求验证

# [邻域建模](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/邻域建模/README.md)

  **邻域建模决定系统功能的可扩展性，邻域建模和需求分析是同时进行的，他们互相参考**

# [确定关键需求](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/确定关键需求/README.md)

**关键需求决定架构，其余需求验证架构，确定关键需求，可谓小系统和大系统架构设计的分水岭，架构设计从此大不同**

# [概念架构设计](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/概念架构设计/README.md)

 **关键功能，关键质量进，概念架构出**，概念架构在系统设计中非常重要，因需求和设计之间存在一道无型的鸿沟，很多人在需求分析后不知道怎么做了。
 概念架构是直指系统设计目标的设计思想和重大选择---是关乎任何系统成败的最关健的 指向性的设计

# [细化架构设计](https://github.com/stevenli91748/Software-Architecture-Design/tree/master/细化架构设计)

 **概念架构 各种需求包括关键需求 领域模型进，细化架构设计出**

# [架构验证](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/架构验证/README.md)

# 软件架构的类设计工具



# 参考的资料
  * 系统架构设计-从程序员向架构师转型之路.pdf
  * 软件是这样“炼”成的  从软件需求分析到软件架构设计.pdf
  * software-architecture-patterns.pdf
  * 软件需求十步走  新一代软件需求工程实践指南.pdf
  * 软件架构设计(第二版)：程序员向架构师转型必备.pdf  温昱  
  * [UML](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/UML/README)
  * [真实软件项目开发流程--从需求到开发的每一步骤](http://www.youmeek.com/java-sofaware-engineer/)
  * [软件架构入门](http://www.ruanyifeng.com/blog/2016/09/software-architecture.html)
  * [10个通用软件架构模式](https://www.jdon.com/artichect/architectural-patterns.html)
