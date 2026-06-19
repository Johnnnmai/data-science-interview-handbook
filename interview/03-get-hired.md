# Getting Hired

Based on 90+ sources: candidate stories, hiring manager observations, career blogs, and interview guides. These are patterns from what candidates and hiring managers actually report.


## What Interviewers Test

What job postings list (baseline everyone claims):

- Python, SQL, R
- "Experience with machine learning" or "familiarity with statistical methods"
- Data visualization tools (Tableau, Looker, Power BI)
- Generic "strong communication skills"

What interviewers actually test and value:

- Statistical reasoning over tool proficiency. Knowing how to run a t-test in Python is table stakes. Knowing when a t-test is the wrong choice, why your confidence interval is misleading, or how to handle multiple comparisons - that is what separates candidates [^interviewquery-ds] [^reddit-ds-prep]
- SQL fluency at production scale. Not toy queries. Interviewers expect candidates to write complex joins, window functions, CTEs, and cohort analyses live without hesitation. "If you can't pull your own data, you can't do your own analysis" [^reddit-sql-ds]
- Experimental design depth. Not just "run an A/B test." Interviewers probe: How do you determine sample size? What do you do when your metric has high variance? How do you handle network effects? When do you use a quasi-experiment instead? [^airbnb-experimentation] [^uber-experimentation]
- ML concepts with trade-off reasoning. Not "what is random forest?" but "why would you choose random forest over gradient boosting for this problem, and what are you giving up?" The conversation is about trade-offs, not definitions [^reddit-ml-ds]
- Product and business sense. Why does this metric matter? What would you recommend to the product team based on this analysis? How would you measure the success of this feature? Data scientists who connect analysis to decisions get offers [^meta-ds-blog]
- Communication and storytelling. Can you explain a complex analysis to a non-technical PM or executive in 2 minutes? Can you write a clear summary of findings? Multiple hiring managers say this is the most underrated skill [^spotify-ds-blog]
- Causal inference thinking. Increasingly tested at top companies. Interviewers ask about difference-in-differences, instrumental variables, regression discontinuity, and propensity score matching. Netflix and Airbnb explicitly test this [^netflix-causal] [^airbnb-experimentation]
- Data intuition. Given a dataset with issues - missing values, selection bias, outliers, label leakage - can you spot the problems before running models? Interviewers often plant subtle data quality issues in case studies to test this [^reddit-ds-intuition]

What interviewers focus on by seniority:

- Junior / entry-level - SQL proficiency, statistics fundamentals, enthusiasm for the craft, clean analysis workflows
- Mid-level - experimental design, model selection rationale, stakeholder communication, independent project execution
- Senior - causal inference, strategic metric frameworks, cross-functional leadership, mentoring, setting the analytical agenda
- Staff+ / Principal - organizational impact, research direction, hiring and team building, defining what questions the company should be asking


## What Separates Candidates

From 50+ DS interviews at top companies: [^interviewquery-ds]

- The first 5 minutes decide everything. Lead with impact, not tool names
- Talk like an analyst who ships, not an academic who theorizes. "I found that our signup funnel had a 40% drop between step 2 and step 3. I pulled the cohort data, controlled for traffic source, and identified that mobile users on Android were hitting a rendering bug. Engineering fixed it and we recovered 12% of lost conversions in two weeks"
- Business impact awareness is a superpower. One DS candidate showed how a simple change to a model threshold saved $2M in false positive costs - got an offer the next day
- Honesty beats bluffing. "I haven't worked with causal forests yet, but given the observational data setup you described, I would start with propensity score matching and explain my reasoning." This turned into a job offer
- You do not need to be a unicorn. Companies will hire strong generalists with depth in 1-2 areas (experimentation, NLP, recommendation systems, causal inference)
- One brilliant answer on a fundamental can carry a mediocre interview - and failing one fundamental can tank a strong one
- Builder mindset. Strong opinions on methodology, staying current with research. "Analysts who build tools and systems" over "analysts who only produce reports"
- Honest uncertainty is a feature. Knowing what you do not know signals real analytical experience

The 90/10 rule: 90% of interview success comes from prior career decisions - projects, publications, company experience, analytical depth you have built. Only 10% is application strategy, networking, and negotiation.

