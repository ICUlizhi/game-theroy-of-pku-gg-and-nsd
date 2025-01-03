## Problem set 2
2024/10/28
徐靖 2200012917
### 1
首先注意到 $R$ 被 $C$ 严格占优
- 纯策略均衡

$(U,L),(M,C)$
- 甲纯策略,乙混合策略的均衡

注意到 $E_L=E_C$ 恒成立,因此$\{(U,p\circ L+(1-p)\circ C):p\in [\frac{4}{7},1)\}$ 和 $\{(M,p\circ L+(1-p)\circ C):p\in (0,\frac{4}{7}]\}$ 是Nash均衡
- 乙纯策略,甲混合策略的均衡不存在

- 混合策略均衡

对乙来说 $L$ 和 $C$ 无差别, 由于 $D$ 被 $\frac{1}{2}\circ U+\frac{1}{2}\circ M$ 严格占优, 因此 $\sigma_1(D)=0$,且
$$3\sigma_2(L)=4(1-\sigma_2(L))\Rightarrow \sigma_2(L)=\frac{4}{7}$$
从而 $\{(\frac{4}{7}\circ L+\frac{3}{7}\circ C,p\circ U+(1-p)\circ M):p\in (0,1)\}$ 是Nash均衡.

### 2
#### (1)
甲的最大最小策略是 $M$, 最大最小值是 $5$
#### (2)
设 $a = \sigma_2(L)$ , 则有
$$\max v_1 = \max \{6-4a,5,4+3a\} \ge 5$$
当 $a\in [\frac{1}{4},\frac{1}{3}]$ 时, $\max v_1 = 5$
乙的最小最大策略是 $\{(a\circ L, (1-a) \circ R)|a\in [\frac{1}{4},\frac{1}{3}]\}$, 甲的最小最大值是 5 
### 3
#### (1)
对于企业 $i$ , 考虑一阶条件
$$ 0 = \frac{\partial u_i}{\partial x_i} = \frac{1}{x_i}-\frac{1}{A-\sum x_i}$$
联立 $i$ 遍历 $[n]$ 后的方程组, 得到
$$x_i = \frac{A}{n+1}$$
这是这个博弈的唯一纯策略纳什均衡, 此时 $u_i = 2\ln A - 2\ln (n+1)$
#### (2)
企业协调行动时, $\sum x_i$ 作为整体被 $i\in [n]$ 平分. 因此,
$$ 0 = \frac{\partial u_i}{\partial x} = \frac{1}{x}-\frac{n}{A-nx}$$
解得 $x_i = x = \frac{A}{2n}$, $u_i = 2\ln (A/2) - \ln n, \forall i$
#### (3)
实际上, $\lim_{n\rightarrow +\infty} 2\ln (A/2) - \ln n  = -\infty = \lim_{n\rightarrow +\infty} 2\ln (A) - 2\ln n $
同时,  $\lim_{n\rightarrow +\infty} x_i = 0$
(1)和(2)两个结果是相同的, 企业的效用均趋于 $-\infty$, 企业的空气消耗均趋于 $0$.

### 4
#### (1)
每个国家都做优化问题:
$$\max (90-q-10)q$$
解得 $q^* = 40$
#### (2)
设 $a, b$ 在 $A$ 产量分别为 $q_{11},q_{21}$, 在 $B$ 产量分别为 $q_{12},q_{22}$. 两家公司面临最优化问题:
$$\underset {q_{i1},q_{i2}}{\max} (90-q_{1i}-q_{2i}-10)q_{ii} + (90 - q_{1j}-q_{2j}-20)q_{ij}, j = 3-i$$ 
考虑一阶条件后解得
$$q_{11}=q_{22} = 30, q_{12}=q_{21}=20$$
#### (3)
最优化问题变为
$$\underset {q_{i1},q_{i2}}{\max} (90-q_{1i}-q_{2i}-10)q_{ii} + (90 - q_{1j}-q_{2j}-50)q_{ij}, j = 3-i$$ 
直接解一阶条件发现 $q_{ij}=0$ 这表明没有出口
因此结果同 (1), $q_{11}=q_{22}=40, q_{12}=q_{21}=0$
### 5
#### (1)
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="3" style="border:none; text-align:center">Player 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">0</th>
        <th style="border:none; text-align:center;">9</th>
        <th style="border:none; text-align:center;">20</th>
    </tr>
    <tr>
        <th rowspan="3" style="border:none; text-align:center; vertical-align:middle">Player 1</th>
        <th style="border:none; text-align:center;">0</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 10</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 11</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">9</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">11, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-9, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">20</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, -9</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-10, -10</td>
    </tr>
