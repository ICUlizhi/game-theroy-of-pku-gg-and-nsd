- 在娄神基础上优化的笔记
  - 感觉证明不会考, 罗列结论时没有写证明
- 博弈论应用题的求解方法往往就蕴含在概念之中, tricks 是摆在明面上的.
- 笔记整体架构参考hj老师相对清晰的博弈论体系, 为ll老师的博弈论额外添加了一些内容
- 额外整理了固定题型和应对方法
  - 🔥表示难度, 3个🔥最难, 4🔥专属于 llhw3.3
- 一些 insight :
  - br 的交点是 ne
  - 代入为博弈玩家, 查询无可获利偏离, 可提高做题注意力
  - 不可置信的威胁
  - 有限博弈下的一些结论往往在连续/无限博弈失效, 存在反例

欢迎补充
___
## Handout 2

1. **正则博弈 (normal form game)**
   - **definition** : 一个三元组(triple) : $(N=[n],\{S_i\}_n,\{v_i\}_n)$
   - **策略组合 (strategy profile)** : $s\in S=S_1\times S_2\times \cdots \times S_n$
     - 有限博弈 $\Leftrightarrow$ 策略组合是有限的 $\Leftrightarrow$ 每个人的策略有限
   - **正则表示也能表示连续情况** : 例如 Cournot 模型

> - **拍卖**
>   - 一价拍卖
>   - **二价拍卖 (Second-price auction)** : 获胜者支付第二高的出价

2. **严格占优 (strictly dominated)**
   - 策略 1 严格占优于策略 2 $\Leftrightarrow$ 对于任意对手的策略, 选 1 的收益都**严格大于** 2 
     - 理性人不会选择被严格占优的策略
   - **严格占优策略 (Strictly dominant strategy)** : 其他策略都被它占优
   - **严格占优策略均衡 (Strictly dominant strategy equilibrium)**
     - 严格占优策略均衡存在则唯一
> - 均衡只指均衡情况下的策略组合, 而非均衡情况下的回报
> - **弱劣策略** : 对于任意对手的策略, 选其他某个策略的收益**大于等于**该策略

3. **帕累托占优 (Pareto dominates)** : 策略组合 $s$ 回报不低于 $s'$, 且存在至少一个玩家回报严格更高
   - **帕累托有效 (Pareto optimal/Pareto efficient)** : 策略组合不被其他策略帕累托更优

> 囚徒困境中的严格占优均衡存在帕累托改进, 是否与**福利经济学第一定理**矛盾？
>    - 有前提: 
>      - 完全竞争市场
>      - 不存在外部性 (externality): 消费者只关心自己的消费, 生产者只关心自己的生产, 而不会受到他人或者外部环境的影响
>   - 市场竞争能够通过价格机制有效调节经济活动, 达到帕累托最优的资源配置

4.  **IESDS (iterated elimination of strictly dominated strategies)** : 不断删除被严格占优的策略
    - 没有严格占优策略时也会有唯一的结果. 
      - 参与者的理性是 common knowledge 时, IESDS 成立
    - **Iterated-elimination equilibrium** : 删完后策略集的策略组合
    - 有限博弈中删除次序和最终结果无关系
    - strictly dominant strategy equilibrium 唯一地在 IESDS 中存活

> - 用 IESDS 来算连续的 Cournot Duopoly : 类似闭区间套定理会收敛到纳什均衡
> - IESDS 无法解决 n 个 Cournot 的问题 : 删了一轮就删不下去了. 

1.  **最优反应 (Best response)** : 最核心的概念, 下简称BR
    - 最优反应 $\Leftrightarrow$ 不被严格占优
    - 严格占优策略是任何策略来说的唯一最优反应
    - **最优反应对应 (Best response correspondence)** : 最优反应的集合

