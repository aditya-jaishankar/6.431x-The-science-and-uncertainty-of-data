# 6.341x-The-science-and-uncertainty-of-data
Course notes from 6.341x EdX course from MIT. 

## Unit 1: Probability models and axioms

### Lecture 1: Probability models and axioms

* The basic concept in probability is that of a *sample space*.

* Probability laws help calculate probabilities of a particular event in the sample space from occuring. These laws have to respect axioms, for example, probabilities cannot be negative; the axioms are few, but powerful.
* There are three chief requirements for a sample space $\Omega$: (1) That the elements of the set are mutually exclusive i.e. only any one event can occur simultaneously at a time, (2) The elements of the set need to be collectively exhaustive i.e. the set captures all possible outcomes and (3) must be at the right granularity i.e.  the probability model must be able to leave out unnecessary details, for example whether it is taining outside. (1) and (2) together means that one and only one outcome in the sample space *must* occur. 
* Sample spaces can be discrete, finite, infintite, continuous, etc. (This listing is not collectively exhaustive :) )
* For easily countable number of outcomes, you can either draw up an outcome table or a outcome tree to enlist all possible outcomes.
* For continuous sample sets, the probability of any one event occuring is 0, because the list of possible outcomes is infinite. All we can talk about in this case is the probability of a subset of the sample space. For example, probability of throwing a dart at the bullseye is zero, but the probability of it ending up in some sub-disk of the board is finite.
* Here are some axioms of probabilities (Consider sample set $\Omega$ and an event $A$:
  - $\mathbf{P}(A) \geq 0$
  - $\mathbf{P}(\Omega) = 1$
  - $\mathbf{P}(A \cap B) = \mathbf{P}(A) + \mathbf{P}(B)$  
  if $\mathbf{P}(A \cup B) = \phi$, i.e., if $A$ and $B$ are disjoint (mutually exclusive) events/outcomes. 
* Definition: A subset of a sample space is called an *event*. 
* A generalization of summation axiom to a set of discrete events $\{s_1, s_2, ..., s_n\}$ is that $\mathbf{P}(\{s_1, s_2, ..., s_n\}) = \sum^i\mathbf{P}(\{s_i\}) = \sum^i\mathbf{P}(s_i)$. This can be proved like the continous case, but considering subsets consisting of one element, event $s_i$. By construction, these subsets are disjoint. 
* When proving theorems on sets, subsets and probabilities, use Venn diagrams. They are your friend. 
* Some more theorems: if $A \subset B$,
  - $\mathbf{P}(A \cup B) = \mathbf{P}(A) + \mathbf{P}(B) - \mathbf{P}(A \cap B)$
  - Union bound: $\mathbf{P}(A \cup B) \leq \mathbf{P}(A) + \mathbf{P}(B)$. 
  - Discrete uniform law: if $\Omega$ has $n$ discrete outcomes, each equally likely (so each outcome has probability $1/n$) and $A \subset \Omega$ has $k$ elements, the $\mathbf{P}(A) = k \cdot 1/n = k/n$ 
* Probability laws are somehwat arbitrary because they are a model. We chose a model of what best captures the situation. 
* Uniform probabilty law: For continuous sample spaces, the probability of a subset $A$ of $\omega$, is the ratio of the areas of $A$ and $\Omega$. 
* There are four steps to the calculations of probabilities:
  - Identify a sample space
  - Identify probability laws (counting, uniform probability law, etc.)
  - Identify an event of interest
  - Calculate
* When calculating probabilities, drawing pictures, trees, tables, enumeration, etc. is highly recommended. Visual cues help a lot. 
* The probability law has to be able to calculate probabilities for every possible outcome i.e. any subset $A$ of $\Omega$. 
* Countable additivity theorem: For any **sequence** of **disjoint** events $A_i$,
$$
\mathbf{P}(A_1 \cup A_2 \cup \cdots) = \sum_{i = 1}^\infty \mathbf{P}(A_i)
$$

* The word **sequence** is very important here. The word sequence can be interepreed as discrete events. For example, if the sample space is continuous, there is no way to arrange the elements in a sequence (like the real line), and this relationship does not hold. 

* I cannot assign uniform probabilities to an infinite sequence of events in the sample space. 