</table>
依次剔除严格劣策略, 最后只有 $B$ 存活

#### (2)
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="3" style="border:none; text-align:center">Player 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">A(0)</th>
        <th style="border:none; text-align:center;">B(9)</th>
        <th style="border:none; text-align:center;">C(15)</th>
        <th style="border:none; text-align:center;">D(20)</th>
    </tr>
    <tr>
        <th rowspan="4" style="border:none; text-align:center; vertical-align:middle">Player 1</th>
        <th style="border:none; text-align:center;">A(0)</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 10</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 11</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">B(9)</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">11, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-9, 5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-9, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">C(15)</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">5, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">5, -9</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-5, -5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-15, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">D(20)</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, -9</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, -15</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-10, -10</td>
    </tr>
</table>

由于是对称博弈, 因此Nash均衡下两位行贿者策略相同
- 没有纯策略Nash均衡
- 设四种纯策略的概率为 $a,b,c,d.\; a+b+c+d=1$
  - 若 $d>0$ , 则 A 严格比 D 更优, 因此 $d=0$
- 对 $a,b,c,\; a+b+c=1$, 解方程组 $v(A)=v(B)=v(C)$ 发现
$(0.4\circ A+0.5\circ B+0.1\circ C,0.4\circ A+0.5\circ B+0.1\circ C)$ 是唯一Nash均衡
### 6
#### (1)
$$(\frac{1}{3},\frac{1}{3},\frac{2}{3})$$
对玩家 1,2, 无论偏移到何值玩家 3 都必胜, 也就是1和2必败, $1/3$ 与其他立场无差异
对玩家 3, 立场为 $2/3$ 时已经获胜, 不可能更优
因此该策略组合是Nash均衡
#### (2)
没有人会选择输掉选举的政治立场, 因为此时不参选是可获利的偏离, 因此所有参选者得票数并列.
考虑nash均衡的情形:
- 假如有2人未参选, 未参选的一个候选人和参选者选择同一个政治立场是可获利的偏移, 因此不存在nash均衡
- 假如只有1人未参选, 设参选者的政治立场是 $x,y$, 
  - 由得票相同可知 $x+y=1$ 或 $x=y$
  - 假如 $x\neq y$, 则 $y\neq 0.5$,  选 $x$ 的侯选者改为 $\frac{y+0.5}{2}$ 可以彻底赢得选举, 矛盾. 因此 $x=y=0.5$
  - 此时未参选者选择 $0.5$ 是可获利的偏离, 因此这一情形下不存在nash均衡
- 假如三个人都参选了, 不妨设三个人的政治立场是 $0\leq x\leq y\leq z \leq 1$
  - 考虑 $x = y = z=k$, 任意一位候选人只需选 $\frac{k+0.5}{2}$ 即可彻底获胜
  - 考虑 $x<y<z,$, 由票数相等解得, $(\frac{1}{6}, \frac{1}{2},\frac{1}{6})$, 第一位候选人选 $\frac{1}{3}$ 即可彻底赢得选举
  - 考虑 $x=y<z$, ($x<y=z$ 同理), 发现 $\frac{x+z}{2} = \frac{2}{3}$, 最后一位候选人选 $\frac{2}{3}$ 即可彻底赢得选举

综上, Nash均衡不存在