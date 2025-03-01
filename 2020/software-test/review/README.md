### 软件测试

:star: **定义：发现并指出软件存在缺陷的过程**

- 这个过程指明和标注问题存在的正确位置，详细记录导致问题出现的操作步骤，及时存储当时的错误状态，便于测试后问题能够准确再现
- 测试对象：包括建模、需求、设计等阶段所产生的大量输出制品及程序代码

**软件缺陷**

:star: **定义：系统所需要实现的某种功能的失效（功能缺失）和违背（功能错误）**

软件缺陷危害巨大，目前还无法完全避免

软件规模和复杂性的增长是软件缺陷的根本原因

产生原因：技术原因（架构有瑕疵、算法有问题、代码有错误）；非技术原因（需求理解不到位、需求变化、需求不一致、需求不完整）

**软件危机**

- 软件规模迅速膨胀：规模变大；复杂程度变高
- 巨大挑战：成本越来越高；软件质量越来越差；项目成功率持续走低
- “没有银弹”

### 软件测试模型

- **瀑布模型**
  - 可分为四个阶段：需求、设计、开发、测试
  - 大部分软件缺陷在软件开发的早期就已经出现
  - 软件测试越早越好，软件缺陷的生存生命周期越短越好
- **V 模型**
- **迭代模型（RUP）**：最理想的开发模式

### 软件测试分类

**多维度分类**

- **测试方法**

  - **白盒测试**（玻璃盒测试、结构测试、逻辑驱动测试）：:star: **把测试对象看作一个透明盒子，利用程序内部的逻辑结构及有关信息，设计或选择测试用例，对程序所有逻辑路径进行测试；**主要标准：输入输出；辅助手段：通过在不同点检查程序的状态名，确定实际的状态是否与预期的状态一致

    **优点**

    - 迫使测试人员去仔细思考软件的实现
  - 揭示隐藏在代码中的错误
    - **对代码的测试比较彻底**
  - 优化代码
  
  **缺点**
  
  - 昂贵（人力 / 开发周期）
  
  **种类：**语句覆盖、判定覆盖、条件覆盖、判定 / 条件覆盖、条件组合覆盖、路径覆盖
  
- **黑盒测试**（数据驱动测试）：:star: **把测试对象看作一个黑盒，测试人员不需要考虑程序内部的逻辑结构和内部特性（不关心，可能确实能看到代码），只依据程序的需求规格说明书，检查程序的功能是否符合它的功能说明；**主要标准：输入输出
  
  **优点**
  
    - 对于较大的代码单元来说，黑盒测试比白盒测试效率要高
  - 测试人员不需要了解实现的细节
    - 测试人员和编码人员是相对独立的
  - 从用户的视角进行测试，很容易被理解和接受
    - 有助于暴露任何规格不一致或有歧义的问题
    - 测试用例可以在规格完成之后马上进行
    
    **缺点**
    
    - 只有一少部分可能的输入被测试到，要测试每个可能的输入几乎是不可能的
    - 没有清晰的和简明的规格，测试用例是很难设计的
    
    **种类**：等价类划分法、边界值分析法、输入组合法、因果图法、基于状态测试法
- **测试阶段（和测试模型、流程相对应）**
  
  - **单元测试：**对软件中最小可测试单元进行检查和验证（函数、类、窗口）
  
    > 面向对象编程中由于函数不一定有明确的输入输出而可能只是改变类内部的成员状态，所以面向对象编程中的最小单元不是函数而是类；同时对象的成员函数之间往往有很多交互和联系，将其拆分开来测试有些不妥；而且由于一个类通常由一个人完成，所以作为最小单元比较合适；
  
  - **集成测试（组装测试、联合测试）：**在单元测试的基础上，将所有模块按照设计要求组装成为子系统或系统，进行的测试活动
  
  - **系统测试：**是将待测软件作为一个整体，与硬件、支持软件和人员等其它系统元素结合在一起，在实际运行环境下，对系统进行一些列的测试活动；**目的在于通过与系统的需求定义做比较，发现实际软件与软件需求不符合或矛盾的地方**
  
  - 验收测试：是检验接受测试的软件系统是否满足用户需求的测试活动，**重点在于软件系统的日常使用场景**；**通常由市场、销售、技术支持人员与最终用户一起完成验收测试**
