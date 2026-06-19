# Product and Business Case Studies

Based on candidate reports from Reddit, Glassdoor, and personal blogs about what they were actually asked in data science interviews.

This section covers case study questions: metric diagnosis, product analytics, business impact estimation, growth analysis, and user behavior analysis. These questions test your ability to connect data analysis to business decisions.


## Format

Typically 45-60 minutes, conversational. The interviewer presents a business scenario and asks you to walk through your analytical approach. There is no coding in most case study rounds - the interviewer evaluates your thinking process, the questions you ask, the metrics you define, and how you connect analysis to action.

Common formats:

- Metric diagnosis: "X metric dropped Y%. Walk me through your investigation."
- Product analytics: "How would you measure the success of feature Z?"
- Business impact estimation: "Estimate the revenue impact of launching feature W."
- Open-ended analysis: "What would you analyze to help the team decide whether to invest in X?"

The best candidates ask clarifying questions before diving in, structure their approach clearly, and connect every analytical step to a business decision.


## Interview Questions

### Metric Diagnosis

These questions test your ability to systematically investigate an unexpected change in a key metric.

- Daily active users dropped 10% week-over-week. Walk me through your investigation. What data would you pull first? What are your hypotheses? [^glassdoor-meta-ds]

- Conversion rate on the checkout page dropped from 8% to 6% over the last two weeks. The PM is panicked. How do you investigate? [^glassdoor-airbnb-ds]

- Revenue per user increased 15% last month, but total revenue is flat. What could explain this? How would you investigate? [^interviewquery-case]

- The 7-day retention rate for new users improved from 35% to 40%. Before we celebrate, what should we check? [^glassdoor-netflix-ds]

- Average session duration increased by 25%. The PM says users are more engaged. You are skeptical. What alternative explanations would you investigate? [^glassdoor-google-ds]

- App crash rate doubled over the weekend. Engineering says nothing changed. How do you investigate from the data side? [^glassdoor-uber-ds]

- Customer support ticket volume increased 30% but NPS stayed the same. What is happening? [^reddit-ds-case]

- The click-through rate on recommendations improved 20%, but purchases from recommendations dropped 5%. Diagnose the contradiction [^glassdoor-spotify-ds]

- Monthly active users are growing 5% month-over-month, but daily active users are flat. What does this tell you? How would you dig deeper? [^interviewquery-case]


### Product Analytics

These questions test your ability to define success metrics and measurement plans for product features.

- We just launched a new search feature. How would you measure whether it is successful? Define the metrics framework: primary metric, secondary metrics, guardrail metrics [^glassdoor-google-ds]

- The PM wants to redesign the user onboarding flow. How would you design an experiment to test it? What metrics would you track? How long would you run it? [^glassdoor-meta-ds]

- How would you measure the impact of a recommendation system? Consider both short-term engagement and long-term user satisfaction [^glassdoor-netflix-ds]

- We have a freemium product with 2M free users and 50K paid users. The PM wants to change the free tier to encourage upgrades. How would you analyze the trade-offs? [^glassdoor-spotify-ds]

- How would you define and measure "user engagement" for a social media platform? Why is this harder than it sounds? [^glassdoor-meta-ds]

- You are the data scientist for a ride-sharing marketplace. How would you design a metric framework that captures both rider satisfaction and driver satisfaction? What happens when these metrics conflict? [^glassdoor-uber-ds]

- We are considering adding a "share with friends" feature. How would you estimate the potential impact on user growth before building it? [^interviewquery-case]

- How would you evaluate whether a pricing change was successful? What metrics matter beyond revenue? [^glassdoor-airbnb-ds]

- The PM asks "should we invest in improving load time or adding a new feature?" How would you frame this as a data question and provide a recommendation? [^reddit-ds-case]


### Business Impact Estimation

These questions test your ability to estimate the business value of proposed changes using data and reasonable assumptions.

