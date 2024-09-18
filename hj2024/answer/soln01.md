## Problem Set 1
2024/9/18
### 1
#### (a) 
**Answer:** 
There are $n$ bidders, $N = [n]$. Every bidder bids a price $b_i\ge 0$. Thus the strategy is $S_i=[0,+\infty)$ Then the payoff is 
$$
v_i(b_i,b_{-i})=
\begin{cases}
\frac{v_i-b_i}{|\{j|b_i=b_j\}|} ,&\forall j, \; b_i \ge b_j \\
0, &o.w.
\end{cases}
$$
#### (b)
For the second price auction, we have,
$$
v_i(b_i,b_{-i})=
\begin{cases}
\frac{v_i-\max_{j<i} b_j}{|\{j|b_i=b_i\}|} ,&\forall j, \;b_i \ge b_j \\
0, &o.w.
\end{cases}
$$

---

### 2. ST Exercise 4.5
**Answer:**
In the first round, $U$ for player 1 is strictly dominated by $M$.
In the first round, $C$ for player 2 is strictly dominated by $H$.
Hence $\{M,D\}\times \{L,R\} $ survives.
|1\2|L|C|R|
|-|-|-|-|
|U|6,8|2.6|8,2|
|M|8,2|4,4|9,5|
|D|8,10|4,6|6,7|

---

### 3. ST Exercise 4.6
**Answer:**
#### (a)
For $i$, when $t_j \ge 10$, his best reponse is $t_i=0$. When $t_j < 10$, the first order condition is $10-t_j-2t_i=0$. Then we find,
$$t_i = \max\{\frac{10-t_i}{2},0\}$$
#### (b)
- $\forall t_i \in [0,5]$ is not strictly dominated because it is a best response to $t_j = 10-2t_i$.
- For $t_i > 5$, assume $k=t_i-5>0$,then we have
$$v_i(5+k,t_j)=(10-t_j)(5+k)-(5+k)^2=25-5t_i-k^2-t_jk\\<25-5t_j=v_i(5,t_j)$$
It means strategy $t_i>5$ is strictly dominated by $t_i = 5$.
- We have $S_1^1=S_2^2=[0,5]$

#### (c)
- Define $f(x) = 5-x/2$. 
- Assume $S_1^{*}=S_2^{*}\subset [l,u]$
  - First, $S_1^{*}=S_2^{*}\subset [0,5]$
  - Second we find, $[f(u),f(l)]\subset [l,u], \forall l,u>0,l+u\leq 5$
  - Similar to (b), we can find $t_i\in [f(u),f(l)]$ is not strictly dominated
  - For $t_i<f(u)$, assume $k=f(u)-t_i>0$,similarly,
  $$ v(f(u),t_j)-v(f(u)-k,t_j)=k(10-t_j-2f(u)+k)\\ \ge k(10-5-2f(5)+k)>0$$
  Thus $t_i$ is strictly dominated by $t_i = f(u)$.
  - For $t_i>f(l)$, similarly, is strictly dominated by $t_i = f(l)$.
- By induction, we can get closed interval $T_n\subset T_{n-1}\subset \dots \subset T_1=[0,5]$, s.t.
$$T_i= [l_i,u_i]\Rightarrow T_{i+1}= [f(u_i),f(l_i)],i\in \mathbb N^+$$
and 
$$S_1^{*}=S_2^{*}\subset T_n$$
- Given that the measure $|f(u)-f(l)|=|u-l|/2$, we can get 
  $$\lim_{n\rightarrow+\infty}|u_n-l_n|=0$$
  By the closed interval theorem, $T_{+\infty}=\{c\} $. And from the method of generating $T_n$, we can know $f(c)=c$, which means $c=10/3$.
- In conclusion , $S_1^*=S_2^*= \bigcap_{n=1}^{+\infty}T_n=T_{+\infty}=\{10/3\}$. The unique pair of strategies that survive IESDS for this game are $t_1 = t_2 = 10/3$

---

### 4. ST Exercise 4.7
**Answer:**
#### (a)
The set of the player is $\{1,2\}$. The strategy spaces are $S_1=S_2=\{P,B,N\}$. The payoffs to player $1$ are: 
$$
\begin{align*}
v_1(P,P) &= 0.5,  & v_1(P,B) &= 0,   & v_1(P,N) &= 0.3, \\
v_1(B,P) &= 1,  & v_1(B,B) &= 0.5,   & v_1(B,N) &= 0.4, \\
v_1(N,P) &= 0.7,  & v_1(N,B) &= 0.6, & v_1(N,N) &= 0.5
\end{align*}
$$