- **测试目标**
  
  - **性能测试：**测试软件系统性能是否满足用户要求的测试；指标：系统响应时间、内存消耗量、能量消耗量
  - **可靠性测试：**测试软件系统的可靠性是否满足用户要求的测试；指标：故障率、重启次数、无故障运行时间长度
  - **功能测试：**测试软件系统是否满足用户的功能性需求的测试；指标：功能是否实现、功能是否正确
  - **强壮性测试**
  - **安全性测试**

- **其它分类**
  
  - **静态测试 / 动态测试**
  - **......**

### 软件测试用例

:star: **完整定义：测试用例是指对软件产品执行一项特定测试任务的描述**

**简要定义：**完成被测软件的某个执行所需的输入值（包括鼠标键盘等交互式输入）

**内容：**测试目标、测试环境、输入数据、测试步骤、预期结果、测试脚本

**作用：**指导测试的实施

- 规划、准备测试数据的依据（输入）

- 评估测试结果的度量基准（预期输出）

- 编写测试脚本的“设计规格书”（需求 VS 代码）


**形式**

- 步骤列表：测试过程的详细步骤
- 数据矩阵：输入 / 输出对
- 测试脚本：编写测试脚本是为了软件版本的快速迭代后的重新测试（回归测试）
- 检查单（静态测试）：不需要编码的测试形式；检查软件的设计和编码是否符合规范等

### 软件测试信息流

**软件测试的三类输入**

- 软件配置：包括软件需求规格说明、软件设计规格说明、源代码
- 测试配置：包括测试计划、测试用例、测试驱动程序等
- 测试工具：为测试的实施提供某种服务的基础性工具（例如测试数据自动生成程序、静态分析程序、动态分析程序、测试结果分析程序以及驱动测试的工作台等）

可靠性分析：可以通过统计方法来告诉测试人员什么时候可以停止测试

### 软件测试的原则

- 尽早不断地进行软件测试：错误无法避免；错误多数都出现在早期；修改成本低
- 程序员应避免检查自己的程序：自己往往发现不了自己的问题；而他人更容易发现你的问题
- 完全测试程序是不可能的：输入空间是极大的，想要完全测试是不可能的
- 软件测试是有风险的行为：需求风险、测试用例风险、缺陷风险等
- 在设计测试用例时，应当包括合理的输入条件和不合理的输入条件：应当越过边界条件进行测试
- 充分注意测试中的群集现象：一个地方出了一个问题，那么在这周围极有可能还有很多问题
- 严格执行测试计划，排除测试的随意性
- 应当对每一个测试结果做全面检查
- 妥善保存测试文档等
- 并非所有软件缺陷都能修复
- bug 的80%原则：多数错误往往来自于少数人

### 软件测试的常见误区

- 调试和测试是一样的：测试是发现错误，调试是消除错误，先发现再修复
- 软件测试对象就是程序
- 软件测试是测试人员的事情，与开发人员无关
- 好的软件质量是通过测试得到的
- 把不合格的开发人员安排做测试
- 关注于测试的执行而忽略测试的设计
- 测试自动化是万能的
- 测试是为了证明软件的正确性：形式化软件方法

### 静态测试和动态测试

**动态测试**

- **定义：**指通过运行被测程序，检查运行结果与预期结果的差异，并分析运行效率、正确性和健壮性等性能
- 动态测试方法由三部分构成：构造测试用例、执行程序、分析程序的输出结果

**静态测试**

- **定义：**指不运行被测程序本身，仅通过分析或检查源程序（或其它软件制品）的语法、结构、过程、接口等来检查程序/设计的正确性；通常不需要测试用例，但需要静态查找表

