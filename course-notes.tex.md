
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
\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) = \mathbf{P}(A_1) \prod\limits_{k=2}^n \mathbf{P}(A_k|A_1 \cap A_2 \cap \cdots \cap A_{k-1})
$$

* This derives straight from a repeated application of 
$$
\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) = \mathbf{P}((A_1 \cap A_2 \cap \cdots \cap A_{n-1}) \cap A_n) = \mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_{n-1})\cdot\mathbf{P}(A_n | A_1 \cap A_2 \cap \cdots \cap A_{n-1})
$$

* In words, the probability of $A_1 \cap A_2 \cap \cdots \cap A_n$ occuring is the probability of $A_1 \cap A_2 \cap \cdots \cap A_{n-1}$ occurring times the probability of $A_n$ occurring given that $A_1 \cap A_2 \cap \cdots \cap A_{n-1}$ occurred. 

* **Total Probability theorem**: If $A_1, A_2, \cdots, A_n$ are disjoint events, then
$$
\mathbf{P}(B) = \sum\limits_{k=1}^n \mathbf{P}(A_i)\cdot \mathbf{P}(B|A_i)
$$

In other words, the total probability that an event $B$ occurs is the weighted sum of the probabilities $B$ occurs under all disjoint scenarios, weighted by the probability of each scenario.  

* **Bayes Theorem**: Consider that we have some set of disjoint events $A_i$, each with probability $A_i$. These are our *prior beliefs*. Let $B$ be an event which could occur under the possible scenarios $A_i$. Bayes' rule essentially allows for updating our prior beliefs given open the observation that $B$ occured. The rule states that
$$
\mathbf{P}(A_i|B) = \dfrac{\mathbf{P}(A_i) \cdot \mathbf{P}(B|A_i)}{\sum\limits_{i=1} \mathbf{P}(A_i) \cdot \mathbf{P}(B|A_i)}
$$

Note that the infinite sum only applies in the case the events $A_i$ are a *sequence* of disjoint events (refer countable additivity theorem). 

* The term inference, which we look at in a lot more detail, is the process of updating prior beliefs given the outcome of an event under the scenario of the belief. 

### Lecture 3: Independence

* Two events are considered independent if the occurrence of one event doesn't change the probability of the other event. One vent doesn't change our beliefs about the other event. 
* More formally, two events $A$ and $B$ are independent if $\mathbf{P}(A \cap B) = \mathbf{P}(A) \cdot \mathbf{P}(B)$. 
* Some intuition here: Indepenence is completely different from two events being disjoint. In fact, if two events are disjoint, the occurrence of one event immediately means that the other event did not occur. So disjoint events are like siamese twins, so to speak. 
* Independence usually arises when the events occur due to some non-interacting physical processes. For example, whether I toss a heads and whether it will rain on New Year's Day. 

* If $A$ and $B$ are independent events, then $A^c$ and $B^c$ are also independent, and so are $A$ and $B^c$. Think about this intuitively. 

* **Conditional Independence**: Two events $A$ and $B$ are conditionaly independent if
$$
\mathbf{P}(A \cap B)|C) = \mathbf{P}(A|C) \cdot \mathbf{P}(B|C)
$$

* Note that if wo events $A$ and $B$ are independent, it does not automatically imply that they are conditionally independent. Can you think of a Venn diagram example as to why this is true?

* Indpendence of multiple events: Events $A_i$ are independent if $\mathbf{P}(A_1 \cap A_2 \cap \cdots \cap A_n) = \mathbf{P}(A_i) \mathbf{P}(A_j) \cdots \mathbf{P}(A_m)$ for any choice and any number of $i, j$, and $m$. 

* For a collection of events, independence is a very difference issue from pairwise independence. Paiwrise independence for all pairs does not imply that all events are independent.

## Unit 3: Counting

### Lecture 4: Counting

* Counting techniques can be used whenever the elements of the sample space are equally likely i.e. the probabiliy of an event is proportional to the number of events in that sample space. 

* The binomial coefficient is defined as
$$
\binom{n}{k}
$$

* This is the same as $^n C_k$ and is very useful is calculating binomial probabilities. For example, if I have a biased coin that gives heads with probability $p$, what is the probability that in $n$ tosses I will get $k$ heads.  

* The binomial coefficient can be expanded as:
$$
(a + b)^n = \sum\limits_{k=0}^n \binom{n}{k} a^k b^{n-k}
$$

