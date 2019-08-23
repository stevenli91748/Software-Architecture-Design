# 从需求到细化架构设计的系统思考路径

**概念架构 各种需求包括关键需求 领域模型进，细化架构设计出**, 根据 5个视图，15个系统设计任务设计出**能实际指导团队并行开发的细化架构**。

     完成概念架构方案的设计和选择后，我们终于可以长出一口气，因为整个架构设计最难的一步己经完成了，但整体方案尚未完成，架构师还需继续努力。接下来我们
     需要再接再厉，将最终确定的概念架构备选方案进行细化，使得概念架构备选方案变成一个可以落地的设计方案。简单来说，详细方案设计就是将方案涉及的关键技
     术细节给确定下来。

<a href="https://ibb.co/s9WBS96"><img src="https://i.ibb.co/XxYwBx3/2.png" alt="2" border="0"></a>

# 细化架构设计规格中的五个视图，十五个设计任务

<a href="https://ibb.co/25V4ncq"><img src="https://i.ibb.co/QXSwbY9/3.png" alt="3" border="0"></a>

 **5视图方法错落有致地将众多技术关注点划分成“群落”，“群落”内高聚合，“群落”间松耦合，有利于设计思维的“有序”展开**
 
 **每个视图都是 “组件 + 交互” 的一种体现**

 * [逻辑视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/逻辑视图.md) = 职责单元 + 协作关系
 
   为了满足**系统功能**等方面的**功能性需求**，必须运用**逻辑架构视图**制定分层 分层细化 功能模块 细化功能模块，通用模块 通用框架的设计决策
   
 * [物理视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/物理视图.md) = 物理节点 + 拓扑连接关系
 
   为了满足**约束**等方面的**约束需求**, 必须运用**物理架构视图**制定物理拓朴的设计决策。
 
 * [开发视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/开发视图.md) = 程序单元 + 编译依赖关系
   
   为了满足**可扩展性，可重用性**等方面的**质量性需求**，必须运用**开发架构视图**深入研究软件系统开发期间的代码文件组织和框架使用，制定相应的设计决策。
   
 * [运行视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/运行视图.md) = 控制流 + 同步关系
 
   为了满足**性能，可用性**等方面的**质量性需求**，必须运用**运行架构视图**制定相应的并行 分时 排队 缓存的设计决策。
   
 * [数据视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/数据视图.md) = 数据单元 + 数据关系
