###### **Mechanism**

| k-RR  | $y_1=\{x_1\}$ | $y_2=\{x_2\}$ | $y_3=\{x_3\}$ | $y_4=\{x_4\}$ |
| ----- | ------------- | ------------- | ------------- | ------------- |
| $x_1$ | $e^\epsilon$  | 1             | 1             | 1             |
| $x_2$ | 1             | $e^\epsilon$  | 1             | 1             |
| $x_3$ | 1             | 1             | $e^\epsilon$  | 1             |
| $x_4$ | 1             | 1             | 1             | $e^\epsilon$  |





| K-RAP      | 000            | 001                       | 010                       | 011            | 100                       | 101            | 110            | 111                      |
| ---------- | -------------- | ------------------------- | ------------------------- | -------------- | ------------------------- | -------------- | -------------- | ------------------------ |
| $x_1(100)$ | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$  | $e^{\frac{\epsilon}{2}}$  | 1              | $e^{\frac{3\epsilon}{2}}$ | $e^{\epsilon}$ | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$ |
| $x_2(010)$ | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$  | $e^{\frac{3\epsilon}{2}}$ | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$  | 1              | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$ |
| $x_3(001)$ | $e^{\epsilon}$ | $e^{\frac{3\epsilon}{2}}$ | $e^{\frac{\epsilon}{2}}$  | $e^{\epsilon}$ | $e^{\frac{\epsilon}{2}}$  | $e^{\epsilon}$ | 1              | $e^{\frac{\epsilon}{2}}$ |



| OUE  | 000             | 001             | 010             | 011            | 100             | 101            | 110            | 111  |
| ---- | --------------- | --------------- | --------------- | -------------- | --------------- | -------------- | -------------- | ---- |
| 100  | $e^{2\epsilon}$ | $e^{\epsilon}$  | $e^{\epsilon}$  | 1              | $e^{2\epsilon}$ | $e^{\epsilon}$ | $e^{\epsilon}$ | 1    |
| 010  | $e^{2\epsilon}$ | $e^{\epsilon}$  | $e^{2\epsilon}$ | $e^{\epsilon}$ | $e^{\epsilon}$  | 1              | $e^{\epsilon}$ | 1    |
| 001  | $e^{2\epsilon}$ | $e^{2\epsilon}$ | $e^{\epsilon}$  | $e^{\epsilon}$ | $e^{\epsilon}$  | $e^{\epsilon}$ | 1              | 1    |

 

| 1/2  | 000  | 001            | 010            | 011            | 100            | 101            | 110            | 111            |
| ---- | ---- | -------------- | -------------- | -------------- | -------------- | -------------- | -------------- | -------------- |
| 100  | 1    | 1              | 1              | 1              | $e^{\epsilon}$ | $e^{\epsilon}$ | $e^{\epsilon}$ | $e^{\epsilon}$ |
| 010  | 1    | 1              | $e^{\epsilon}$ | $e^{\epsilon}$ | 1              | 1              | $e^{\epsilon}$ | $e^{\epsilon}$ |
| 001  | 1    | $e^{\epsilon}$ | 1              | $e^{\epsilon}$ | 1              | $e^{\epsilon}$ | 1              | $e^{\epsilon}$ |



| k-subset | 1100         | 1010         | 1001         | 0110         | 0101         | 0011         |
| -------- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| $x_1$    | $e^\epsilon$ | $e^\epsilon$ | $e^\epsilon$ | 1            | 1            | 1            |
| $x_2$    | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ | $e^\epsilon$ | 1            |
| $x_3$    | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ |
| $x_4$    | 1            | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ | $e^\epsilon$ |



| HR                     | 111          | 010          | 100          | 001          |
| ---------------------- | ------------ | ------------ | ------------ | ------------ |
| $x_1: C_1=\{y_1,y_3\}$ | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            |
| $x_2 :C_2=\{y_1,y_2\}$ | $e^\epsilon$ | $e^\epsilon$ | 1            | 1            |
| $x_3:C_3=\{y_1,y_4\}$  | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ |



