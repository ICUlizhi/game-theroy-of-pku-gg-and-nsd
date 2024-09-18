# Game Theory HW03

<center>2100010850 娄峻赫

## 5.4 分披萨

1. If $j \in [0, 8)$ $BR_i(j) = 8 - j$; If $j = 8$, $BR_i(j) = \{1,2,3,4,5,6,7,8\}$ 

2. $\forall i \in [0, 8]\cap Z, (i, 8 - i)$ is a nash equilibria. Besides, $(8, 8)$ is also a nash equilibria.

   In fact, we can easily tell the answer by viewing the interactions of their best response lines.

   

## 5.9 室友悲剧

1. If $c<1$, $BR_i(s_{-i}) = \arg \max_{s_i} (-cs_i + \sum_j s_j) = \{5\}$. Therefore, the nash equilibria is $(5,5, \ldots, 5)$
2. If  $c>1$, $BR_i(s_{-i}) = \arg \max_{s_i} (-cs_i + \sum_j s_j) = \{0\}$. Therefore, the nash equilibria is $(0,0, \ldots, 0)$
3. When $n=5$ and $c=2$, we can use the result of the second scenario: the nash equilibria is $(0,0, 0,0, 0)$. However, this equiliria is not Pareto effective, since $(1,1,1,1,1)$ Pareto-dominates $(0,0, 0,0, 0)$ by raising everyone’s payoff from 0 to 3 and no one is worse off.

## 5.10 协同

1.  Participant i’s best response is given by maximizing his payoff function with a fixed strategy of the other. That is $BR_i(e_j) =  \arg \max_{e_i} (a + e_j)e_i - e_i^2 = \dfrac{a+e_j}{2}, \forall (i,j) \in\{(0,1), (1,0)\}$
2. Actually, the best response here will increase as the other’s effort increased, contrary to the Cournot game(the best response here will decrease as the other’s production increased). This is because the effort here is a complement to each other while the product in Cournot game is a substitute to each other, which means the effort will benefit each other but the product will not.
3. Consider the interaction of their best response: $e_i = \dfrac{a+e_j}{2} \quad and \quad e_j = \dfrac{a+e_i}{2} \Rightarrow e_i = e_j = a$. Since the interaction is unique, nash equilibrium is unique.

## 5.12 非对称伯特兰模型

