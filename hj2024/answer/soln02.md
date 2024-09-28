## Problem Set 2
2024/9/24
徐靖 2200012917

### 1 ST Exercise 5.4
**Answer:**
#### (a)
Assume the players can ask for amounts that are not restricted to integers, then the best response is 
$$BR_i(s_j)=\begin{cases}8-s_j, \quad & s_j \in [0,8),\\ [0,8], &s_j=8.\end{cases}$$
In fact, the integer case is the subset of above fomula.
#### (b)
From the best response correspondence, we find every $(i,8-i), i\in [0,8]$ will be a Nash equilibrium. 
And there is another Nash equilibrium $(8,8)$. That is because there are no difference among all of one's requests including $8$, when the other player is asking for $8$ slices.

___
### 2 ST Exercise 5.5
**Answer:**
#### (a)
Let $s_1,s_2,s_3$ represent whether to contribute, $1$ if contribute, $0$ if not, then the best responses is 
$$
BR_i(s_{-i})=
\begin{cases}
0,\quad &-s_i+\sum_{j\in [3]} s_j = 2,\\
1,\quad &-s_i+\sum_{j\in [3]} s_j = 1,\\
0,\quad &-s_i+\sum_{j\in [3]} s_j = 0,\\
\end{cases}
$$
#### (b)
Traversing all $2 ^ 3=8 $ strategy combinations, it was found that only $(0,0,0) , (0,1,1) , (1,0,1) , (1,1,0)$ are pure strategy Nash equilibria.
___
### 3 ST Exercise 5.9
**Answer:**
#### (a)
Assume $n\ge 2$ , one will of course maximize his clean time when $c>1$ regardless of the other's choice. Thus the unique Nash equilibrium is $s_i=5, \forall i\in [n]$.
#### (b)
One will of course minimize his clean time when $c>1$ regardless of the other's choice. Thus the unique Nash equilibrium is $s_i=0, \forall i\in [n]$.
#### (c)
The Nash equilibrium is obviously not Pareto efficient. Let $s_i=5$ and we have $v_i=-2s_i+\sum_{i=1}^5s_i=15>0$. In this case everyone is better.
___
### 4 ST Exercise 5.10
**Answer:**
#### (a)
First order condition:
$$a+\mathrm e_j-2\mathrm e_i=0$$
Best response function:
$$BR_i(\mathrm e_j)=\frac{a+\mathrm e_j}{2}$$

#### (b)
The best response of player $i$ is increasing in the choice of player $j$ whereas in the Cournot model it is decreasing in the choice of player $j$. That's because in this the choices of the two players are strategic complements while ins the Cournot game they are strategic substitutes.
#### (c)
Solve the first order condition
$$a+\mathrm e_1-2\mathrm e_2=0,+\mathrm e_2-2\mathrm e_1=0,$$
we get
$$e_1=e_2=a$$
The solution is unique because it is the only point at which these two best response functions cross.
___
### 5 ST Exercise 5.12
**Answers:**
#### (a)
Another Nash equilibrium is $(1.5,1.51)$. In this equilibrium firm $1$ fulfills market demand at the price of $1.5$ and has no incentive the change the price in every direction. Firm 2 is indifferent between the current price and any higher price, and no incentive to decrease price because it will lose money if it sells the product at a price less than $2$. 
#### (b)
Consider the best response of firms,
$$BR_1(p_2)=\begin{cases}(p_2,+\infty],\quad &p_2< 1,\\ [1,+\infty], &p_2=1,\\1.01, &p_2=1.01\\p_2-0.01, &1.01<p_2<50.51,\\50.5, &p_2\ge 50.51\end{cases}$$
$$BR_2(p_1)=\begin{cases}(p_1,+\infty],\quad &p_1< 2,\\ [2,+\infty], &p_1=2,\\2.01, &p_1=2.01\\p_1-0.01, &2.01<p_1<51.01,\\51, &p_1\ge 50.51\end{cases}$$
And we find there are $100$ Nash equilibria from the above formula. They start with $(1.01,1.02)$ and go all the way up with one-cnet increases to $(2.00,2.01)$. The same logic to $(a)$ explain why they are.
___
### 6
**Answer:**
Nash equilibrium exists only when $p_1$ is between firm $1$ and firm $2$ because:
- When $p_1<0$, both firms lose money at this price, and they will definitely raise prices in turn
- When $p_1>\text{firm 2's marginal cost}=2$, both firms make money at this price, and they will definitely lower prices in turn to gain market share

Consider the case of $1\ge p_1 \ge 2$, at which firm $2$ makes no profit and firm $1$ makes no loss. For firm $2$, $p_2$ has no difference within $[p_1,+\infty)$ , and is better than a price lower than $p_1$. For firm $1$, the best response is $p_2$, so $p_1=p_2\in [1,2]$ are Nash equilibrium

___
### 7 ST Exercise 5.16
**Answer:**
#### (a)
For $x^*$, we have
$$v-p_1-x^*=v-p_2-(1-x^*)\Rightarrow x^*=\frac{1+p_2-p_1}{2}$$
Buyers in $[0,x^*)$ are served by $1$ and the other by $2$, thus we have
$$
v_i(p_1,p_2)=(\frac{1+p_j-p_i}{2})p_i \quad 
$$ 
Solve the first order condition,we get
$$p_1=\frac{1+p_2}{2},p_2=\frac{1+p_1}{2}$$
#### (b)
The case of everyone will be served by one of the firms is discussed above and we could get a unique Nash equilirium $p_1=p_2=1$ . But when $v=1$ the utility of $x*=\frac{1}{2}$ is $v-p_1-\frac{1}{2}=-\frac{1}{2}$ thus he will not buy.  Assume $x^*$ will not choose either one.
Then $1$ firm maximizes
$$\max_{p_1}=(1-p_1)p_1$$
which yields the solution $p_1=\frac{1}{2}$, which means everyone in the interval $x\in [0,\frac{1}{2}]$ wished to buy from firm $1$. This implies if both firms set their prices $\frac{1}{2}$ then each would maximize profits ignoring the other firm, which is the unique Nash equilibrium.
#### (c)
We have $x^*=\frac{1}{2}+p_2-p_1$ Thus profits of two firms are:
$$
v_i(p_1,p_2)=(\frac{1}{2}+p_j-p_i)p_i \quad 
$$
And the response functions are:
$$p_1=\frac{1+2p_2}{4},p_2=\frac{1+2p_1}{4}$$
which yields $p_1=p_2=\frac{1}{2}$ and $x^*$ 's utility is $0$. That means it is the Nash equilibrium.
#### (d)
About $x^*$:
$$v-p_1-\alpha x^*=v-p_2-\alpha (1-x^*)\Rightarrow x^*=\frac{1}{2}+\frac{1}{2\alpha}(p_2-p_1)$$
Then the profits :
$$v_i=\left(\frac{1}{2}+\frac{1}{2\alpha}(p_2-p_1)\right)p_1$$
Then the best response:
$$p_i=\frac{\alpha}{2}+\frac{p_j}{2}$$
which yields $p_i=\alpha$, From the analysis in (c) above we know that for any $\alpha \in [0,\frac{1}{2})$ , $x^*$ will strictly prefer to buy over not buying and so will every other customer.