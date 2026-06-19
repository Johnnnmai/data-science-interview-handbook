# Interview Process Analysis: Data Science Job Market

## Summary Statistics

Out of 1,950+ job descriptions analyzed, approximately 120 (~6.2%) include a structured interview process across 68 unique companies. The majority either omit the process entirely or describe it only at a high level.


## Interview Process

The median process has 5 steps, with most companies falling in the 4-6 range. A few lean processes have just 3 stages (smaller startups, contract roles), while the longest reach 7-8 stages (Google, Meta, Amazon at senior levels).

Most frequently mentioned steps:

1. Recruiter/phone screen - Usually 15-30 min, covers background, role fit, salary expectations
2. Statistics and probability screen - 45-60 min, hypothesis testing, experimental design, probability puzzles
3. SQL/coding round - 45-60 min, live SQL queries or Python data manipulation
4. Machine learning deep dive - 45-60 min, model selection, evaluation metrics, feature engineering
5. Case study / product analytics - 45-60 min, metric diagnosis, experiment design, business impact estimation
6. Behavioral interview - 30-60 min, values, collaboration, leadership
7. Take-home analysis project - Typically 4-8 hours, with a follow-up presentation
8. Hiring manager / team-match interview - 30-45 min, usually the final step


Examples from candidate reports:

Google, Data Scientist (L4-L5) [^reddit-google-ds]:

1. Recruiter screen (30 min)
2. Phone screen - statistics and coding (45 min each, two separate calls)
3. Onsite - four rounds: statistics/probability, SQL/coding, quantitative analysis case, Googliness/behavioral
4. Team matching and offer

Meta, Data Scientist (IC4-IC5) [^yuan-meng-ds]:

1. Recruiter screen
2. Technical screen - SQL query and statistics question (45 min)
3. Onsite - three rounds: quantitative analysis, SQL + experimentation, behavioral/leadership
4. Cross-functional panel with product and engineering partners

Amazon, Data Scientist (L5-L6) [^reddit-amazon-ds]:

1. Recruiter screen
2. Online assessment - SQL and statistics problems
3. Onsite loop - four rounds: statistics, coding (SQL + Python), case study (metric deep-dive), behavioral (Leadership Principles)
4. Bar raiser interview (behavioral + analytical)

Netflix, Data Scientist [^reddit-netflix-ds]:

1. Recruiter call
2. Hiring manager call (45 min) - background, technical depth check
3. Technical screen - SQL and statistics (60 min)
4. Onsite - four rounds: causal inference case, experimentation design, product analytics, cultural values

Airbnb, Data Scientist [^glassdoor-airbnb-ds]:

1. Recruiter call
2. Technical phone screen - SQL and probability
3. Onsite - five rounds: statistics, SQL/coding, metric investigation case, product sense, core values
4. Hiring committee review

Spotify, Data Scientist [^glassdoor-spotify-ds]:

1. Recruiter screen
2. Coding challenge - SQL and Python (take-home, 90 min timed)
3. Technical interview - statistics, experimentation, ML concepts (60 min)
4. Case study interview - product analytics, metric diagnosis (60 min)
5. Behavioral interview - collaboration, values

Uber, Data Scientist [^glassdoor-uber-ds]:

1. Recruiter call
2. Technical screen - SQL live coding (45 min)
3. Onsite - four rounds: statistics/probability, Python coding, case study (experimentation), behavioral
4. Hiring manager final round


## What Candidates Actually Experience

Candidate reports from Reddit, Glassdoor, and personal blogs confirm the data and add detail on what each round looks like in practice:

| Round | Duration | What people report |
|-------|----------|-------------------|
| Recruiter screen | 15-30 min | Basic fit, salary expectations, timeline |
| Statistics/probability | 45-60 min | Hypothesis testing, distributions, Bayesian reasoning, conditional probability |
| SQL/coding | 45-60 min | Live SQL (joins, window functions, CTEs), sometimes Python pandas |
| ML concepts | 45-60 min | Model selection, bias-variance, evaluation metrics, feature engineering |
| Case study / product analytics | 45-60 min | Metric drops, experiment design, business impact estimation |
| Take-home project | 4-48 hours | EDA, modeling, A/B test analysis, presentation |
| Behavioral | 30-60 min | STAR format, leadership, cross-functional collaboration |

Not every company includes all rounds. Total: 4-7 rounds, 2-6 weeks.

Lyft, Data Scientist [^reddit-lyft-ds]:

1. Recruiter screen (20 min)
2. SQL coding (45 min) - two moderately complex queries with window functions
3. Statistics deep-dive (45 min) - experimental design, power analysis, multiple testing
4. Case study (60 min) - diagnose why a metric dropped, propose solutions, estimate impact
5. Behavioral (45 min)

Stripe, Data Scientist [^glassdoor-stripe-ds]:

