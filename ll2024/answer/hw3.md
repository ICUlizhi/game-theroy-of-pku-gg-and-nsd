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
二阶段是最后一轮, 一定玩单阶段博弈nash均衡.但由于有两个均衡, 因此较差的 $(C,C)$ 可以作为威胁. 这一威胁可能造成被威胁方的损失为 $5-1=4$
枚举第一轮可能的行动组合:
- AA, 此时一次偏离收益 $\leq 13-10=3<4$, 对应存在的 SPE 的充要条件为:
$$s_1^1=s_2^1=A,s_1^2(h)=\begin{cases}B,\quad & h = AA,\\C, &h = AB,AC\end{cases},\\s_2^2(h)=\begin{cases}B,\quad & h = AA,\\C, &h = BA,BC\end{cases},s_1^2(h) = s_2^2(h)\in \{B,C\}$$
这样的 SPE 共 $2^4 = 16$ 种. 实际上是在4个无需威胁的历史下每个历史两种可能的均衡的排列数.
- BA, 此时甲的一次偏离收益 $\leq 13-12=1<4$, 乙的一次偏离收益 $\leq 5-2=3<4$, 对应的策略是SPE:
$$s_1^1=B,s_1^2(h)=\begin{cases}B,\quad & h = BA,\\C, &h = BB\end{cases},s_2^1=A,\\s_2^2(h)=\begin{cases}B,\quad & h = BA,\\C, &h = CA\end{cases},s_1^2(h) = s_2^2(h)\in \{B,C\}$$
同理, 这样的 SPE 共 $2^6=64$ 种
  - AB 是对称的情况, 也有 $64$ 种
- CA, 此时甲在一阶段也没有更好选择, 乙的一次偏离收益 $\leq 1-0=1<4$
$$s_1^1=C,s_1^2(h)=\begin{cases}B,\quad & h = CA,\\C, &h = CC\end{cases},s_2^1=A,s_1^2(CA)=B,\\s_1^2(h) = s_2^2(h)\in \{B,C\}$$
同理, 这样的 SPE 共 $2^7=128$ 种
  - AC 是对称的情况, 也有 $128$ 种
- BB
  - 若第二轮也玩 $BB$, 则任何策略不被威胁, 均没有偏离必要, SPE只需满足 
$$s_i^1=B,s_i^2(BB)=B,s_1^2(h)=s_2^2(h)\in \{B,C\}$$ 
这样的 SPE 共 $2^8=256$ 种
  - 若第二轮玩 $CC$, 则在部分历史下不能玩 $BB$, 因为偏离收益是 $4$. 此时 SPE 满足
$$s_i^1=B,s_1^2(h)=s_2^2(h)\in \{B,C\},s_i^2(h)=\begin{cases}C,\quad & h = AB,BA,BB\end{cases}$$  
这样的 SPE 共 $2^6=64$ 种
- CC
  - 若第二轮玩 $BB$, 则任何策略不被威胁, 均没有偏离必要, SPE只需满足 
$$s_i^1=C,s_i^2(CC)=B,s_1^2(h)=s_2^2(h)\in \{B,C\}$$ 
这样的 SPE 共 $2^8=256$ 种
  - 若第二轮玩 $CC$, 则在部分历史下不能玩 $BB$, 因为偏离收益是 $4$. 此时 SPE 满足
$$s_i^1=B,s_1^2(h)=s_2^2(h)\in \{B,C\},s_i^2(h)=\begin{cases}C,\quad & h = CA,CB,CC,BC,AC\end{cases}$$  
这样的 SPE 共 $2^6=16$ 种
- BC, 此时乙存在可获利一次偏离$B$, 收益为 $5-0=5>4$, 不受威胁, 因此不存在 SPE
  - CB 是对称的情况

以上枚举了全部情形, 给出总共 $992$ 个纯策略 SPE.




## 4
我们做逆向归纳:
- 首先考虑步骤 (5), 这一轮所有委员都 "诚实" 地选择与自己立场最近的方案. 我们发现只要方案在 $(0,5)$ 内, 全体会议中 $ABC$ 相对于保持现状都更倾向于该方案, 只要方案在 $(5,+\infty)$内, 全体会议中 $ABC$ 都保持现状. 当方案为 $0$ 时, $AB$ 投 $0$ 而 $DE$ 保持现状, 对 $C$ 来说二者无差异 
- 对于步骤 (4), 当现状$,X_c,X_d$ 三个可能情形中现状对某个委员最优时, 该委员可能不诚实地选择 $X_d$ 以期淘汰掉 $X_c$ 且在步骤 (5) 中让更多的人选择现状. 假如现状不是最优, 那么步骤 (4) 的选择也是诚实的, 因为选择另一个法案于事无补. 
- 考虑步骤 (3), 对组长 $C$ 来说, 最终方案 $= 2.5$ 是最理想的情况
  - 当 $X_d \ge 2.5$ 时, $X_c=2.5$ 一定能在后面两轮中都得到 $ABC$ 的票从而通过
  - 对于 $0 <X_d < 2.5$, 此时 $X_d$ 对 $ABC$ 来说都比现状更优, 因此他们都在最后两个步骤诚实选择, $C$ 的最优反应比较复杂, 但如果 $C$ 也选择 $X_c = 2.5$, 最终结果也优于现状, 因此此时 $C$ 的最优反应一定优于现状
  - 当 $X_d = 0$ 时, $AB$ 最后两轮诚实, $C$ 的最优反应比较复杂, 但如果 $C$ 选择了 $X_c=1.9$ 这一方案, 能在后面两轮中赢得 $AB$ 的票, 对 $C$ 来说比 $X_d$ 和现状更优, 因此此时 $C$ 的最优反应一定优于现状
- 考虑步骤 (2), 由(3) 的讨论知, 在任意历史 ($X_d$) 下, $C$ 支持 $X_d$ 比不支持(结果为现状)更优, 而 $D$ 一定支持自己的方案, 否则 $D$ 可以直接在第一轮不提出方案, 后者优于前者. 
- 考虑步骤 (1), 由以上讨论知, 如果 $D$ 提出了方案, 最终通过的结果对 $D$ 一定劣于现状, 因此 D 的最优决策是不提出改革方案, 直接让博弈结束.

综上, $D$ 的最优策略是不提出改革方案, 保持现状. $ABC$ 若希望更优, 应当与 $D$ 私下达成妥协通过一个对 $D$ 来说比现状更优的方案, 否则在规则内无法改变现状. $E$ 无论如何无法更优.

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

#### (4) (修改后)(思考题)
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




#### (4) (修改前)
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