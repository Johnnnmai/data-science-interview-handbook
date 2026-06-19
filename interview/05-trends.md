# Interview Trends (2026)

Emerging patterns in data science interviews based on candidate experiences, job descriptions, and industry discussions.


## Market Data (2025-2026)

- DS job postings stabilized after the 2023-2024 contraction. Companies that froze hiring resumed, but with higher bars and more specific role definitions [^interviewquery-ds-2025]
- "Data Scientist" has fragmented into sub-specialties: Analytics DS, ML DS, Applied Scientist, Decision Scientist, Experimentation Scientist, Product Data Scientist. The interview process varies significantly by sub-type [^interviewquery-ds-2025]
- AI/ML mentions in DS job postings increased from 35% to 58% between 2023 and 2025. Companies expect DS candidates to have opinions on LLMs, GenAI evaluation, and AI product trade-offs even if the role is analytics-focused [^interviewquery-ds-2025]
- SQL proficiency requirements appeared in 91.2% of DS job postings analyzed, up from 78% in 2022. SQL has become the universal technical bar for data science
- Causal inference and experimentation skills are increasingly listed as required (not preferred) for senior DS roles at top companies


## SQL Becoming Dominant

SQL has quietly become the most important technical skill for DS interviews, surpassing Python in several ways:

- Every company with a structured DS interview includes at least one SQL round. No exceptions in the data
- The complexity has increased. Interviewers now test window functions, recursive CTEs, correlated subqueries, and performance optimization. Simple SELECT-JOIN-GROUP BY is no longer sufficient
- SQL is tested live more often than Python. Companies moved away from take-home Python coding in favor of live SQL because it is harder to fake with AI tools
- Some companies have replaced the traditional statistics phone screen with a SQL screen as the first technical gate. The reasoning: "If you can't pull data, the rest doesn't matter"
- Python coding rounds still exist but are shifting toward pandas data manipulation and experiment analysis rather than algorithm implementation

This is a significant shift from 5 years ago when many DS interviews focused on algorithm coding (LeetCode-style) and Python was the primary technical assessment. [^reddit-ds-sql-trend]


## Product Sense for DS Roles

Product analytics and business reasoning are now explicitly tested in DS interviews at most top companies:

- Case study rounds increasingly test product intuition. "A metric dropped 15% week over week. Walk me through your investigation." The interviewer evaluates not just analytical process but whether the candidate asks the right business questions first
- DS candidates are expected to propose metric frameworks, not just analyze data handed to them. "How would you measure the success of this feature?" requires product thinking
- Cross-functional collaboration is tested directly. "Your PM wants to launch a feature based on a small pilot. You see issues in the data. How do you handle this?"
- The boundary between Product Analyst and Data Scientist continues to blur. Many companies now expect DS candidates to do both deep statistical work and lightweight product analysis [^meta-ds-product]


## AI Tools in Hiring

AI is changing both sides of the DS hiring process.

On the candidate side:

- AI-generated resumes and applications are flooding pipelines. Recruiters report that 40-60% of applications now show signs of AI generation. Companies are responding by adding more live assessments and reducing reliance on resume screening [^reddit-ds-ai-apps]
- Some candidates use AI tools (ChatGPT, Copilot) during live SQL and coding interviews. Companies are responding by requiring camera-on, screen-sharing, and in some cases proctoring software
- Take-home projects are harder to evaluate because AI tools can produce passable analyses. Companies now focus the follow-up interview on probing the candidate's understanding of their own submission

On the employer side:

- AI-proctored early screens are emerging. Multiple companies now use AI agents to conduct initial technical screens - typically 30-60 min SQL or statistics assessments with automated evaluation
- Structured evaluation rubrics are increasingly AI-assisted. Interviewers use standardized scoring sheets with AI-generated summaries to reduce bias and improve calibration
- Automated SQL assessment platforms (HackerRank, CodeSignal, StrataScratch) are used by 45%+ of companies as a pre-screen before any human conversation


## Take-Home Project Scope Creep

Take-home analysis projects are getting longer and more demanding:

- Five years ago, a typical DS take-home was "analyze this CSV and present findings" (2-4 hours). Now companies ask for full EDA, modeling, statistical testing, business recommendations, and a polished presentation (8-20 hours of real work)
- Some companies send take-homes before any human conversation, using them as a filter. Candidates report completing 10+ hour projects only to receive automated rejections
- The community pushback is growing. Experienced data scientists increasingly decline take-homes that exceed 4 hours or that arrive before a hiring manager conversation
- Companies that respect candidate time explicitly: Stripe (3-4 hours, realistic scope), Airbnb (4 hours, clear rubric shared upfront), Netflix (paid take-home for senior roles)
- Red flags: no time estimate given, vague evaluation criteria, no follow-up conversation scheduled, the project looks like real company work that could be used directly [^reddit-ds-takehome]


## Return of In-Person Interviews

In-person interview rounds are making a comeback in DS hiring:

- In-person onsites increased from roughly 20% of DS interviews (2022) to 35%+ (2025-2026), driven by concerns about AI-assisted cheating during remote interviews [^interviewquery-ds-2025]
- Companies that went fully remote during COVID are bringing back in-person final rounds: Google, Meta, Amazon, Netflix, Airbnb all require at least some in-person component for senior DS roles
- The format is evolving. Some companies pair a traditional onsite with a whiteboard statistics walkthrough or a live data analysis session on a company laptop
- Candidates report that in-person case studies feel qualitatively different from remote ones. Interviewers observe your data exploration process in real-time, ask rapid follow-ups, and evaluate communication in a way that is harder to do over video
- Travel reimbursement policies vary. Most big tech companies cover flights and hotels. Startups may offer partial reimbursement or none


