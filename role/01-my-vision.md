# My Vision of the Data Scientist Role

Based on my experience as an Amazon AI/Robotics Lead PM, working alongside data science teams building products from zero-to-one through scale.

This is my personal vision of the role. To see how it compares with what companies actually look for, I analyzed 1,350+ job descriptions - the rest of this [role section](README.md) is based on that research.


## Core Responsibility

- Turning raw data into decisions that move the business forward
- Working with engineering, product, and business teams to identify problems worth solving with data
- Building the analytical and modeling infrastructure that makes data-driven decisions possible at scale
- Not "let me train a model because it's cool" - starts from a real business problem with real data


## Beyond "Just Build a Model"

Even for a seemingly simple task like predicting customer churn, professional data science requires:

1. Problem framing - understand the business context, define what "churn" actually means for this product, align with stakeholders on success criteria
2. Data exploration - audit available data sources, assess data quality, identify gaps and biases
3. Feature engineering - transform raw data into predictive signals, handle missing values, create interaction features
4. Experimentation - test multiple approaches (logistic regression, gradient boosting, neural nets), validate assumptions
5. Evaluation - define appropriate metrics (precision-recall tradeoff, business cost matrix), test on held-out data
6. Deployment - work with engineering to productionize the model, set up monitoring for drift
7. Impact measurement - A/B test the intervention, measure actual business impact vs. predicted impact
8. Iteration - retrain on new data, handle concept drift, expand to new segments
9. Communication - present findings to stakeholders who do not speak statistics
10. Documentation - version control models, log experiments, maintain reproducibility


## Progressive Complexity

- Simple case: ad hoc analysis -> SQL query -> insight shared in a slide deck
- Analytical product (~5x harder): add experimentation design, causal inference, automated dashboards, cross-team dependencies
- ML system (~10x harder): add model training pipelines, feature stores, real-time inference, monitoring infrastructure, multi-quarter roadmaps


## How It Compares to Other Roles

### vs MLE (Machine Learning Engineer)

- MLEs own the infrastructure and systems that run models in production
- Data scientists own the modeling methodology and experimental design
- MLEs focus on latency, throughput, reliability; data scientists focus on accuracy, bias, business impact
- Some companies merge these roles; at larger companies they are distinct
- MLEs need to add: statistical rigor, experimental design, business framing

### vs Data Analyst (DA)

- DAs focus on descriptive analytics, dashboards, and reporting
- Data scientists add predictive modeling, causal inference, and experimental design
- The boundary is blurring - many analyst roles now expect statistical modeling skills
- DAs need to add: ML fundamentals, Python fluency, statistical testing depth

### vs Analytics Engineer

- Analytics Engineers own the data transformation layer (dbt, SQL, data modeling)
- Data scientists consume cleaned data and build models on top of it
- Analytics Engineers focus on data quality and accessibility; data scientists focus on extracting insights and building predictive systems
- Analytics Engineers need to add: statistical methods, ML, experimentation

### What Data Scientists Don't Do

- Build production microservices from scratch
- Own the data warehouse architecture
- Design user interfaces
- Manage people (unless in a DS Manager role)

### What Data Scientists Focus On

- Statistical analysis and hypothesis testing
- Predictive and prescriptive modeling
- Experimental design (A/B tests, multi-armed bandits)
- Translating business questions into quantitative frameworks
- Communicating findings to technical and non-technical audiences


## In Bigger Organizations

- Data science responsibilities often split between DS, MLE, DA, and Analytics Engineer roles
- MLEs: model deployment, inference infrastructure, feature stores
- DAs: dashboards, ad hoc reporting, executive summaries
- Analytics Engineers: data pipelines, transformation, data quality
- Eventually dedicated data scientists own each product domain (search, ads, recommendations, trust and safety)
- Not every data problem needs a data scientist - some are pure engineering or analytics problems
