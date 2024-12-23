# Game Theory HW05

<center>2100010850 娄峻赫

## 7.2 策略和均衡

1. The extensive form can be shown by:

   <img src="/Users/curve/Library/Application Support/typora-user-images/截屏2023-10-21 18.01.39.png" alt="截屏2023-10-21 18.01.39" style="zoom:33%;" />

   This is a game of perfect information, because every information set is a singleton.

2. There are 4 terminal nodes and 3 information sets.

3. For player 1: $|\{A,B\}\times\{E,F\}| = 4$, there are 4 pure strategies.

   For player 2: there are only 2 pure strategies: $\{C\},\{D\}$

4. |      |  C   |  D   |
   | :--: | :--: | :--: |
   |  AE  | 2,0  | 2,0  |
   |  AF  | 2,0  | 2,0  |
   |  BE  | 3,1  | 0,0  |
   |  BF  | 3,1  | 1,2  |

* From the normal form we can easily find NEs:$ (BE, C), (AE,D),(AF,D)$

* Mixed Strategies:

  *  Given 2 chooses C for sure, 1 will only mix between BE and BF. For 2, he/she has no intencive to choose D only when: $\sigma_1(BE) + 1 -\sigma_1(BE) > 2(1-\sigma_1(BE)) \Rightarrow \sigma_1(BE) > 0.5$

  * ​	So $(\sigma_1(BE) \circ BE + (1-\sigma_1(BE))\circ BF, C)$ , $\sigma_1(BE) > 0.5$ is an NE .
  * Given 2 chooses D for sure, 1 will only mix between AE and AF. For 2, he/she has no intencive to choose C. So $(\sigma_1(AE) \circ AE + (1-\sigma_1(AE))\circ AF, D)$  is an NE
  * Given 2 mixes between C and D, for 1, BF strictly dominates BE so that BE will not be mixed. If 1 mix BF, then choosing D is apparently different with choosing C for 2 so 2 will not mix. So 1 will only mix between AE and AF. To assure that 1 will not deviate, 
  * $$2 \geq 3\sigma_2(C)$$, 
  * $$2 \geq 3\sigma_2(C) + (1-\sigma_2(C))$$
  * $$\Rightarrow \sigma_2(C) \leq 0.5$$
  * So $(\sigma_1(AE) \circ AE + (1-\sigma_1(AE))\circ AF, \sigma_2(C)\circ C + (1-\sigma_2(C))\circ D)$  , $\sigma_2(C) \leq 0.5$ is an NE.
  * $(AF,D)$ is the most appealing NE because it survives the backward induction, thus it is the most reasonable NE.
  
  

## 7.3 一字棋

1. This is a game of perfect information for that everyone know what has happened before exactly
2. There are 18 information sets because player 1 can have 9 different choices after choosing O or X.
3. There are $18\times 8 = 144$ information sets because player 2 has 8 different choices after 1 chooses.
4. For player1, there are 1 + 18 × 8 + 18 × 8 × 7 × 6 + 18 × 8 × 7 × 6 × 5 × 4 + 18 ×8 × 7 × 6 × 5 × 4 × 3 × 2 = 852913 information sets. For player 2, there are 18 + 18 × 8 × 7 + 18 × 8 × 7 × 6 × 5 + 18 × 8 × 7 × 6 × 5 × 4 × 3 = 394146 information sets.
5. There are 18×8! = 725760 terminal nodes.

## 7.5 否决权

1. Let us denote $v_1(a) = v_2(c) = 3, v_1(b) = v_2(b) = 2, v_1(c) = v_2(a) = 1$

<img src="/Users/curve/Library/Application Support/typora-user-images/截屏2023-10-21 18.01.22.png" alt="截屏2023-10-21 18.01.22" style="zoom:25%;" />