- Estimate the annual revenue impact of reducing checkout page load time by 2 seconds. State your assumptions and show your reasoning [^glassdoor-amazon-ds]

- Our notification system sends 5 emails per week per user. The PM wants to test sending 3 per week instead. How would you estimate the impact on engagement and revenue before running the experiment? [^glassdoor-meta-ds]

- You found that users who complete their profile are 3x more likely to become paying customers. The PM wants to force profile completion during signup. Estimate the business impact and identify the risks [^glassdoor-airbnb-ds]

- We are considering expanding to a new market (country). What data would you analyze to estimate the revenue opportunity? What is your framework for sizing the market? [^glassdoor-uber-ds]

- A machine learning model that predicts customer churn has 80% accuracy. Estimate the value of deploying this model versus the status quo (no prediction, reactive retention) [^interviewquery-case]

- The data team spends 40% of its time answering ad-hoc requests from stakeholders. Estimate the ROI of building a self-service analytics dashboard [^glassdoor-google-ds]

- Our fraud detection system catches 90% of fraudulent transactions but has a 2% false positive rate. The PM wants to tighten the model to catch 95%. Estimate the cost-benefit trade-off [^glassdoor-stripe-ds]


### Growth Analysis

These questions test your understanding of growth mechanics, acquisition funnels, and retention dynamics.

- You notice that 30% of new users drop off within the first 3 days. How would you investigate the root causes? What data would you look at? [^glassdoor-meta-ds]

- Define the "aha moment" for a music streaming service. How would you identify it from data? How would you use it to improve activation? [^glassdoor-spotify-ds]

- Our user acquisition cost has increased 40% year-over-year while retention has stayed flat. What would you analyze? What recommendations might you make? [^interviewquery-case]

- Walk me through how you would build a cohort-based retention analysis for a subscription product. What would the output look like? How would you present it to the product team? [^glassdoor-netflix-ds]

- How would you distinguish between organic growth and paid growth in a marketplace? Why does this distinction matter for long-term strategy? [^glassdoor-uber-ds]

- A referral program gives both the referrer and the new user $10. How would you measure whether the program is creating truly incremental users or just subsidizing users who would have signed up anyway? [^glassdoor-airbnb-ds]

- We see that users from SEO have higher retention than users from paid ads. Should we shift all budget to SEO? Walk through the analytical pitfalls [^reddit-ds-case]


### User Behavior Analysis

These questions test your ability to extract insights from behavioral data and translate them into product recommendations.

- You have access to clickstream data for a news app. What analysis would you run to understand how users discover and consume content? [^glassdoor-google-ds]

- Users of a fitness app have two usage patterns: daily users and weekly users. How would you segment them? Should the product team treat them differently? [^glassdoor-meta-ds]

- You notice that power users (top 10% by engagement) generate 60% of all content on a social platform. How would you investigate whether this is healthy or a risk? [^glassdoor-netflix-ds]

- A food delivery app has users who order 4+ times per week and users who order once per month. Are these the same product? How would you analyze the behavioral differences and recommend product strategy for each segment? [^glassdoor-uber-ds]

- How would you identify users who are likely to churn in the next 30 days? What features would you use? How would you validate your predictions? [^interviewquery-case]

- Users who interact with customer support have 2x higher retention than those who do not. Should we encourage all users to contact support? What is wrong with this reasoning? [^glassdoor-airbnb-ds]

- You have user session data showing that some users spend 5 minutes on a page and others spend 30 seconds. Both convert at similar rates. What could explain this? Should you optimize for shorter sessions? [^reddit-ds-case]


## How to Prepare

The best approach for case study preparation:

