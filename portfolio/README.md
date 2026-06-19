# Portfolio Project Ideas

Project ideas that demonstrate data science skills relevant to the job market. Each project covers patterns that appear frequently in DS job descriptions and interview loops.


## Exploratory Data Analysis: E-commerce Customer Behavior

Analyze customer purchase behavior from a public dataset (e.g., Instacart, Brazilian E-Commerce). Identify segments, patterns, and actionable insights.

Skills demonstrated:

- Data cleaning and preparation with pandas
- Statistical summaries and distribution analysis
- Customer segmentation using RFM analysis
- Visualization with matplotlib and seaborn
- Business recommendations grounded in data evidence

Deliverable: Jupyter notebook with clear narrative, visualizations, and a 1-page executive summary.

Complexity: beginner. Good first DS portfolio project.


## A/B Test Analysis: Feature Launch Evaluation

Design and analyze an A/B test for a product feature change. Use a simulated or public dataset. Define hypothesis, sample size, and success metrics.

Skills demonstrated:

- Experimental design with power analysis and MDE
- Statistical hypothesis testing (t-test, chi-squared, bootstrap)
- Metric definition (primary, secondary, guardrail)
- Handling common pitfalls (multiple comparisons, peeking, novelty effects)
- Ship/no-ship recommendation with confidence intervals

Complexity: intermediate. Shows real-world experimentation skills.


## Predictive Modeling: Customer Churn Prediction

Build an end-to-end churn prediction model. Include feature engineering, model selection, evaluation, and business impact quantification.

Skills demonstrated:

- Feature engineering from raw transactional data
- Model comparison (logistic regression, random forest, XGBoost)
- Evaluation metrics appropriate for imbalanced classes (precision-recall, lift)
- Business impact analysis (cost of false positives vs. false negatives)
- Model interpretability (SHAP values, feature importance)

Complexity: intermediate to advanced.


## SQL Case Study: Product Metrics Dashboard

Build a comprehensive SQL analysis answering real product questions from a database schema.

Skills demonstrated:

- Complex SQL queries (CTEs, window functions, self-joins)
- Cohort retention analysis
- Funnel conversion metrics
- Revenue and growth KPIs
- Query optimization reasoning

Complexity: intermediate. SQL fluency is tested in nearly every DS interview.


## Causal Inference: Measuring a Policy Change

Apply causal inference methods to estimate the effect of a policy change or natural experiment using observational data.

Skills demonstrated:

- Difference-in-differences methodology
- Propensity score matching
- Regression discontinuity design
- Sensitivity analysis and robustness checks
- Clear communication of causal claims and limitations

Complexity: advanced. Demonstrates statistical sophistication.


## NLP Project: Review Sentiment and Topic Analysis

Build a text analytics pipeline on product reviews or support tickets. Extract sentiment, topics, and actionable patterns.

Skills demonstrated:

- Text preprocessing and cleaning
- Sentiment classification (rule-based and ML-based approaches)
- Topic modeling (LDA or embedding-based)
- Visualization of text patterns
- Business recommendations from unstructured data

Complexity: intermediate. NLP appears in 28% of DS job descriptions.


## Interview-Specific Portfolio Tips

From interviews and hiring manager observations:

- Every project should include a clear problem statement, methodology, and business impact. A notebook without context is an incomplete analysis.
- Show your SQL work. Many DS portfolios only show Python. Include SQL queries that demonstrate analytical depth - cohort analyses, funnel metrics, window functions.
- Include evaluation metrics appropriate to the problem. A classification model without precision-recall analysis is incomplete.
- Record a Loom video walking through your analysis for take-home case studies.
- Published writing (Medium, Substack, personal blog) carries weight. A well-written analysis post can replace a traditional portfolio for some hiring managers.

Project ideas that impress in interviews:

1. End-to-end ML pipeline with business impact - from data collection through model deployment through impact measurement
2. A/B test analysis with proper statistical rigor - hypothesis, power analysis, results interpretation, recommendation
3. SQL-based metric investigation - detective work using SQL to diagnose a metric change
4. Causal inference case study - demonstrating you can go beyond correlation
5. Kaggle competition breakdown - not just your score, but your approach, iterations, and learnings


## How to Pick a Project

1. Pick a specific domain (e-commerce, healthcare, fintech, social media)
2. Find a real dataset (Kaggle, UCI ML Repository, public APIs, company data challenges)
3. Frame a real business question
4. Build the analysis end-to-end: exploration, modeling, evaluation, communication
5. Write it up for two audiences: a peer who will check your methodology, and a hiring manager who has 5 minutes

Build 5-6 focused projects rather than one massive analysis. Spend 1-2 weeks on each. Cover different competencies: one on EDA, one on experimentation, one on ML modeling, one on SQL, one on causal inference.

For more on structuring DS portfolio projects, see [The 0→1 Data Scientist Interview Playbook](https://valenx.org/books/ds).
