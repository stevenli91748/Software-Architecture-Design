# 从需求到细化架构设计的系统思考路径

**概念架构 各种需求包括关键需求 领域模型进，细化架构设计出**, 根据 5个视图，15个系统设计任务设计出**能实际指导团队并行开发的细化架构**。

     完成概念架构方案的设计和选择后，我们终于可以长出一口气，因为整个架构设计最难的一步己经完成了，但整体方案尚未完成，架构师还需继续努力。接下来我们
     需要再接再厉，将最终确定的概念架构备选方案进行细化，使得概念架构备选方案变成一个可以落地的设计方案。简单来说，详细方案设计就是将方案涉及的关键技
     术细节给确定下来。详细设计方案里面其实也有一些技术点和备选方案类似。
     
     例如， Nginx 的负载均衡策略:
     
           备选有轮询、权重分配、ip_hash 、fair 、url_hash 五个，具体选哪个呢？看起来和备选方案阶段面临的问题类似，但实际上这里的技术方案选择是
           很轻量级的，我们无须像备选方案阶段那样操作，而只需要简单根据这些技术的适用场景选择就可以了。
     
     详细设计方案阶段可能遇到的一种极端情况就是在详细设计阶段发现备选方案不可行:
     
           一般情况下主要的原因是备选方案设计时遗漏了某个关键技术点或关键的质量属性。
     
           例如，笔者曾经参与过一个项目，在备选方案阶段确定是可行的，但在详细方案设计阶段， 发现由于细节点太多， 方案非常庞大，整个项目可能要
           开发长达1 年时间，最后只得废弃原来的备选方案，重新调整项目目标、计划和方案。这个项目的主要失误就是在备选方案评估时忽略了开发周期这
           个质量属性。
           
     解决方法：
     
           • 架构师不但要进行备选方案设计和选型，还需要对备选方案的关键细节有较深入的理解。
           
                例如，架构师选择了E la sticsearch 作为全文搜索解决方案，前提必须是架构师自己对Elasticsearch 的设计原理有深入的理解，比如索引、
                自lj 本、集群等技术点：而不能道昕途说E lasticsearch 很牛，所以选择它，更不能成为把“细节我们不讨论”这句话挂在l嘴边的“ PPT 
                架构师”。
     
          • 通过分步骤、分阶段、分系统等方式， 尽量降低方案复杂度，方案本身的复杂度越高，某个细节推翻整个方案的可能性就越高，适当降低复杂性，
            可以减少这种风险。
            
          • 如果方案本身就很复杂，那么就采取设计团队的方式来进行设计，博采众长，汇集大家的智慧和经验，防止l 、2 个设计师时可能出现的思维盲点或
            经验盲区。  

<a href="https://ibb.co/s9WBS96"><img src="https://i.ibb.co/XxYwBx3/2.png" alt="2" border="0"></a>

# 细化架构设计规格中的五个视图，十五个设计任务

<a href="https://ibb.co/25V4ncq"><img src="https://i.ibb.co/QXSwbY9/3.png" alt="3" border="0"></a>

 **5视图方法错落有致地将众多技术关注点划分成“群落”，“群落”内高聚合，“群落”间松耦合，有利于设计思维的“有序”展开**
 
 **每个视图都是 “组件 + 交互” 的一种体现**

 * [架构设计的五视图理论](https://www.jianshu.com/p/3a3a82256303)

 * [逻辑视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/逻辑视图.md) = 职责单元 + 协作关系
 
   为了满足**系统功能**等方面的**功能性需求**，必须运用**逻辑架构视图**制定分层 分层细化 功能模块 细化功能模块，通用模块 通用框架的设计决策
   逻辑视图设计是面向对象或结构化，目标是设计职责划分和职责间协作，例如分模块、分层、划分垂直功能子系统，为模块、层、子系统定义接口
   
 * [物理视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/物理视图.md) = 物理节点 + 拓扑连接关系
 
   为了满足**约束**等方面的**约束需求**, 必须运用**物理架构视图**制定物理拓朴的设计决策。
   物理视图设计是面向节点，目标是设计物理节点和物理节点拓扑，例如，PC机、服务器、单片机的机型与拓扑连接等
   
 * [开发视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/开发视图.md) = 程序单元 + 编译依赖关系
   
   为了满足**可扩展性，可重用性**等方面的**质量性需求**，必须运用**开发架构视图**深入研究软件系统开发期间的代码文件组织和框架使用，制定相应的设计决策。
   开发视图设计是面向文件，目标是设计程序单元和程序单元组织，例如，开发语言选型、应用程序框架选择、编译依赖关系等
   
 * [运行视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/运行视图.md) = 控制流 + 同步关系
 
   为了满足**性能，可用性**等方面的**质量性需求**，必须运用**运行架构视图**制定相应的并行 分时 排队 缓存的设计决策。
   运行视图设计是面向控制流，目标是设计控制流和控制流组织，例如，多进程技术、多线程技术、中断服务程序等
   
 * [数据视图](https://github.com/stevenli91748/Software-Architecture-Design/blob/master/细化架构设计/数据视图.md) = 数据单元 + 数据关系
   
   数据视图设计是面向表或文件，目标是设计数据存储格式和持久化设计，例如，关系数据库、实时数据库、文件等
