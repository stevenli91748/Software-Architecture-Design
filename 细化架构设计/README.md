# 从需求到细化架构设计的系统思考路径

  * 概念架构 各种需求包括关键需求 领域模型进，细化架构设计出

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