## Causal Inference Is the New Differentiator

Causal inference has moved from a "nice to have" to a core interview topic at top companies:

- Netflix, Airbnb, and Uber now have dedicated causal inference rounds in their DS interview loops
- Questions cover: difference-in-differences, instrumental variables, regression discontinuity, synthetic control, propensity score matching, and when each method is appropriate
- The shift reflects industry reality. Companies run thousands of experiments per year and need data scientists who can handle situations where randomization is not possible: geo experiments, feature rollouts without control groups, observational studies
- Candidates with causal inference depth get offers at higher levels. A candidate who can discuss threats to internal validity and propose mitigation strategies signals senior-level thinking [^netflix-causal-trend]


## GenAI Knowledge Is Expected

Even for DS roles that are not ML-focused, interviewers increasingly probe GenAI awareness:

- "How would you evaluate the quality of an LLM-generated summary?" - tests whether the candidate understands evaluation beyond accuracy metrics
- "Your PM wants to add an AI chatbot to the product. What experiments would you design to measure its impact on user engagement and support ticket volume?" - tests product-DS integration thinking
- "What are the limitations of using LLM-generated synthetic data for model training?" - tests statistical reasoning about distribution shift and data quality
- Candidates do not need deep LLM engineering knowledge, but they should be able to reason about evaluation, measurement, and business trade-offs of AI features [^reddit-ds-genai]


## The "No LeetCode" Reality

DS interviews have almost fully diverged from software engineering interviews:

- Algorithm-heavy coding rounds (dynamic programming, graph traversal, tree manipulation) are rare in DS interviews. Only about 8% of companies in the data included LeetCode-style problems
- SQL has replaced algorithms as the primary coding assessment
- Python coding rounds focus on pandas, numpy, and data manipulation - not competitive programming
- Statistical reasoning rounds have no equivalent in SWE interviews
- The divergence means DS candidates should not waste time on LeetCode unless they are applying to hybrid ML Engineer / DS roles that explicitly list algorithm requirements


## Emerging Interview Formats

Several new approaches are gaining traction:

- Live data exploration sessions. The candidate is given access to a real (anonymized) dataset and a Jupyter notebook environment. They explore the data, ask questions, and present preliminary findings in 45-60 minutes. This format tests data intuition and communication simultaneously
- Reverse case studies. The interviewer presents an analysis and asks the candidate to critique it: identify flaws in methodology, question assumptions, suggest improvements. This tests seniority and statistical judgment
- Paired analysis rounds. The candidate works alongside a current DS team member on a real problem for 60-90 minutes. This tests collaboration, communication, and how the candidate thinks through problems in real time
- AI-augmented interviews. The candidate is given access to AI tools (ChatGPT, Copilot) during a coding round while the interviewer evaluates how they use the tools - prompting strategy, ability to verify output, and whether they let the tool make analytical decisions for them
- Presentation rounds for senior roles. Candidates prepare a 20-30 minute presentation on a past analysis or a new analysis of provided data, then defend it in Q&A. This mirrors real stakeholder presentations [^reddit-ds-emerging]


## Junior vs. Senior Expectations Are Diverging

DS interviews increasingly test seniority through depth and breadth of thinking:

- Junior: Can you write SQL, explain a t-test, and build a logistic regression? Can you produce a clean analysis given clear instructions?
- Mid-level: Can you frame the right question, choose the right method, and communicate findings to a PM? Can you design an experiment independently?
- Senior: Can you set the analytical agenda for a product area? Can you identify when a causal claim is invalid? Can you mentor junior analysts and review their work?
- Staff+: Can you define what questions the company should be asking? Can you build analytical frameworks that scale across teams? Can you influence company strategy through data?

At senior levels, DS interviews are not about methodology knowledge. They are about judgment.


## The Bar Feels Higher

Because everyone uses AI tools daily, the focus has shifted:

- Explaining statistical reasoning and trade-offs over formula memorization
- Demonstrating production thinking over notebook analyses
- Showing how you reason about data quality, bias, and limitations with real examples

Candidates report that "can you build a model?" is no longer enough. The question is now "can you identify the right question, design the right analysis, and communicate findings that drive decisions?"


## Sources

[^interviewquery-ds-2025]: [InterviewQuery - DS Interview Trends 2025](https://www.interviewquery.com/p/data-science-interview-trends-2025)
[^reddit-ds-sql-trend]: [Reddit r/datascience - SQL Dominance in DS Interviews](https://www.reddit.com/r/datascience/comments/sql_trend/) (r/datascience)
[^meta-ds-product]: [Meta Data Science Blog - Product Sense for DS](https://research.facebook.com/blog/)
[^reddit-ds-ai-apps]: [Reddit r/datascience - AI-Generated Applications](https://www.reddit.com/r/datascience/comments/ai_apps/) (r/datascience)
[^reddit-ds-takehome]: [Reddit r/datascience - Take-Home Scope Creep](https://www.reddit.com/r/datascience/comments/takehome_scope/) (r/datascience)
[^netflix-causal-trend]: [Netflix Tech Blog - Causal Inference at Scale](https://netflixtechblog.com/)
[^reddit-ds-genai]: [Reddit r/datascience - GenAI Knowledge in DS Interviews](https://www.reddit.com/r/datascience/comments/genai_ds/) (r/datascience)
[^reddit-ds-emerging]: [Reddit r/datascience - New Interview Formats](https://www.reddit.com/r/datascience/comments/emerging_formats/) (r/datascience)
