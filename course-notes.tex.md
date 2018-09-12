
# 6.431x-The-science-and-uncertainty-of-data
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
### Lecture 2:  Mathematical background: Sets; sequences, limits, and series; (un)countable sets. 

* There are fundamental differences in the approaches used for discrete sample spaces and continuous sample spaces. 
* A **set** is a collection of **distinct** elements.
* Notation: 
	- $\{a, b, c, d\}$ denotes a finite set where we can enumerate elements.
	- For uncountable sets, $\{x \in \mathbb{R}: \cos(x) > 1/2\}$ means set of all real numbers $x$ such that $\cos(x) > 1/2$.  
	- $\bigcup\limits_n S_n$ denotes unions of all sets $S_i$. Therefore $x \in \bigcup\limits_n S_n \iff x \in S_i$ for any $i$ in $1, 2, ..., n$. Similarly, intersections can be defined. 
* **De Morgan's laws:** These can be proved with some basic logical arguments. 
	- $\left(\bigcup\limits_n S_n\right)^c = \bigcap\limits_n S_n^c$
	- $\left(\bigcap\limits_n S_n\right)^c = \bigcup\limits_n S_n^c$
* A **sequence** $\{a_i\}$ can be thought of as a function that assigns a value to every natural number, i.e., $f:\mathbb{N} \to a_i, a_i \in S$. 
* What we care about a lot is **convergent sequences**, where $\lim\limits_{i \to \infty} a_i = a$. The formal definition is that $\{a_i\}$ converges to $a$ if for any arbitrary $\varepsilon > 0, \varepsilon \in \mathbb{R}$ there exists $i > i_0$ such that $|a_i - a| < \varepsilon$ for some large enough $i_0 \in \mathbb{N}$. 
* In an infinite series $\sum^\infty a_i$, the series is well defined if $a_i \geq 0$; the limit is either finite or infinite. That is, if the sequence of partial sums is monotonic as $n$ is made larger the limit exists (could be $\infty$). If the sequence of partial sums is non-monotonic i.e. if $a_i$ can be negative, then it is possible the sum of the series exists, but also that if we rearrange the order of performing the sum, we may get a different limit. These problems can be avoided by considering $S = \sum^\infty |a_i|$. If $S < \infty$ for *some* particular order of arranging the terms, then the original sequence of partial sums is guaranteed to converge to a finite limit, regardless of the particular order of adding the terms. This condition also applies to double series $\sum\limits_{i, j}^\infty a_{ij}$. If $\sum |a_{ij}| < \infty$ for *some* particular ordering of the terms, then the series (i.e. the sequence of partial sums) converges to a finite value, and order of summation of terms does not matter. *The lecture includes a beautiful graphical example of adding row-wise and column-wise to demonstrate this point.*
* **Countable** and **Uncountable** sets: if I can assign a positive integer index to every element in the sample space, then the set is known as countable. In other words, if I can arrange the elements of the set in a sequence with positive integer indices. For example, the positive integers, all integers, rational numbers, etc. However, any interval on the real line is uncountable.  Cantor's diagnolization theorem is a beautiful way to prove this. 
#### Solved problem set:
* **Bonferroni's inequality**: For any n  events $A_1, A_2, ..., A_n$,
$$
\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) \geq \mathbf{P}(A_1) + \mathbf{P}(A_2) + \cdots \mathbf{P}(A_n) - (n-1)
$$

## Unit 2: Conditioning and Independence

### Lecture 2: Conditioning and Bayes' Rule

* The conditional probability of event $B$ occurring, given that event $A$ has occured is given by
$$
\mathbf{P}(B|A) = \dfrac{\mathbf{P}(B \cap A)}{\mathbf{P}(A)}
$$

* This is a definition - there is no question about whether it is correct or not. There is a useful intuition trick based on redefining the sample space i.e. when talking about $\mathbf{P}(B|A)$, because we are given that $A$ definitely occured, all the elements in the sample space in $A^c$ are automatically eliminated. $A$ becomes the new sample space. 
* It can be shown that conditional probabilities obey the axioms of probabilities. This is powerful because any results derived for regular probabilities also apply to conditional probabilities. 

* In general, it can be shown that for $n$ events $A_1, A-2, \cdots, A_n$, 
$$
\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) = \mathbf{P}(A_1) \Pi\limits_{k=2}^n \mathbf{P}(A_k|A_1 \cap A_2 \cap \cdots \cap A_{k-1})
$$

* This derives straight from a repeated application of $\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) = \mathbf{P}((A_1 \cap A_2 \cap \cdots \cap A_{n-1}) \cap A_n) = \mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_{n-1})\cdot\mathbf{P}(A_n | \cap A_1 \cap A_2 \cap \cdots \cap A_{n-1})$. 

* In words, the probability of $A_1 \cap A_2 \cap \cdots \cap A_n$ occuring is the probability of $$A_1 \cap A_2 \cap \cdots \cap A_{n-1}$ occurring times the probability of $A_n$ occurring given that $A_1 \cap A_2 \cap \cdots \cap A_{n-1}$ occurred. 