1. 1 has 3 pure strategies : $\{a, b,c\}$ and 2 has $|\{b,c\}\times\{a,c\}\times\{b,a\}| = 8$ pure strategies.
2. Considering that we can not find mixed NEs for that we do not have the precise utility function, we only discuss pure strategy NEs here:
   * $BR_1(s_2) = \begin{cases}
      b & \text{ if } s_2\in \{bab, cab\} \\
      c & \text{ if } s_2\in\{bca,cca,ccb\}\\
      \{a,c\} & \text{ if } s_2= bcb\\
       \{b, c\}& \text{ if } s_2\in\{baa,caa\}
     \end{cases}$
   * $BR_2(s_1) = \begin{cases}
      \{cca,ccb,caa,cab\} & \text{ if } s_1=a \\
      \{bca,bcb,cca,ccb\} & \text{ if } s_1= b\\
       \{bcb, bab,ccb,cab\}& \text{ if } s_1=c
     \end{cases}$
   * So NEs are $(c,bcb), (c,ccb)$

## 7.8 兄弟

1. We denote giving 20 as A(All) and giving 10 as P(Partly)

<img src="/Users/curve/Library/Application Support/typora-user-images/截屏2023-10-21 18.00.34.png" alt="截屏2023-10-21 18.00.34" style="zoom:33%;" />

2. For 1: $\{OO,OF,FO,FF\}$

   For 2: $\{AOO,AOF,AFO,AFF,POO,POF,PFO,PFF\}$

3. 

4. |      |  AOO  |  AOF  |  AFO  |  AFF  |  POO  |  POF  |  PFO  |  PFF  |
   | :--: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
   |  OO  | 36,12 | 36,12 | 20,0  | 20,0  | 26,22 | 10,10 | 26,22 | 10,10 |
   |  OF  | 36,12 | 36,12 | 20,0  | 20,0  | 10,10 | 22,26 | 10,10 | 22,26 |
   |  FO  | 20,0  | 20,0  | 32,16 | 32,16 | 26,22 | 10,10 | 26,22 | 10,10 |
   |  FF  | 20,0  | 20,0  | 32,16 | 32,16 | 10,10 | 22,26 | 10,10 | 22,26 |

   We can consider pure strategy as a special type of mixed strategy with a p at 1. So we can easily tell that every pure strategy in the form of “Axx”is strictly dominated by $(0.501\circ POO + 0.499\circ POF)$，so we can solve this problem without thinking 2 choosing A.

   Now the problem is:

   |      |  PO   |  PF   |
   | :--: | :---: | :---: |
   |  O   | 26,22 | 10,10 |
   |  F   | 10,10 | 22,26 |

   Pure strategies NEs are: $(O,PO), (F,PF)$

   Consider 2 mix PO with p and 1 mix O with q, so we have:

   $26p + 10(1-p)  = 10p + 22(1-p) \Rightarrow p = \dfrac{3}{7}$

   $22q + 10(1-q) = 10q + 26(1-q) \Rightarrow q = \dfrac47$

   So back to the original game, we have NEs:

   $(p\circ OO + (1-p)\circ FO, q\circ PFO + (1-q)\circ POO) \cup (p\circ OF + (1-p)\circ FF, q\circ POF + (1-q)\circ PFF) \cup $

   $(c\circ OO + (\dfrac47 - c)\circ FO+ d\circ OF + (\dfrac37-d)\circ FF,a\circ POO+(\dfrac37-a)\circ PFO +b\circ POF + (\dfrac47-b)\circ PFF  ), \forall a,d \in [0,\dfrac37], b,c\in [0,\dfrac47],p,q\in [0,1]$

   

## 7.9 教务长的困境

1. The game tree is:

<img src="/Users/curve/Library/Application Support/typora-user-images/截屏2023-10-21 18.00.13.png" alt="截屏2023-10-21 18.00.13" style="zoom:30%;" />

2. Normal form game is:

​	

|      | C    | D    |
| ---- | ---- | ---- |
| AA   | 2,-2 | 0,0  |
| AB   | 1,-1 | 2,-2 |
| BA   | 1,-1 | -2,2 |
| BB   | 0,0  | 0,0  |

3. We first examine the pure strategies: None

​	  Then we assume 2 mixs C with p and we discuss strategies of 1.

