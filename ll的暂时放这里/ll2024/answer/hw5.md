# 2024/12/11
2200012917 徐靖
## 1
#### (1) 
情形1 : 玩家 1 手高时下注手低时放弃
- 此时玩家 2 的信念中 $\mu = 1$, 最优反应是 Fold.
- 当玩家手高时, 最优反应是 Bet, 因为收益是 1 大于 Resign 时的 -1.
- 当玩家手低时, 最优反应也是 Bet, 因为收益是 1 大于 Resign 时的 -1. 发生了偏离
 
因此玩家 1 手高时下注手低时放弃的分离均衡不是PBE.

情形2 : 玩家 1 手高时放弃手低时下注
- 此时玩家 2 的信念中 $\mu = 0$, 最优反应是 Call.
- 当玩家手高时, 最优反应是 Bet, 因为收益是 2 大于 Resign 时的 -1. 发生了偏离
- 当玩家手低时, 最优反应是 Resign, 因为收益是 -1 大于 Bet 时的 -2. 发生了偏离

因此玩家 1 手高时放弃手低时下注的分离均衡不是PBE

综上, 参与者 1 采取纯策略的分离完美贝叶斯均衡不存在.

#### (2)
情形1 : 玩家 1 始终下注
- 此时玩家 2 的信念中 $\mu = \frac{1}{2}$, 最优反应是 Call.
- 当玩家手高时, 最优反应是 Bet, 因为收益是 2 大于 Resign 时的 -1. 
- 当玩家手低时, 最优反应是 Resign, 因为收益是 -1 大于 Bet 时的 -2. 发生了偏离

因此玩家 1 始终下注的混同均衡不是PBE.

情形1 : 玩家 1 始终放弃
- 此时玩家 2 的信念不受限制, 最优反应是 Call 的充要条件是 $2-4\mu>-1\Leftrightarrow \mu<\frac{3}{4}$
  - $\mu<\frac{3}{4}$ 时, 若玩家手高, 最优反应是 Bet, 因为收益是 2 大于 Resign 时的 -1. 发生了偏离.
  - $\mu>\frac{3}{4}$ 时, 若玩家手高, 最优反应是 Bet, 因为收益是 1 大于 Resign 时的 -1. 发生了偏离.

因此玩家 1 始终放弃的混同均衡不是PBE.

综上, 参与者 1 采取纯策略的混同完美贝叶斯均衡不存在.

#### (3)
- 玩家 1 手高时, Bet是严格占优策略
- 玩家 1 手低时, 假如在 Bet 和 Resign 之间混合, 则二者对于玩家 1 无差异, 这意味着玩家 2 在 Call 和 Fold 之间混合:

$$-2\mu +2 (1-\mu)= -\mu-1+\mu\Rightarrow \mu = \frac{3}{4}$$

- 假如玩家 1 手低时有 $p$ 的概率选择下注, 则

$$\frac{3}{4} = \mu = \frac{\frac{1}{2}}{\frac{1}{2}+\frac{p}{2}}\Rightarrow p =\frac{1}{3}$$

- 对玩家 1 手低时的无差异条件, 

$$-1 = -2\sigma(call)+(1-\sigma(call))\Rightarrow \sigma(call) = \frac{2}{3}$$

综上, 所求半分离 PBE 为:
- 当玩家 1 手高时, 采取 Bet 的纯策略
- 当玩家 1 手低时, 采取 Bet 概率为 $\frac{1}{3}$, Resign 概率为 $\frac{2}{3} $ 的混合策略
- 玩家 2 信念中 $\mu = \frac{3}{4}$, 采取 Call 概率为 $\frac{2}{3}$, Fold 概率为 $\frac{1}{3}$ 的混合策略.

## 2
#### (1) 
不妨设 Receiver 在信息集 $h_i = (t_1m_i,t_2m_i)$ 上的信念为 $[\mu_i],[1-\mu_i]$, 其中 $i\in [2]$. 

- 当 $t_1$ 类型的 Sender 发送信号 $m_1$, 而 $t_2$ 类型的 Sender 发送信号 $m_2$, 则 $\mu_1=1,\mu_2 =0$, 此时 Receiver 的最优反应为 $bc$ (这里 $xy$ 表示在 $h_1$ 上选择策略 $x$ , 在 $h_2$ 上选择策略 $y$)
- 对于 $t_1$ 类型的 Sender, 发送 $m_1$ 的收益为 $2$, 大于发送 $m_2$ 的收益 $1$.
- 对于 $t_2$ 类型的 Sender, 发送 $m_2$ 的收益为 $3$, 大于发送 $m_1$ 的收益 $1$.

综上, 所求分离 PBE 为:
- $t_1$ 类型的 Sender 发送信号 $m_1$, 而 $t_2$ 类型的 Sender 发送信号 $m_2$
- Receiver 信念为 $\mu_1=1,\mu_2 =0$, 策略为 $bc$

