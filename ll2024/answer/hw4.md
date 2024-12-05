# 2024/11/22
2200012917 徐靖
## 1
#### (1)

XY 表示在自己国家军队强时选择 $X\in \{A,N\}$, 弱时选择 $Y\in \{A,N\}$
不同路径下最终收益为:

<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="4" style="border:none; text-align:center">国家 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">攻击-强</th>
        <th style="border:none; text-align:center;">攻击-弱</th>
        <th style="border:none; text-align:center;">不攻击-强</th>
        <th style="border:none; text-align:center;">不攻击-弱</th>
    </tr>
    <tr>
        <th rowspan="4" style="border:none; text-align:center; vertical-align:middle">国家 1</th>
        <th style="border:none; text-align:center;">攻击-强</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">- c_h, -c_h</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">v - c_h, -c_l</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">v, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">v, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">攻击-弱</th>
         <td style="border: 1px solid black; text-align:center; vertical-align:middle;">- c_l,v -c_h</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;"> - c_l, -c_l</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">v, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">v, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">不攻击-强</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, v</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, v</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">不攻击-弱</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, v</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, v</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
</table>

双变量矩阵形式的博弈表述:

|国家1\国家2|AA|AF|FA|FF|
|-|-|-|-|-|
|AA|$\frac{v-2c_l-2c_h}{4},\frac{v-2c_l-2c_h}{4}$|$\frac{2v-c_l-c_h}{4},\frac{v-2c_h}{4}$|$\frac{3v-c_h-c_l}{4},-\frac{c_l}{2}$|$v,0$|
|AF|$\frac{v-2c_h}{4},\frac{2v-c_l-c_h}{4}$|$\frac{v-c_h}{4},\frac{v-c_h}{4}$|$\frac{2v-c_h}{4},\frac{v-c_l}{4}$|$\frac{v}{2},0$|
|FA|$-\frac{c_l}{2},\frac{3v-c_h-c_l}{4}$|$\frac{v-c_l}{4},\frac{2v-c_h}{4}$|$\frac{v-c_l}{4},\frac{v-c_l}{4}$|$\frac{v}{2},0$|
|FF|$0,v$|$0,\frac{v}{2}$|$0,\frac{v}{2}$|$0,0$|

#### (2)
对于 $v=12,c_l=4,c_h=8$, 我们有
|国家1\国家2|AA|AF|FA|FF|
|-|-|-|-|-|
|AA|-3,-3|3,-1|6,-2|12,0|
|AF|-1,3|1,1|4,2|6,0|
|FA|-2,6|2,4|2,2|6,0|
|FF|0,12|0,6|0,6|0,0|

纯策略贝叶斯纳什均衡只有 $(FF,AA)$ 和 $(AA,FF)$
#### (3)
对于 $v=12,c_l=8,c_h=16$, 我们有
|国家1\国家2|AA|AF|FA|FF|
|-|-|-|-|-|
|AA|-9,-9|0,-5|3,-8|12,0|
|AF|-5,0|1,1|4,1|6,0|
|FA|-8,3|1,4|-1,-1|6,0|
|FF|0,12|0,6|0,6|0,0|

纯策略贝叶斯纳什均衡只有 $(FF,AA)$ , $(AA,FF)$, $(AF,AF)$

## 2
#### (1)
$T_1=\{\{\alpha\},\{\beta,\gamma\},\{\delta\}\}$
$T_2=\{\{\alpha,\beta\},\{\gamma,\delta\}\}$
#### (2)
$K_1A=\{\beta,\gamma,\delta\}$
$K_2K_1A=\{\gamma,\delta\}$
$K_1K_2K_1A=\{\delta\}$
$K_2K_1K_2K_1A = \emptyset$

## 3
设进入为$E$, 不进入为 $N$, 对于给定的 $c_1,c_2$, 收益矩阵为:

<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">企业2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">E</th>
        <th style="border:none; text-align:center;">N</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">企业1</th>
        <th style="border:none; text-align:center;">E</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">3-c_1,3-c_2</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10-c_1, 0</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">N</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 10-c_2</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
    </tr>
</table>

规定 $s_i(\theta_i) =1 $ 表示在私人信息为 $\theta_1$ 的情形下选 $E$, 反之 $s_i(\theta_i) =0 $ 表示选 $N$
假如参与者 $2$ 的最优反应是 $E$, 当且仅当
$$\begin{align*}&\mathbb E(v_2(1,s_j(\theta_j))|c_2)\ge E(v_2(0,s_j(\theta_j))|c_2)\\\Leftrightarrow &\frac{1}{5}\int_{0}^5 10-c_2-7s_1(\theta_1)\mathrm d\theta_1\ge 0\\\Leftrightarrow &c_2\leq10-\frac{7}{5}\int_{0}^5s_1(\theta_1)\mathrm d\theta_1\end{align*}$$
由于两方是对称的, 因此双方都执行阈值策略, 不妨设阈值分别为 $\hat{\theta_1},\hat{\theta_2}$, 则有
$$\hat{\theta_i}=10-\frac{7}{5}\int_0^5s_j(\theta_j)\mathrm d\theta_j = 10-\frac{7}{5}\int_0^{\min\{\hat{\theta_j},5\}}\mathrm d\theta_j = 10-\frac{7}{5}\min\{\hat{\theta_j},5\}$$
解得 $\hat{\theta_1}=\hat{\theta_2}=\frac{25}{6}<5$

综上, 唯一的nash均衡为 $s_i=\begin{cases}E, \quad & c_i\leq \frac{25}{6},\\N, &c_i>\frac{25}{6}\end{cases}, i\in \{1,2\}$


## 4
不妨设该对称策略为 $s(v)$. 对玩家1 我们记除他之外的最高私人价值为 $b$

首先 $s$ 是单调增的, 假如存在 $s(v_1)<s(v_2), v_1>v_2$. 对 $s(b)$ 情形, 若 $s(b)\leq s(v_1) \text{ or } b\ge s(v_2)$, 玩家1 在私人价值为 $v_1, v_2$ 时 $s(v_1)$, $s(v_2)$ 均无差异. 若 $s(v_1)<s(b)<s(v_2)$, 由 $s$ 无可获利一次偏离知玩家1 在私人价值为 $v_2$ 时有 $v_2\ge s(b)$. 从而 $v_1>v_2\ge s(b)\ge s(v_1)$, 此时 $s$ 略微提价即为可获利偏离, 矛盾.

考虑玩家1 私人价格为 $v$ , 出价为 $s'$, 其他人出价遵循 $s$ 时的期望收益:
$$\mathbb E(u(v)) = \frac{\int_{0}^{s^{-1}(s')}\frac{1}{2}(2v-s(b)-s')b^{n-2}\mathrm db}{\int_{0}^{1}b^{n-2}\mathrm db}$$
解一阶条件 $\frac{\partial{\mathbb E(u(v))}}{\partial s'}\Big|_{s(v)}=0$ 得, 
$$(2v-2s'^*)\frac{\partial s^{-1}(s'^*)}{\partial s'}=\frac{s^{-1}(s'^*)}{n-1}$$
假如所有人出价遵循 $s$ 是nash均衡, 则 $s'^*=s(v)$, 从而得到 $s$ 满足的常微分方程
$$s(v)+\frac{v}{2n-2}s'(v)-v=0$$

解得 $s(v) = \frac{2n-2}{2n-1} v$
