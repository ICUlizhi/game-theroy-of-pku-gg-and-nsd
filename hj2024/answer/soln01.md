## Problem Set 1
2024/9/18
### 1
#### (a) 
**Answer:** 
There are $n$ bidders, $N = [n]$. Every bidder bids a price $b_i\ge 0$. Thus the strategy is $S_i=[0,+\infty)$ Then the payoff is 
$$
v_i(b_i,b_{-i})=
\begin{cases}
\frac{v_i-b_i}{|\{j|b_i=b_i\}|} ,&\forall j \;s.t. \;b_i \ge b_j \\
0, &o.w.
\end{cases}
#### (b)
For the second price auction, we have,
$$
v_i(b_i,b_{-i})=
\begin{cases}
\frac{v_i-\max_{j<i} b_j}{|\{j|b_i=b_i\}|} ,&\forall j \;s.t. \;b_i \ge b_j \\
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
#### (a)
**Answer:**
For $i$, when $t_j \ge 10$, his best reponse is $t_i=0$. When $t_j < 10$, the first order condition is $10-t_j-2t_i=0$. Then we find,
$$t_i = \max\{\frac{10-t_i}{2},0\}$$
#### (b)
**Answer:**
- $\forall t_i \in [0,5]$ is not strictly dominated because it is a best response to $t_j = 10-2t_i$.
- For $t_i > 5$, assume $k=t_i-5>0$,then we have
$$v_i(5+k,t_j)=(10-t_j)(5+k)-(5+k)^2=25-5t_i-k^2-t_jk\\<25-5t_j=v_i(5,t_j)$$
It means strategy $t_i>5$ is strictly dominated by $t_i = 5$.
- We have $S_1^1=S_2^2=[0,5]$

#### (c)
**Answer:**
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
#### (a)
**Answer:**
The set of the player is $\{1,2\}$. The strategy spaces are $S_1=S_2=\{P,B,N\}$. The payoffs to player $1$ are: 
\begin{align*}
v_1(P,P) &= 0.5  &, \quad v_1(P,B) &= 0   &, \quad v_1(P,N) &= 0.3, \\
v_1(B,P) &= 0.5  &, \quad v_1(B,B) &= 0   &, \quad v_1(B,N) &= 0.3, \\
v_1(N,P) &= 0.7  &, \quad v_1(N,B) &= 0.6 &, \quad v_1(N,N) &= 0.5
\end{align*}


---

### 5. ST Exercise 4.8


---

### 6.

---


### 7.