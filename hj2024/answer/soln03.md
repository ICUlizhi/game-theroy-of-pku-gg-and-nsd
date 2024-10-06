## Problem Set 3
2024/10/3
徐靖 2200012917

### 1. ST Exercise 6.5
#### (a) 
Use $\{H,P\}$ to denote $\{\text{Hanging out, Patrolling}\}$ or $\{\text{Staying hidden, Prowling}\}$.
The matrix is below:
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="2" style="border:none; text-align:center">Robber</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">H</th>
        <th style="border:none; text-align:center;">P</th>
    </tr>
    <tr>
        <th rowspan="2" style="border:none; text-align:center; vertical-align:middle">Cop</th>
        <th style="border:none; text-align:center;">H</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">10, 10</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">P</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">20, -10</td>
    </tr>
</table>

#### (b)
Assume $\sigma_1(H)=p,\sigma_2(H)=q$, then the payoffs are:
$$\begin{align*}v_1(\sigma_1,\sigma_2)&=10pq+10p(1-q)+20(1-p)(1-q)\\&=20(p-1)(q-1/2)+10\\v_2(\sigma_1,\sigma_2)&=10p(1-q)-10(1-p)(1-q)\\&=-20(p-1/2)(q-1)\end{align*}$$
Then we have:
$$BR_1(q)=\begin{cases}0,\quad & q<0.5,\\ [0,1], &q=0.5,\\1,&q>0.5\end{cases}$$
$$BR_2(p)=\begin{cases}1,\quad & p<0.5,\\ [0,1], &p=0.5,\\0,&p>0.5\end{cases}$$
![](images\3-2b.png)
#### (c)
From the best-response function graph, we know there is a unique Nash equilibrium $(\frac{1}{2}\circ H+\frac{1}{2}\circ P, \frac{1}{2}\circ H+\frac{1}{2}\circ P)$
___
### 2. ST Exercise 6.8
#### (a)
Use $s_i,i\in [3]$ to denote whewher firm $i$  enters the market or not. Then we get the value function:
$$V_i(s_i,s_{-i})=\begin{cases}0, \quad &s_i=0\\ -12 &s_i=1,\sum_{j\in [3]} s_j=3\\13 &s_i=1,\sum_{j\in [3]} s_j=2\\88 &s_i=1,\sum_{j\in [3]} s_j=1\end{cases}$$
Then we can get the best-response function:
$$BR_i(s_{-i})=\begin{cases}0 &\sum_{j\in [3],j\neq i} s_i=2\\1, \quad &\text{o.w.}\\\end{cases}$$
We find $(0,1,1),(1,0,1),(1,1,0)$ are equilibria.
#### (b)
___
### 3. ST Exercise 6.9
#### (a)
Matrix representation is as follow:
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="3" style="border:none; text-align:center">Bidder 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">0</th>
        <th style="border:none; text-align:center;">1</th>
        <th style="border:none; text-align:center;">2</th>
    </tr>
    <tr>
        <th rowspan="3" style="border:none; text-align:center; vertical-align:middle">Bidder 1</th>
        <th style="border:none; text-align:center;">0</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1.5, 2.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 4</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 3</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">1</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">2, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.5, 1.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-1, 3</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">2</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, -1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">-0.5, 0.5</td>
    </tr>
</table>

About IESDS:
- In the first round, $0$ for bidder 2 is strictly dominated by 2.
- In the second round, $1$ for bidder 1 is strictly dominated by 2.And no strategy is strictly dominated in the remaining game.
- Thus ${0,2}\times \{1.2\}$ survives IESDS

#### (b)
Only need to consider the reduced game.
For bidder 1 to mix between 0 and 2, 
$$\begin{align*}&\sigma_2(1)-0.5\sigma_2(2)=0,\sigma_2(1)+\sigma_2(2)=1\\\Rightarrow &\sigma_2(1)=1/3,\sigma_2(2)=2/3\end{align*}$$
For bidder 2 to mix between 1 and 2, 
$$\begin{align*}&4\sigma_1(0)-\sigma_1(2)=3\sigma_1(0)+0.5\sigma_1(2),\sigma_1(0)+\sigma_1(2)=1\\\Rightarrow &\sigma_1(0)=0.6,\sigma_1(2)=0.4\end{align*}$$
Therefore,there is a unique Nash equilibrium $(\frac{3}{5}\circ0+\frac{2}{5}\circ 2,\frac{1}{3}\circ 1+\frac{2}{3}\circ 2)$.

___
### 4
#### (a)
The set of players is $N=\{1,2,\dots,n\}$. Strategy space is $S_i=\{0,1\}, i\in N$. The payoff function is derived as:
$$v_i(s_i,s_{-i})=\begin{cases}1-s_ic, \quad &\sum_{i\in N}s_i\neq 0,\\0, &\sum_{i\in N}s_i=0.\end{cases}$$
#### (b)
All victims keeping quiet is not a Nash equilibrium, since every victim has an incentive to deviate and report. More than one victims report is not a Nash equilibrium because keeping quiet can save the cost without losing the payoff of punishing the perpetrator. Strategy profile with only one victim reports is Nash equilibrium. That means in total $n$ pure strategy Nash equilibria.
#### (c)
Consider a symmetric equilibrium. Suppose every victim keeping quiet with the probability $p$. Thus we have:
$$0\cdot p^{n-1} +1\cdot (1-p^{n-1})=1-c$$
That means $p=c^{1/{n-1}}$, which leads to a Nash equilibrium.