#### (2)
- 当两种类型的 Sender 都发送信号 $m_1$. 则 $\mu_1 = 0.8$, $\mu_2$ 不受限. 注意到 $t_im_1$ 和 $t_im_2$ 的相应选择的回报相同, 我们只需计算:
$$\begin{align*}u_2(a) &= 3\mu+4(1-\mu) = 4-\mu\\u_2(b) &= 4\mu + 0 (1-\mu) = 4\mu\\u_2(c) &= 0\mu + 5(1-\mu)  = 5-5\mu\end{align*}$$
容易发现, 
$$BR_2(\mu) = \begin{cases}c,\quad &0\leq\mu<\frac{1}{4},\\ \{a,c\}, &\mu=\frac{1}{4}\\a,&\frac{1}{4}<\mu<\frac{4}{5},\\\{a,b\}, &\mu = \frac{4}{5},\\b, &\frac{4}{5}<\mu\leq 1 \end{cases}$$
- 对于信息集 $h_1$, 由于$\mu_1 = 0.6$, Receiver 选择 $a$. 对信息集 $h_2$, 假设 Receiver 采用 $(1-\beta-\gamma)\circ a+\beta \circ b+\gamma\circ c$, 其中 $\beta,\gamma$ 不全为正.
- Sender 不偏离的条件:
  - 对于 $t_1$ 类型的 Sender: 一定不偏离, 因为纯策略选 $a$ 收益最大 
  - 对于 $t_2$ 类型的 Sender:
  $$\mathbb E(u_1(m_1|t_2))\ge \mathbb E(u_1(m_2|t_2))\Rightarrow \beta\ge\gamma\tag{2}$$
- 对不同的 $\mu_2$:
  - $0<\mu_2<\frac{1}{4}$ : 此时 $\beta = 0, \gamma =1$ , 由 (2) 知矛盾
  - $\frac{1}{4}\leq \mu_2 < \frac{4}{5}$ : 此时 $\beta = 0$, 由 (2) 知$\gamma = 0$ 满足条件
  - $\mu_2 = \frac{4}{5}$ : 此时 $\gamma = 0$, 只要 $\beta\ge 0$ 就满足条件
  - $\frac{4}{5}<\mu_2\leq 1$ : 此时 $\beta = 1, \gamma = 0$ 满足条件
- 综上, 以下为所求的混同 PBE :
  - Sender 都选 $m_1$, Receiver 选 $aa$, 信念为 $\mu_1 = 0.6, \mu_2\in[\frac{1}{4}, \frac{4}{5}]$
  - Sender 都选 $m_1$, Receiver 在 $h_1$ 选 $a$, 在 $h_2$ 选择 $a,b$ 任意混合或纯策略, 信念为 $\mu_1 = 0.6, \mu_2 = \frac{4}{5}$
  - Sender 都选 $m_1$, Receiver 选 $ab$, 信念为 $\mu_1 = 0.6, \mu_2\in(\frac{4}{5},1]$

## 3
#### (a)
![](5-3a.png)

#### (b)
- 玩家 1 选择 $XY$ 表示类型优秀时选择策略 $X$, 类型非常好时选择策略 $Y$.
- 玩家 2 选择 $XY$ 表示在 $h_1=(EB,GB)$ 上选择策略 $X$, 在 $h_2=(ES,GS)$ 上选择策略 $Y$.
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="4" style="border:none; text-align:center">参与人 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">LL</th>
        <th style="border:none; text-align:center;">LH</th>
        <th style="border:none; text-align:center;">HL</th>
        <th style="border:none; text-align:center;">HH</th>
    </tr>
    <tr>
        <th rowspan="4" style="border:none; text-align:center; vertical-align:middle">参与人 1</th>
        <th style="border:none; text-align:center;">BB</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-3,3.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-3,3.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 5</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">BS</th>
         <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0,1.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2,0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2,2.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4,1</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">SB</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-2,1.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0,0.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0,2</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2,1</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">SS</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1,-0.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">5,-3</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1,-0.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">5,-3</td>
    </tr>
</table>

#### (c)

<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="4" style="border:none; text-align:center">参与人 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">LL</th>
        <th style="border:none; text-align:center;">LH</th>
        <th style="border:none; text-align:center;">HL</th>
        <th style="border:none; text-align:center;">HH</th>
    </tr>
    <tr>
        <th rowspan="4" style="border:none; text-align:center; vertical-align:middle">参与人 1</th>
        <th style="border:none; text-align:center;">BB</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">6p-6,p+3</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">6p-6,p+3</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">6p-2,4+2p</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">6p-2,4+2p</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">BS</th>
         <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0,5p-1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4-4p,8p-4</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4p,7p-1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4,10p-4</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">SB</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">8p-6,3-3p</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">12p-6,3-5p</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4p-2,4-4p</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">8p-2,4-6p</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">SS</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2p,p-1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4+2p,2p-4</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2p,p-1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">4+2p,2p-4</td>
    </tr>
</table>

当 $p\in(0,1)$ 时, 由划线法知纯策略 BNE 为 $(SS,LL)$ 和 $(BS,HL)$
- $P=0,1$ 时, 退化为完全信息动态博弈, NE 分别为 $(S,LL)$, $(S,HL)$

#### (d)
设 $\mu$ 是 $h_1=(EB,GB)$ 上 $EB$ 的信念, $\lambda$ 是 $h_2 = (ES,GS)$ 上 $ES$ 的信念

由于 PBE 一定是 BNE, 我们发现 $p\in(0,1)$ 时, 纯策略 PBE 唯一:
$$(BS,HL),\mu = 1,\lambda = 0$$

#### (e)
- c 中的 BNE 是静态均衡, 不考虑动态过程中后手根据观察到的局面更新对局面的信念, 从而作修正
- d 中的 PBE 一定蕴含 c 中的 BNE, 而 c 中的 BE 不一定为 d 中的 PBE