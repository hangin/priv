Locally Differentially Private Frequent Itemset Mining



###### Abstract

The basic LDP frequent oracle (**FO**) protocol enables an aggregator to estimate the frequency of any value. 

But when each user has a set of values, one needs an additional padding and sampling step to ﬁnd the frequent values and estimate their frequencies. 

In this paper, we formally deﬁne such padding and sample based frequency oracles (PSFO). 

As a result, we propose SVIM, a protocol for ﬁnding frequent items in the set-valued LDP setting. 

With SVIM to ﬁnd frequent items, we propose SVSM to effectively ﬁnd frequent itemsets.



###### Introduction

Existing research has developed multiple **frequency oracle** (FO) protocols.

This problem is challenging because the number of items each user has is different. To deal with this, a core technique is “**padding and sampling**”.

We observe that, since the sampling step randomly selects an item, it has an **privacy ampliﬁcation** effect.

Surprisingly, in our study of **padding-and-sampling-based frequency oracle** (PSFO), we found that one cannot always get this privacy ampliﬁcation effect. 

Whether this beneﬁt is applicable or not depends on the internal structure of the FO protocol.

the three best performing FO protocols are Generalized Random Response, Optimized Unary Encoding, and Optimized Local Hash. 

 It was found that Generalized Random Response offers the best accuracy when $|D| < 3e^{\epsilon}+2$, and Optimized Local Hash offers the best accuracy when $|D|≥3e^\epsilon +2$ . 

We found that, the privacy ampliﬁcation effect exists for Generalized Random Response, but not for Optimized Local Hash.

The difference in the ability to beneﬁt from sampling changes the criterion to decide which of Generalized Random Response and Optimized Local Hash to use.

We thus propose to adaptively select the best FO protocol in PSFO.

Essentially, each user pads her itemset to size $l$, generating **two sources of errors**.

1. When $l$ is small, one would underestimate the frequency counts.
2. since $l$ is multiplied to a noisy estimate, increasing $l$ magniﬁes the noises.

We observe that for the purpose of identifying candidates for the frequent items, setting $l=1$ is ﬁne.  

However, when the goal is to estimate frequency, selecting $l$ is a trade-off between under-estimation and noise. 

Following these insights, we propose Set-Value Item Mining (SVIM) protocol.

There are four steps: 

1. users use PSFO with a small $l$ to report; the aggregator identiﬁes frequent items as candidates, and sends this set to users.
2. users report (using a standard FO protocol) the number of candidate items they have; the aggregator estimates the distribution of how many candidate items the users have and selects appropriate $l$, and sends $l$ to users. 
3. users use PSFO with the given  to report occurrences of items in the candidate set; the aggregator estimates the frequency of these items.
4. the aggregator selects the top k frequent items and use the size distribution in step two to further correct undercounts.

 Frequent itemset mining (FIM) is a well recognized data-mining problem.

we are able to provide the ﬁrst solution to FIM in the LDP setting. We call the protocol Set-Value itemSet Mining (SVSM) protocol.



######  Background

**FO:**

***Generalized Randomized Response (GRR):***

Variance

***Optimized Local Hashing (OLH)*** :

it is found that the optimal (minimal variance) choice of g is $\lceil e^\epsilon+1\rceil$.

Variance



Encoding each transaction as a single value in the domain $D = \mathcal P(I)$ (i.e., $D$ is the power set of $I$), and using existing FO protocols does not work. 



**The LDPMiner** 

Phase 1: Candidate Set Identiﬁcation

Phase 2: Frequency Estimation.



###### PADDING-AND-SAMPLING-BASED FREQUENCY ORACLES 

Deﬁnition 2 (PS).

Deﬁnition 3 (PSFO). 

Using this notation,the two phases of LDPMiner can be cast as using $PSFO(L,FO,\epsilon/2)$ in Phase 1 and $PSFO(2k,FO,\epsilon/2)$ in Phase 2.



**Privacy Ampliﬁcation of GRR**

**No Privacy Ampliﬁcation of other FO**

**Utility of PSFO** 

**Adaptive FO** 

**Choosing $l$**

