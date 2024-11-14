## Problem Set 7
2024/11/13
徐靖 2200012917

### 1. ST Exercise 10.2
#### (a)
Obviously $(B,R)$ is the unique stage Nash equilibrium. And we have the trigger stragegies:
$$s_1^t(h) = \begin{cases}M,\quad &h=\empty \text{ or } MC^{t}\\B, &o.w.\end{cases}, s_2^t(h) = \begin{cases}C,\quad &h=\empty \text{ or } MC^{t}\\R, &o.w.\end{cases}$$
Player 1's payoff from playing his strategy is 
$$v_1(MC)=4$$
and from deviating to $B$ is
$$(1-\delta)v_1(BC)+\delta v_1(BR) = 5(1-\delta)$$ 
Thus player 1 does not have a profitable one-shot deviation if $\delta\ge \frac{1}{5}$. And the critical value is the same for player 2.
Then consider any history in which there exists at least one deviation. It is the repetition of the stage Nash equilibrium, so it is a SPE for all $\delta$.
In conclusion, when $\delta \ge \frac{1}{5}$, $s$ is a SPE.
#### (b)
The same as (a), the non profitable one-shot deviation condition requires:
$$v_1(TL)\ge (1-\delta)v_1(BL)+\delta v_1(BR)$$
Thus when $\delta\ge \frac{1}{4}$, $(T,L)$ is played in every period.
### 2. ST Exercise 10.3
#### (a)
It requires the additional benefit of a deviation is negative: 
$$(5-4)+\delta(1-4)\leq 0 \Rightarrow \delta  \ge \frac{1}{3}$$
#### (b)
It requires the additional benefit of a deviation is negative: 
$$(5-4)+(\delta+\delta^2)(1-4)\leq 0 \Rightarrow \delta  \ge -\frac{1}{2}+\frac{\sqrt{21}}{6} \approx 0.264$$
#### (c)
The punishment in (b) last for two periods which is more severe than the one period punishment in part (a). This means that it can be supported with a lower discount factor because the intensity of the punishment is increasing either in the length or when we have less discounting. And $\delta_T$ is one of the solution of the following equation:
$$\frac{\delta^{T+1}-1}{\delta-1}=\frac{1}{3}$$

### 3.
$$s_i(h) = \begin{cases}E,\quad & |\{r|1\ge r\ge t-1, a^r \neq EE,\text{where } h=(a^1,a^2,\dots,a^{t-1}) \}|\leq 1,\\S. & o.w.\end{cases}$$

Consider the $s_1'$ which differs from $s_1$ only at the beginning : $s_1^1= S$. The outcome path under the strategy $(s_1',s_2)$ is $(SE,EE,\dots)$ , which means the payoff of player $1$ is $3(1-\delta)+2\delta>2$.  Thus $s_1'$ is a profitable deviation and $s$ is not a SPE for any $\delta$.

### 4.
$SS$ is the unique stage Nash equilibrium. 
First consider the one-shot deviation. Players obviously would not change from $S$ to $E$. If $s_1'$ differs from $s_1$ only at the begining $s_1^1 = S$, the payoff is $3(1-\sigma)+0\cdot \sigma$. And payoff when $(s_1,s_2)$ is $2$, which is more than $3(1-\sigma)$ when $\delta$ is sufficiently large. Thus player $1$ has no profitable one-shot deviation.
Then consider any history in which there exists at least one deviation. It is the repetition of the stage Nash equilibrium, so it is a SPE for all.
In conclusion, $s$ is a SPE when $\delta \ge \frac{1}{3}$.

### 5. ST Exercise 10.8
#### (a)
In static stage-game, form $i$ maximizes:
$$\underset{q_i}{\max} (200-q_1-q_2)q_i$$
By FOC we have $BR_i = \max\{0,100-\frac{q_{-i}}{2}\}$. Thus $q_1^*=q_2^*=\frac{200}{3}$ and $\pi_1^*=\pi_2^*=\frac{40000}{9}$
#### (b)
To achieve the monopoly profit,
$$\underset{q_1,q_2>0}{\max} (200-q_1-q_2)(q_1+q_2)$$
By FOC we have $q_1'=q_2'=50$. And $\pi'_1=\pi'_2=5000$. Then construct the grim trigger stragety:
$$s_i^t(h)=\begin{cases}q',\quad & h=\empty \text{ or } (q'q')^{k}, k\in \mathbb N\\q^*, &o.w.\end{cases}$$
This strategy is a SPE when there is no profitable one-shot deviation, i.e.
$$\begin{align*}&\pi'\ge (1-\delta) \max_{q_i\ge 0} (200-q^c_{-i}-q_i)q_i +\delta \pi^*\\\Leftrightarrow & 5000\ge 5625(1-\delta)+\frac{40000}{9}\delta\\\Leftrightarrow & \delta \ge \frac{9}{17}\end{align*}$$
#### (c)
Firm $i$ 's best response is 
$$
BR_i(p_{-i}) = \begin{cases} \mathbb R^+,\quad &p_{-i}=0\\p_{-i}-\epsilon, & 0<p_{-i}\leq 100,\\100, & p_{-i}>100\end{cases}
$$
Thus there's a unique static stage-game $p_1^*=p_2^*=0$. And $\pi_1^*=\pi_2^*=0$
#### (d)
To gain the monopoly profit, we have $p'_1 = p'_2 = 100$. Then construct the grim trigger stragety:
$$s_i^t(h)=\begin{cases}p',\quad & h=\empty \text{ or } (p'p')^{k}, k\in \mathbb N\\p^*, &o.w.\end{cases}$$
This strategy profile is a SPE when there is no profitable one-shot deviation, i.e.
$$\begin{align*}&\pi'\ge (1-\delta) \max_{p_i<100} (200-p_i)p_i +\delta \pi^*\\\Leftrightarrow & 5000\ge (10000-\epsilon^2)(1-\delta)+0\cdot\delta\\\Leftrightarrow & \delta \ge \frac{1}{2}\end{align*}$$

