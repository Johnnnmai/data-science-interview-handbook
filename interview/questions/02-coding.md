# SQL and Python Coding Questions

Based on candidate reports from Reddit, Glassdoor, and personal blogs about what they were actually asked in data science interviews.

This section covers SQL queries, Python data manipulation, and coding problems specific to DS roles. These are not LeetCode algorithm problems - they focus on data extraction, transformation, and analysis.


## Format

Typically 45-60 minutes, live coding in a shared environment (CoderPad, HackerRank, or a company-internal tool). The interviewer presents a schema and asks you to write queries or code to answer analytical questions. You are expected to talk through your approach as you write.

Some companies use two formats:
- Live coding: write queries in real-time while the interviewer watches
- Take-home timed assessment: 60-90 minutes, multiple SQL problems, auto-graded

SQL is tested at every company. Python is tested at about 60% of companies. The questions overlap significantly with real day-to-day DS work.


## SQL Interview Questions

### Joins and Aggregations

- Write a query to find the top 5 customers by total revenue in the last 90 days. The schema has `orders` (order_id, customer_id, amount, order_date) and `customers` (customer_id, name, signup_date) [^glassdoor-google-ds]

- Write a query to find all users who signed up in January 2025 but never made a purchase. Schema: `users` (user_id, signup_date), `purchases` (purchase_id, user_id, purchase_date) [^interviewquery-sql]

- Given tables `employees` (employee_id, department_id, salary) and `departments` (department_id, department_name), find departments where the average salary exceeds the company-wide average salary [^reddit-ds-sql]

- Write a query to find the second-highest salary in each department. Handle ties [^glassdoor-meta-ds]

- Given `events` (user_id, event_type, event_date), find users who performed event A and event B on the same day but never performed event C [^glassdoor-airbnb-ds]

- Write a query to find all products that were purchased together in the same order more than 100 times. Schema: `order_items` (order_id, product_id) [^interviewquery-sql]


### Window Functions

- Given a table of daily revenue by product, write a query to calculate the 7-day rolling average for each product [^glassdoor-google-ds]

- For each user, find the time difference between their first and second purchase. Schema: `purchases` (user_id, purchase_date, amount) [^glassdoor-meta-ds]

- Rank all employees within each department by salary, and also show their company-wide rank. Schema: `employees` (employee_id, department_id, salary) [^reddit-ds-sql]

- Write a query to find users whose spending increased month-over-month for at least 3 consecutive months. Schema: `transactions` (user_id, amount, transaction_date) [^glassdoor-netflix-ds]

- For each day, calculate the percentage of daily active users who were also active the previous day (day-over-day retention). Schema: `user_activity` (user_id, activity_date) [^interviewquery-sql]

- Given `page_views` (user_id, page, timestamp), find the most common page transition (page A followed immediately by page B) for each user session. Define a session as activity with gaps of less than 30 minutes [^glassdoor-uber-ds]

- Write a query to find the median order value per month. Do not use a built-in MEDIAN function [^reddit-ds-sql]


### CTEs and Subqueries

- Write a query using a CTE to calculate the retention rate: what percentage of users who signed up in month M were active in month M+1? Schema: `users` (user_id, signup_date), `activity` (user_id, activity_date) [^glassdoor-airbnb-ds]

- Build a funnel analysis query: given events (page_view, add_to_cart, checkout, purchase), calculate the conversion rate between each step, broken down by traffic source. Schema: `events` (user_id, event_type, event_timestamp, traffic_source) [^glassdoor-meta-ds]

- Write a query to find power users: users who were active on at least 20 of the last 30 days. Use a CTE to first calculate daily activity, then aggregate [^interviewquery-sql]

- Given a self-referencing table `employees` (employee_id, manager_id, name), write a query to find the full management chain for a given employee (recursive CTE) [^glassdoor-google-ds]

- Write a query that calculates customer lifetime value (LTV) as the total revenue per customer divided by the number of months since their first purchase. Use CTEs to break the problem into readable steps [^glassdoor-netflix-ds]


### Cohort Analysis

- Given `users` (user_id, signup_date) and `sessions` (user_id, session_date), build a cohort retention table showing the percentage of each monthly signup cohort that returned in months 1, 2, 3, 4, 5, 6 after signup [^glassdoor-airbnb-ds]

- Write a query to compare the average order value of users who signed up via organic search vs. paid ads, broken down by their signup month cohort. Schema: `users` (user_id, signup_date, acquisition_channel), `orders` (user_id, order_date, amount) [^interviewquery-sql]

