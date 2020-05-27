**Excercise 2.1 In "-greedy action selection, for the case of two actions and " =0 .5, what is the probability that the greedy action is selected?**

    Answer 2.1

**Excercise 2.2 Bandit example Consider a k-armed bandit problem with k = 4 actions, denoted 1, 2, 3, and 4. Consider applying to this problem a bandit algorithm using "-greedy action selection, sample-average action-value estimates, and initial estimates of Q1(a) = 0, for all a. Suppose the initial sequence of actions and rewards is A1 = 1, R1 =1, A2 = 2, R2 = 1, A3 = 2, R3 =2, A4 = 2, R4 = 2, A5 = 3, R5 = 0. On some of these time steps the " case may have occurred, causing an action to be selected at random. On which time steps did this deﬁnitely occur? On which time steps could this possibly have occurred?**

   Answer 2.1

**Excercise 2.3 In the comparison shown in Figure 2.2, which method will perform best in the long run in terms of cumulative reward and probability of selecting the best action? How much better will it be? Express your answer quantitatively.**

    Answer 2.3

**Excercise 2.4 If the step-size parameters, ↵n, are not constant, then the estimate Qn is a weighted average of previously received rewards with a weighting di↵erent from that given by (2.6). What is the weighting on each prior reward for the general case, analogous to (2.6), in terms of the sequence of step-size parameters?**

    Answer 2.4

**Exercise 2.5 (programming) Design and conduct an experiment to demonstrate the diculties that sample-average methods have for nonstationary problems. Use a modified version of the 10-armed testbed in which all the q⇤(a) start out equal and then take independent random walks (say by adding a normally distributed increment with mean 0 and standard deviation 0.01 to all the q\*(a) on each step). Prepare plots like Figure 2.2 for an action-value method using sample averages, incrementally computed, and another action-value  ethod using a constant step-size parameter, ↵ = 0.1. Use " = 0.1 and
longer runs, say of 10,000 steps.**

    Answer 2.5

**Exercise 2.6: Mysterious Spikes The results shown in Figure 2.3 should be quite reliable because they are averages over 2000 individual, randomly chosen 10-armed bandit tasks.Why, then, are there oscillations and spikes in the early part of the curve for the optimisticmethod? In other words, what might make this method perform particularly better orworse, on average, on particular early steps?**

    Answer 2.6

**Exercise 2.7: Unbiased Constant-Step-Size Trick In most of this chapter we have usedsample averages to estimate action values because sample averages do not produce theinitial bias that constant step sizes do (see the analysis leading to (2.6)). However, sampleaverages are not a completely satisfactory solution because they may perform poorlyon nonstationary problems. Is it possible to avoid the bias of constant step sizes whileretaining their advantages on nonstationary problems? One way is to use a step size of**

$\beta$ n.= $\alpha$/$\bar(o)$n,            (2.8)

**to process the nth reward for a particular action, where $\alpha$ > 0 is a conventional constantstep size, and ¯on is a trace of one that starts at 0:**

$\bar(o)$<sub>n</sub>:= $\bar(o)$<sub>n-1</sub> + $\alpha$(1 - $\bar(o)$<sub>n-1</sub>), for n $\ge$ 0, with $\bar(o)$<sub>0</sub> = 0. (2.9)

**Carry out an analysis like that in (2.6) to show that Qn is an exponential recency-weightedaverage without initial bias.**

    Answer 2.7

