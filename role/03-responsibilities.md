# Data Science Responsibilities Analysis

Based on 4,200+ responsibilities extracted from 1,350+ job descriptions.

Methodology note: I collected all responsibilities into a single file and used AI (Claude) to analyze and categorize them. This is not a quantitative analysis like the [skills analysis](02-skills.md) - it is based on the questions I asked and the patterns identified in the data.


## Frequency Guide

| Category | Description |
|----------|-------------|
| Very common | Core responsibility - majority of roles |
| Common | Standard responsibility - many roles |
| Uncommon | Secondary responsibility - some roles |
| Rare | Occasional responsibility - few roles |


## Very Common

### Analyzing Data to Drive Decisions

Problem: Organizations have data but lack the analytical rigor to extract actionable insights from it.

What data scientists do:

- Write SQL queries and build analytical pipelines to answer business questions
- Conduct exploratory data analysis to identify patterns, anomalies, and opportunities
- Build dashboards and reports for key metrics
- Translate business questions into quantitative frameworks
- Present findings to product, engineering, and leadership teams

Core challenge: Separating signal from noise in messy, real-world data while communicating findings clearly enough to influence decisions.


### Designing and Analyzing Experiments

Problem: Companies need to know whether product changes actually work. Intuition is not enough.

What data scientists do:

- Design A/B tests with proper sample size calculations and success metrics
- Analyze experiment results with appropriate statistical tests
- Handle multiple comparison corrections and novelty effects
- Build experimentation infrastructure and best practices
- Advise product teams on experiment design before launch

Core challenge: Maintaining statistical rigor in a fast-moving product environment where stakeholders want quick answers.


### Building Predictive Models

Problem: Products need to anticipate user behavior - who will churn, what they will buy, what content they want to see.

What data scientists do:

- Build classification, regression, and ranking models
- Engineer features from raw data sources
- Evaluate model performance using appropriate metrics
- Work with MLEs to deploy models to production
- Monitor model performance and retrain as needed

Core challenge: Building models that generalize to production data while balancing accuracy, latency, and maintainability.


### Measuring Product Success

Problem: Products launch but teams cannot tell if they actually moved the needle.

What data scientists do:

- Define success metrics and KPI frameworks for products
- Build metrics trees connecting feature-level metrics to business outcomes
- Conduct post-launch analyses measuring actual impact
- Identify leading and lagging indicators
- Build automated alerting for metric anomalies

Core challenge: Defining meaningful metrics that capture real user value rather than vanity metrics that look good but mean nothing.


## Common

### Customer and User Analytics

Problem: Companies need to understand their users at scale - who they are, what they do, why they leave.

What data scientists do:

- Build customer segmentation models
- Analyze user funnels and identify drop-off points
- Build cohort analyses tracking behavior over time
- Conduct churn analysis and build retention models
- Identify "aha moments" that predict long-term engagement

Core challenge: Building a complete picture of user behavior from fragmented data sources while respecting privacy constraints.


### Cross-Functional Partnership

Problem: Data insights are useless if they do not reach the people who make decisions.

What data scientists do:

- Partner with product managers to define metrics and experiment designs
- Work with engineers on data pipeline requirements and model deployment
- Collaborate with marketing on attribution and campaign measurement
- Present to leadership with clear recommendations and trade-offs
- Mentor other team members on data literacy

Core challenge: Communicating statistical concepts to audiences who think in business terms, not p-values.


### Feature Engineering and Data Pipelines

Problem: Raw data is messy. Models need clean, informative features to perform well.

What data scientists do:

- Transform raw data into predictive features
- Build and maintain feature pipelines
- Work with analytics engineers on data quality
- Handle missing data, outliers, and data drift
- Document feature logic and data dependencies

Core challenge: Building features that are both informative for models and maintainable in production.


## Uncommon

### Causal Inference

Problem: Correlation is not causation, but businesses need to know what actually causes outcomes.

What data scientists do:

- Apply quasi-experimental methods (diff-in-diff, regression discontinuity, instrumental variables)
- Build propensity score models for observational studies
- Design natural experiments when A/B tests are not feasible
- Estimate treatment effects with appropriate confidence intervals

Core challenge: Drawing causal conclusions from observational data without the luxury of randomized experiments.


### Search and Recommendations

Problem: Users need to find relevant items in massive catalogs. Default sorting does not work at scale.

What data scientists do:

- Build and evaluate ranking models
- Design recommendation algorithms (collaborative filtering, content-based, hybrid)
- Optimize for relevance, diversity, and serendipity
- Build evaluation frameworks for search quality

Core challenge: Balancing relevance with exploration, and short-term engagement with long-term user satisfaction.


### NLP and Text Analytics

Problem: Vast amounts of unstructured text contain valuable signals - support tickets, reviews, social media.

What data scientists do:

- Build text classification and sentiment analysis models
- Extract entities and relationships from unstructured text
- Build topic models and document clustering
- Apply transformer models for domain-specific NLP tasks

Core challenge: Handling noisy, ambiguous text data while building models that work across domains and languages.


## Rare

### Forecasting and Optimization

Problem: Businesses need to predict demand, optimize pricing, and allocate resources efficiently.

What data scientists do:

- Build time series forecasting models
- Optimize pricing and inventory allocation
- Design and implement supply-demand matching algorithms
- Build simulation models for scenario planning

Core challenge: Forecasting in the presence of structural breaks, seasonality, and external shocks while managing business expectations about prediction uncertainty.


## Key Insights

### 1. Analysis and Communication Dominate Day-to-Day Work

Most data scientists spend more time on exploratory analysis, SQL queries, and stakeholder communication than on model building. The romantic image of training deep learning models all day is a minority of the actual work.

### 2. Experimentation is a Core Skill, Not a Nice-to-Have

Designing and analyzing experiments is a standard data science responsibility. If you cannot design a proper A/B test, you are missing a fundamental part of the job.

### 3. Cross-Functional Work is the Norm

Data science is not a solo activity. Most of the job involves working with product managers, engineers, designers, and leadership. Communication skills are not optional.

### 4. Production ML is Common but Not Universal

About 42% of roles involve building models for production features. The rest focus on analytics, experimentation, and insight generation. Both paths are valid careers.

### 5. Deep Research Roles are Rare

Only 5.1% of roles are pure research. The vast majority of data science jobs require shipping analyses and models that directly impact business decisions.
