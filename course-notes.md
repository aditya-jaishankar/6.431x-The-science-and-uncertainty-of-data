# 6.341x-The-science-and-uncertainty-of-data
Course notes from 6.341x EdX course from MIT. 

## Unit 1: Probability models and axioms

### Lecture 1: Probability models and axioms

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
  - <img src="/tex/72621880dbe90dfe4c16f8c98950ad1b.svg?invert_in_darkmode&sanitize=true" align=middle width=278.32698135pt height=24.65753399999998pt/>
  - Union bound: <img src="/tex/8a976522751d4188b6a0f8111cc8ee45.svg?invert_in_darkmode&sanitize=true" align=middle width=188.64114884999998pt height=24.65753399999998pt/>. 
  - Discrete uniform law: if <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/> has <img src="/tex/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode&sanitize=true" align=middle width=9.86687624999999pt height=14.15524440000002pt/> discrete outcomes, each equally likely (so each outcome has probability <img src="/tex/2d77e685bfa7e0c249fa2e10b3d67677.svg?invert_in_darkmode&sanitize=true" align=middle width=26.30529494999999pt height=24.65753399999998pt/>) and <img src="/tex/1231297529d2008532e3699fbea6a612.svg?invert_in_darkmode&sanitize=true" align=middle width=46.11860879999999pt height=22.465723500000017pt/> has <img src="/tex/63bb9849783d01d91403bc9a5fea12a2.svg?invert_in_darkmode&sanitize=true" align=middle width=9.075367949999992pt height=22.831056599999986pt/> elements, the <img src="/tex/f67cb514dc3c1ab95b3c8ee6fec9ef42.svg?invert_in_darkmode&sanitize=true" align=middle width=156.28588799999997pt height=24.65753399999998pt/> 
* Probability laws are somehwat arbitrary because they are a model. We chose a model of what best captures the situation. 
* Uniform probabilty law: For continuous sample spaces, the probability of a subset <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> of <img src="/tex/ae4fb5973f393577570881fc24fc2054.svg?invert_in_darkmode&sanitize=true" align=middle width=10.82192594999999pt height=14.15524440000002pt/>, is the ratio of the areas of <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> and <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/>. 
* There are four steps to the calculations of probabilities:
  - Identify a sample space
  - Identify probability laws (counting, uniform probability law, etc.)
  - Identify an event of interest
  - Calculate
* When calculating probabilities, drawing pictures, trees, tables, enumeration, etc. is highly recommended. Visual cues help a lot. 
* The probability law has to be able to calculate probabilities for every possible outcome i.e. any subset <img src="/tex/53d147e7f3fe6e47ee05b88b166bd3f6.svg?invert_in_darkmode&sanitize=true" align=middle width=12.32879834999999pt height=22.465723500000017pt/> of <img src="/tex/9432d83304c1eb0dcb05f092d30a767f.svg?invert_in_darkmode&sanitize=true" align=middle width=11.87217899999999pt height=22.465723500000017pt/>. 
* Countable additivity theorem: For any **sequence** of **disjoint** events <img src="/tex/4ebf880807deff5796460f39aea46f80.svg?invert_in_darkmode&sanitize=true" align=middle width=16.97969789999999pt height=22.465723500000017pt/>,
<p align="center"><img src="/tex/c758d4bd323d82d6823e672d4cbc4441.svg?invert_in_darkmode&sanitize=true" align=middle width=215.47227075pt height=44.89738935pt/></p>
  The word **sequence** is very important here. The word sequence can be interepreed as discrete events. For example, if the sample space is continuous, there is no way to arrange the elements in a sequence (like the real line), and this relationship does not hold. 

* I cannot assign uniform probabilities to an infinite sequence of events in the sample space. 
