# Game Theory HW04

## Harassment

1. 

   * Strategy space: $S_i = \{R, K\},\forall i = 1,2,\ldots, n$

   * Players set: $\{1,2,\ldots, n\}$

   * Payoff: 

     * $v_i(R, s_{-i}) = 1-c$

     * $v_i(K, s_{-i})= \begin{cases}
        0 & \text{ if } s_{-i} = (K,K,\ldots, K)\\
        1 & \text{ }else
       \end{cases}$

2. 

   * Firstly, $(K,K,\ldots, K)$ is not a NE for everyone gets a payoff at 0 now, but they can get better off by choosing R because :$v_i(R, s_{-i}) = 1-c >0$
   * Secondly, an S with more than 1 R cannot be a NE for that keeping others still, the one who choose R can get better off by choosing K, from which he/she can get a payoff 1 rather than 1-c.
   * Finally, we only get S with only 1 R and this is the exact NE because the one choosing R will not choose K. If he/she turns to K, then he/she will get 0 instead of 1-c.
   * So, $(R,K,\ldots, K), (K,R,K,\ldots, K),\cdots, (K,K,\ldots, K, R)$ are  all NE. There are n NE in total.

3. We suppose that everyone mixes with a same p to report, then we can derive with the indifferent condition that 

   $$(1-p)^{n-1}\times0 + 1-(1-p)^{n-1}=1-c$$

$$\Rightarrow p^* = 1-c^{\frac{1}{n-1}}$$

​	We should verify that this is an NE. By symmetry, we only should confirm that $v_1(\sigma^*,\sigma^*,\ldots, \sigma^* ) \geq v_1(s,\sigma^*,\ldots, \sigma^* ), \forall s \in S_1$

​	$v_1(\sigma^*,\sigma^*,\ldots, \sigma^* ) = p^*(1-c) + (1-p^*)(1-(1-p^*)^{n-1}) = 1-cp^* - (1-p^*)^n$

$v_1(R,\sigma^*,\ldots, \sigma^* ) = 1-c$  and  $v_1(K,\sigma^*,\ldots, \sigma^* ) = 1-(1-p^*)^{n-1} = 1- c$

$v_1(\sigma^*,\sigma^*,\ldots, \sigma^* ) \geq v_1(R,\sigma^*,\ldots, \sigma^* ) \Leftrightarrow c \geq (1-p^*)^{n-1} = c$

$v_1(\sigma^*,\sigma^*,\ldots, \sigma^* ) \geq v_1(K,\sigma^*,\ldots, \sigma^* ) \Leftrightarrow c \geq (1-p^*)^{n-1} = c$















## 离散式全支付拍卖

1. |      | 0        | 1        | 2         |
   | ---- | -------- | -------- | --------- |
   | 0    | 1.5，2.5 | 0，4     | 0，3      |
   | 1    | 2，0     | 0.5，1.5 | -1，3     |
   | 2    | 1，0     | 1，-1    | -0.5，0.5 |

* For player 2, choosing 2 dominates choosing 0; 

* |      | 1        | 2         |
  | ---- | -------- | --------- |
  | 0    | 0，4     | 0，3      |
  | 1    | 0.5，1.5 | -1，3     |
  | 2    | 1，-1    | -0.5，0.5 |

* For player 1, choosing 2 dominates choosing 1;

* |      | 1     | 2         |
  | ---- | ----- | --------- |
  | 0    | 0，4  | 0，3      |
  | 2    | 1，-1 | -0.5，0.5 |

2. We can tell that in the reduced game, there is not a pure strategy NE.

* Consider that player 1 choose 0 at probability p and player 2 choose 1 at q.
* Indifferent condition: 
  * $q\times (-1) +(1-q)\times 0.5 = 0 \Rightarrow q = \dfrac{1}{3} $
  * $4p-(1-p) = 3p + 0.5(1-p) \Rightarrow p = \dfrac{3}{5}$
* （既然nash均衡存在，那么根据必要条件推出的唯一条件就决定了这个nash均衡吗？）
* So NE is $(\dfrac{3}{5} \circ 0 + \dfrac{2}{5}\circ2, \dfrac{1}{3}\circ 1 + \dfrac{2}{3}\circ 2)$

​	



