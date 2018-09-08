# 6.341x-The-science-and-uncertainty-of-data
Course notes from 6.341x EdX course from MIT. 

## Lecture 1: Probability models and axioms

* The basic concept in probability is that of a *sample space*.

* Probability laws help calculate probabilities of a particular event in the sample space from occuring. These laws have to respect axioms, for example, probabilities cannot be negative; the axioms are few, but powerful.
* There are three chief requirements for a sample space <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/>: (1) That the elements of the set are mutually exclusive i.e. only any one event can occur simultaneously at a time, (2) The elements of the set need to be collectively exhaustive i.e. the set captures all possible outcomes and (3) must be at the right granularity i.e.  the probability model must be able to leave out unnecessary details, for example whether it is taining outside. (1) and (2) together means that one and only one outcome in the sample space *must* occur. 
* Sample spaces can be discrete, finite, infintite, continuous, etc. (This listing is not collectively exhaustive :) )
* For easily countable number of outcomes, you can either draw up an outcome table or a outcome tree to enlist all possible outcomes.
* For continuous sample sets, the probability of any one event occuring is 0, because the list of possible outcomes is infinite. All we can talk about in this case is the probability of a subset of the sample space. For example, probability of throwing a dart at the bullseye is zero, but the probability of it ending up in some sub-disk of the board is finite.
* Here are some axioms of probabilities (Consider sample set <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/> and an event <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/>:
  - <img src="/tex/07e065a61d38e003fdb98d49d824c6f3.svg?invert_in_darkmode&sanitize=true" align=middle width=68.17337999999998pt height=24.65753399999998pt/>
  - <img src="/tex/501880e6d3131b2e2786d6691f6d6406.svg?invert_in_darkmode&sanitize=true" align=middle width=67.71676064999998pt height=24.65753399999998pt/>
  - <img src="/tex/5faf238573fb3fcb6b5ac80caa701f05.svg?invert_in_darkmode&sanitize=true" align=middle width=188.64114884999998pt height=24.65753399999998pt/>  
  if <img src="/tex/77862dde40851307c41617fcc1392e82.svg?invert_in_darkmode&sanitize=true" align=middle width=101.30681549999998pt height=24.65753399999998pt/>, i.e., if <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> and <img src="/tex/61e84f854bc6258d4108d08d4c4a0852.svg?invert_in_darkmode&sanitize=true" align=middle width=13.29340979999999pt height=22.465723500000017pt/> are disjoint (mutually exclusive) events/outcomes. 
* Definition: A subset of a sample space is called an *event*. 
* A generalization of summation axiom to a set of discrete events <img src="/tex/d4f8272eb11869fed8530d24ab3b9c6c.svg?invert_in_darkmode&sanitize=true" align=middle width=98.86803629999997pt height=24.65753399999998pt/> is that <img src="/tex/bba7410c8963563c44ff8c2d8c5e82c4.svg?invert_in_darkmode&sanitize=true" align=middle width=313.74970605pt height=31.75825949999999pt/>. This can be proved like the continous case, but considering subsets consisting of one element, event <img src="/tex/4fa3ac8fe93c68be3fe7ab53bdeb2efa.svg?invert_in_darkmode&sanitize=true" align=middle width=12.35637809999999pt height=14.15524440000002pt/>. By construction, these subsets are disjoint. 
* When proving theorems on sets, subsets and probabilities, use Venn diagrams. They are your friend. 
* Some more theorems: if <img src="/tex/2c847daba8344c93c2058ff8ae05ce44.svg?invert_in_darkmode&sanitize=true" align=middle width=47.539839599999986pt height=22.465723500000017pt/>,
  - \mathbf{P}(A \cup B) = \mathbf{P}(A) + \mathbf{P}(B) - \mathbf{P}(A \cap B)<img src="/tex/fffc0df4a365f9485534a10a71c3374a.svg?invert_in_darkmode&sanitize=true" align=middle width=304.36193369999995pt height=24.65753399999998pt/>. 