- Given a subscription product, write a query to calculate monthly churn rate by signup cohort. A user churns in month M if they were active in month M-1 but not in month M. Schema: `subscriptions` (user_id, start_date, end_date) [^glassdoor-spotify-ds]

- Build a query that shows the cumulative revenue per cohort over time (revenue curve by signup month) [^glassdoor-meta-ds]


### Date and Time Manipulation

- Write a query to find the average time between a user's first and second order. Exclude users with only one order. Report the result in days [^glassdoor-uber-ds]

- Given `events` (user_id, event_type, event_timestamp), define a user session as a sequence of events where no two consecutive events are more than 30 minutes apart. Calculate the average session duration per user [^glassdoor-airbnb-ds]

- Write a query to find the day of the week with the highest average order value. Account for timezone (all timestamps are in UTC, the business operates in US Pacific time) [^interviewquery-sql]

- Given `logins` (user_id, login_timestamp), find users who logged in every day for at least 7 consecutive days [^glassdoor-google-ds]


### Performance and Edge Cases

- You wrote a query that takes 45 minutes to run on a 100M-row table. How would you optimize it? Discuss indexing, partitioning, and query restructuring [^reddit-ds-sql-perf]

- What is the difference between WHERE and HAVING? When must you use HAVING? [^interviewquery-sql]

- Explain the difference between INNER JOIN, LEFT JOIN, CROSS JOIN, and FULL OUTER JOIN. When would you use each in an analytical context? [^glassdoor-google-ds]

- You have NULL values in a column you are aggregating. How do COUNT, SUM, and AVG handle NULLs? How might this lead to incorrect results in a cohort analysis? [^reddit-ds-sql]

- What is the difference between UNION and UNION ALL? When does the distinction matter for performance? [^interviewquery-sql]


## Python Coding Questions

### Pandas Data Manipulation

- Given a DataFrame of user transactions with columns [user_id, date, amount], write code to calculate the 30-day rolling average spend per user [^glassdoor-meta-ds]

- Given a DataFrame with columns [user_id, session_start, session_end], write code to find overlapping sessions for each user [^glassdoor-google-ds]

- You have two DataFrames: `users` with columns [user_id, country] and `orders` with columns [user_id, order_date, revenue]. Write code to calculate the average revenue per user per country, excluding users with fewer than 3 orders [^interviewquery-python]

- Given a DataFrame of clickstream data [user_id, page, timestamp], write a function that calculates the most common navigation path (sequence of 3 pages) [^glassdoor-airbnb-ds]

- Write a function that takes a DataFrame of daily metric values and detects anomalies (values more than 3 standard deviations from the 30-day rolling mean). Return the dates and values of anomalies [^glassdoor-netflix-ds]

- Given a DataFrame with columns [experiment_id, user_id, variant, metric_value], write code to perform a two-sample t-test for each experiment and return a summary DataFrame with columns [experiment_id, control_mean, treatment_mean, p_value, significant] [^reddit-ds-python]


### NumPy and Statistical Computing

- Implement a bootstrap confidence interval for the mean of a dataset. Generate 10,000 bootstrap samples and return the 2.5th and 97.5th percentiles [^glassdoor-google-ds]

- Write a function that performs a permutation test to compare two groups. Return the p-value [^interviewquery-python]

- Given a 2D numpy array representing a confusion matrix, write a function that calculates precision, recall, F1 score, and accuracy [^glassdoor-meta-ds]

- Implement stratified sampling: given a DataFrame and a column to stratify by, return a sample of N rows that preserves the distribution of the stratification column [^glassdoor-airbnb-ds]

- Write a function to calculate the Gini coefficient from an array of values [^reddit-ds-python]


### Algorithm Implementation

Note: these are DS-specific algorithms, not LeetCode-style problems.

- Implement a function that detects seasonality in a time series. Given daily metric values for 2 years, determine if there is a weekly or monthly pattern [^glassdoor-netflix-ds]

- Write a function that implements k-fold cross-validation from scratch. Given a dataset, a model, and k, return the average validation metric [^glassdoor-google-ds]

- Implement a simple decision tree classifier from scratch (binary splits, information gain). You do not need to handle pruning [^interviewquery-python]

- Write a function that calculates the Area Under the ROC Curve (AUC) given true labels and predicted probabilities, without using sklearn [^glassdoor-meta-ds]