- **内容和目标**

  - 检查需求文档，是否切合实际，是否自相矛盾，是否清晰明确
  - 检查详细设计文档，是否符合概要设计要求
  - 检查代码风格，是否符合规范
  - 检查程序设计和结构，是否合理
  - 检查业务逻辑，

- **方法**

  - **同行评审：**由软件工作产品创建者的同行们检查该工作产品，识别产品的缺陷，改进产品的不足；**是最常见的静态测试方法**

    >  同行：指项目成员和具有同等开发专业技能的并熟知工作的人员。具体来说指项目组成员或公司内其它项目组成员以及少量公司外专家
    >
    > 产品：指最终产品的组成部分，包括源代码、设计、文档等

    **形式**：都有正式和非正式之分

    - 走读（Walkthrough）：最自由的一种形式
  - 主要目的：评价软件制品（比如软件代码）（做修改）
      - 其它目的：技术的交换、参与人员的技术培训、设计思想的介绍等
      - 评价对象：代码正确性、效率、可读性
      - 走读成员：项目内部的其他开发人员
      - 方式：对照检查表（checklist）检查代码
    - 小组评审（Team Review）：
      - 主要目的：评估产品的价值和市场可行性；给出意见和建议：确认某个制品是否符合要求，是否可以进入下一个阶段，如何提高制品的质量，如何使之符合要求（做决策）
      - 评价对象：主要适用于需求文档和概要设计
      - 评审人员：主要是公司技术领导或权威及公司外专家
    - 审查（Inspection）：
      - 主要目的：检查针对实际的产品或半成品，目的是发现存在的错误
      - 形式：遵循一个严格的过程，人员经过培训，检查过程有标准
      - 评审人员：公司内部设计、开发、测试、质量等部门中工作性质相关的员工
    
    **过程**

    - 计划阶段：明确评审标的，确定参加人员并分配角色和职责（作者、组织者、评审员、记录员）
- 评审实施：主要是会议的形式
    - 评审情况统计：对会议中提出的问题进行统计整理，并形成文档
    - 问题跟踪：作者根据评审中提出的问题进行产品修改，相关人员进行检查
    
  - **数据流测试：**检查程序的控制流程，根据事件的顺序，探索跟踪变量的值以及变量的使用情况（自己测自己，测比较关键的部分）

**详细设计的静态测试**

- **测试依据：**概要设计（总体设计）
- **测试方法：**采用同行评审的形式为审查或走读
- **检查要素：**清晰性、完整性、规范性、一致性、正确性、数据、可靠性、可追溯性、接口

### 代码走读

是代码静态测试的主要手段

**主要对象**

- **代码风格和规则**
  - 程序风格的一致性和规范性
  - 标识符定义的规范性和一致性
    - 保证变量命名能够见名知意，并且简洁。长度适当、命名规范、容易记忆、能够拼读
    - 用相同的标识符代表相同功能的软件实体，不要用相同的标识符表示不同功能的软件实体
  - 程序是否清晰、简洁、容易理解
    - 冗长的程序并不一定就不清晰
  - 注释
    - 注释是否完整
    - 是否清晰简洁
    - 是否正确的反应了代码的功能
    - 是否做了多余的注释
  - 注释文档是否完整
    - 对包、类、属性、方法、参数、返回值的注释是否正确且容易理解
    - 参数类型、参数的限定值的注释是否正确
- **程序设计和结构**
  - 模块接口的正确性检查
    - 确定形参个数、数据类型、顺序是否正确
    - 确定返回值类型及返回值的正确值
    - 以详细设计为基准
  - 输入参数是否有正确性检查
    - 缺少参数正确性检查的代码是造成软件系统不稳定的主要原因之一
  - 调用其它方法接口的正确性
    - 检查实参类型正确与否、传入的参数值正确与否、参数的个数正确与否
    - 返回值正确与否，有没有误解返回值所表示的意思
    - 最好对每个被调用的方法的返回值用显式代码做正确性检查
    - 如果被调用方法出现异常或错误，程序应该给予返回并添加适当的出错处理代码
  - 出错处理
    - 出错的描述难以理解
    - 出错的描述不足以对错误定位，不足以确定出错的原因
    - 显示的错误信息与实际的错误原因不符
    - 对错误条件的处理不正确
    - 在对错误进行处理之前，错误条件已经引起系统干预
  - 表达式或 SQL 语句的正确性
    - 检查所编写的 SQL 语句的语法、逻辑的正确性
    - 检查表达式是否具有二义性（如运算符优先级等）
  - 检查常见变量和全局变量使用的正确性
    - 检查常量或全局变量的取值和数据类型
    - 保证常量的每次引用，是否保持数值和类型的一致性
  - 数字是否进行了命名
    - 包括各种常数、数组的大小、字符位置以及程序中以文字形式写出的数值
  - 检查代码是否可以优化、算法效率是否最高