1. Recruiter screen
2. Take-home SQL and analysis project (3-4 hours)
3. Technical deep-dive on take-home (60 min)
4. Statistics and experimentation round (60 min)
5. Behavioral and values (45 min)

DoorDash, Data Scientist [^reddit-doordash-ds]:

1. Recruiter call
2. SQL screen (45 min)
3. Onsite - statistics, case study (marketplace metrics), ML design, behavioral
4. Hiring manager chat

LinkedIn, Data Scientist [^glassdoor-linkedin-ds]:

1. Recruiter screen
2. Phone screen - SQL and statistics (45 min)
3. Onsite - four rounds: coding, statistics, product analytics case, behavioral
4. Hiring committee review


## Common Patterns Across Companies

Several patterns emerged from analyzing these processes:

- SQL is universal. Every single company with a structured interview includes at least one SQL round. It has replaced coding algorithms as the default technical screen for DS roles
- Statistics never disappeared. Unlike some engineering roles where ML fluency overtook fundamentals, DS interviews still heavily test probability, distributions, hypothesis testing, and experimental design
- Case studies are practical, not abstract. Companies ask about real metric scenarios: "DAU dropped 10% last week, walk me through your investigation." Not textbook exercises
- Take-home projects are polarizing. About 35.0% of companies include them. Candidates report frustration with scope creep, but companies that use them say the signal quality is higher than live coding
- Behavioral rounds map to company values. Amazon uses Leadership Principles explicitly. Google tests Googliness. Meta asks about cross-functional influence. The questions differ, but every company has this round
- The bar raiser concept is spreading beyond Amazon. Several companies now include a calibration interviewer from outside the hiring team to reduce bias
- Product sense is increasingly expected. Even for roles that sit on analytics or ML teams, interviewers want to see that candidates understand why they are building what they are building, not just how


## Key Differences from Software Engineering Interviews

- No LeetCode-style algorithm grinding. DS interviews rarely include dynamic programming, graph traversal, or algorithm optimization. The coding bar is SQL fluency and practical Python
- Statistics is a standalone round. Software engineers rarely get tested on hypothesis testing or experimental design as a separate interview
- Case studies require business reasoning. DS candidates must connect analysis to business outcomes - revenue, retention, user growth - not just produce correct code
- Communication is weighted more heavily. Presenting analysis results clearly to non-technical stakeholders is explicitly evaluated in most DS loops
- Take-home projects are more common. About 35.0% of DS roles include a take-home vs roughly 20.0% for SWE roles


For a structured deep-dive with 200+ real DS interview examples, check out [The 0-1 Data Scientist Interview Playbook](https://valenx.org/books/ds).


## Sources

[^reddit-google-ds]: [Reddit - Google DS Interview Experience](https://www.reddit.com/r/datascience/comments/1jrdrpx/google_data_scientist_interview/) (r/datascience)
[^yuan-meng-ds]: [Yuan Meng - DS Interviews 2.0](https://www.yuan-meng.com/posts/mle_interviews_2.0/)
[^reddit-amazon-ds]: [Reddit - Amazon DS Interview Loop](https://www.reddit.com/r/datascience/comments/1ovf9k2/amazon_data_scientist_interview/) (r/datascience)
[^reddit-netflix-ds]: [Reddit - Netflix DS Interview](https://www.reddit.com/r/datascience/comments/1p1dklk/netflix_data_scientist_interview/) (r/datascience)
[^glassdoor-airbnb-ds]: [Glassdoor - Airbnb Data Scientist Interview](https://www.glassdoor.com/Interview/Airbnb-Data-Scientist-Interview-Questions-EI_IE391850.0,6_KO7,21.htm)
[^glassdoor-spotify-ds]: [Glassdoor - Spotify Data Scientist Interview](https://www.glassdoor.com/Interview/Spotify-Data-Scientist-Interview-Questions-EI_IE408251.0,7_KO8,22.htm)
[^glassdoor-uber-ds]: [Glassdoor - Uber Data Scientist Interview](https://www.glassdoor.com/Interview/Uber-Data-Scientist-Interview-Questions-EI_IE575263.0,4_KO5,19.htm)
[^reddit-lyft-ds]: [Reddit - Lyft DS Interview](https://www.reddit.com/r/datascience/comments/lyft_ds_interview/) (r/datascience)
[^glassdoor-stripe-ds]: [Glassdoor - Stripe Data Scientist Interview](https://www.glassdoor.com/Interview/Stripe-Data-Scientist-Interview-Questions-EI_IE671932.0,6_KO7,21.htm)
[^reddit-doordash-ds]: [Reddit - DoorDash DS Interview](https://www.reddit.com/r/datascience/comments/doordash_ds/) (r/datascience)
[^glassdoor-linkedin-ds]: [Glassdoor - LinkedIn Data Scientist Interview](https://www.glassdoor.com/Interview/LinkedIn-Data-Scientist-Interview-Questions-EI_IE34865.0,8_KO9,23.htm)
