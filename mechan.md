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



| HR    | 111          | 010          | 100          | 001          |
| ----- | ------------ | ------------ | ------------ | ------------ |
| $x_1$ | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            |
| $x_2$ | $e^\epsilon$ | $e^\epsilon$ | 1            | 1            |
| $x_3$ | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ |



| SH(BLH) | $<H_1,+1>$   | $<H_1,-1>$   | $<H_2,+1>$   | $<H_2,-1>$   | ...  | $<H_m,+1>$   | $<H_m,-1>$   |
| ------- | ------------ | ------------ | ------------ | ------------ | ---- | ------------ | ------------ |
| $x_1$   | $e^\epsilon$ | 1            | 1            | $e^\epsilon$ |      | 1            | $e^\epsilon$ |
| $x_2$   | $e^\epsilon$ | 1            | $e^\epsilon$ | 1            |      | 1            | $e^\epsilon$ |
| ...     |              |              |              |              |      |              |              |
| $x_d$   | 1            | $e^\epsilon$ | 1            | $e^\epsilon$ |      | $e^\epsilon$ | 1            |



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





**Error**

KRR:

$q_i=Cp_i+D$

=> $p_i=Aq_i+B$

$\hat q_i=c(y_i)/n$

$\hat p_i=A \hat q_i + B$

$E(\hat q_i)=q_i$ (Since $c(y_i)$ is Bernoulli(n, $q_i$).)

=>$E(\hat p_i)=p_i$

$E(l_2^2(\hat p,p))=$$\sum Var(p_i)=A^2\sum Var(q_i)=\frac{A^2}{n^2}\sum Var(c(y_i))= \frac{A^2}{n}\sum q_i(1-q_i)$





K-subset:

