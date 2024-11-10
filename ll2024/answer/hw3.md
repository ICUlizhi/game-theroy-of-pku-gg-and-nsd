# 2024/10/8
2200012917 徐靖
## 1
第一次作业给出了博弈树,和双方策略,不再赘述 ($X$表示哥哥给了弟弟20,$Y$表示给了10)
#### (1)
注意到哥哥的策略 $XMN$ 被 $YMN$ 严格占优, 其中 $ M,N \in \{A,B\}$,因此我们得到简化博弈
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">哥哥</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">YA</th>
        <th style="border:none; text-align:center;">YB</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">弟弟</th>
        <th style="border:none; text-align:center;">A</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">26, 22</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 10</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">B</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 10</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">22, 26</td>
    </tr>
</table>

简化博弈的纯策略nash均衡有 $(A,YA),(B,YB)$
因此原形式的纯策略nash均衡有 $(AA,YAA),(AA,YAB),(AB,YAA),(AB,YAB),(BB,YBB),(BB,YBA),(BA,YBB),(BA,YBA)$

#### (2)
考虑利用两个子博弈的nash均衡去构造原博弈的SPE. 实际上, SPE在每个子博弈上都是nash均衡. 且SPE中哥哥一定在第一轮选Y
由上题讨论, 在均衡路径上的子博弈的nash均衡为 $(A,YA),(B,YB),(\frac{4}{7}\circ A+\frac{3}{7}\circ B,\frac{3}{7}\circ YA+\frac{4}{7}\circ YB)$
另一个子博弈是
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">哥哥</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">YA</th>
        <th style="border:none; text-align:center;">YB</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">弟弟</th>
        <th style="border:none; text-align:center;">A</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">36, 12</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">20, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">B</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">20, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">32, 16</td>
    </tr>
</table>

nash均衡也为 $(A,YA),(B,YB),(\frac{4}{7}\circ A+\frac{3}{7}\circ B,\frac{3}{7}\circ YA+\frac{4}{7}\circ YB)$

那么所有的SPE都在两个子博弈的3*3个组合中, 共9个.

## 2
#### (1)
子博弈只有给定$q_1$ 后 $q_2,q_3$ 同时作选择
考虑这个子博弈, 对 $i\in {2,3}$, 企业 $i$ 作优化问题:
$$\underset {q_i\ge 0}{\max} \; q_i(a-q_1-q_2-q_3-c)$$
其一阶条件
$$a-q_1-q_2-q_3-c = q_i $$
解得
$$q_2=q_3=\max\{\frac{a-c-q_1}{3},0\}$$
返回企业1的选择, 它注意到 $q_2,q_3$ 的最优反应, 因此
$$\underset {q_1\ge 0}{\max} \; q_1(a-q_1-2\max\{\frac{a-c-q_1}{3},0\}-c)$$
解优化问题得到 $q_1 = \frac{a-c}{2}$

从而得到唯一的SPE:
$$q_1 = \frac{a-c}{2}, q_2=q_3=\max\{\frac{a-c-q_1}{3},0\}$$

#### (2)
令
$$q_1 = \frac{a-c}{2}, q_2=q_3= \begin{cases}\frac{a-c}{6}, \quad &q_1 = \frac{a-c}{2},\\a, &o.w. \end{cases}$$
这显然是该扩展博弈的纳什均衡, 双方都没有可获利的偏离. 而它不是SPE, 因为当 $q_1\neq \frac{a-c}{2}$ 时, 企业2和3都亏损.

## 3
纯策略单阶段博弈nash均衡是 $(B,B),(C,C)$ 收益分别为 $(5,5),(1,1)$
二阶段是最后一轮, 一定玩单阶段博弈nash均衡.

考虑触发策略:  
$$a^1_i=A,a^2_i=\begin{cases}B,\quad &h_1=AA\\C, &o.w.\end{cases}$$
当两个玩家都采用这个策略时, 双方都没有可获利的一次偏离, 因此是SPE
玩家可以通过二阶段的选择威胁另一方遵从某种历史, 但这个威胁小于等于 $5-1=4$, 而一阶段中 $A$ 相对 $B,C$ 的获利不小于 $7$, 而当有一方选 $A$ 时, 另一方也会选 $A$. 因此SPE中两位玩家一阶段都选 $A$ , 从而触发策略是唯一的纯策略 SPE
## 4
首先考虑步骤 (5), 我们发现只要方案在 $(0,5)$ 内, 全体会议中 ABC 相对于保持现状都更倾向于该方案
注意到 $X_d\in [3,5]$, 否则 D 更倾向于保持现状而非 $X_d$, 这导致 D 存在可获利偏离 : 第一轮直接不提出 $X_d$ , 博弈结束. 此外, 步骤(2)时 CD 都会支持 $X_d$.
当 $X_d \ge 3$ 时, 只需 $X_c<X_d$, 则 $ABC$ 都会选择 $X_c$ 而非 $X_d$, 进而 $X_c$ 胜出, 这符合 C 的利益, 因此当博弈能够进行到步骤(3)时, $X_C = 2.5$
当 D 提出 $X_d$ 的结果是 $X_c=2.5$ 通过最终投票表决并取代现状, 这对于D来说比现状更劣. 因此 D 的最优决策是不提出改革方案, 直接让博弈结束.