2.  **纳什均衡 (Nash Equilibrium)** : 下简称NE
    - 策略组合里面的每个策略都是对手策略的最优反应
    - **可获利的偏离 (Profitable deviation)**: 给定策略组合, $i$ 的另一个策略使其回报更大
      - NE $\Leftrightarrow$ 无可获利的偏离 $\Leftrightarrow$ **互为最优反应 (mutual BR)**
    - **一致性** : 玩家对对手的看法是正确的 (即均衡状态下知道对方的策略)
    - 严格占优策略均衡一定是唯一的 NE
    - NE 会在 IESDS 中存活 


7.  **混合策略** : $\Delta S_i$ ($S_i$ 上面的所有概率分布) 的元素
    - **支撑集** : $\text{supp } \sigma_i = \{s_i | \sigma_i(s_i) > 0\}$
    - 混合策略 $\sigma_{i}$ 是 $\sigma_{-i}$ 的BR $\Leftrightarrow$ 不存在可获利的纯策略偏离 $\Leftrightarrow$ 支撑集中**每一个**纯策略都是 $\sigma_{-i}$ 的 BR
      - 支撑集无差异 
      - 从而可以定义混合策略的 NE : mutual BR
    - 有限正则博弈一定有 NE
    - **混合策略占优** ：混合策略对纯策略占优 
      - 相应有 IESDS 
      - original game 的 NE $\Leftrightarrow$  IESDS 后的 reduced game 的 NE

### Topic : 双人零和博弈
两个玩家的目标完全对立, 一个人的收益就是另一个人的损失
  - **maxmin值** : 玩家 $i$ 的最大最小策略
  - **minmax值** : 另一玩家的最小最大策略
  - 总有 $\max_{s_i}\min_{s_{-i}}v_1(s_1,s_2)\leq \min_{s_{-i}}\max_{s_i}v_1(s_1,s_2)$
  - 双人零和博弈下考虑所有策略(混合, 纯)时, maxmin值和minmax值相等

## Handout 3

1. **扩展形式博弈 (extensive form game)** : 序贯博弈 (sequential game)
   - 博弈🌲,节点(nodes), 玩家分配(player assignment), 可用行动(available action). 
   - **信息集** : 节点集的一种划分, 可以是单点
     - 玩家不清楚处于信息集中的哪个节点
     - 可用行动相同
   - **完美记忆 (perfect recall)** : 每个玩家在决策时都能知道自己所有的历史行动和观察到的所有信息. (对任意参与者 $i$ 的任意信息集中的节点 $x,y$, 以及 $x$ 的前继 $u(u\to \dots \to x)$, 都存在 $v$ 满足 : $v$ 是 $y$ 的前继, $v$ 与 $u$ 在同一个信息集. )
   - **完美信息博弈 (game of perfect information)** : 每个信息集都是**单点(singleton)**
     - 完美信息博弈参与者拥有完美回忆
> 注意区分完美回忆(perfect recall), 完美信息(perfect information), 完全信息(complete information), 完美贝叶斯均衡(PBE), 四"完"各不相同

2. **扩展形式博弈的策略**: 不论选择路径如何, 为每个信息集匹配行动. 
   - 纯策略 : 从信息集到行动集的映射
     - 每个策略组合都会到达唯一的终点, 称为结果
   - 混合策略 : 纯策略的分布
   - **行为策略**: 为每个信息集提供一个行动集元素的分布
   - 在完美回忆条件下, 对于每一个mixed strategy, 存在一个behavioral strategy和前者等价, 反之亦然.
> - 混合策略维度不低于行为策略 : 前者蕴含了路径经过同一信息集上不同节点的概率分布. 自然完美信息博弈时这个概率分布的维度为0.
> - 完美回忆条件下, 行为策略$\to$混合策略$\to$行为策略是恒同映射, 但混合策略$\to$行为策略$\to$混合策略不是



3. **扩展形式博弈的NE** : 即写成正则表达的NE. 
   - 如果 $\sigma$ 可以正概率到达一个信息集, 则该信息集在均衡路径上.
