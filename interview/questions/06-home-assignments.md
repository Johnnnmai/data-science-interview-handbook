# Take-Home Analysis Projects

Take-home assignments, case studies, and asynchronous assessments for data science roles. Based on 1,950+ job descriptions, company interview guides, and practitioner reports.

Of the 68 companies with disclosed interview processes, 24 (35.3%) include a take-home or asynchronous assignment. An additional 4 companies use paid analysis sessions or on-site case presentations instead. Analysis of reported DS take-home projects (Q4 2025 / Q1 2026) shows what companies actually ask:

- Exploratory data analysis and insight generation (45.0%+): analyze a dataset, find patterns, present actionable insights
- A/B test analysis (30.0%+): given experiment data, determine whether the treatment was effective and recommend next steps
- Predictive modeling challenges (25.0%+): build a model, evaluate it, and explain the business implications
- SQL case studies (20.0%+): answer business questions using SQL queries on provided schemas
- Metric investigation and diagnosis (15.0%+): investigate a metric change, identify root causes, propose solutions
- Presentation deliverables (10.0%+): prepare slides and present findings to a panel


## Format

Asynchronous assignments completed on your own time, typically with a deadline of 2-7 days. You submit a Jupyter notebook, slide deck, or written report, then discuss your solution in a follow-up interview.

Typical assignment formats:

- Take-home analysis project (most common): analyze a dataset and present findings, typically 4-8 hours of actual work. Companies emphasize analytical thinking and communication over model complexity
- Defence round: present and defend your analysis in a 45-60 minute walkthrough interview. The defence is often more important than the submission itself

Most companies do not restrict the use of AI tools for take-home assignments. The emphasis is on your analytical reasoning, not whether you used AI to draft code or clean data.


## Assignment Examples

Actual take-home assignments from candidate reports, job listings, and DS interview guides.


### Exploratory Data Analysis Projects

The most common assignment type (45.0%+ of reported cases).

- Given a dataset of 50,000 e-commerce transactions with columns [user_id, product_category, purchase_amount, timestamp, device_type, country], write an EDA report. Identify the top 3 actionable insights and recommend product changes. Present in a Jupyter notebook with visualizations [^glassdoor-airbnb-ds] [^reddit-ds-takehome]

- Analyze a dataset of user engagement for a mobile app. The dataset includes daily active usage, feature interactions, and demographic information. Identify user segments, characterize their behavior, and recommend retention strategies for the segment most at risk of churning [^glassdoor-spotify-ds]

- You are given 6 months of customer support ticket data with columns [ticket_id, user_id, category, priority, resolution_time, satisfaction_score]. Identify patterns in ticket volume, resolution time, and satisfaction. Recommend 3 process improvements with estimated impact [^glassdoor-meta-ds]

- Analyze a dataset of ride-sharing trips. Identify peak demand patterns, estimate the impact of surge pricing on rider behavior, and propose a data-driven pricing strategy. Submit a Jupyter notebook and a 5-slide executive summary [^glassdoor-uber-ds]

- Given a dataset of content engagement on a streaming platform (views, completion rate, ratings, time of day, device), identify what drives content success. Build a content scoring framework and explain how it could be used by the content team [^glassdoor-netflix-ds]


### A/B Test Analysis

Second most common (30.0%+).

- You are given the results of an A/B test on a checkout flow redesign. The dataset includes [user_id, variant, converted, revenue, timestamp, device_type, country]. Determine whether the new design is better. Consider: statistical significance, practical significance, segment effects, and any data quality issues you find. Write a 1-page recommendation memo [^glassdoor-google-ds]

- A product team ran an experiment testing a new recommendation algorithm. Treatment users saw more diverse recommendations. The dataset includes daily engagement metrics for 4 weeks. Analyze the results, address the novelty effect, and recommend whether to ship [^glassdoor-netflix-ds]

- Given data from a pricing experiment on a subscription product, analyze the impact on conversion rate, revenue per user, and churn. The experiment ran for 3 weeks. Determine if the duration was sufficient. Present your analysis with statistical rigor and business recommendations [^glassdoor-spotify-ds]