- **业务逻辑**

### 代码走读检查列表（对照表）

代码走读依赖检查列表

检查列表基于一般性规则和公司文化

### 等价类测试

**等价类定义**

- **如果软件的行为对于一组值来说是相同的，那么这组值就叫等价类**
- **等价类是指测试相同目标或者暴露相同软件缺陷的一组测试用例（查错能力一样的用例）**

**等价类由需求规约产生，而不是根据代码产生（一看不到代码，二代码可能本身就是错的）**

**等价类划分方法**

- 把所有可能的输入数据划分成若干部分（等价类），然后从每一个等价类中选取少数有代表性的数据作为测试用例
- 测试用例的选择：

  - 设计一个测试用例，**尽可能多地覆盖尚未覆盖的有效等价类**。重复这个步骤直到覆盖所有有效等价类为止
  - 设计一个测试用例，**尽可能少地覆盖尚未被覆盖的无效等价类**（大于等于一）。重复这个步骤，直到所有无效等价类都被覆盖为止

**e.g.** 设计一组测试用例，覆盖其有效等价类和无效等价类

- 将输入的百分制成绩转换为 A、B、C、D 四档成绩
  - 90以上：A
  - 80-90：B
  - 70-80：C
  - 70以下：D
- 解
  - **四个有效等价类；两个无效等价类（超范围）（要编号）**
  - **有几个等价类，设计几个测试用例（也要编号，写出同等价类的对应关系）**
  - *图片省略*

**e.g.** 设计一组测试用例，覆盖其有效等价类和无效等价类

- 题目描述
  - *图片省略*

- 解
  - *图片省略*

### 边界值测试

**边界值定义**

- 五点式边界
  - 最大值
  - 最小值
  - 中间值
  - 比最小值大一点
  - 比最大值小一点
- 七点式边界
  - 五点式边界
  - 比最小值小一点
  - 比最大值大一点

**测试原则**

- **一组用例最好只涉及一个边界值，其它值都取中间值（正常值）**
- **注意去除重复的测试用例（即均为中间值的测试用例会多次出现）**

**e.g.**

- 题目描述
  - *图片省略*
- 解
  - 五点式边界*图片省略*
  - 七点式边界*图片省略*

### 等价类边界值测试

是结合等价类测试和边界值测试的测试方法，其测试充分性优于等价类测试和边界值测试

**e.g.**

- 题目描述
  - *图片省略*
- 解
  - *图片省略*

### 因果图测试

**因果图的基本元素：因果图上所有的点都是变量，只能表示0或1，代表有或没有**

- 原因（Cause）
- 结果（Effect）
- 原因和结果之间的因果关系
- 原因和原因之间的关系
- 结果和结果之间的关系

原因：程序的输入引发了什么事件、满足了某一个要求（带有特殊字符、按动某个按钮）

结果：程序的输出满足了某个有意义的触发条件（程序异常、程序终端）

**原因和结果之间的关系**

- 恒等：若 $C_i$ 是 $1$（$0$），则 $E_j$ 也是 $1$（$0$）
- 非：若 $C_i$ 是 $1$（$0$），则  $E_j$也是 $0$（$1$）
- 与：（需要写符号和圆弧）$C_1$、$C_2$、$C_3$、...全部为 $1$，则 $E_j$ 是 $1$
- 或：（需要写符号和圆弧）$C_1$、$C_2$、$C_3$、...至少有一个为 $1$，则 $E_j$ 是 $1$