> **不可置信的威胁**会出现在均衡路径外
4. **逆向归纳法 (backward inducion)** : 下简称BI, 其解为BI solution.
   - NE只要求在均衡路径上每个人都最优化, 而BI则要求任何路径上都要做最优选择
   - **序贯理性 (sequentially rational)**: 在任何一个信息集上, 当前策略都是对手策略的BR. 无论在路径上还是在路径外
   - BI不考虑未来能否改(也即给定后续结果), 且不关注当前会不会到达. 
   - 一些定理
     - 存在性条件 : 任意有限完美信息博弈存在BI solution. 
     - 唯一性条件 : 若没有人认为两个终点**无差异**, 则有限完美信息博弈BI solution唯一. 
     - 纯策略情况下, BI solution一定是NE.

5.  **拓展形式博弈的子博弈 (subgame)** 
    - 根所属信息集是单点集, 根继承者的所属信息集中的点也是根继承者, 则该根诱导子博弈. 
    - **子博弈完美均衡 (SPE)** : 行为策略组在所有的子博弈中都是NE.
      - SPE要求所有路径上的策略组合都是mutual BR, 无论是否在均衡路径上. 
    - 有限完美信息博弈中, **SPE $\Leftrightarrow$ 没有可获利的一次偏离 $\Leftrightarrow$ BI solution**
> "SPE $\Leftrightarrow$ 没有可获利的一次偏离" $\Rightarrow$ "SPE $\Leftrightarrow$ BI solution" $\Rightarrow$ "纯策略BI solution = NE"
      
### Topic : 重复博弈

1. **重复博弈 (repeated game)** 
   - **阶段博弈 (stage game)** : 指重复的 $n$ 个period中的一个 
     - 阶段博弈的全部策略组合 $A^n = A_1 \times ... \times A_n$. 
     - 第 $t$ 期的所有可能历史 $H_t = A^t$ (set of all possible histories up to period $t$), 是t维向量的集合, 每个元素都是所有人的策略组合的某个实现(动作组合). 
     - 阶段博弈纳什均衡 (stage NE): 依于当前轮收益的 NE
   - **总回报 (total payoff)**: 总和阶段博弈收益贴现之和. 其中 $\delta \in (0,1]$ 是贴现率 
$$v_i\equiv \sum_{t=1}^n\delta^{t-1}v_i^t$$
2. **重复博弈的策略**
$$s_i : \bigcup_{t=0}^{T-1}H_t\rightarrow A_i, \quad s_i=(s_i^1,s_i^2,\cdots,s_i^T),\quad s_i^t : H_{t-1}\to A_i.$$
3. **有限期重复博弈**
   - 对于在每个历史下玩出动作组合 $a^*=(a_1^*,\cdots,a_n^*)$ 的策略 $s$, 如果 $a^*$ 是stage NE则 $s$ 是SPE, 如果 $a^*$ 唯一则 SPE 唯一
   - 最后一期一定玩的是 stage NE. 
4. **无限期重复博弈**
   - 无穷博弈下, 一直玩同一个stage NE, 得到的是SPE. 
   - 若 stage NE 有帕累托严格改进 $a$, 那么一定存在足够大的贴现值, 使得存在一个SPE, 均衡结果上在路径上一直在玩a. 

### Topic : 知识算子与信息分割 
> (只有通选博弈论考)
- **信息分割** : 对于参与者 \(i\)，用 $\Gamma_i$ 表示对于 $Y$的一个分割. (即 $i$ 的信息集的组合)
  - 事件 $A$ 是 \(Y\) 的一个子集, 如果 $w\in A$, 则称事件 $A$ 在状态 $w$ 上成立
  - 分割$\Gamma_i$下, 包含状态 $w\in Y$ 的集合表示为 $F_i(w)$
  - 如果 $F_i(w)\subset A$, 则称 $i$ 在状态 $w$ 上知道事件 $A$ 成立
  - 参与者 $i$ 知道 $A$ 成立, 记作 $K_iA = \{w\in Y|F_i(w)\subset A\}$
  - 参与者 $j$ 知道参与者 $i$ 知道 $A$ 成立, 记作 $K_jK_iA = \{w\in Y|F_j(w)\subset K_iA\}$