- You receive data from an email campaign A/B test. Variant A: personalized subject line. Variant B: generic subject line. The data shows Variant A has higher open rate but lower conversion rate. Analyze the full funnel, diagnose the contradiction, and recommend next steps [^interviewquery-takehome]

- A marketplace ran a test reducing seller fees by 10%. Analyze the impact on seller activity, buyer experience, and platform revenue. Consider network effects between the two sides. The dataset spans 6 weeks with 2 weeks pre-period and 4 weeks treatment [^glassdoor-uber-ds]


### Predictive Modeling Challenges

- Build a model to predict which users will churn in the next 30 days. The dataset includes user behavior data for 100,000 users over 6 months. Deliverables: feature engineering rationale, model selection justification, evaluation metrics, and a business-oriented summary of how to use the predictions [^glassdoor-airbnb-ds]

- Given historical data on loan applications (features, approval decision, default status), build a model to predict loan default. Discuss fairness considerations, model interpretability, and how you would monitor the model in production. Submit a notebook and a 3-slide summary [^glassdoor-stripe-ds]

- Build a model to predict the number of customer support tickets next week, broken down by category. The dataset includes 2 years of daily ticket counts, product release dates, and marketing campaign dates. Evaluate your model and discuss how it could be used for staffing decisions [^glassdoor-meta-ds]

- Given a dataset of property listings with features and prices, build a price estimation model. Evaluate it, identify the most important features, and discuss the limitations of your approach. Bonus: identify listings that appear to be mispriced [^glassdoor-airbnb-ds]

- Build a customer segmentation model using purchase history data. Use unsupervised methods to identify distinct customer groups. For each group, describe their characteristics and recommend a marketing strategy. Present in a slide deck with visualizations [^glassdoor-uber-ds]


### SQL Case Studies

- Given a schema with tables [users, orders, products, sessions], answer these 5 business questions using SQL. Questions range from basic aggregations to complex window functions and cohort analyses. Time limit: 90 minutes [^glassdoor-google-ds]

- Write SQL queries to build a weekly KPI dashboard for a subscription product. The schema includes [subscriptions, payments, user_activity, support_tickets]. Required metrics: weekly active users, churn rate, MRR, average revenue per user, support tickets per user [^glassdoor-meta-ds]

- Given a database of marketplace transactions, write queries to: (1) calculate seller performance scores, (2) identify the top 10 sellers at risk of leaving the platform, (3) build a cohort retention table for buyers. Time limit: 2 hours [^glassdoor-uber-ds]

- Write SQL to investigate why revenue dropped 12% last month. The schema includes [orders, users, products, marketing_campaigns, pricing_changes]. Your analysis should include at least 5 queries, each answering a specific hypothesis [^interviewquery-takehome]

- Given a schema for an e-learning platform [users, courses, enrollments, completions, ratings], write queries to answer: What is the course completion rate by category? Which courses have the highest drop-off between enrollment and first lesson? What predicts course satisfaction? [^glassdoor-spotify-ds]


### Presentation Deliverables

A subset of companies require a formal presentation as part of the take-home.

- Analyze the provided dataset and prepare a 20-minute presentation for the data science team. The presentation should cover: your approach, key findings, statistical methods used, business recommendations, and limitations. Prepare for 15 minutes of Q&A [^glassdoor-netflix-ds]

- Given a dataset and a business question, prepare a 10-slide deck targeted at a non-technical product team. The deck should tell a clear story: what is the question, what does the data show, and what should we do. Submit slides and a Jupyter notebook with supporting analysis [^glassdoor-airbnb-ds]

- Analyze a month of product data and prepare two deliverables: (1) a technical Jupyter notebook with your full analysis, (2) a 3-page executive summary written for a VP of Product who does not read code [^glassdoor-google-ds]

- Prepare a "data review" presentation: given 3 months of engagement data for a mobile app, present a 15-minute analysis that identifies the 3 most important trends and proposes 3 actionable recommendations. Practice defending your methodology in Q&A [^glassdoor-meta-ds]


### Evaluation Criteria Found in Assignments

Many assignments include explicit evaluation criteria. Patterns across reports:

