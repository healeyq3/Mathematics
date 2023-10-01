# Motivation
Answering the question "what is probability" is nontrivial. Wikipedia's definition is pretty decent: "Probability is the branch of mathematics concerning numerical descriptions of how likely an event is to occur, or how likely it is that a proposition is true". I may contend my own definition later, but for now I'll instead use the question "what does probabilty hope to 'solve'" to motivate the axiomatic approach to probability (as a reminder, I believe that Hamming has qualms with this view of probability as well; however, from my own understanding I believe this measure theoretic framework accurately captures the idea of an experiment, and it is simply the probability $\mathbb{P}$ measure which can be varied to in turn define different models of the idea of "probability" - which is of course relates back to the question of "what is probability").

**What is the role of probability?**\
Suppose we have some experiment we wish to conduct, for instance, flipping a coin or measuring the reaction time of an individual. Specifically, we have some experiment where the outcome of the experiment is *unknown* (this may also be referred to as a *random* experiment, but this is somewhat redundant as there would be no point in conducting the experiment if the exact outcome was already known). Furthermore, we may wish to construct a mathematical model of this experiment which we can use to gain insight into which events are likely to occur. As an example, in a casino setting, one may construct a probabilistic model of the game they are playing in hopes of using the resulting probabilities to make better decisions. One way (and I posit perhaps the most rigorous way) to model such a real-world situation is through the mathematical triplet $(\Omega, E, \mathbb{P})$ which we refer to as a **probability space**.

# Probability Space
## Key Terms and Examples
- Experiment: The real-world circumstance one is trying to model, which can consist of infinitely many idealizations of that particular circumstance.
- Trial: an idealization of the real-world circumstance the experiment is attempting to model. In other words, an experiment is composed of many trials.
- Sample Space ($\Omega$): the set of all possible outcomes of an experiment
- Event ($E_i \in E$, where $E$ is the event space): A subset of outcomes of the sample space, or rather, any collection of possible outcomes of an experiment. 

**Example 1:** Flipping a coin once.\
There is only one trial and $\Omega = \{H, T\}$. In other words, the only outcomes of the experiment are either a heads or a tails.

**Example 2:** Flipping a coin twice.\
There are now *two* trials: the real-world circumstance we are modeling, flipping a coin, is happening *twice*. Furthermore, $\Omega = \{(H, H), (H, T), (T, H), (T, T)\}$ (note that sometimes a tuple is not used to indicate multiple trials and instead the sample space may be written as $\{HH, HT, TH, TT\}$). Here we note that there are *four* outcomes of the experiment.\
This particular experiment is also a good time to define an *event*, which can sometimes be confused with an *outcome.* However, recall that an event is a subset of the sample space, or rather, a set of multiple outcomes. For instance, an event could be: "in the experiment, a head was flipped at least once." In this case, letting $E_1$ denote the event, $E_1 = \{HH, HT, TH\} \subseteq \Omega$.

## Rigorous Definition
We now look back at our triplet $(\Omega, E, \mathbb{P})$. We have already specificed that the sample space $\Omega$ is simply a set of all possible outcomes of the experiment. However, the remaining two objects, $E$ and $\mathbb{P}$, are a bit more complex. Indeed, one must first learn or re-familiarize themselves with the beginnings of [measure theory](../Analysis/measure-theory.md).

Given one now has the appropriate background, we define $E$ to be a $\sigma$-algebra (or $\sigma$-field) of $\Omega$. To gain a little bit of intuition with this concept, we note that $\{\emptyset, \Omega\}$ and the power set $\mathcal{P}(\Omega)$ are both $\sigma$-algebras of $\Omega$.

Now, imagine that we wish to construct $E$ in such a way that it has the event "flipped heads at least once" in it. Furthermore, we know $\{HH, HT, TH\} \in E$. However, we now must continue to construct $E$ in such a way that it completes the three requirements of being a $\sigma$-algebra...this could become tedious and frustrating. Furthermore, we let $\mathcal{C}$ denote a class of events of interest that we wish to be included in $E$. Hence, we wish to "complete" $\mathcal{C}$ by adding events to it so that we get a $\sigma$-algebra. Considering the two-coin toss example again, this would be the smallest $\sigma$-algebra containing 

$$

$$