And, $\forall s\in \{P,B,N\}\times \{P,B,N\}, v_2(s)=1-v_1(s).$

#### (b)
The matrix is following.
<table>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th colspan="3" style="border:none; text-align:center">Player 2</th>
    </tr>
    <tr>
        <th colspan="2" style="border:none;"></th>
        <th style="border:none; text-align:center;">P</th>
        <th style="border:none; text-align:center;">B</th>
        <th style="border:none; text-align:center;">N</th>
    </tr>
    <tr>
        <th rowspan="3" style="border:none; text-align:center; vertical-align:middle">Player 1</th>
        <th style="border:none; text-align:center;">P</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.5, 0.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0, 1</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.3, 0.7</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">B</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">1, 0</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.5, 0.5</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.4, 0.6</td>
    </tr>
    <tr>
        <th style="border:none; text-align:center;">N</th>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.7, 0.3</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.6, 0.4</td>
        <td style="border: 1px solid black; text-align:center; vertical-align:middle;">0.5, 0.5</td>
    </tr>
</table>

#### (c)
In the first round, $P$ for both players is strictly dominated by $B$. 
In the second round, $B$ for both players is strictly dominated by $N$.
Thus $\{N\}\times \{N\}$ survives, which leads to a clear prediction. 



---

### 5. ST Exercise 4.8
**Answer:**
#### (a)
The average is less than $20$ regardless of the number of players, and $3/4$ of the average is less than $15$, This means $18$ also makes $i$ the only winner.
#### (b)
- $x=20$ is not one of the best responses because there will be many winners.
- For $x<20$, the average is $\frac{20(n-1)+x}{n}$, thus player $i$ is the only winner $\Leftrightarrow$
$$|20-\frac{20(n-1)+x}{n}|>|\frac{20(n-1)+x}{n}|$$
When $x<20$, it is equivalent to $x>10-\frac{30}{2n-3}$
- Therefore the set of best responses is 
$$\left\{x\in\mathbb Z \bigg|10-\frac{30}{2n-3}<x<20 \right\}, n\ge2,$$
which depends on the number of players .
---

### 6.
**Answer:**
#### (a)
$$v_i(x_i,x_j)=\arctan x_i<\arctan (x_i+1)=v_i(x_i+1,x_j)$$
Thus $x_i$ is strictly dominated.
#### (b)
$$\forall x_i>0,\;v_i(0,1)=2>\arctan x_i =v_i(x_i,1)$$
Thus 0 for player i is a best response to $x_j=1$, which is not strictly dominated.
#### (c)
$$v_i(0,0)=\arctan 0<\arctan 1=v_i(1,0)$$
They are obviously not mutual best responses.

---


### 7.

**Answer:**
#### (a)
$n$ firms, $N=[n]$. $S_i=\mathbb R_+$. The payoff is:
$$v_i(q_1,q_2,\dots,q_n)=(\max\{0,100-\sum_{j\in N}q_j\}-10)q_i$$
#### (b)
Maximize the above payoff function,we get,
$$q_i=\max\left\{0,\frac{90-\sum_{j\neq i}q_j}{2}\right\}$$
- Given that $q_j>0$, when $90-\sum_{j\neq i}q_j=c>0$, $q_i=c$ is the best response , which traverses $[0,45]$ when $n\ge 3$
    - On the contrary, when $n\ge 3$ , we can always construct a $q_{-1}$ such that $90-\sum_{j\neq i}q_j$ can traverse $[0,45]$, that means $[0,45]$ survives IESDS.
- for $q_j>45$, 
    - if $90-\sum_{j\neq i}q_j\ge q_i$,
$$v_i(0,q_{-i})-v_i(q_i,q_{-i})= 0-(-10q_i)>0  $$
    - if $90-\sum_{j\neq i}q_j< q_i$,
$$v_i(45,q_{-i})-v_i(q_i,q_{-i})= (q_i-45)(q_i-45+\sum_{j\neq i}q_j)>0  $$
- That means $(45,+\infty)$ is strictly dominated. And $[0,45]$ survives IESDS when $n\ge 3$
- When $n=2$, similar to 4.6(c) $, S_1^*=S_2^*=\{\text{Fixed point of function} \;f(x)=45-x/2\}=\{30\}$  
- In conclusion,
$$
S_i^*=\begin{cases}
\{30\} , &n=2,\\
[0,45] , &n\ge 3
\end{cases}
$$
