- 在前人基础上优化的笔记, 感觉证明不会考就没有写证明, 仅罗列结论.
- 博弈论问题的求解往往蕴含在概念之中, tricks 是摆在明面上的.
- 认为比较核心的思想 :
  - br 的交点是 ne
  - 不可置信的威胁
  - 有限博弈下的一些结论往往在连续/无限博弈失效, 存在反例

欢迎补充

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
> 均衡只指均衡情况下的策略组合, 而非均衡情况下的回报

3. **帕累托占优 (Pareto dominates)** : 策略组合 $s$ 回报不低于 $s'$, 且存在至少一个玩家回报严格更高
   - **帕累托有效 (Pareto optimal/Pareto efficient)** : 策略组合不被其他策略帕累托更优

> 囚徒困境中的严格占优均衡存在帕累托改进, 是否与**福利经济学第一定理**矛盾？
>    - 有前提: 
>      - 完全竞争市场
>      - 不存在外部性 (externality): 消费者只关心自己的消费, 生产者只关心自己的生产, 而不会受到他人或者外部环境的影响
>   - 市场竞争能够通过价格机制有效调节经济活动, 达到帕累托最优的资源配置

4.  **IESDS (iterated elimination of strictly dominated strategies)**
    - 没有严格占优策略时也会有唯一的结果. 
      - 参与者的理性是 common knowledge 时, IESDS 成立
    - **Iterated-elimination equilibrium** : 删完后策略集的策略组合
    - 有限博弈中删除次序和最终结果无关系
    - strictly dominant strategy equilibrium 唯一地在 IESDS 中存活

> - 用 IESDS 来算连续的 Cournot Duopoly : 类似闭区间套定理会收敛到纳什均衡
> - IESDS 无法解决 n 个 Cournot 的问题 : 删了一轮就删不下去了. 

5.  **最优反应 (Best response)** : 最核心的概念, 下简称BR
    - 最优反应 $\Leftrightarrow$ 不被严格占优
    - 严格占优策略是任何策略来说的唯一最优反应
    - **最优反应对应 (Best response correspondence)** : 最优反应的集合

6.  **纳什均衡 (Nash Equilibrium)** : 下简称NE
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

## Handout 3

1. **扩展形式博弈 (extensive form game)** : 序贯博弈 (sequential game)
   - 博弈🌲,节点(nodes), 玩家分配(player assignment), 可用行动(available action). 
   - **信息集** : 节点集的一种划分 
     - 玩家不清楚处于信息集中的哪个节点
     - 可用行动相同
   - **完美记忆 (perfect recall)** : 玩家记住他们以前所选择的行动. 
   - **完美信息博弈 (game of perfect information)** : 每个信息集都是**单点(singleton)**
     - 完美信息博弈参与者拥有完美回忆


2. **扩展形式博弈的策略**: 不论选择路径如何, 为每个信息集匹配行动. 
   - 纯策略 : 从信息集到行动集的映射
     - 每个策略组合都会到达唯一的终点, 称为结果
   - 混合策略 : 纯策略的分布
   - **行为策略**: 为每个信息集提供一个行动集元素的分布
> 混合策略维度不低于行为策略 : 前者蕴含了路径经过同一信息集上不同节点的概率分布. 自然完美信息博弈时这个概率分布的维度为0.
   - 在Perfect Recall条件下, 对于每一个mixed strategy, 存在一个behavioral strategy和前者等价, 反之亦然.

3. **扩展形式博弈的NE** : 即写成正则表达的NE. 
   - 如果 $\sigma$ 可以正概率到达一个信息集, 则该信息集在均衡路径上.
> **不可置信的威胁**会出现在均衡路径外
4. **逆向归纳法 (backward inducion)** : 下简称BI, 其解为BI solution.
   - NE只要求在均衡路径上每个人都最优化, 而BI则要求任何路径上都要做最优选择
   - **序贯理性 (sequentially rational)**: 在任何一个信息集上, 当前策略都是对手策略的BR. 
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
      
## Topic 1: 重复博弈

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


