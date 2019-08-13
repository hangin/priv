#### **Privacy Preserving Deep Learning**

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

 our objective is to collaboratively train a neural network that can be used privately and independently by each participant.

Differential privacy is a popular approach to privacy-preserving machine learning. It has been applied to boosting, principal component analysis, linear and logistic regression, support vector machines, risk minimization, and continuous data processing. 

Noisy variant of stochastic gradient descent achieves optimal error for minimizing Lipschitz convex functions over $l$2-bounded sets 

randomized “dropout,” used to prevent overﬁtting, cal also strengthen the privacy guarantee in a simple 1-layer neural network

Unfortunately, averaging neural-network parameters does not necessarily result in a better model.  ???



###### Deep learning

batch gradient descent

stochastic gradient descent

Note that each parameter in vector w is updated independently from other parameters.

We will rely on this property when designing our system for privacy-preserving, collaborative stochastic gradient descent in the rest of this paper. 



###### Distributed Selective SGD

The core of our approach is a distributed, collaborative deep learning protocol that relies upon the following observations: 

1. updates to different parameters during gradient descent are inherently independent.
2. different training datasets contribute to different parameters
3. different features do not contribute equally to the objective function. 

SSGD achieves comparable accuracy to conventional SGD but involves updating 1 or even 2 orders of magnitude fewer parameters in each learning iteration. 



**Selective parameter update**

Some parameters undergo bigger changes.

In selective SGD, the learner chooses a fraction of parameters to be updated at each iteration. 

This selection can be completely random, but a smart strategy is to select the parameters whose current values are farther away from their local optima, i.e., those that have a larger gradient. 

We refer to the ratio of θ over the total number of parameters as the ***parameter selection rate.*** 