- Implement gradient descent for linear regression. Given X, y, and learning rate, return the fitted coefficients after N iterations [^reddit-ds-python]

- Write a function that detects changepoints in a time series using cumulative sum (CUSUM). Given a sequence of values and a threshold, return the indices where a shift occurred [^glassdoor-uber-ds]


### Data Cleaning and Preparation

- You receive a CSV with 1M rows. 15% of rows have missing values in the target variable. 5% of rows have missing values in 3 feature columns. Write code to handle this: describe your strategy, then implement it [^glassdoor-airbnb-ds]

- Given a DataFrame with a column containing free-text user feedback, write code to clean the text (remove punctuation, lowercase, remove stopwords) and count the 20 most common words [^interviewquery-python]

- Write a function that detects and handles duplicate records in a DataFrame. Consider exact duplicates and near-duplicates (same user, same date, similar amount within 1%) [^glassdoor-meta-ds]

- Given a DataFrame with columns [user_id, event, timestamp], write code to create a feature matrix for a churn prediction model. Features should include: number of events in last 7/14/30 days, average time between events, number of distinct event types, days since last activity [^glassdoor-netflix-ds]


## How to Prepare

SQL:

- Practice daily on StrataScratch and DataLemur. Start with medium difficulty and work up to hard
- Focus on window functions (ROW_NUMBER, RANK, LAG, LEAD, SUM OVER) - they appear in 70%+ of DS SQL interviews
- Master CTEs. Break complex queries into readable steps. Interviewers evaluate code readability
- Practice cohort analysis queries until you can write them without hesitation
- Know how NULLs behave in aggregations, JOINs, and WHERE clauses
- Time yourself. In a 45-minute interview with 2 SQL problems, you have roughly 18-20 minutes per query including discussion

Python:

- Focus on pandas over numpy for most interview scenarios. Know groupby, merge, pivot_table, rolling, and apply
- Be comfortable writing statistical tests (t-test, chi-squared, bootstrap) in scipy and from scratch
- Practice data cleaning workflows: missing values, duplicates, type conversions, outlier detection
- Know how to create feature matrices from raw event data

Common mistakes:

- Writing overly complex queries when a simpler approach exists. Start simple, then optimize
- Not talking through your approach before writing. Interviewers want to see your thinking process
- Forgetting edge cases: empty groups, NULL handling, division by zero, single-row partitions
- Not testing with small examples first. Walk through your query with a 5-row sample dataset before claiming it works
- Using Python when SQL would be more appropriate (or vice versa). Know which tool is better for which task


## Sources

[^glassdoor-google-ds]: [Glassdoor - Google Data Scientist Interview](https://www.glassdoor.com/Interview/Google-Data-Scientist-Interview-Questions-EI_IE9079.0,6_KO7,21.htm)
[^interviewquery-sql]: [InterviewQuery - SQL Interview Questions](https://www.interviewquery.com/questions?tag=sql)
[^reddit-ds-sql]: [Reddit r/datascience - SQL Interview Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^glassdoor-meta-ds]: [Glassdoor - Meta Data Scientist Interview](https://www.glassdoor.com/Interview/Meta-Data-Scientist-Interview-Questions-EI_IE40772.0,4_KO5,19.htm)
[^glassdoor-airbnb-ds]: [Glassdoor - Airbnb Data Scientist Interview](https://www.glassdoor.com/Interview/Airbnb-Data-Scientist-Interview-Questions-EI_IE391850.0,6_KO7,21.htm)
[^glassdoor-netflix-ds]: [Glassdoor - Netflix Data Scientist Interview](https://www.glassdoor.com/Interview/Netflix-Data-Scientist-Interview-Questions-EI_IE11891.0,7_KO8,22.htm)
[^glassdoor-uber-ds]: [Glassdoor - Uber Data Scientist Interview](https://www.glassdoor.com/Interview/Uber-Data-Scientist-Interview-Questions-EI_IE575263.0,4_KO5,19.htm)
[^glassdoor-spotify-ds]: [Glassdoor - Spotify Data Scientist Interview](https://www.glassdoor.com/Interview/Spotify-Data-Scientist-Interview-Questions-EI_IE408251.0,7_KO8,22.htm)
[^interviewquery-python]: [InterviewQuery - Python Interview Questions](https://www.interviewquery.com/questions?tag=python)
[^reddit-ds-python]: [Reddit r/datascience - Python Coding Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-sql-perf]: [Reddit r/datascience - SQL Performance](https://www.reddit.com/r/datascience/) (r/datascience)
