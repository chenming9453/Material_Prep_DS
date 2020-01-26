- [ ] Finish Top 100 easy level leecode
- [ ] Finish Top 100 median level leecode
- [ ] review sql(hackerank)
- [ ] python packages:TensorFlow, Keras, PyTorch
- [ ] R packages:dply, Tidyverse
- [ ] hive
- [ ] A/B test, product analysis
- [ ] review basic methods in normal machine learning
- [ ] feature engineering, metrics
- [ ] Big Data techniques, hadoop/spark
- [ ] Future: more kaggle projects(with NLP dataset)
- [ ] Future: Hadoop and Spark
- [ ] Future: build up my github

# Leetcode-notes
**Understand the problem first!!!**

1. Two Sum(1)
- **enumerate** to gain index and elements at the same time
- Unlike R, **remove, del, pop** will remove elements of the original list, so avoid using them when you do not want to change the original list

2. Valid Parentheses(20): stack: LIFO <-> queue: FIFO
- unlike R, logics are **True** or **False**
- consider conditions using if/elif

3. Nested List Weight Sum(339): iteration 
- should understand the functions defined to the object first

4.  Maximum Depth of Binary Tree (104):iteration 
- **None** is like NA in R,any number/string cannot be **None**.Use **if xx is not None** to determine

5. 733

 # A/B test
 
- terminology: 
 1. individual: unit
 2. experimental variable(independent/treatment variable), target variable(outcome), control variable(predictor), and lurking variable(confounder)

- key points:
 1. When not to use A/B test: if the change is too large, if control/test group cannot be decided only by the change. if the testing time is too long(need to observe at least one cycle)/cost is too high/. if something is missing.
 
 2. A/B test gives you broad and quantitative data
 
 3. how to select control variables: list variables -> collect data -> test correlation between ctrl and target variables -> test correlation between ctrl variables
 
 4. experiment design:randomized design & matched pair design(when observations are small & expernsive)
 
 5. randomized design: the unit of diversion, population, duration and size
 
 6. matched-pair design: need to choose the test units first, then assign the control units accordingly. so how to choose the test units:identify outliers, # of treatment units, randomly select
 
 7. how to generate metrics: defining customer funnel, external data, UER(user experiment study), focus group, survey(less depth, more people), retrospective analysis, experiments
 
 8. metrics: filtering, segmenting, summary(sums&counts,distribution(retrospective analysis),probablities&rates,ratios) -> sensitivity and robustness: experiment or retrospective , A/A test(sanity check) within A/B test can be used to examine the variability(can also use empirical methods to estimate variance) of metrics
 
 9. 
 

# github tutorial
- [link](https://www.linkedin.com/learning/learning-git-and-github/working-with-the-staging-environment)
 
 
 
 
 
 
 
 
 
 
