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
 3. learning effect: people get adaptive to the treatment

- overview:
 1. When not to use A/B test: if the change is too large, if control/test group cannot be decided only by the change. if the testing time is too long(need to observe at least one cycle)/cost is too high/. if something is missing.
 
 2. A/B test gives you broad and quantitative data
 
 3. how to select control variables: list variables -> collect data -> test correlation between ctrl and target variables -> test correlation between ctrl variables
 
 4. experiment design:randomized design & matched pair design(when observations are small & expernsive)
 
 5. randomized design: the unit of diversion, population, duration and size
 
 6. matched-pair design: need to choose the test units first, then assign the control units accordingly. so how to choose the test units:identify outliers, # of treatment units, randomly select
 
- choose metrics

 7. how to generate metrics: defining customer funnel, external data, UER(user experiment study), focus group, survey(less depth, more people), retrospective analysis, experiments
 
 8. metrics: filtering, segmenting, summary(sums&counts,distribution(retrospective analysis),probablities&rates,ratios) -> sensitivity and robustness: experiment or retrospective , A/A test(sanity check) within A/B test can be used to examine the variability(can also use empirical methods to estimate variance) of metrics
 
 - Design experiment
 
 9. Diversion: consistency(to what level can the objective notice the difference),ethical(additional information collected might related to identification), variability(unit of analysis and unit of diversion)
 
 10. intra-user experiments(treatment/control to the same person), inter-user experiments(different people for treatment/control)
 
 11. cohort or population: cohort in within the population, use cohort when: anything requiring user to be establish
 
 12. things keep changing over time, use pre(A/A test)/pro(A/A test)-periods together with cohort to solve learning effect 
 
 - Analyze results
 
 13. sanity checks: choose invariant metrics(should not differ between treatment & control ) -> check invariants(CI)
 
 14. multiple metrics: multiple comparision to adjust significance level; direction; overall evaluation criteria(OEC)

# SQL

1. basic syntex: **SELECT** west **AS** "West Region", **LIMIT** 100, **WHERE**,  **ORDER BY** XX **(DESC)**, 
2. logic:
 - Equal to	**=**
 - Not equal to **!=**
 - Greater than **>**
 - Less than	**<**
 - Greater than or equal to	**>=**
 - Less than or equal to	**<=**
 - **LIKE** and **ILIKE** allows you to match similar values, **ILIKE** is not case-sensitive. 
 - **IN** allows you to specify a list of values you'd like to include. 
 - **BETWEEN** allows you to select only rows within a certain range.
 - **IS NULL** allows you to select rows that contain no data in a given column.
 - **AND** allows you to select only rows that satisfy two conditions.
 - **OR** allows you to select rows that satisfy either of two conditions. 
 - **NOT** allows you to select rows that do not match a certain condition.

 ex: 
 ```**WHERE** year_rank **IN** (1, 2, 3)```
 
 ex:(pay attention to ' ' and " ") 
 ```**AND** ("group" **ILIKE** '%macklemore%' **OR** "group" **ILIKE** '%timberlake%') ```

3. Aggregate: 
 - **COUNT** counts how many rows are in a particular column that is NOT NULL
 - **SUM** adds together all the values in a particular column: treat NULL as 0 
 - **MIN** and **MAX** return the lowest and highest values in a particular column, respectively.
 - **AVG** calculates the average of a group of selected values.
 - **GROUP BY** 
 - **DISTINCT var** select distinct values
 - **CASE** similar to if/then/else, must end with **END**
 
  Query clause order:
 - SELECT
 - FROM
 - WHERE
 - GROUP BY
 - HAVING
 - ORDER BY
  
 ex: 
 **SELECT** year,month,MAX(high) **AS** month_high
  **FROM** tutorial.aapl_historical_stock_price
  **GROUP BY** year, month
  **HAVING** MAX(high) > 400
  **ORDER BY** year, month
 
  ex:(pay attention to the "," at the end of **SELECT** line)
  ```**SELECT** player_name,year,
        **CASE WHEN** year = 'SR'  **THEN ** 'yes'
             **ELSE ** 'no'  **END AS** is_a_senior
   **FROM** benn.college_football_players```
   
   ex:(pay attention to the **1** here, **1** actually refer to year_group, so we can use **GROUP BY** year_group. But we cannot use COUNT(year_group), because by that time year_group do not exist)
 ```  **SELECT CASE WHEN** year = 'FR' **THEN** 'FR'
            **WHEN** year = 'SO' **THEN** 'SO'
            **WHEN** year = 'JR' **THEN** 'JR'
            **WHEN** year = 'SR' **THEN** 'SR'
            **ELSE** 'No Year Data' **END AS** year_group,
            **COUNT(1) AS** count
  **FROM** benn.college_football_players
  **GROUP BY** 1 ```
 
 4. 




# github tutorial
- [link](https://www.linkedin.com/learning/learning-git-and-github/working-with-the-staging-environment)
 
 
 
 
 
 
 
 
 
 
