# 6.341x-The-science-and-uncertainty-of-data
Course notes from 6.341x EdX course from MIT. 

## Lecture 1: Probability models and axioms

* The basic concept in probability is that of a *sample space*.

* Probability laws help calculate probabilities of a particular event in the sample space from occuring. These laws have to respect axioms, for example, probabilities cannot be negative; the axioms are few, but powerful.
* There are three chief requirements for a sample space $\Omega$: (1) That the elements of the set are mutually exclusive i.e. only any one event can occur simultaneously at a time, (2) The elements of the set need to be collectively exhaustive i.e. the set captures all possible outcomes and (3) must be at the right granularity i.e.  the probability model must be able to leave out unnecessary details, for example whether it is taining outside. (1) and (2) together means that one and only one outcome in the sample space *must* occur. 
* Sample spaces can be discrete, finite, infintite, continuous, etc. (This listing is not collectively exhaustive :) )
* For easily countable number of outcomes, you can either draw up an outcome table or a outcome tree to enlist all possible outcomes.
* For continuous sample sets, the probability of any one event occuring is 0, because the list of possible outcomes is infinite. All we can talk about in this case is the probability of a subset of the sample space. For example, probability of throwing a dart at the bullseye is zero, but the probability of it ending up in some sub-disk of the board is finite.
* Here are some axioms of probabilities (Consider sample set $\Omega$ and an event $A$:

\begin{equation}
  \mathbf{P}(A) \geq 0 \\
  \mathbf{P}(\Omega) = 1 \\
  \mathbf{P}(A \cap B) = \mathbf{P}(A) + \mathbf{P}(B)
\end{equation}

if $\mathbf{P}(A \cup B) = \phi$, i.e., if $A$ and $B$ are disjoint (mutually exclusive) events/outcomes. 
* Definition: A subset of a sample space is called an *event*. 
* A generalization of summation axiom to a set of discrete events $\{s_1, s_2, ..., s_n\}$ is that $\mathbf{P}(\{s_1, s_2, ..., s_n\}) = \sum^i\mathbf{P}(\{s_i\}) = \sum^i\mathbf{P}(s_i)$. This can be proved like the continous case, but considering subsets consisting of one element, event $s_i$. By construction, these subsets are disjoint. 
