# Data Scientist Role: Reality vs. Job Postings

Based on real discussions from Reddit, Blind, and X, and conversations with hiring managers and candidates. Complements the quantitative job analysis with qualitative insights from what people actually report once they are in the role.

From a DS hiring manager I spoke with: "the JD said 'build cutting-edge ML models.' The actual job was 80% writing SQL queries, cleaning data, and making slides for the VP. The ML model part was maybe 10% of the work, and it was gradient boosted trees, not deep learning."


## Data Scientist vs MLE vs DA: The Confusion

Problem: Titles are misaligned. Recruiters post "Data Scientist" but mean Data Analyst, or companies hire a DS but need an MLE.

Consensus from discussions:

- Data Scientists focus on statistical analysis, modeling, and experimentation
- MLEs focus on model deployment, infrastructure, and production systems
- Data Analysts focus on dashboards, reporting, and business metrics
- "Data Scientist" is often just a rebrand driven by the data hype cycle


### What People Actually Report

- Applying for Data Scientist -> Get asked only SQL and dashboard questions (it was a DA role)
- Expecting to build ML models -> Asked to maintain legacy Excel reports
- Wanting research work -> Evaluated on stakeholder management and product sense
- Hired as "Senior Data Scientist" -> Spend 70% of time in meetings and writing documents


## What Data Scientists Actually Do

### Three Primary Work Types

Analytics and Insight Generation (~50%): SQL, dashboards, ad hoc analysis
- Writing hundreds of SQL queries per week to answer stakeholder questions
- Building and maintaining dashboards in Tableau, Looker, or Mode
- Conducting deep-dive analyses when metrics move unexpectedly
- Presenting findings to product, engineering, and leadership
- Defining success metrics for product launches

Experimentation and Causal Inference (~30%): A/B tests, quasi-experiments
- Designing experiments with proper sample sizes and success metrics
- Analyzing experiment results and making ship/no-ship recommendations
- Building experimentation tooling and best practices for the team
- Applying causal methods when randomization is not possible

Model Building (~20%): ML models for production or strategic decisions
- Training classification and regression models
- Feature engineering and feature store development
- Model evaluation and offline/online testing
- Working with MLEs to deploy models to production


### Day-to-Day vs. Assumptions

- "Build deep learning models" -> Writing SQL and building Looker dashboards
- "Apply cutting-edge ML" -> XGBoost with carefully engineered features
- "Research-oriented" -> Delivering weekly metric reviews to the VP
- "Work on NLP" -> Text cleaning and regex before any modeling starts


### The Decision Loop

Real challenges people report:

- Navigating why leadership ignored a statistically significant experiment result
- Cleaning data for weeks before any analysis can begin
- Explaining p-values to a PM who wants a yes/no answer in 5 minutes
- Handling the politics of being the "bearer of bad news" when data contradicts strategy


## Jobs vs. Reality Gap

| Dimension | Job Postings Say | People Actually Experience |
|-----------|------------------|---------------------------|
| Deep learning | Often mentioned | Rarely used - most models are gradient boosted trees or logistic regression |
| SQL | Sometimes mentioned | The primary daily tool - used more than Python in many analytics roles |
| Communication | "Strong communication skills" | The single most important differentiator for career growth |
| Research | Mentioned in 20%+ of postings | Less than 5% of roles do actual research |
| Python | Always required | Used heavily, but SQL often accounts for more daily work |


## The "Full-Stack DS" Problem

Common complaint: Jobs demand statistics, ML, engineering, product sense, and communication all at once.

Reality: "Data Scientist" often means:

- Data Analyst (SQL, dashboards, business metrics)
- ML Engineer (model deployment, infrastructure, pipelines)
- Statistician (experimental design, causal inference)
- Product Analyst (metrics definition, feature impact analysis)
- Or actual Data Scientist (some blend of the above)


## Key Takeaways

1. Titles are broken: "Data Scientist" means different things at different companies
2. SQL and communication win: The most successful data scientists are the ones who can query data and explain findings clearly, not the ones with the best Kaggle scores
3. Experimentation is the real differentiator: Anyone can fit an XGBoost model. Designing a proper experiment and interpreting results correctly is harder and more valuable
4. Production ML is a subset: Most DS roles are analytics-first. If you want to build production models, look for MLE or Applied Scientist titles
5. The gap persists: Job postings describe ambition; the actual work is more pragmatic