- Analytical rigor: does the candidate choose appropriate statistical methods, check assumptions, and acknowledge limitations
- Data quality awareness: does the candidate identify and handle data quality issues (missing values, outliers, selection bias) before drawing conclusions
- Communication clarity: is the analysis well-structured, clearly narrated, and accessible to the target audience (technical or non-technical)
- Business relevance: does the candidate connect findings to actionable business decisions, not just produce charts and statistics
- Code quality: is the notebook organized, well-commented, and reproducible
- Statistical correctness: are tests applied correctly, are p-values interpreted properly, are confidence intervals used appropriately
- Weighted rubrics: some assignments provide explicit scoring, for example 30.0% analytical rigor, 25.0% communication, 25.0% business impact, 20.0% code quality


## How to Prepare

The best submissions share these traits:

- Ask clarifying questions before starting. Double your time estimate
- Start with the business question, not the model. Frame every analysis around what decision it informs
- Show your exploration process. Include dead ends and why you abandoned them. This demonstrates real analytical thinking
- Check data quality first. Before any analysis, profile the data: missing values, distributions, outliers, duplicate records. Report what you found
- Use simple methods first. A well-executed EDA with clear insights beats a poorly explained neural network
- Include a 5-minute Loom video walkthrough of your submission if allowed
- Make your analysis actionable: one strong recommendation with clear next steps beats a list of 10 generic findings
- Show statistical rigor without over-engineering. If a t-test answers the question, do not build a Bayesian hierarchical model
- Include limitations and next steps. What would you do with more time? What assumptions could be violated?
- Connect analysis to business outcomes: revenue, retention, engagement, cost reduction

Common mistakes:

- Not asking clarifying questions before starting
- Jumping straight to modeling without exploring the data first
- Submitting a notebook with no narrative - just code and charts without explanation
- Over-fitting a model on the take-home data and reporting inflated metrics
- Ignoring data quality issues that the interviewer planted deliberately
- Not preparing for the defence round: the follow-up interview is often more important than the notebook itself
- Writing for a technical audience when the prompt asks for a business recommendation (or vice versa)
- Submitting work that is clearly AI-generated without evidence of personal analytical judgment


## Sources

[^glassdoor-google-ds]: [Glassdoor - Google Data Scientist Interview](https://www.glassdoor.com/Interview/Google-Data-Scientist-Interview-Questions-EI_IE9079.0,6_KO7,21.htm)
[^glassdoor-meta-ds]: [Glassdoor - Meta Data Scientist Interview](https://www.glassdoor.com/Interview/Meta-Data-Scientist-Interview-Questions-EI_IE40772.0,4_KO5,19.htm)
[^glassdoor-netflix-ds]: [Glassdoor - Netflix Data Scientist Interview](https://www.glassdoor.com/Interview/Netflix-Data-Scientist-Interview-Questions-EI_IE11891.0,7_KO8,22.htm)
[^glassdoor-airbnb-ds]: [Glassdoor - Airbnb Data Scientist Interview](https://www.glassdoor.com/Interview/Airbnb-Data-Scientist-Interview-Questions-EI_IE391850.0,6_KO7,21.htm)
[^glassdoor-uber-ds]: [Glassdoor - Uber Data Scientist Interview](https://www.glassdoor.com/Interview/Uber-Data-Scientist-Interview-Questions-EI_IE575263.0,4_KO5,19.htm)
[^glassdoor-spotify-ds]: [Glassdoor - Spotify Data Scientist Interview](https://www.glassdoor.com/Interview/Spotify-Data-Scientist-Interview-Questions-EI_IE408251.0,7_KO8,22.htm)
[^glassdoor-stripe-ds]: [Glassdoor - Stripe Data Scientist Interview](https://www.glassdoor.com/Interview/Stripe-Data-Scientist-Interview-Questions-EI_IE671932.0,6_KO7,21.htm)
[^interviewquery-takehome]: [InterviewQuery - DS Take-Home Questions](https://www.interviewquery.com/questions?tag=take-home)
[^reddit-ds-takehome]: [Reddit r/datascience - Take-Home Projects](https://www.reddit.com/r/datascience/) (r/datascience)
