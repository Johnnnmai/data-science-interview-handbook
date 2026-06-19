# Statistics and Probability Questions

Based on candidate reports from Reddit, Glassdoor, and personal blogs about what they were actually asked in data science interviews.

This section covers knowledge-based questions: "What is X?", "How does X work?", "Explain Y", and applied statistical reasoning problems.


## Format

Typically 45-60 minutes, conversational with some whiteboard or shared-doc work. The interviewer asks conceptual questions to probe your understanding of statistical methods, then follows up with applied scenarios. Some companies present a dataset or scenario and ask you to walk through your analytical approach.

Statistics questions are rarely a standalone "quiz." They typically surface as part of a broader case study, experimental design discussion, or technical screen. The interviewer wants to see if you can apply statistical reasoning to real problems, not recite textbook definitions.


## Interview Questions

Actual questions reported by candidates and interviewers, compiled from blog posts, interview reports, and community discussions.

### Probability Fundamentals

- You flip a fair coin 10 times and get 10 heads. What is the probability the next flip is heads? Why do people get this wrong? [^reddit-ds-prob]
- You have two dice. What is the probability that the sum is 7? What about the probability that at least one die shows a 6, given that the sum is 7? [^glassdoor-google-ds]
- A disease affects 1 in 10,000 people. A test for the disease has a 99% sensitivity and 99% specificity. If a person tests positive, what is the probability they actually have the disease? Walk through your reasoning step by step [^reddit-ds-bayes]
- You are sampling users for a survey. 60% of users are on mobile, 40% on desktop. Mobile users respond at 5%, desktop users at 15%. A response comes in. What is the probability the respondent is a mobile user? [^interviewquery-ds-stats]
- Explain the difference between independent and mutually exclusive events. Give an example of each from a product analytics context [^glassdoor-meta-ds]
- You draw cards from a standard deck without replacement. What is the probability of drawing 3 aces in a row? How does this change if you replace cards after each draw? [^reddit-ds-prob]
- A company sends two versions of an email campaign. Version A goes to 10,000 users, Version B goes to 10,000 users. 500 users in A convert, 520 users in B convert. Is B better? What additional information would you want before making a decision? [^airbnb-ds-interview]

### Distributions

- Explain the difference between normal, binomial, Poisson, and exponential distributions. When would you use each in practice? [^glassdoor-google-ds]
- Your team tracks daily active users. The distribution is right-skewed. Why might this be? What summary statistics would you report instead of the mean? [^reddit-ds-distributions]
- Explain the Central Limit Theorem. Why does it matter for A/B testing? What happens when your sample size is small? [^interviewquery-ds-stats]
- You observe that user session lengths follow a log-normal distribution. How would you compare session lengths between two user groups? Would you use a t-test? Why or why not? [^glassdoor-netflix-ds]
- What is the difference between a probability density function and a cumulative distribution function? Draw both for a normal distribution [^reddit-ds-distributions]
- Your click-through rate data has many zeros (most users do not click). What distribution would you use to model this? How does this affect your choice of statistical test? [^glassdoor-uber-ds]
- Explain what a heavy-tailed distribution is. Give an example from industry data (revenue, session length, order values). Why does this matter for experimentation? [^uber-experimentation]

### Hypothesis Testing

- Explain the full process of hypothesis testing: null hypothesis, alternative hypothesis, test statistic, p-value, significance level, decision. Use a real example from product analytics [^glassdoor-google-ds]
- What is a p-value? What is it not? A PM asks "so the p-value is 0.03, that means there is a 3% chance the result is wrong, right?" How do you respond? [^reddit-ds-pvalue]
- Explain Type I and Type II errors. Which is worse in the context of (a) launching a new feature, (b) a medical trial, (c) a fraud detection system? [^glassdoor-meta-ds]
- You run an A/B test and get a p-value of 0.06. Your PM says "just run it longer until it becomes significant." What is wrong with this approach? [^airbnb-experimentation]
- What is the difference between one-tailed and two-tailed tests? When would you use each? Give a concrete DS scenario [^interviewquery-ds-stats]
- Explain the multiple comparisons problem. You run 20 A/B tests simultaneously. How many would you expect to show statistical significance by chance at alpha = 0.05? What corrections would you apply? [^netflix-experimentation]
- What is the difference between a parametric and a non-parametric test? When would you choose a Mann-Whitney U test over a t-test? [^glassdoor-spotify-ds]
- You are testing a new recommendation algorithm. Your primary metric is revenue per user. The test shows a 2% lift with p = 0.04. But average order value dropped 5% (p = 0.01). What do you do? [^reddit-ds-conflicting]

### Confidence Intervals