* BB is strictly dominated by AB and BA is strictly dominated by $(0.5\circ AA + 0.5 \circ AB)$, so we can discuss choices of 1 without thinking BA and BB.
* Now we assume 1 mix AA with q, so we have:
* $2p + 0 = p + 2(1-p) \Rightarrow p = \dfrac23$
* $-2q-(1-q) = -2(1-q) \Rightarrow q = \dfrac13$
* As the theorum tells us, there exists an NE, so the only NE is $(\dfrac13◦AA+ \dfrac23◦AB, \dfrac23◦C + \dfrac13 ◦D)$

## Find all NE

Consider the following normal form representation of the centipede game we covered in class. Find all Nash equilibria.

<img src="/Users/curve/Library/Application Support/typora-user-images/截屏2023-10-18 19.55.16.png" alt="截屏2023-10-18 19.55.16" style="zoom:50%;" />

1. 4 pure strategy NE are : 

   $(NN, nn), (NN,nc), (NC,nn), (NC, nc)$

2. Consider the mixed NE:

   * We can tell that: If $(p\circ NN+(1-p)\circ NC, \sigma_1 \circ nn+\sigma_2 \circ nc+\sigma_3 \circ cn+\sigma_4 \circ cc)$ is an NE, then 1 has no intention to deviate only when $1 \geq 2(\sigma_3 + \sigma_4)$ and $1\geq \sigma_3 + 3\sigma_4$ 
     * So $(p\circ NN+(1-p)\circ NC, \sigma_1 \circ nn+\sigma_2 \circ nc+\sigma_3 \circ cn+\sigma_4 \circ cc)$ $\forall p \in (0,1), (\sigma_1,\sigma_2,\sigma_3,\sigma_4) \in \{[0,1]^4|\sum \sigma_i = 1, \sigma_3+\sigma_4 \leq 0.5, \sigma_3 + 3\sigma_4 \leq 1\}$ are mixed NEs.
     
   * for that each pure stategy of this mixed strategy is the best response for the action of the other player(as shown in pure strategies)
   
   * Then we try to show the rest mixed strategies do not satisfy the indifferent condition.
   
   1. If 1 mixes 4 strategies, which means each strategy has got a positive possibility, then 2 will not choose cn or cc beacuse there exists no possibility of 1 to make the choices between cn and cc are indifferent. So:
      1. 2 will not use pure strategy because 1 will use his best responce of that pure strategy, which violates the assumption.（The same is true in other cases.） 
      2. If 2 only mixes nn and nc,  there exists no possibility of 1 to make the choices between NN or NC and CN or CC are indifferent.
      3. If 2 only mixes cn and cc, CC will not be chosen by 1 because there exists no possibility of 1 to make the choices between NN/NC and CC are indifferent.
      4. If 2 mixes between $\{nn,nc\}$ and $ \{cn,cc\}$, CN and CC must be different for their payoff vary between $(0,2)$ against $(0,1)$, or $(0,2)$ against $(0,3)$
   2. If 1 mixes 3 strategies 
      1. If 1 mixes NN, NC, CN: $\{nn,nc\}$ and $ \{cn,cc\}$ are different to 2, so 2 only can mixes between one set of the  two. Whether 2 choose which of the two, CN and NN/NC are apparently different.(2.1)
      2. If 1 mixes NN, NC, CC:  for 2, only cn is the best response given that $\sigma_1(CC) > 0$ .(2.2)
      3. If 1 mixes NN/NC, CN, CC: for 2, cc is different for there exists no possibility of 1 to make cc to have the same payoff with other strategies. Now, however 2 mix between nn, nc, cc, CC will be different from NN/NC
   3. If 1 mixes 2 strategies: 
      1. If 1 mixes NN/NC with CN: the same with (2.1)
      2. If 1 mixes NN/NC with CC: the same with (2.2)
      3. If 1 mixes CN with CC: for 2, cc is different.Now, however 2 mix between nn, nc, cc, CN will be different from CC. 