## Handout 4

1. **贝叶斯博弈/静态非完全信息博弈 (Bayesian game)**
   - **definition** : 一个五元组 : $(N=[n],\{A_i\}_n,\{\Theta_i\}_n,\{v_i\}_n,\mathbb P)$
     - $A_i$ : 玩家 $i$ 的动作空间
     - $\Theta_i$ : 玩家 $i$ 的类型空间
     - $v_i : A\times \Theta \to \mathbb R$ : 玩家 $i$ 的支付函数, 例如 $v_i(a;\theta)$
     - $\mathbb P$ : $\Theta$ 上的分布, 玩家们具备的一个**共同先验(common prior)**.
   - **关于类型的后验概率(posterior belief about his opponents’ types)**  : $\phi(\cdot|\theta_i)$. 其中 $\phi(\theta_{-i}|\theta_i)=\mathbb P(\theta_i,\theta_{-i})/\mathbb P(\theta_i)$
   - 纯策略 $s_i : \Theta_i\to A_i$, 混合策略 $\sigma_i : \Theta_i\to\Delta(A_i)$
   - **纯策略贝叶斯纳什均衡(BNE)** : $s^*=(s_1^*,s_2^*,\dots,s_n^*) \;\text{s.t.}\;\forall i,\forall \theta_{ij}\in \Theta_i,\forall a_i\in A_i$
$$\sum_{\theta_{-i}\in \Theta_{-i}}\phi_i(\theta_{-i}|\theta_{ij})v_i(s_i^*(\theta_{ij}),s^*_{-i}(\theta_{-i});\theta_i,\theta_{-i})\\\leq \sum_{\theta_{-i}\in \Theta_{-i}}\phi_i(\theta_{-i}|\theta_{ij})v_i(a_i,s^*_{-i}(\theta_{-i});\theta_i,\theta_{-i})$$ 
> $P(B|A) = P(AB)/P(A)$

## Handout 5
1. **信念系统 (system of beliefs)**
   - **definition** : 信念系统 $\mu$ 是指在一个扩展形式博弈中, 对于每个信息集 \( h \in H \) 和其中的每个决策节点 \( x \in h \), 为玩家 \( i \) 在信息集 \( h \) 中选择决策时分配一个概率 \( \mu(x) \in [0, 1] \), 表示玩家 \( i \) 认为自己位于决策节点 \( x \) 的概率. 对于每个信息集 \( h \in H \), 有 $\sum_{x \in h} \mu(x) = 1$
     - 完美信息只有一个信念系统
   - $(\text{BNE }\sigma^*,\mu)$ 成为**PBE (perfect Bayesian equilibrium)** 的四个要求: (这里的完美和完美信息的完美不同)
     - 博弈有信念系统.
     - 路径上信息集的信念与贝叶斯法则一致, $\mu(x)=\mathbb P^{\sigma^*}(x)/\mathbb P^{\sigma^*}(h)$.
     - 对于不在均衡路径上的信息集, 贝叶斯法则不适用, 任何信念都可以分配.
     - 给定信念, 玩家的策略必须是序贯理性的. 也就是说, 在每个信息集中, 玩家都会做最佳反应. $\mathbb E[v_i(\sigma_i,\sigma_{-i},\theta)|h,\mu]\ge \mathbb E[v_i(s_i,\sigma_{-i},\theta)|h,\mu], \forall s_i$. 无论在不在均衡路径上 (无论贝叶斯法则适不适用)
    - 假如BNE的任何信息集都在均衡路径上, 则它就是PBE
      - PBE一定是BNE
      - 对于完美信息, PBE等价于SPE

2. **信号博弈 (Signaling Games)**
   - **分离均衡 (Separating Equilibrium)** 指均衡下不同类型的发送者选择不同的信号, 这些信号能够清楚地反映发送者的类型, 并且接收者能够根据接收到的信号准确推断发送者的类型. 比如高能力者选择接受教育, 低能力者选择不接受.
   - **混同均衡 (Pooling Equilibrium)** 指均衡下不同类型的玩家选择相同的信号，因此接收者无法从信号中区分出玩家的类型.