1. The first question is a consequence of the second.
2. For enterprise 1, its best response function is $BR_1(p_2) = \left\{\begin{matrix}
     \{p_2 + 0.01,p_2 + 0.02 ,\ldots\}&  if\quad p_2 <1\\
     \{1,1.01,1.02,\ldots\}& if\quad p_2 =1\\
     \{1.01\}& if \quad p_2 = 1.01\\
     \{p_2-0.01\} & if \quad 1.01 < p_2 < 50.51\\
     \{50.5\} & if \quad p_2 \geq 50.51
   \end{matrix}\right.$

​	For enterprise 2, the best response function is similar:

​	$BR_2(p_1) = \left\{\begin{matrix}
  \{p_1 + 0.01,p_1 + 0.02 ,\ldots\}&  if\quad p_1 <2\\
  \{2,2.01,2.02,\ldots\}& if\quad p_1 =2\\
  \{2.01\}& if \quad p_1 = 2.01\\
  \{p_1-0.01\} & if \quad 2.01 < p_1 < 51.01\\
  \{51\} & if \quad p_1 \geq 51.01
\end{matrix}\right.$

​	So we can find the interaction of them, which is also the nash equilibrium in this case: 

$(1+0.01k, 1.01+0.01k) \quad \forall k \in \{1,2,3,\ldots, 100\}$ ，therefore we get 100 Nash equilibria in total. (We can find it by noticing that $q_1<q_2$ means $q_2 > q_1$ as well, so we can pay attention to the order in the two functions)


## 非对称伯特兰模型（续）

* In this case, we can modify the function we give in the 5.12

* For enterprise 1, its best response function is 

* $BR_1(q_2) = \left\{\begin{matrix}
    (p_2, +\infty)&  if\quad p_2 <1\\
   [1,+\infty) & if\quad p_2 =1\\
    \{p_2\} & if \quad 1 < p_2 \leq 50.5\\
    \{50.5\} & if \quad p_2 > 50.5
  \end{matrix}\right.$

* For enterprise 2, the best response function is similar:

  ​	$BR_2(p_1) = \left\{\begin{matrix}
    [p_1,+\infty)&  if\quad p_1 \leq 2\\
    \empty & if \quad 2 < p_1 < 51\\
    \{51\} & if \quad p_1 > 51
  \end{matrix}\right.$

* So the equilibrium is easy to find: $(a，a) \quad \forall a \in [1,2]$

## 5.16 霍特林价格竞争模型

1. In this section, we firstly find the balance point $x^*$, where the customer is indifferent between 1 and 2. 
   * So we have : $v - p_1 -x^* = v - p_2 - 1 + x^* \Rightarrow x^* = \dfrac{1+p_2-p_1}{2}$
   * For $x < x^*$, they will come to 1 while others come to 2. So we find the profit of the firms, and the best response is the argument maximizing the profit: 
   * $BR_1(p_2) = \arg \max_{p_1} p_1 x^* = \{\dfrac{1+p_2}{2}\}$
   * By symmetry we have :$BR_2(p_1) = \arg \max_{p_2} p_2 (1-x^*) = \{\dfrac{1+p_1}{2}\}$
2. The one located at x will buy from 1 only when :
   * $1-p_1-x\geq 0 \quad and \quad 1-p_1-x \geq 1-p_2-(1-x)$ ,  i.e. $x \leq min\{1-p_1, \dfrac{1+p_2-p_1}{2}\}$
   * $v_1 = \left\{\begin{matrix}
     0.5p_1(1+p_2-p_1)  & p_1 \leq 1-p_2\\
      p_1(1-p_1) &p_1 > 1-p_2
     \end{matrix}\right.$
   * $BR_1(p_2) = \left\{\begin{matrix}
     0.5  & 1-p_2 \leq 0.5<\dfrac{p_2+1}{2} \Leftrightarrow p_2\geq0.5\\
      1-p_2 &  0.5<1-p_2 \leq\dfrac{p_2+1}{2} \Leftrightarrow \dfrac{1}{3}\leq p_2< 0.5\\
     \dfrac{p_2+1}{2} &  0.5 <\dfrac{p_2+1}{2}<1-p_2 \Leftrightarrow p_2< \dfrac{1}{3}\\
     \end{matrix}\right.$
   * By symmetry, $BR_2(p_1)$ can be derived by switching the place of $p_1,p_2$ above.
   * Thus we can find the only equilibrium of this:(0.5, 0.5)
3. Like the discussion in 1, we can get the balance point $x^*$ for the assumption that everyone will buy : 
   * $v-p_1 - 0.5x^* = v - p_2 - 0.5(1-x^*) \Rightarrow x^* = 0.5 + p_2 - p_1$
   * $BR_1(p_2) = \arg \max_{p_1} p_1 x^* = \{\dfrac{0.5+p_2}{2}\}$
   * $BR_2(p_1) = \arg \max_{p_2} p_2 x^* = \{\dfrac{0.5+p_1}{2}\}$
   * Thus we can find the only equilibrium of this:(0.5, 0.5)
4. Similar to 3, we can get
   * $v-p_1 - \alpha x^* = v - p_2 - \alpha (1-x^*) \Rightarrow x^* = \dfrac{0.5 + p_2 - p_1}{2\alpha}$
   * $BR_1(p_2) = \arg \max_{p_1} p_1 x^* = \{\dfrac{\alpha+p_2}{2}\}$
   * $BR_2(p_1) = \arg \max_{p_2} p_2 x^* = \{\dfrac{\alpha+p_1}{2}\}$
   * Thus we can find the only equilibrium of this:$(\alpha, \alpha)$
   * When $\alpha \to 0$, each of the enterprise will earn 0, which is intuitive for that each of them will lose his advantages for the smaller weight of d, thus a game similar to Betrand is shown.

## 6.5 警察与小偷

1. We call the police as the P1 and the robber as the P2. The choices of p1 are P(patrol), C(Coffee) and the choices of p2 are H(hide) and R(rob), so the matrix of this game is:

   * |      |   H   |    R    |
     | :--: | :---: | :-----: |
     |  P   | 0, 0  | 20, -10 |
     |  C   | 10, 0 | 10, 10  |

2. If each of them plays a  pure strategy, then the best response is : $BR_1(H) = \{C\}, BR_1(R) = \{P\}; BR_2(P) = \{H\}. BR_2(C) = \{R\}$

​	If they are playing mixed strategy, we suppose 

​	$$\sigma_1(P) = p, \sigma_1(C) = 1-p\quad and\quad \sigma_2(H) = q, \sigma_2(R) = 1-q$$

​	$EU_1 = 20p(1-q) + 10(1-p)q + 10(1-p)(1-q) = 10(1-2q)p + 10$

​	$EU_2 = -10p(1-q) + 10(1-p)(1-q) = 10(1-2p)(1-q)$

​	$\max EU_1 \Rightarrow  $ $BR_1(q) = \left\{\begin{matrix}
  1 &  if\quad q <0.5\\
  [0,1]& if\quad q =0.5\\
  0& if \quad q>0.5\\
\end{matrix}\right.$

​	$BR_2(p)$ is similar： $BR_2(p) = \left\{\begin{matrix}
  0 &  if\quad p <0.5\\
  [0,1]& if\quad p =0.5\\
  1& if \quad p>0.5\\
\end{matrix}\right.$

3. We can easily find the interaction of the BRs: $(0.5,0.5)$ is the unique Nash equilibria here. Besides, the best responses here are quite similar with Matching coins game.

## 6.8 市场准入

1. Considering the symmetry in this case, we can merely examine one of the three. $s_1$ is a pure strategy of the first firm and $s_1 \in \{0,1\} ,\quad s_{-1} \in \{0, 1, 2\}$$BR_1(0) = \{1\}, BR_1(1) = \{1\}, BR_1(2) = \{0\}$

   1. Firstly we consider a scenario where only one of the three choose to enter the market: $(0, 0, 1)$. This is not a Nash equilibria for 1 and 2 for they do not use their best response. Similarly (1, 0, 0) and (0, 1, 0) are not nash equilibrium.
   2. Secondly, (1, 1, 0) is a Nash equilibria because everyone is doing his/her best response. Similarly (1, 0, 1) and (0, 1, 1) are nash equilibrium.
   3. Lastly, (1,1,1) is not a Nash equilibria. 

2. Let us suppose $\sigma_1(0) = r, \sigma_1(1) = 1-r$, $\sigma_2(0) = s, \sigma_2(1) = 1-s$, $\sigma_3(0) = t, \sigma_3(1) = 1-t$

   The indifference lemma requires that choosing 0 or 1 will have the same expectation. By symmetry we know $r=s=t := p$  at last.

   $E_0 = 0 = E_1 = -12p^2 + 2\times 13 p(1-p) + 88(1-p)^2 $

   So $r=s=t=p = 0.8$ is the final equilibria. 

   