| SH(BLH) | $<H_1,+1>$   | $<H_1,-1>$   | $<H_2,+1>$   | $<H_2,-1>$   | ...  | $<H_m,+1>$   | $<H_m,-1>$   |
| ------- | ------------ | ------------ | ------------ | ------------ | ---- | ------------ | ------------ |
| $x_1$   | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ |      | 1            | $e^\epsilon$ |
| $x_2$   | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            |      | 1            | $e^\epsilon$ |
| ...     |              |              |              |              |      |              |              |
| $x_d$   | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ |      | $e^\epsilon$ | 1            |



**OLH**



| 1/2   | $+++$        | $++-$        | $+-+$        | $-++$        | $+--$        | $-+-$        | $--+$        | $---$ |
| ----- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ----- |
| $x_1$ | $e^\epsilon$ | $e^\epsilon$ | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            | 1            | 1     |
| $x_2$ | $e^\epsilon$ | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            | 1     |
| $x_3$ | $e^\epsilon$ | 1            | $e^\epsilon$ | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ | 1     |



| PS+GRR | 1              | 2              | 3              | 4    |
| ------ | -------------- | -------------- | -------------- | ---- |
| {1,2}  | $e^\epsilon+1$ | $e^\epsilon+1$ | 2              | 2    |
| {1,3}  | $e^\epsilon+1$ | 2              | $e^\epsilon+1$ | 2    |
|        |                |                |                |      |



**PS+RAP**



**PS+SH**





**EH(public randomness)**





###### **Error Analysis**



**Note:**

all $\hat q_i$ is an empirical frequency estimator ?

the difference is value $A, q_i$ 

all are pure LDP, and how to construct a pure LDP meachnism? efficiently

pure LDP => Bernoulli(n, $p_i$)                           

How to aggregate in pure LDP without using the pure property?

Is the aggregation with pure property achieve optimal error?

How to aggregate in non-pure LDP mechanism？

Can non-pure LDP achieve optimal error?



URR:

pure LDP: $q_i=p^**p_i+q^**(1-p_i)$

$q_i=Ep_i+F(1-p_i)$   (this property is pure LDP in UP17) 

=> $q_i=Cp_i+D$

=> $p_i=Aq_i+B$

$\hat q_i=c_i(y^n)/n$            where $c_i(y^n)=\sum_{j\in[n]} I(y_j[i]=1)$)

$\hat p_i=A \hat q_i + B$

$E(\hat q_i)=q_i$ (Since $c(y_i)$ ~ Bernoulli(n, $q_i$).)

=>$E(\hat p_i)=p_i$

$E(l_2^2(\hat p,p))=$$\sum Var(p_i)=A^2\sum Var(q_i)=\frac{A^2}{n^2}\sum Var(c(y_i))= \frac{A^2}{n}\sum q_i(1-q_i)$



KRR:

$P(y_i)=q_i=p_i*\frac{e^\epsilon}{e^\epsilon+d-1}+(1-p_i)*\frac{1}{e^\epsilon+d-1}$

=>$q_i=p_i*\frac{e^\epsilon-1}{e^\epsilon+d-1}+\frac{1}{e^\epsilon+d-1}$

$q_i=Ep_i+F(1-p_i)$   (this property)

=> $q_i=Cp_i+D$

=> $p_i=Aq_i+B$

$\hat q_i=c_i(y^n)/n$            where $c_i(y^n)=\sum_{j\in[n]} I(y_j[i]=1)$)

$\hat p_i=A \hat q_i + B$

$E(\hat q_i)=q_i$ (Since $c(y_i)$ ~ Bernoulli(n, $q_i$).)

=>$E(\hat p_i)=p_i$

$E(l_2^2(\hat p,p))=$$\sum Var(p_i)=A^2\sum Var(q_i)=\frac{A^2}{n^2}\sum Var(c(y_i))= \frac{A^2}{n}\sum q_i(1-q_i)$

