###### abstract

deep learning

privacy issues

In this paper, we design, implement, and evaluate a practical system that enables multiple parities to jointly learn an accurate neural-network model for a given objective without sharing their input datasets.

stochastic gradient descent can be parallelized and executed asynchronously.



###### Introduction

We design, implement, and evaluate a practical system for collaborative deep learning that offers an attractive tradeoff between utility and privacy.

Our key technical innovation is the selective sharing of model parameters during training. This parameter sharing, interleaved with local parameter updates during stochastic gradient descent, allows participants to beneﬁt from other participants’ models without explicit sharing of training inputs. 

Selective parameter sharing is effective because ...

experiment:  

1. collaborative model (parameter sharing) 
2. centralized, privacy-violating
3. non-collaborative model (learned by participants individually )

Instead of directly revealing all training data, the only leakage in our system is indirect, via a small fraction of neural-network parameters. To minimize even this leakage, we show how to apply differential privacy to parameter updates using the sparse vector technique, thus mitigating privacy loss due to both parameter selection (i.e., choosing which parameters to share) and shared parameter values



###### Related work

 Large scale distributed deep networks. In NIPS, 2012. 

Differential privacy is a popular approach to privacy-preserving machine learning. It has been applied to boosting,principal component analysis, linear and logistic regression, support vector machines, risk minimization, and continuous data processing.

Recent results show that a noisy variant of stochastic gradient descent achieves optimal error for minimizing Lipschitz convex functions over $l$2-bounded sets [4]

randomized “dropout,” used to prevent overﬁtting, cal also strengthen the privacy guarantee in a simple 1-layer neural network



test notes