- Explain what a 95% confidence interval means. A stakeholder says "there is a 95% probability the true value is in this interval." Is that correct? [^glassdoor-google-ds]
- You report a confidence interval of [2.1%, 4.3%] for the lift from a new feature. Your PM asks if the feature is worth launching. What additional context do you need to answer that question? [^reddit-ds-ci]
- How does sample size affect the width of a confidence interval? How does variance affect it? If you wanted to halve the width, how much larger would your sample need to be? [^interviewquery-ds-stats]
- What is the relationship between confidence intervals and hypothesis testing? If the 95% CI for the difference between two groups includes zero, what does that mean for your hypothesis test? [^glassdoor-meta-ds]
- When would you use a bootstrap confidence interval instead of an analytical one? Describe the procedure [^reddit-ds-bootstrap]

### Power Analysis

- What is statistical power? Why does it matter before you run an experiment? [^glassdoor-airbnb-ds]
- Your PM wants to run an A/B test to detect a 1% improvement in conversion rate (baseline 5%). Your traffic is 100,000 users per week. How long do you need to run the test? Walk through the calculation conceptually [^netflix-experimentation]
- What are the four components of a power analysis? How do they relate to each other? [^interviewquery-ds-stats]
- You ran a test for 2 weeks and saw no significant result. Your PM asks "does this mean the treatment has no effect?" How do you respond? [^reddit-ds-power]
- How does minimum detectable effect (MDE) relate to business decisions? Who should decide the MDE - the data scientist or the PM? [^airbnb-experimentation]
- Your A/B test platform shows that you need 500,000 users per variant to detect a 0.5% lift. You only have 50,000 users per week. What are your options? [^uber-experimentation]

### Bayesian Reasoning

- Explain the difference between frequentist and Bayesian approaches to hypothesis testing. When would you prefer one over the other? [^glassdoor-google-ds]
- What is a prior? How do you choose a prior in practice? What happens if you choose a bad prior? [^reddit-ds-bayesian]
- Explain Bayes' theorem using a real example from product analytics (spam detection, user classification, conversion prediction) [^interviewquery-ds-stats]
- Your company uses a Bayesian A/B testing framework. Your PM asks "what is the probability that variant B is better than variant A?" How does this differ from a frequentist p-value? [^glassdoor-netflix-ds]
- What are conjugate priors and why are they useful in practice? [^reddit-ds-bayesian]
- You have a prior belief that a new feature will improve conversion by 2% (based on similar past features). Your A/B test data shows a 3% improvement. How would a Bayesian approach combine these? [^glassdoor-spotify-ds]

### Regression

- Explain the assumptions of linear regression. How do you check each one? What happens if they are violated? [^glassdoor-google-ds]
- What is multicollinearity? How do you detect it? Why does it matter? [^interviewquery-ds-stats]
- What is the difference between R-squared and adjusted R-squared? When would they diverge significantly? [^glassdoor-meta-ds]
- Explain regularization in regression. What is the difference between L1 (Lasso) and L2 (Ridge) regularization? When would you use each? [^reddit-ds-regression]
- You build a logistic regression to predict user churn. The model has high accuracy (95%) but poor recall (20%). What is happening and how would you fix it? [^glassdoor-airbnb-ds]
- What is the difference between correlation and causation? Give a concrete example from industry data where a strong correlation would be misleading [^reddit-ds-causal]
- Explain heteroscedasticity. How do you detect it and what are the consequences for your regression coefficients? [^glassdoor-uber-ds]
- You have a dataset with 50 features and 500 observations. What problems might arise if you run a standard linear regression? What would you do instead? [^interviewquery-ds-stats]

### Experimental Design

- You want to test a new checkout flow. How do you design the experiment? Cover: randomization unit, sample size, duration, primary and secondary metrics, guardrail metrics [^airbnb-experimentation]
- What is an A/A test and why would you run one? [^netflix-experimentation]
- Explain the difference between a randomized controlled trial and a quasi-experiment. When would you use each? [^glassdoor-netflix-ds]
- What is the novelty effect? How do you account for it in your experiment? [^uber-experimentation]
- You are running an experiment on a two-sided marketplace. Treating one side randomly could create interference effects. How do you handle this? [^airbnb-experimentation]
- Your experiment ran for 4 weeks. The first week showed a 5% lift. By week 4, the lift was 1%. What might explain this pattern? [^reddit-ds-experiment]
- How do you handle multiple metrics in an experiment? If your primary metric improves but a guardrail metric degrades, what is your decision framework? [^netflix-experimentation]
- What is Simpson's paradox? Give an example from A/B testing where aggregated results could mislead you [^glassdoor-google-ds]

### Causal Inference

- What are the assumptions required for a difference-in-differences analysis? How do you validate the parallel trends assumption? [^glassdoor-netflix-ds]
- Explain instrumental variables. Give a real-world example of a valid instrument [^reddit-ds-causal-methods]
- What is propensity score matching? When would you use it? What are its limitations? [^glassdoor-airbnb-ds]
- You launched a feature to all users in California but not in other states. Your PM wants to know if the feature caused a 10% increase in engagement. How would you analyze this? [^uber-experimentation]
- What is the difference between average treatment effect (ATE) and conditional average treatment effect (CATE)? Why does the distinction matter for product decisions? [^netflix-causal-ds]
- Explain regression discontinuity design. Give an example of where it would apply in a product context [^glassdoor-netflix-ds]
- You cannot randomize users into treatment and control for ethical reasons. What observational causal methods would you consider? List the assumptions each requires [^reddit-ds-causal-methods]