**原因和原因之间的关系**

- 异（Exclusive）：符号为 $E$ ；$C_1$、$C_2$、$C_3$、...原因中最多只有一个可能为 $1$（互斥的）；**图示为尖角折线加字母**
- 或（I）：符号为 $I$ ；$C_1$、$C_2$、$C_3$、...原因中最少有一个为 $1$；**图示为尖角折线加字母**
- 唯一（Only）：符号为 $O$ ；$C_1$、$C_2$、$C_3$、...原因中有且只有一个为 $1$；**等价为 E / I 约束**；**图示为尖角折线加字母**
- 要求（Require）：符号为 $R$ ；$C_1$、$C_2$ 原因中，要求方如果为 $1$ 则被要求方必须为 $1$；**图示为圆弧虚线加字母带箭头**

**结果和结果之间的关系**

- 强制（Mandatory）：符号为 $M$ ；$E_1$、$E_2$ 结果中，要求方为 $1$ 则被要求方必须为 $0$；**图示为圆弧虚线加字母带箭头**

**因果图测试方法**

利用图解法分析输入的各种组合情况，进而根据设计测试用例

- 检查输入条件的各种组合以及输入条件之间的相互制约关系
-  特别适合程序输入之间具有复杂关系的那些软件的测试工作（检查程序输入条件的各种组合）

**因果图测试方法的具体步骤**

1. 首先从程序规格说明书的描述中，找出因（输入条件）和果（输出结果或者程序状态的改变）
2. 找出原因与结果之间的因果关系，原因和原因之间的约束关系，画出因果图
3. 然后通过因果图转换为判定表
4. 最后为判定表中的每一列设计一个测试用例

**因果图测试的优点**

- 考虑到了输入的各种组合以及各个输入情况之间的相互制约关系
- 能够帮助测试人员按照一定的步骤，高效率地开发测试用例
- 因果图法是将自然语言规格说明转化成形式语言规格说明的一种严格的方法，可以指出规格说明存在的不完整性和二义性

**e.g.**

- 题目描述
  - *图片省略*
- 解
  - 根据程序规格说明书，提取出原因和结果，并转化为因果图*图片省略*
  - 根据因果图写出判定表，并写出对应的测试用例*图片省略*

**e.g.**

- 题目描述
  - *图片省略*
- 解
  - 根据程序规格说明书，提取出原因和结果，并转化为因果图*图片省略*
  - 根据因果图写出判定表，并写出对应的测试用例*图片省略*

### 覆盖率测试

白盒测试以代码覆盖率为主要目标

**都要画流程图**

**语句覆盖**

- 选取足够多的测试数据，使被测试程序中每个语句至少执行一次
- 可执行的语句，不包括注释、标记等
- 设计流程
  - 画流程图
  - 设计测试用例（尽可能少的测试用例）覆盖流程（尽可能多的流程）
  - 写测试用例
  - 写执行路径

**e.g.**

- 题目一
  - **最后需要写出执行路径***图片省略*
- 题目二
  - *图片省略*
  - *图片省略*
- 题目三
  - *图片省略*
  - *图片省略*

**判定覆盖（分支 / 判定覆盖）**

选取足够多的测试数据，使被测试程序中不仅每个语句至少执行一次，而且每个判定的每种可能的结果都至少执行一次（多数情况下，测试用例的数目可能同最大分支数是相同的）

**条件覆盖**

选取足够多的测试数据，使被测试程序中每个判定表达式中的每个条件都取到各种可能的结果

**条件 / 判定覆盖**

条件 / 判定覆盖 == 条件覆盖 + 判定覆盖

选取足够多的测试数据，使被测试程序中不仅每个语句至少执行一次，而且每个判定的每种可能的结果都至少执行一次

**条件组合覆盖（覆盖条件最高的一种覆盖）**

选取足够多的测试数据，使得判定表达式中条件的各种可能组合都至少出现一次