$=\frac{A^2}{n}\sum [Cp_i+D-（CP_i+D)^2]=\frac{A^2}{n}(C+Dd-\sum(Cp_i+D)^2)$

$=\frac{C-2CD+Dd+D^2d}{C^2n}-\frac{\sum p_i^2}{n}$



K-subset:

$q_i=Ep_i+F(1-p_i)$    (this property)

=> $q_i=Cp_i+D$

=> $p_i=Aq_i+B$

$\hat q_i=c_i(y_i)/n$             where $c_i(y^n)=\sum_{j\in[n]}I(y_j[i]=1)$

$\hat p_i=A \hat q_i + B$

$E(\hat q_i)=q_i$ (Since $c(y_i)$ ~ Bernoulli(n, $q_i$).)

=>$E(\hat p_i)=p_i$

$E(l_2^2(\hat p,p))=$$\sum Var(p_i)=A^2\sum Var(q_i)=\frac{A^2}{n^2}\sum Var(c(y_i))= \frac{A^2}{n}\sum q_i(1-q_i)$



HR:

$p(C_i)=q_i=\frac{e^\epsilon -1}{2(e^\epsilon+1)}p_i+\frac{1}{2}$



$q_i=Ep_i+F(1-p_i)$    (this property)

=> $q_i=Cp_i+D$

=> $p_i=Aq_i+B$

$\hat q_i=c_i(y_i)/n$             where $c_i(y^n)=\sum_{j\in[n]}I(y_j[i]=1)$

$\hat p_i=A \hat q_i + B$

$E(\hat q_i)=q_i$ (Since $c(y_i)$ ~ Bernoulli(n, $q_i$).)

=>$E(\hat p_i)=p_i$

$E(l_2^2(\hat p,p))=$$\sum Var(p_i)=A^2\sum Var(q_i)=\frac{A^2}{n^2}\sum Var(c(y_i))= \frac{A^2}{n}\sum q_i(1-q_i)$









|       | $l_2^2$ risk                                                 | $l_1$ risk |
| ----- | ------------------------------------------------------------ | ---------- |
| k-RR  | $=\frac{k-1}{n}(\frac{2（e^\epsilon-1)+k}{(e^\epsilon-1)^2})+\frac{1-\sum_{i=1}^kp_i^2}{n}$ |            |
| k-SS  | $<\frac{4ke^\epsilon}{n(e^\epsilon-1)^2}(1+\frac{2e^\epsilon+3}{4k})$ |            |
| HR    | $<\frac{4k}{n}\cdot\frac{(e^\epsilon+1)^2}{(e^\epsilon -1)^2}$ |            |
| k-RAP | $=\frac{ke^{\epsilon/2}}{n(e^{\epsilon/2}-1)^2}+\frac{1-\sum_{i=1}^kp_i^2}{n}$ |            |





| $1<<e^\epsilon<<k$ (median) | $l_2^2$ risk                         | $l_1$ risk                                  |
| --------------------------- | ------------------------------------ | ------------------------------------------- |
| k-RR                        | $\Theta(\frac{k^2}{ne^{2\epsilon}})$ | $\Theta(\frac{k^{3/2}}{\sqrt ne^\epsilon})$ |
| k-SS                        | $\Theta(\frac{k}{ne^\epsilon})$      | $\Theta(\frac{k}{\sqrt{ne^\epsilon}})$      |
| HR                          |                                      |                                             |
| k-RAP                       |                                      |                                             |





###### **bound of minimax risk**

for $\epsilon\in[0,1]$ in 

[Local privacy,data processing inequalities, and statistical minimax rates.]

[Minimax optimal procedures for locally private estimation]

a tight lower bound in 

[Optimal Schemes for Discrete Distribution Estimation under Locally Differential Privacy]

for $\epsilon<ln3:$ 

for $\epsilon>=ln3:$