#### (e)
There is no profitable one-shot deviation if:
$$\begin{align*}&\pi'\ge (1-\delta) \max_{p_i<100} (200-p_i)p_i +(1-\delta)\delta\pi^*+(1-\delta)\delta^2 \pi^*+\delta^3\pi'\\\Leftrightarrow & 5000\ge (10000-\epsilon^2)(1-\delta)+5000\delta^3\\\Leftrightarrow & \delta \ge \frac{\sqrt{5}-1}{2}\end{align*}$$
The critical value is higher than that in (d). This is because the penalty has been reduced.
### 6. ST Exercise 10.9
#### (a)
Firm $i$ maximizes : 
$$\max_{q_i\ge 0} (30-q_{-i})q_i-q_i^2$$
By FOC we have $BR_i(q_{-i})=\max\{0,15-\frac{q_{-i}}{2}\}$. Then we have $q_1^*=q_2^*=10$ and $\pi_1^*=\pi^*_2=100$.
To maximize the social welfare, we have :
$$\max_{q_1,q_2\ge 0} (30-q_2)q_1-q_1^2+(30-q_1)q_2-q_2^2$$
By FOC we have $q_1'+q_2'=15$. As $q_1^*+q_2^*=20>15$, the Nash equilibrium is not Pareto optimal.
#### (b)
Split the profit equally, we have
$$q_1'=q_2'=\frac{15}{2},\pi_1'=\pi_2'=\frac{225}{2}$$
Then the non profitable one-shot deviation condition is:

$$\begin{align*}&\pi_i'\ge(1-\delta)\max_{q_i}((30-q_{-i}')q_i-q_i^2)+\delta \pi_i^*\\\Leftrightarrow & \delta \ge \frac{9}{17}\end{align*}$$
### 7. ST Exercise 11.2
#### (a)
The unique SPE of this game is:
$$s_2^1=L,s_1^1(L)=(x_L,0),s_1^1(H)=(x_H,0),s_2^2(h)=\text{Accept}$$
Note that Player $1$ can propose $(x,x_L-x)$ when Player $2$  chooses a low level of investment.  If $(x, x_L − x)$ is accepted, the players’ payoffs are $x$ and $x_L − x − c_L$ respectively; otherwise their payoffs are $0$ and $−c_L$. $x_L-x-c_L\ge -c_L$, thus player $1$ proposes $(x_L,0)$ and player $2$ accepts all is the unique SPE in the subgame.
Situation when $H$ is the same. Given that $-c_L>-c_H$, player $2$ choose $L$ at first.
#### (b)
Assume $y=\frac{x_L+x_H+\min \{0,c_L-c_H\}}{2}$, thus we have $x_L<y<x_H,x_H-Y-c_H>-c_L$. Consider the strategy profile below:
$$s_2^1=H,s_1^1 = (y,x_H-y),s_2^2(h) = \begin{cases}\text{Accept},\quad & h =(H,(y,x_H-y)),\\\text{Refuse}, &o.w.\end{cases}$$
No player has a proﬁtable deviation. The equilibrium payoﬀs are $y$ and $x_H − y − c_H$ respectively. For both players, the payoﬀs are higher than the unique SPE payoﬀs.
### 8. ST Exercise 11.4

#### (a) 
In the subgame after player 2 rejects an offer in the first period, the unique SPE is for player 2 to propose \((0, 1)\) and player 1 to accept. The payoffs are \(-c_1\) and \(1 - c_2\).

In the first period:
- Player 2 accepts offer \((x, 1 - x)\) if \(1 - x \geq 1 - c_2\), and rejects if \(1 - x < 1 - c_2\).
- Therefore, player 1 should propose \((\min\{1, c_2\}, 1 - \min\{1, c_2\})\): \((1, 0)\) if \(c_2 \geq 1\) and \((c_2, 1 - c_2)\) if \(c_2 < 1\).

Thus, the unique SPE:
- If \(c_2 \geq 1\): Player 1 proposes \((1, 0)\) in the first period.
- If \(c_2 < 1\): Player 1 proposes \((c_2, 1 - c_2)\) in the first period.

#### (b)
Consider a strategy where player 1 proposes \((x, 1 - x)\) in the first period and rejects all offers in the second. Player 2 only accepts \((x, 1 - x)\) in the first period and proposes \((0, 1)\) in the second.

Under this strategy:
- Player 1 cannot profitably deviate, as any rejection leads to a payoff of \(-c_1\).
- Player 2 also cannot profitably deviate, as rejecting the first period offer results in a payoff of \(-c_2 < 0\).

Thus, this is a Nash equilibrium.

#### (c)
From (a), we know the outcome after player 2’s rejection. Now consider two cases:

- If \(c_1 \geq 1\):
  - Player 2 accepts \((x, 1 - x)\) if \(1 - x \geq 1 - c_2\).
  - If \(c_2 \geq 1\): Player 1 proposes \((1, 0)\).
  - If \(c_2 < 1\): Player 1 proposes \((c_2, 1 - c_2)\).

- If \(c_1 < 1\):
  - Player 2 accepts \((x, 1 - x)\) if \(1 - x \geq c_1 - c_2\).
  - If \(c_2 \geq c_1\): Player 1 proposes \((1, 0)\).
  - If \(c_2 < c_1\): Player 1 proposes \((1 - c_1 + c_2, c_1 - c_2)\).

Each player’s payoff decreases with their own cost and increases with their opponent’s cost.