综上, D默认的最优策略是不提出改革方案, 保持现状. ABC若希望更优, 应当与 D 私下达成妥协通过一个 $(3,4]$ 的方案, 否则在规则内无法改变现状. E无论如何无法更优.

## 5
#### (1)
企业策略 : $H$ (生产高品质药物), $L$ (生产低品质药物)
消费者策略 : $B$ (购买药物), $N$ (不购买药物)

<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">消费者</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">B</th>
        <th style="border:none; text-align:center;">N</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">企业</th>
        <th style="border:none; text-align:center;">H</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2, 1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-4, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">L</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">6, -2</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
</table>

在这个单阶段博弈中, $H$ 被 $L$ 严格占优, 因此企业只会选 L , 此时对于消费者 B和N有差异不能混合,  因此纳什均衡只有 $(L,N)$

#### (2)
由于只有一个单阶段nash均衡, 因此SPE唯一且在每一轮玩出这个均衡:
$$s_1^1=s_1^2=L,s_2^1=s_2^2=N$$

#### (3)
为两边都设计触发策略:
$$s_1^t = \begin{cases}H, \quad &h_t=(H,B)^{t-1},\\L , &o.w.\end{cases},s_2^t = \begin{cases}B, \quad &h_t=(H,B)^{t-1},\\N , &o.w.\end{cases}$$

该SPE下二者的收益分别为:
$$v_1=\sum_{i=1}^{+\infty}2\delta^{i-1}=\frac{2}{1-\delta},v_2=\sum_{i=1}^{+\infty}\delta^{i-1}=\frac{1}{1-\delta}$$
考虑企业的一次偏离, 由于在偏离的时间前收益和SPE的情形相等, 因此不妨设在第一阶段就偏离,此时
$$v_1'=6+\sum_{i=1}^{+\infty}0\cdot \delta^{i-1}=6$$
消费者没有一次偏离的意愿, 因为 $1$ 是各种情形下的最大收益.
因此"企业生产高品质药物, 消费者每个阶段都购买"能作为均衡结果出现的条件为
$$v_1'\leq v_1\Leftrightarrow \frac{2}{3}\leq \delta $$

#### (4)
降价后单阶段博弈变为:
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">消费者</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">B</th>
        <th style="border:none; text-align:center;">N</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">企业</th>
        <th style="border:none; text-align:center;">H</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 2</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-4, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">L</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">5, -1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
</table>

假设此时企业打算威胁消费者始终买药, 它执行如下的周期生产高低质量产品的触发策略:
$$s_1^t = \begin{cases}H, \quad &2\nmid t , N\notin h_t\\L , &o.w.\end{cases}$$

此时对消费者来说, 一直买药的收益为
$$\sum_{t=1}^{+\infty} (2-\delta)\delta^{2t-2} = \frac{2-\delta}{1-\delta^2}$$
由于在奇数轮时消费者买药更有利, 因此消费者的一次偏离, 即 $2k$ 轮博弈时不买药后的收益的上界为:
$$\sum_{t=1}^{k} (2-\delta)\delta^{2t-2}+\delta^{2k} = \frac{(2-\delta)(1-\delta^{2k})}{1-\delta^2}+\delta^{2k} = \frac{2-\delta}{1-\delta^2} -\frac{\delta^{2k}(1-\delta+\delta^2)}{1-\delta^2}<\frac{2-\delta}{1-\delta}$$

从而消费者无可获利偏移, 被迫始终购买药品, 此时企业的收益为
$$\sum_{t=1}^{+\infty} (1+5\delta)\delta^{t-1} = \frac{1+5\delta}{1-\delta^2} >\frac{1}{1-\delta}$$

上不等式的成立条件是 $\delta>0$ .从而企业更倾向于选择周期生产高低质量产品的触发策略而非一直生产高质量药品的触发策略. 当 $\frac{2-\delta}{1-\delta^2}<\frac{1}{1-\delta}\Leftrightarrow \delta>\frac{1}{2}$ 时消费者在该情形下的收益比降价前小. 而当 $\delta\leq \frac{1}{2}$ 时, 企业始终生产低质量产品的收益更高, 这导致消费者完全买不到高质量药品. 
综上所述, 无论$\delta$取值如何, 将药品价格降低都反而使得消费者处境更劣,  为企业和消费者带来两败俱伤的恶果.