# Learning Path for Data Scientists

What to learn and in what order, based on skill demand from 1,350+ DS job descriptions and real hiring data across FAANG, growth-stage, and Series A companies.

For a structured deep-dive with real interview examples, check out [The 0→1 Data Scientist Interview Playbook](https://valenx.org/books/ds).


## Core Skills

The most important 20% that accounts for 80% of the work. Based on hiring manager interviews, DS community surveys, and [job market research](../role/02-skills.md).

### Statistics and Probability

- Distributions - normal, binomial, Poisson, exponential and when each applies
- Hypothesis testing - t-tests, chi-squared, ANOVA, multiple comparison corrections
- Confidence intervals and p-values - what they actually mean and common misinterpretations
- Bayesian reasoning - priors, posteriors, Bayes' theorem applied to real problems
- Regression - linear, logistic, assumptions, diagnostics, interpretation

Practice projects: analyze a real dataset with hypothesis tests, build a regression model and interpret coefficients, simulate sampling distributions

### SQL and Data Manipulation

- Joins, subqueries, CTEs - the foundation of every data science workflow
- Window functions - ranking, running totals, lag/lead for time series
- Aggregation patterns - GROUP BY with HAVING, conditional aggregation
- Performance - query optimization, indexing concepts, handling large tables
- Cohort analysis and funnel queries - the bread and butter of product analytics

Practice projects: solve 50+ SQL problems on StrataScratch or DataLemur, build a cohort retention query from scratch

### Python for Data Science

- pandas and NumPy - data manipulation, cleaning, reshaping
- scikit-learn - classification, regression, clustering, model evaluation
- matplotlib and seaborn - data visualization for exploration and communication
- statsmodels - statistical modeling and hypothesis testing
- Jupyter notebooks - exploratory analysis workflow

Practice projects: complete an end-to-end analysis in a notebook, build and evaluate a classification model

### Machine Learning

- Supervised learning - linear models, decision trees, random forests, gradient boosting
- Unsupervised learning - k-means, hierarchical clustering, PCA, dimensionality reduction
- Model evaluation - cross-validation, precision-recall, ROC-AUC, calibration
- Feature engineering - encoding categoricals, handling missing data, interaction features
- Overfitting and regularization - L1, L2, early stopping, dropout

### Experimentation

- A/B testing - sample size calculation, power analysis, minimum detectable effect
- Causal inference basics - difference-in-differences, propensity score matching
- Experimental pitfalls - peeking, multiple comparisons, novelty effects, network effects
- Metric definition - choosing the right metric, guardrail metrics, proxy metrics

### Communication

- Data storytelling - structuring findings into a narrative
- Visualization best practices - choosing chart types, avoiding clutter, labeling
- Stakeholder management - translating technical findings for business audiences
- Written communication - analysis write-ups, experiment reports, documentation


## Other Skills

Based on the [job market research](../role/02-skills.md). These are not covered in the core path above but frequently appear in job descriptions.

### Deep Learning

- Neural network fundamentals - backpropagation, activation functions, optimization
- NLP basics - text preprocessing, embeddings, transformer architectures
- When to use deep learning vs. simpler models - a critical judgment call

### Data Engineering Literacy

- ETL concepts - how data moves from source to warehouse
- Data modeling basics - star schema, fact and dimension tables
- Spark/PySpark - for when pandas cannot handle the data volume
- Airflow/orchestration - understanding scheduled data pipelines

### Business Fundamentals

- Unit economics - CAC, LTV, payback period, contribution margin
- Product metrics - DAU/MAU, retention, conversion, engagement
- Revenue modeling - subscription, marketplace, advertising
- Market sizing - TAM, SAM, SOM for opportunity estimation

### Domain Knowledge

- Industry-specific patterns - fintech, healthcare, e-commerce, advertising
- Regulatory considerations - GDPR, HIPAA, PII handling
- Ethical AI - fairness, bias detection, model interpretability


## Role-Specific Guides

Already have experience in another field? Start from where you are:

- [From Data Analyst](from-analyst.md) - smoothest transition, add statistics depth and ML, 2-3 months
- [From Software Engineer](from-software-engineer.md) - add statistics, experimental design, and data storytelling, 3-4 months
- [From Academia / PhD](from-academia.md) - add SQL, business framing, and production awareness, 2-4 months
- [From Business / MBA](from-business.md) - add Python, statistics, ML fundamentals, 4-6 months
- [From Self-Taught](from-self-taught.md) - structured path from zero, 6-9 months


## The Typical Data Science Tool Stack

- Languages - Python, SQL, R (some teams)
- Data manipulation - pandas, NumPy, Spark
- ML frameworks - scikit-learn, XGBoost, LightGBM, TensorFlow, PyTorch
- Visualization - matplotlib, seaborn, Plotly, Tableau, Looker
- Experimentation - internal A/B platforms, Optimizely, custom frameworks
- Notebooks - Jupyter, Databricks, Google Colab
- Data warehouses - BigQuery, Snowflake, Redshift, Databricks
- Version control - Git, GitHub
- Orchestration - Airflow, dbt, Dagster


## Skills by Priority

### Must have

- SQL (91.2% of job descriptions)
- Python (94.7% of job descriptions)
- Statistics fundamentals (hypothesis testing, regression, distributions)
- Data visualization and communication
- Experiment design (A/B testing)

### High value

- Machine learning (classification, regression, clustering)
- Feature engineering
- Causal inference methods
- Product analytics and metrics
- Stakeholder communication

### Differentiators

- Deep learning (NLP, computer vision)
- Production ML experience
- Domain expertise (fintech, healthcare, advertising)
- Bayesian methods
- Large-scale data processing (Spark, distributed systems)