## How to Prepare

Focus on applied reasoning over formula memorization. Interviewers care more about when and why you would use a method than whether you can derive it mathematically.

- Probability: practice conditional probability and Bayes' theorem with real scenarios. The disease/test question appears in some form at nearly every company
- Hypothesis testing: be able to explain p-values, Type I/II errors, and power in plain language. Know when a t-test is wrong
- Experimental design: practice end-to-end experiment design: question, hypothesis, randomization, metrics, sample size, duration, analysis plan, decision criteria
- Causal inference: for senior roles, know at least 3 methods (diff-in-diff, propensity matching, instrumental variables) and when each applies
- Regression: know assumptions, violations, and how to diagnose them. This is still a common interview topic

Common mistakes:

- Reciting definitions without showing when you would use each method in practice
- Not discussing assumptions and limitations when describing a method
- Ignoring practical considerations: sample size constraints, business context, metric selection
- Treating statistical significance as the only criterion for a decision

See also: https://github.com/alexeygrigorev/data-science-interviews


## Sources

[^reddit-ds-prob]: [Reddit r/datascience - Probability Questions in DS Interviews](https://www.reddit.com/r/datascience/) (r/datascience)
[^glassdoor-google-ds]: [Glassdoor - Google Data Scientist Interview Questions](https://www.glassdoor.com/Interview/Google-Data-Scientist-Interview-Questions-EI_IE9079.0,6_KO7,21.htm)
[^reddit-ds-bayes]: [Reddit r/datascience - Bayesian Interview Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^interviewquery-ds-stats]: [InterviewQuery - DS Statistics Questions](https://www.interviewquery.com/questions?tag=statistics)
[^glassdoor-meta-ds]: [Glassdoor - Meta Data Scientist Interview](https://www.glassdoor.com/Interview/Meta-Data-Scientist-Interview-Questions-EI_IE40772.0,4_KO5,19.htm)
[^airbnb-ds-interview]: [Airbnb Engineering Blog - Experimentation](https://medium.com/airbnb-engineering/experiments-at-airbnb-e2db3abf39e7)
[^reddit-ds-distributions]: [Reddit r/datascience - Distribution Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^glassdoor-netflix-ds]: [Glassdoor - Netflix Data Scientist Interview](https://www.glassdoor.com/Interview/Netflix-Data-Scientist-Interview-Questions-EI_IE11891.0,7_KO8,22.htm)
[^glassdoor-uber-ds]: [Glassdoor - Uber Data Scientist Interview](https://www.glassdoor.com/Interview/Uber-Data-Scientist-Interview-Questions-EI_IE575263.0,4_KO5,19.htm)
[^uber-experimentation]: [Uber Engineering - XP Experimentation Platform](https://www.uber.com/blog/xp/)
[^reddit-ds-pvalue]: [Reddit r/datascience - P-Value Misconceptions](https://www.reddit.com/r/datascience/) (r/datascience)
[^airbnb-experimentation]: [Airbnb Engineering - Experimentation at Scale](https://medium.com/airbnb-engineering/)
[^netflix-experimentation]: [Netflix Tech Blog - Experimentation](https://netflixtechblog.com/)
[^glassdoor-spotify-ds]: [Glassdoor - Spotify Data Scientist Interview](https://www.glassdoor.com/Interview/Spotify-Data-Scientist-Interview-Questions-EI_IE408251.0,7_KO8,22.htm)
[^reddit-ds-conflicting]: [Reddit r/datascience - Conflicting Metrics](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-ci]: [Reddit r/datascience - Confidence Intervals](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-bootstrap]: [Reddit r/datascience - Bootstrap Methods](https://www.reddit.com/r/datascience/) (r/datascience)
[^glassdoor-airbnb-ds]: [Glassdoor - Airbnb Data Scientist Interview](https://www.glassdoor.com/Interview/Airbnb-Data-Scientist-Interview-Questions-EI_IE391850.0,6_KO7,21.htm)
[^reddit-ds-power]: [Reddit r/datascience - Power Analysis](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-bayesian]: [Reddit r/datascience - Bayesian Methods](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-regression]: [Reddit r/datascience - Regression Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-causal]: [Reddit r/datascience - Correlation vs Causation](https://www.reddit.com/r/datascience/) (r/datascience)
[^reddit-ds-experiment]: [Reddit r/datascience - Experiment Design](https://www.reddit.com/r/datascience/) (r/datascience)
[^netflix-causal-ds]: [Netflix Tech Blog - Causal Inference](https://netflixtechblog.com/)
[^reddit-ds-causal-methods]: [Reddit r/datascience - Causal Inference Methods](https://www.reddit.com/r/datascience/) (r/datascience)