> 当传递信号无需付出成本时 (所谓空谈博弈), 一定存在一个混同均衡

___

## 往年题型整理
> - 不同形式语言的复杂度不同, 而人的演算能力是定值. 因此形式语言或者模型越复杂, 问题本身越简单.
> - 不同问题的规模不同, 而人的演算能力是定值. 因此问题规模越大, 越容易存在巧妙的trick.
> - 如果不亲自做题, 整理的再有insight都没有用 
### 1. 双变量矩阵题型
即策略有限, 从多个选择中混合or纯策略, 往往能看到双变量矩阵
> (1) 🔥 Does player 1 have a strictly dominated strategy? If yes, show which strategy strictly dominates which strategy. If no, explain why.
- 首先需要注意 dominance 是否考虑混合策略
- 直接看矩阵数值, 如果某策略在对手的某个纯策略下是最优反应, 则必不可能被占优, 利用这个做排除法
  - 如果存在某个策略被占优, 直接写谁被谁占
  - 如果不存在, 理由如下: Player 1 has no strictly dominated strategy. This is because each (pure) strategy is a best response to some of player 1’s strategy.
> (2) 🔥 What strategies survive the process of iterated elimination of strictly dominated strategies? In each step of your deletion, show which strategy is strictly dominated by which strategy.
- 按部就班IESDS即可, 注意能不能混合以及不要把严格占优和帕累托更优混淆, 一般没有陷阱
- IESDS可以删被混合策略占优的纯策略, 这一点与题设无关, 因为如果纯策略是存在的，那么必然不会被某个混合策略占优
- 弱劣策略可能也可以删, 取决于题意
> (3) 🔥 Find all pure strategy NE.
- 著名的划线法, 找到每一个对手纯策略下的最优反应, 上下线同时出现的方格即为NE
> (4) 🔥🔥🔥 Find all Nash equilibria (pure and mixed) of this game.
- 首先参考1(2)得到 reduced form
- 一般两种思路, 前者可能稍繁琐, 后者需要注意力, 实战大多是后者
  - 一种是**从下至上**, 枚举并给出支撑集上nash均衡的全部必要条件
    - 纯策略有限, 直接找
    - 混合策略用好NE的充要条件 : 混合的一方支撑集无差异且均最优
  - 另一种是**从上到下**, 对一些条件给出相应的约束来缩小答案范围
    - 常见的条件包括:
      - $\sigma_1(X)>0$ 用于排除被帕累托更优的 X
      - $\sigma_1(X)=1$ 用于讨论一方纯策略另一方混合策略的情形
- **不必囿于公式做题或者NE充要条件**, 把自己代入玩家去考虑可获利偏离可以提高注意力
- 补充1: 双人博弈不存在一个使得nash均衡分布在对角线上的一般条件, 因此不能假设纳什均衡下两人或者多人的策略分布相同
  - 一些规模较大的问题, 可能出现参与者地位对称的情形以降低计算量. 补充1告诉我们, **对称性只能同理对参与者的讨论, 而不为NE提供额外的性质**
- 补充2: 有限博弈下nash均衡当然往往是有界闭的, 但这不代表可以用混合策略讨论纯策略, 因为单点和线段也有界闭
  - 任何情况下**都将纯策略和混合策略分类讨论**
