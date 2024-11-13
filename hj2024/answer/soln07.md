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

### 7. ST Exercise 11.2

### 8. ST Exercise 11.4