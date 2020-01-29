- [ ] Finish Top 100 easy level leecode
- [ ] Finish Top 100 median level leecode
- [ ] review sql(hackerank)
- [ ] python packages:TensorFlow, Keras, PyTorch,pandas,numpy,Matplotlib,Tableau,Scikit-Learn 
- [ ] R packages:dply, Tidyverse
- [ ] hive
- [ ] A/B test, product analysis
- [ ] review basic methods in normal machine learning
- [ ] feature engineering, metrics
- [ ] Big Data techniques, hadoop/spark
- [ ] Future: more kaggle projects(with NLP dataset)
- [ ] Future: Hadoop and Spark
- [ ] Future: build up my github


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
 
 **WHERE** year_rank **IN** (1, 2, 3)
 
 ex:(pay attention to ' ' and " ")
 
 **AND** ("group" **ILIKE** '%macklemore%' **OR** "group" **ILIKE** '%timberlake%')

3. Aggregate: 
 - **COUNT** counts how many rows are in a particular column that is NOT NULL
 - **SUM** adds together all the values in a particular column: treat NULL as 0 
 - **MIN** and **MAX** return the lowest and highest values in a particular column, respectively.
 - **AVG** calculates the average of a group of selected values.
 - **GROUP BY** 
 - **HAVING** 
 - **ORDER BY** 
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
 
 ```
 SELECT year,month,MAX(high) **AS** month_high
        FROM tutorial.aapl_historical_stock_price
        GROUP BY year, month
        HAVING MAX(high) > 400
        ORDER BY year, month
 ```
 
  ex:(pay attention to the "," at the end of **SELECT** line)
  
  ```
  SELECT player_name,year,
        CASE WHEN year = 'SR' THEN 'yes'
             ELSE 'no'  END AS is_a_senior
   FROM benn.college_football_players
  ```
   
   ex:(pay attention to the **1** here, **1** actually refer to year_group, so we can use **GROUP BY** year_group. But we cannot use COUNT(year_group), because by that time year_group do not exist)
   
   ```
   SELECT CASE WHEN year = 'FR' THEN 'FR'
            WHEN year = 'SO' THEN 'SO'
            WHEN year = 'JR' THEN 'JR'
            WHEN year = 'SR' THEN 'SR'
            ELSE 'No Year Data' END AS year_group,
            COUNT(1) AS count
   FROM benn.college_football_players
   GROUP BY 1 
  ```
 
 4. 



# github tutorial
- [link](https://www.linkedin.com/learning/learning-git-and-github/working-with-the-staging-environment)
 
 
 
 
 
 
 
 
 
 