> (5) 🔥🔥 Find all Pareto efficient strategy profiles.
- 容易被忽略的一种题型, 并且需要注意力
- 当你枚举了被帕累托占优的所有其他均衡后, 就可以写显然了
> (6) 🔥 画出三变量矩阵
- 就是多个双变量矩阵
### 2. 出价类题型
这意味着策略集是连续区间, 包括拍卖, 古诺模型等
> (1) 🔥 Show that XXX is a Nash equilibrium.
- 能问出这个问题br大概率比较难写, 别求交点了.
- 写出效用函数, 验证每个玩家无可获利偏离即可
> (2) 🔥🔥 Find a Nash equilibrium
- 揣摩NE的条件给出构造, 再类似上题, 需要注意力
- 一般往对称策略或者单方面碾压获胜的策略想
> (3) 🔥🔥 Find all Nash equilibrium
- 这个问题我们微观经济中一般都做过
- 先根据题意写效用函数
- 再对效用函数求一阶条件, 写出br
- 求br交点即为NE
- 注意 (0,0) 处可能不可导, 需要挖点单独讨论
### 3. 博弈树题型
这里特指完全信息的序贯博弈
> (1) 🔥 Find a mixed strategy Nash equilibrium.
- 参考 2(2), 一般只用考虑对称的策略, 设出所有其他人的分布为 $p$, 再解最后一个人的混合充要条件 (支撑集无差异且均最优), 解出 $p$ 后大家都用这个 $p$, 就省去了验证
> (2) 🔥 Draw the game tree for this game, including the payoffs. 
- 直接画即可, 注意审题, 信息集容易漏
> (3) 🔥🔥🔥 Find all pure strategy Nash equilibria in which the road is built.
- 复杂的题, 先列策略集, 即每个人对属于其的每个信息集给出策略.
> (4) 🔥 Find a backward induction solution.
- 逆向归纳, 给出的solution应当形如 $(\sigma_1,\sigma_2,\cdots,\sigma_n)$

> (5) 🔥🔥 Find a Nash equilibrium that is not a backward induction solution.

- 需要专门构造, 使得在非均衡路径上不是nash均衡.

___

期中期末分割线(hj)

___

### 4. 触发策略
> (1) 🔥🔥设计触发策略, 找出该触发策略成为 SPE 对 $\delta$ 的要求
- 一般是两种考法, 一种是两阶段博弈但是每阶段相对复杂, 另一种是相对简单的重复博弈
- 本质上是利用返回后的收益威胁反悔前的选择
  - 给出触发策略
  - 计算合作收益 $v_1$
  - 计算背信者第一轮偏离的收益 $v_2$
  - 解 $v_2<v_1$ 得到 $\delta$
> (2) 🔥🔥🔥🔥 找出所有的SPE
- 只见过两阶段博弈, 非常难, 例如llhw3.3我总共解出了992个SPE, 如果遇到请严格依照以下步骤:
  - 计算二阶段背信损失 (唯一)
  - 枚举一阶段结束的局面 (双方的动作组合)
    - 计算每一方的每个一阶段一次偏移收益
      - 若存在大于背信损失的偏移, 则该一阶段局面下没有SPE
      - 若为一方的可获利偏移, 则该局面需要被对手在二阶段中威胁
      - 若为一方的不可获利偏移或者不是该局面的一次偏离, 则不需要被威胁, 二阶段对该历史的策略随意 (这里可能需要计数)
    - 列出 SPE, 一阶段策略直接指定, 二阶段在每个历史下的策略由以上三个层面的讨论给定

### 5. 贝叶斯均衡
- 注意我们的策略 : (纯策略 $s_i : \Theta_i\to A_i$, 混合策略 $\sigma_i : \Theta_i\to\Delta(A_i)$)
> (1) 🔥🔥用双变量形式表示贝叶斯博弈
- 这意味着类型和动作都是离散的(纯的而非混合的)
- 先列双变量收益矩阵, 行列是动作组合
- 再列贝叶斯博弈的双变量矩阵, 每个策略都指定了每个类型下的行动, 行列都是对纯策略的枚举, 方格内是双方的期望收益(分布来自于类型的先验)
> (2) 🔥类型离散, 找纯策略BNE
- 基于 5(1) 的双变量矩阵用划线法, 简单
> (3) 🔥类型连续, 找纯策略BNE
- 也就是所谓阈值策略, 即某个类型的某个动作是阈值, 低于阈值的类型选择一种动作, 高于阈值的类型选择另一种动作.
- 先待定对手策略函数 $s_{-i}(\theta_{-i})$
- 对于自己的动作 $a$, 解不等式 $\mathbb E(v_i(a,s_{-i}(\theta_{-i}))|\theta_i)\ge\mathbb E(v_i(b,s_{-i}(\theta_{-i}))|\theta_i)$, 得到对 $\theta_i$的限制条件
  - 这意味着该条件范围内的 $\theta_i$ 的最优反应是 $a$, 这一条件往往是对 $s_{-i}(\theta_{-i})$ 的积分