- Structure your response. Use a framework: define the question, state your hypotheses, describe the data you need, outline the analysis, discuss trade-offs, and end with a recommendation
- Ask clarifying questions first. "What business outcome are we optimizing for?" "What is the current baseline?" "Are there any known data quality issues?" Asking good questions is half the evaluation
- Think about metrics hierarchically. Start with the north star metric, break it down into components, identify leading and lagging indicators, define guardrails
- Connect every analysis to a decision. "If I find X, I would recommend Y." Do not just describe what you would analyze - describe what you would do with the results
- Acknowledge uncertainty. "My estimate assumes constant conversion rate, but in practice there could be cannibalization effects. I would validate this by looking at..." This signals maturity
- Practice with company data science blogs. Airbnb, Netflix, Spotify, Uber, and Lyft publish real case studies that mirror interview questions closely

Read company DS blogs before your interview:

- Airbnb Engineering (Medium) - experimentation, marketplace metrics, search ranking
- Netflix Tech Blog - causal inference, recommendation evaluation, content analytics
- Spotify R&D Blog - user segmentation, engagement metrics, ML evaluation
- Uber Engineering Blog - marketplace dynamics, geo-spatial analysis, experimentation platform
- Lyft Engineering Blog - pricing, driver supply, experiment design

Common mistakes:

- Jumping to a solution without understanding the problem. Always ask "what business question are we trying to answer?"
- Proposing an analysis without considering how the results would change the decision. If the answer would not change anything, the analysis is not worth doing
- Ignoring selection bias, survivorship bias, and confounding variables. These are the most common analytical pitfalls and interviewers specifically test for them
- Being too vague. "I would look at the data" is not a useful answer. Specify which data, which metrics, which comparisons
- Not considering practical constraints. Data availability, sample size, timeline, organizational buy-in for recommendations

For a structured deep-dive with 200+ real DS case studies, check out [The 0-1 Data Scientist Interview Playbook](https://valenx.org/books/ds).


## Sources

[^glassdoor-meta-ds]: [Glassdoor - Meta Data Scientist Interview](https://www.glassdoor.com/Interview/Meta-Data-Scientist-Interview-Questions-EI_IE40772.0,4_KO5,19.htm)
[^glassdoor-airbnb-ds]: [Glassdoor - Airbnb Data Scientist Interview](https://www.glassdoor.com/Interview/Airbnb-Data-Scientist-Interview-Questions-EI_IE391850.0,6_KO7,21.htm)
[^interviewquery-case]: [InterviewQuery - DS Case Study Questions](https://www.interviewquery.com/questions?tag=case-study)
[^glassdoor-netflix-ds]: [Glassdoor - Netflix Data Scientist Interview](https://www.glassdoor.com/Interview/Netflix-Data-Scientist-Interview-Questions-EI_IE11891.0,7_KO8,22.htm)
[^glassdoor-google-ds]: [Glassdoor - Google Data Scientist Interview](https://www.glassdoor.com/Interview/Google-Data-Scientist-Interview-Questions-EI_IE9079.0,6_KO7,21.htm)
[^glassdoor-uber-ds]: [Glassdoor - Uber Data Scientist Interview](https://www.glassdoor.com/Interview/Uber-Data-Scientist-Interview-Questions-EI_IE575263.0,4_KO5,19.htm)
[^reddit-ds-case]: [Reddit r/datascience - Case Study Questions](https://www.reddit.com/r/datascience/) (r/datascience)
[^glassdoor-spotify-ds]: [Glassdoor - Spotify Data Scientist Interview](https://www.glassdoor.com/Interview/Spotify-Data-Scientist-Interview-Questions-EI_IE408251.0,7_KO8,22.htm)
[^glassdoor-amazon-ds]: [Glassdoor - Amazon Data Scientist Interview](https://www.glassdoor.com/Interview/Amazon-Data-Scientist-Interview-Questions-EI_IE6036.0,6_KO7,21.htm)
[^glassdoor-stripe-ds]: [Glassdoor - Stripe Data Scientist Interview](https://www.glassdoor.com/Interview/Stripe-Data-Scientist-Interview-Questions-EI_IE671932.0,6_KO7,21.htm)