* *Keep in mind the physical interpretation of the RHS of the above equation:* The quantity $\binom{n}{k}p^k (1-p)^{n-k}$ is the porbability that an unfair coin with probability $p$ of getting a head will give $k$ heads when tossed $n$ times; these heads can be mixed and arranged in $\binom{n}{k}$ ways. Also, the sum in the above equation (with $a = p$ and $b = 1-p$) covers the entire sample space, i.e., the probability of getting 1 head or 2 heads or, $\cdots$, $n$ heads, and therefore that sum is one. Very useful physical interpretation of binomial probabilities.   

## Unit 4: Discrete Random Variables

### Lecture 5: Probability mass functions and expectations

* A **random variable** is a variables whose value depends on the outcome of a probabilistic experiment. A **discrete random variable** is a random variable whose value is in a finite or countably infinite set. Thnumber of possible values a discrete random variable can take is finite or countably infinite. 

* A random variable can be thought of as a function that takes a particular element in the sample space $\Omega$ and maps it to a particular value (in the case of a discrete random variable, the value is in a finite set or a countably infinite set). 

* **Notation:** Random variables are denoted by a capital letter $X$ as opposed to the value of a particular outcome of the random variable, which is denoted in lower-case letters $x$. 

* We can define a random variable that is a function of random variable i.e. $Z = X + Y$ which produces the value $z$ when the value of $X$ is $x$ and the value of $Y$ is $y$. 

* A key concept is that of a **probability mass function** or the **probability distribution** which determines the probability that a discrete random variable $X$ takes value $x$. The notation is $p_X(x)$ or $\mathbf{P}(X=x)$. Some properties: $p_X(x) \geq 0$ and $\sum_ip_X(x)=1$ where $x_i$ captures every element of the sample space (these are all disjoint because the sample space here is considered to be discrete. For example, think about two successive rolls of a die. Let the value of the first roll is described by the discrete random variable $X$ and the second be $Y$. Define $Z = X+Y$. Then $p_Z(2) = 1/16$, $p_Z(3) = 2/16$ (the outcome that $X=1$ and $Y=2$ or $X=2$ and $Y=1$), etc. 

* The formal definition of a probability mass function is 
$$
p_X(x) = \mathbf{P}({\omega \in \Omega : X(\omega)=x})
$$

* In words, the probability distribution or the probability mass function is described as the probability of the event containing those elements $\omega \in \Omega$ such that the value of the discrete random variable $X(\omega) = x$. Find all the event consisting of the elements $\omega$ for which the value of the discrete random variable $X$ at those $\omega$ is $x$.  

* **Bernoulli Random Variables**: They only take two values 0 and 1 with probability $1-p$ and $p$ respectively. i.e the PMF can be written as
$
p_X(x) = p if x=1; 1-p if x=0
$

* Bernoulli Random Variables can be linked to **indicator random variables** $I_A$. These random variables tell us whether an event $A$ occured or its complement $A^c$ occurred i.e. $A$ did not occur. $I_A =1$ if $A$ occured and 0 if $A^c$ occurred. 
$
p_{I_A}(1) = \mathbf{P}(I_A = 1) = \mathbf{P}(A)
$

* **Discrete uniform random variable:** Parameters $a, b$. The random variable $X(\omega) = \omega$ and $\omega \in {a,b}$ where $a$ and $b$ are integers. Therefore there are $b - a +1$ integers in the range. The PMF for this random variable is
$
p_X(x) = \frac{1}{b-a +1}
$

* **Binomial random variable**: Parameters $n ,p$. This random variables describes the number of successes in an experiment consisting of $n$ trials, all identical, where a 'success' occurs with probability $p$ and a failure with probability $1-p$. For example, tosses of a biased coin with probability $p$ of getting a head. The random variable that describes the number of heads is a binomial random variable. For a binomial random variable $X$, 
$$
p_X(k) = \binom{n}{k}p^k(1-p)^{n-k}
$$

* **Geometric random variable:** Parameter $p$. Let the experiment be a sequence of coin tosses and the random variable $X$ to be the first occurrence of a head. Then $p_X(k)$ describes the probabilit that the first head is achieved on the $k$-th toss. Therefore we have (and think about why this is the result) $p_X(k) = (1-p)^k p$

