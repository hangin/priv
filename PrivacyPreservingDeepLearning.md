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



**Distributed collaborative learning**

The server adds all gradients to the value of the corresponding parameter.

Each participant downloads a subset of the parameters from the server and uses them to update his local model.

The download criterion for a given parameter can be the frequency or recency of updates or the moving average of gradients added to that parameter. 



###### System Architecture

**overview**

We assume that there are N participants, each of which has a local private dataset available for training. 

All participants agree in advance on a common network architecture and common learning objective.

We assume the existence of a parameter server which is responsible for maintaining the latest values of parameters available to all parties. 

**Local training**

DSSGD is run independently by every participant and consists of **ﬁve steps** in each learning epoch:

1. the participant downloads a $\theta_d$ fraction of parameters from the server and overwrites his local parameters with the downloaded values. 
2. He then runs one epoch of SGD training on his local dataset. This training can be done on a sequence of mini-batches.
3. In the third step, the participant computes $\Delta \mathbf w^{(i)}$, the vector of **changes** in all parameters in step 2.
4. We assume that at most $\theta_u$ fraction of parameters can be selected for upload at each epoch. We consider two selection criteria. (1) ***largest values*** (2) ***random with threshold***
5. Before uploading the selected gradients $\Delta \mathbf w^{(i)}$, their values are truncated in to the $[−γ,γ]$ range.

**Parameter server**

When someone uploads gradients, the server adds the uploaded $\Delta \mathbf w_j$ value to the corresponding global parameters and updates the meta-data and the update counter $stat_j $for each parameter j.

To increase the weight of more recently updated parameters, the server can periodically multiply the counter by a decay factor β, i.e., stat := β · stat.

**Why distributed selective SGD works**

Some participants may undergo a higher number of updates, due to better computation and throughput capabilities. Some participants may fail to upload their selected parameters due to network errors or other failures. 

Not only do race conditions not cripple our distributed SSGD, in fact they contribute to its success by increasing stochasticity. 

Stochasticity due to asynchronous parameter update is known to be effective for training accurate deep neural networks.

This is also consistent with regularizing techniques.



**Parameter exchange protocol**

With round robin

With random order, but access to the server is atomic

With asynchronous



###### **Evaluation**



**Privacy**

1. all training data is revealed to a third party .
2. data owners have no control over the learning objective.
3. the learned model is not available directly to data owners.

protect privacy of the training data, ensure public knowledge of the learning objective, and protect privacy of the data to which the learned model is applied, as well as privacy of the model’s output. 

The scenarios we consider: a “passive” adversary model

**Preventing direct leakage**

**Preventing indirect leakage**

Participants may indirectly reveal some information about their training datasets via public updates to a fraction of the neural-network parameters during training.



In our case, f computes parameter gradients and selects which of them to share with other participants. 

There are two sources of potential leakage: how gradients are selected for sharing and the actual values of the shared gradients

To mitigate both types of leakage, we use the **sparse vector technique** to:

1. randomly select a small subset of gradients whose values are above a threshold
2. share perturbed values of the selected gradients



In the following,we assume the same sensitivity $∆f$ for all parameters, but this is not a requirement, and different parameters may have different sensitivities.  ????



**Estimating sensitivity**

Estimating the true sensitivity of stochastic gradient descent is challenging.

Instead,we modify the function so that its output stays within ﬁxed, input-independent bounds and use these bounds to estimate sensitivity. 

We then (over-)estimate the sensitivity of our algorithm as 2γ and truncate the uploaded gradients into the [−γ,γ] range. 

Limiting the range of values that parameters and gradients can take even improves the training process by helping to avoid overﬁtting. 

Therefore, small values of γ (implying smaller sensitivity and thus smaller noise and higher accuracy) would inﬂuence the learning rate of the algorithm but not whether the optimal solution is achievable. 

traverse through local optima. ???





###### MY

Privacy budget per parameter need to be set more than 10 to achieve high accuracy, so the total privacy budget will be extremely large. 