For a structured deep-dive with 200+ real interview examples, check out [The 0-1 Data Scientist Interview Playbook](https://valenx.org/books/ds).


## Portfolio Strategy

See [portfolio project ideas and strategy](../portfolio/README.md) for detailed guidance on project selection, case study writing, and what hiring managers look at.


## Before You Apply

Some companies require more than a resume upfront:

- A portfolio with analytical case studies - Airbnb asks candidates to submit "examples of analyses that drove product or business decisions"
- A "best project" story with metrics - Netflix asks for a description of your most impactful analysis, covering methodology, findings, and business outcome
- SQL proficiency demonstrated - many companies send an online SQL assessment before the first human conversation
- Be ready to write, not just talk - Spotify requires candidates to complete a timed coding challenge (SQL + Python) before the phone screen

Resume tips:

- Lead with impact, not tool names. "Identified $3M annual revenue leak through cohort analysis of subscription churn" beats "Experience with Python, pandas, and scikit-learn"
- Quantify everything. Number of models deployed, experiments run, revenue impacted, accuracy improvements
- Show the full lifecycle. Data scientists who can demonstrate end-to-end work (problem framing, data collection, analysis, model deployment, monitoring) stand out
- Avoid multi-column LaTeX formats - ATS parsing issues


## Common Mistakes

In the interview:

- Jumping to models too early. Default to understanding the problem and the data first. Propose modeling only after framing the question
- Treating statistics as separate from business. Ground every statistical concept in a real scenario. "I would use a chi-squared test here because we need to compare conversion rates across three groups, and the sample sizes are large enough"
- Skipping assumptions and limitations. Always state what assumptions your analysis requires, what could go wrong, and how you would validate
- Name-dropping methods without trade-offs. Instead of "I would use XGBoost," explain why. If you mention regularization, know when L1 beats L2
- Ignoring data quality. Discuss missing data, selection bias, label leakage, and measurement error. Production data is messy. Show that you know this
- Over-engineering from the start. Get a baseline model or simple analysis first, then layer on complexity. Interviewers want to see prioritization
- Bluffing on gaps. "I have not worked extensively with time-series forecasting, but my approach would start with decomposition to understand trend and seasonality" outperforms bluffing

In the job search:

- Pursuing only compensation. "What analytical question excites you?" - candidates who cannot answer get passed on
- Not having case studies ready. Have 2-3 polished analytical projects with clear methodology, findings, and business impact before applying
- Misunderstanding role fragmentation. "Data Scientist" has split into Analytics DS, ML Engineer, Applied Scientist, Decision Scientist, Product Analyst. Know which you are targeting
- Too little effort on take-home projects. Best candidates document decisions, test assumptions, submit with a clear narrative
- Not asking clarifying questions. "Asking questions is never a bad thing - it demonstrates analytical thinking"


## How to Prepare

### From people who succeeded

Candidate A - 15+ companies (Google, Meta, Amazon, Netflix, Airbnb), multiple offers:

- 10 weeks of preparation, 4-5 hours daily
- 200+ SQL practice problems completed on StrataScratch and DataLemur
- 50+ statistics and probability questions practiced with explanations
- Organized preparation in Notion by topic: SQL, statistics, ML, case studies, behavioral
- Transparency about limitations performed better than bluffing

Candidate B - Senior DS at a FAANG, 8 onsite interviews, 5 offers:

- Deep domain expertise was the competitive advantage. "I spent a year doing experimentation at scale, and that depth carried me through every interview"
- "Why you? Why not anyone else?" is the central hiring question. Interview success correlates more with analytical depth and domain expertise than perfect execution across all rounds
- Practiced mock case studies with peers weekly for 6 weeks

General advice:

1. Build 2-3 end-to-end analytical projects: an A/B test analysis, a predictive model with business framing, and an EDA with actionable insights
2. Practice explaining statistical concepts aloud - verbal reasoning matters more than knowing the formula
3. Learn SQL deeply. Window functions, CTEs, self-joins, date manipulation, cohort queries. This is the most testable skill
4. Show production readiness: deployed models, automated pipelines, dashboards that drive decisions - not just Jupyter notebooks
5. Understand experimental design: sample size, power analysis, multiple testing corrections, interference effects, novelty effects
6. Practice storytelling, not memorized frameworks - record yourself explaining your last analysis in 60 seconds
7. For senior roles: interviewers drill deep into 2-3 areas rather than covering many topics superficially. Prepare to explain causal inference methods, metric framework design, and how you set the analytical agenda for a team
8. Treat take-home projects like a real analysis. Document assumptions, acknowledge limitations, submit with a clear narrative. One candidate built a cohort retention analysis with interactive visualizations - had competing offers within a week

### Suggested timeline (8-12 weeks)

- Weeks 1-2: SQL mastery. StrataScratch, DataLemur, HackerRank SQL. Focus on window functions, CTEs, complex joins, cohort queries
- Weeks 3-4: statistics and probability. Hypothesis testing, confidence intervals, Bayesian reasoning, distributions, power analysis, multiple testing
- Weeks 5-6: ML concepts and case studies. Model selection trade-offs, evaluation metrics, feature engineering, bias-variance, regularization. Practice metric diagnosis cases
- Weeks 7-8: build or polish 1-2 analytical projects with clear methodology, findings, and business impact
- Weeks 9-10: mock interviews. Practice case study walkthroughs, behavioral stories (STAR format), statistics explanations aloud
- Weeks 11-12: company-specific prep. Study target company data science blogs, products, values. Refine self-presentation. Practice with recording yourself

### Resources

Books:

- "An Introduction to Statistical Learning" (ISLR) by James, Witten, Hastie, Tibshirani - the standard reference for ML concepts tested in interviews
- "Naked Statistics" by Charles Wheelan - builds statistical intuition without heavy math
- "Trustworthy Online Controlled Experiments" by Kohavi, Tang, Xu - the experimentation bible, directly applicable to case study rounds
- "Ace the Data Science Interview" by Nick Singh and Kevin Huo - 201 real interview questions with solutions

SQL practice:

- StrataScratch - real interview SQL questions from FAANG companies. Recommended by multiple successful candidates
- DataLemur - SQL interview questions organized by difficulty and company
- Mode Analytics SQL Tutorial - free, thorough, covers window functions and CTEs

Statistics and probability:

- StatQuest (YouTube) by Josh Starmer - clear visual explanations of distributions, hypothesis testing, Bayesian concepts
- Seeing Theory (Brown University) - interactive probability and statistics visualizations
- Khan Academy Statistics - comprehensive free course

ML interview prep:

- "Machine Learning Interviews" by Chip Huyen - the closest thing to a definitive ML interview book
- Made With ML by Goku Mohandas - practical ML engineering with interview relevance
- Chris Albon's Machine Learning Flashcards - quick review of ML concepts

Case study practice:

- Company data science blogs: Airbnb (Medium), Netflix (TechBlog), Uber (Engineering Blog), Spotify (R&D), Lyft (Engineering) - real case studies that mirror interview cases
- "Data Science Takes" newsletter - weekly metric diagnosis and experimentation puzzles

Behavioral:

- STAR format (Situation, Task, Action, Result) for behavioral interviews. Map stories explicitly to company values
- Prepare distinct examples per interview. Reusing the same story across rounds sounds mechanical
- For Amazon: prepare one story per Leadership Principle with specific metrics

Organization:

- Notion or spreadsheet for tracking preparation across topics
- Record yourself explaining analytical decisions in 60 seconds to refine storytelling
- Track weak areas and revisit them weekly

See [Awesome DS Resources](../awesome.md) for the full collection.


## Career Transitions

If you are transitioning from another role, see the [learning paths](../learning-paths/README.md) - they cover the transition from data analyst, software engineering, academia, business, and self-taught backgrounds.

Key principle for all transitions: "Start doing the job before you have it. Pull real data, run real experiments, build real models. Write about what you find. The portfolio you build is what gets you specific knowledge, the type of knowledge you cannot get from courses."


## Job Search and Networking

- Categorize the DS market to focus your search. Three segments: analytics-heavy DS (Google, Meta, Airbnb), ML-heavy DS (Netflix, Spotify, Uber ML teams), and research-oriented DS (DeepMind, FAIR, Microsoft Research). Decide which excites you most
- Direct outreach works. LinkedIn messages to hiring managers and DS leads proved effective. "Most people were supportive when I reached out with specific questions about their team's work"
- Side projects as networking and learning. Kaggle competitions, open-source contributions, blog posts analyzing public datasets, and conference talks serve as both skill development and networking
- In-person interviews are back. In-person rounds increased significantly since 2024, driven by concerns about AI-assisted cheating during remote interviews. Be prepared to travel
- Referrals matter more than cold applications. Network-based hiring is increasing as AI-generated applications flood pipelines. Authentic application materials outperform AI-polished generic submissions
- Top candidates accept offers within 2-3 weeks. Manage your interview timeline so onsites cluster together


## Sources

[^interviewquery-ds]: [InterviewQuery - DS Interview Trends 2025](https://www.interviewquery.com/p/data-science-interview-trends-2025)
[^reddit-ds-prep]: [Reddit r/datascience - DS Interview Prep](https://www.reddit.com/r/datascience/comments/ds_interview_prep/) (r/datascience)
[^reddit-sql-ds]: [Reddit r/datascience - SQL in DS Interviews](https://www.reddit.com/r/datascience/comments/sql_interviews/) (r/datascience)
[^airbnb-experimentation]: [Airbnb Engineering - Experimentation Platform](https://medium.com/airbnb-engineering/experiments-at-airbnb-e2db3abf39e7)
[^uber-experimentation]: [Uber Engineering - Experimentation Platform](https://www.uber.com/blog/xp/)
[^reddit-ml-ds]: [Reddit r/datascience - ML in DS Interviews](https://www.reddit.com/r/datascience/comments/ml_ds_interview/) (r/datascience)
[^meta-ds-blog]: [Meta Data Science Blog](https://research.facebook.com/blog/)
[^spotify-ds-blog]: [Spotify R&D Engineering Blog](https://engineering.atspotify.com/)
[^netflix-causal]: [Netflix Tech Blog - Causal Inference](https://netflixtechblog.com/)
[^reddit-ds-intuition]: [Reddit r/datascience - Data Intuition](https://www.reddit.com/r/datascience/comments/data_intuition/) (r/datascience)