- 利用上一步结果构造出所有参与者的策略, 阈值待定
- 将策略带入阈值中的积分, 解出阈值
- 重复以上步骤, 直到所有阈值都为定值, 所有策略都为定策略
> (4) 🔥🔥类型离散, 找混合策略BNE
- ?
> (5) 🔥🔥🔥类型连续, 找混合策略BNE
- 所谓拍卖问题
- 一般题目会提示允许假设策略是线性的, 否则太难

|允许假设策略是线性的|没有提示|没有提示的话, 可能需要用到的数学|
|-|-|-|
|待定一次项系数|待定所有人的策略, 证明策略的单调性||
|求期望收益|求期望收益|概率密度函数|
|求一阶条件|求一阶条件|变上下限含参变量积分求导|
|解得之前待定的系数|得到关于策略的常微分方程,解出策略|常微分方程求解|

### 6. 信号博弈
这里指不完全信息动态博弈, 主要的题型是信号博弈
- 信号博弈也是贝叶斯博弈, 双变量矩阵题型参考 5(1), BNE求解参考 5(2)...
> (1) 🔥🔥求 PBE
- 先求 BNE, 因为 PBE 是 BNE 的加强版
- 对每个BNE, 检查或补充PBE的条件 (四个条件中指检查两个就可以, 另外两个是废话)
  - 沿着均衡路径计算信念, (为 BNE 补充信念系统)
  - 对于不在均衡路径上的信息集, 信念不受约束, 但策略也要满足序贯理性
> (2) 🔥🔥🔥求分离/混同均衡
- 先确定/待定信息发送者的策略
- 根据策略确定/待定信念系统
- 根据信念系统探寻信息接受者的最优选择/无差异条件
- 回到信息发送者, 判断是否偏离
  - 偏离则该均衡不存在, 不偏离就已求出均衡
> - "待定"指待定系数
> - 当某个信息集的信念不在均衡路径上时, 信念不受约束, 则需要对信息接受者的不同反应对应的信念区间分类讨论
___
### ll特有屑题屑概念
ll博弈论特有的幽默题目, 一般只在作业中, 但是万一呢?
> (1) 🔥求信息集个数.
- 理解博弈树和信息集的概念后很好求, 过于基础
> (2) 🔥哪些参与人具有完美回忆?
- 思路是反证法, 假设有完美回忆, 由博弈树我们能发现一些节点不应该处于同一个信息集, 如果处于了, 就说明这些节点的参与人没有完美回忆
> (3) 🔥行为策略和混合策略互相转化
- 混合策略 $\to$ 行为策略 : 在博弈树上为终结点标概率, 回到信息集的决策就一目了然了
- 行为策略 $\to$ 混合策略 : 乘起来就对了
> (4) 🔥当参与人趋于无穷大时, 比较帕累托最优结果和NE
- 理论上言之有理即可, 但是助教是做商比较一个相对大小
> (5) 🔥🔥🔥效用(收益)离散但策略连续的NE问题
- 比如多人选举, 输掉选举劣于不参与劣与并列第一, 但是政治立场连续
- 需要带入参与者就题分析是否有可获利偏离, 比较考验注意力, 对于多人的连续立场, 不妨设 $0\leq x\leq y\leq z\leq 1$
> (6) 🔥🔥简述 BNE 和 PBE 的区别
- BNE 是静态均衡, 不像 PBE 会考虑动态过程中后手根据观察到的局面更新对局面的信念
- BNE 只要求在均衡路径上每个人都最优化, 而 PBE 则要求任何路径上都要做最优选择
- PBE 一定蕴含 BNE, 反之不然