# [Exercises](../Exercises/README.md): Chapter-3

3.1 **Devise three example tasks of your own that fit into the MDP framework, identifying for each its states, actions, and rewards. Make the three examples as di↵erent from each other as possible. The framework is abstract and flexible and can be applied in many di↵erent ways. Stretch its limits in some way in at least one of your examples.**

    Answer 3.1

3.2 **Is the MDP framework adequate to usefully represent all goal-directed learning tasks? Can you think of any clear exceptions?**

    Answer 3.2

3.3 **Consider the problem of driving. You could define the actions in terms of the accelerator, steering wheel, and brake, that is, where your body meets the machine. Or you could define them farther out—say, where the rubber meets the road, considering your actions to be tire torques. Or you could define them farther in—say, where your brain meets your body, the actions being muscle twitches to control your limbs. Or you could go to a really high level and say that your actions are your choices of where to drive. What is the right level, the right place to draw the line between agent and environment? On what basis is one location of the line to be preferred over another? Is there any fundamental reason for preferring one location over another, or is it a free choice?**

    Answer 3.3

3.4 **Give a table analogous to that in Example 3.3, but for p(s', r|s, a). It should have columns for s, a, s', r, and p(s', r|s, a), and a row for every 4-tuple for which p(s', r|s, a) > 0.**

    R = {R_search, R_wait, R_recharge, R_rescue:-3, R_0:0S}

|s|a|s'|r|p(s',r/s,a)|
|-|-|-|-|-|
|high|search|high|R_search|alpha*1|
|high|search|high|R_wait|0|
|high|search|high|R_recharge|0|
|high|search|high|R_rescue|0|
|high|search|high|R_0|0|
|-|-|-|-|-|
|high|search|high|R_search|alpha*1|
|high|search|low|R_search|(1-alpha)*1|
|low|search|high|R_rescue|(1-beta)*1|
|low|search|low|R_search|beta*1|
|high|wait|high|R_wait|1|
|low|wait|low|R_wait|1|
|low|recharge|high|R_0|1|
----

    basically, p(s',r/s,a) = p(s'/s,a) because there is only 1 type of reward possible for given (s,a,s') pair.


3.5 **The equations in Section 3.1 are for the continuing case and need to be modified (very slightly) to apply to episodic tasks. Show that you know the modifications needed by giving the modified version of (3.3).**

    Answer 3.5

3.6 **Suppose you treated pole-balancing as an episodic task but also used discounting, with all rewards zero except for -1 upon failure. What then would the return be at each time? How does this return di↵er from that in the discounted, continuing formulation of this task?**

    Answer 3.6

3.7 **Imagine that you are designing a robot to run a maze. You decide to give it a reward of +1 for escaping from the maze and a reward of zero at all other times. The task seems to break down naturally into episodes—the successive runs through the maze—so you decide to treat it as an episodic task, where the goal is to maximize expected total reward (3.7). After running the learning agent for a while, you find that it is showing no improvement in escaping from the maze. What is going wrong? Have you e↵ectively communicated to the agent what you want it to achieve?**

    Answer 3.7

3.8 **Suppose \gamma = 0.5 and the following sequence of rewards is received R<sub>1</sub> = -1, R<sub>2</sub> = 2, R<sub>3</sub> = 6, R<sub>4</sub> = 3, and R<sub>5</sub> = 2, with T = 5. What are G<sub>0</sub>, G<sub>1</sub>, . . ., G<sub>5</sub>? Hint: Work backwards.**

    Answer 3.8

3.9 **Suppose $\gamma$ = 0.9 and the reward sequence is R<sub>1</sub> = 2 followed by an infinite sequence of 7s. What are G<sub>1</sub> and G<sub>0</sub>?**

    Answer 3.9

3.10 **Prove the second equality in (3.10).**

    Answer 3.10

3.11 **If the current state is S<sub>t</sub>, and actions are selected according to a stochastic policy $\pi$, then what is the expectation of R<sub>t+1</sub> in terms of $\pi$ and the four-argument function p (3.2)?**

    Answer 3.11

3.12 **Give an equation for v<sub>$\pi$</sub> in terms of q<sub>$\pi$</sub> and $\pi$.**

    Answer 3.12

3.13 **Give an equation for q<sub>$\pi$</sub> in terms of v<sub>$\pi$</sub> and the four-argument p.**

    Answer 3.13

3.14 **The Bellman equation (3.14) must hold for each state for the value function v<sub>$\pi$</sub> shown in Figure 3.2 (right) of Example 3.5. Show numerically that this equation holds for the center state, valued at +0.7, with respect to its four neighboring states, valued at +2.3, +0.4, -0.4, and +0.7. (These numbers are accurate only to one decimal place.)**

    Answer 3.14

3.15 **In the gridworld example, rewards are positive for goals, negative for running into the edge of the world, and zero the rest of the time. Are the signs of these rewards important, or only the intervals between them? Prove, using (3.8), that adding a constant c to all the rewards adds a constant, vc, to the values of all states, and thus does not a↵ect the relative values of any states under any policies. What is v<sub>c</sub> in terms of c and $\gamma$?**

    Answer 3.15

3.16 **Now consider adding a constant c to all the rewards in an episodic task, such as maze running. Would this have any e↵ect, or would it leave the task unchanged as in the continuing task above? Why or why not? Give an example.**

    Answer 3.16

3.17 **What is the Bellman equation for action values, that is, for q<sub>$\pi$</sub>? It must give the action value q<sub>$\pi$</sub>(s, a) in terms of the action values, q<sub>$\pi$</sub>(s0, a0), of possible successors to the state–action pair (s, a). Hint: the backup diagram to the right corresponds to this equation. Show the sequence of equations analogous to (3.14), but for action values.**

    Answer 3.17

3.18 **The value of a state depends on the values of the actions possible in that state and on how likely each action is to be taken under the current policy. We can think of this in terms of a small backup diagram rooted at the state and considering each possible action:**

**Give the equation corresponding to this intuition and diagram for the value at the root node, v<sub>$\pi$</sub>(s), in terms of the value at the expected leaf node, q<sub>$\pi$</sub>(s, a), given St = s. This equation should include an expectation conditioned on following the policy, $\pi$. Then give a second equation in which the expected value is written out explicitly in terms of $\pi$(a|s) such that no expected value notation appears in the equation.**

    Answer 3.18

3.19 **The value of an action, q<sub>$\pi$</sub>(s, a), depends on the expected next reward and the expected sum of the remaining rewards. Again we can think of this in terms of a small backup diagram, this one rooted at an action (state–action pair) and branching to the possible next states:**

**Give the equation corresponding to this intuition and diagram for the action value, q<sub>$\pi$</sub>(s, a), in terms of the expected next reward, R<sub>t+1</sub>, and the expected next state value, v<sub>$\pi$</sub>(S<sub>t+1</sub>), given that S<sub>t</sub> =s and A<sub>t</sub> =a. This equation should include an expectation but not one conditioned on following the policy. Then give a second equation, writing out the expected value explicitly in terms of p(s', r|s, a) defined by (3.2), such that no expected value notation appears in the equation.**

    Answer 3.19

3.20 **Draw or describe the optimal state-value function for the golf example.**

    Answer 3.20

3.21 **Draw or describe the contours of the optimal action-value function for putting, q<sub>\*</sub>(s, putter), for the golf example.**

    Answer 3.21

3.22 **Consider the continuing MDP shown to the right. The only decision to be made is that in the top state, where two actions are available, left and right. The numbers show the rewards that are received deterministically after each action. There are exactly two deterministic policies, $\pi$<sub>left</sub> and $\pi$<sub>right</sub>. What policy is optimal if $\gamma$ = 0? If $\gamma$ = 0.9? If $\gamma$ = 0.5?**

    Answer 3.22

3.23 **Give the Bellman equation for q<sub>\*</sub> for the recycling robot.**

    Answer 3.23

3.24 **Figure 3.5 gives the optimal value of the best state of the gridworld as 24.4, to one decimal place. Use your knowledge of the optimal policy and (3.8) to express this value symbolically, and then to compute it to three decimal places.**

    Answer 3.24

3.25 **Give an equation for v<sub>\*</sub> in terms of q<sub>\*</sub>.**

    Answer 3.25

3.26 **Give an equation for q<sub>\*</sub> in terms of v<sub>\*</sub> and the four-argument p.**

    Answer 3.26

3.27 **Give an equation for $\pi$<sub>\*</sub> in terms of q<sub>\*</sub>.**

    Answer 3.27

3.28 **Give an equation for $\pi$<sub>\*</sub> in terms of v<sub>\*</sub> and the four-argument p.**

    Answer 3.28

3.29 **Rewrite the four Bellman equations for the four value functions (v<sub>$\pi$</sub>, v<sub>\*</sub>, q<sub>$\pi$</sub>, and q<sub>\*</sub>) in terms of the three argument function p (3.4) and the two-argument function r (3.5).**

    Answer 3.29

