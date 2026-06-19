# After the Interview

What to do after completing the interview process - handling offers, rejections, and negotiations.


## Handling Rejections

Do not take rejections personally. Do a retrospective: understand what went wrong. Often nothing was wrong with you personally - someone was just stronger in one specific area, the company ran out of headcount, or priorities changed.

Common rejection reasons specific to DS roles:

- Statistics depth. Candidates who could not explain when to use a non-parametric test, or who confused statistical significance with practical significance, get cut early
- SQL speed. Timed SQL rounds are brutal. Candidates who need 20 minutes for a window function query when the expectation is 8 minutes do not advance
- Case study framing. Jumping to a model without first understanding the business question is the single most common reason for case study round failures
- Communication gaps. Technically strong candidates who cannot explain their analysis to a non-technical interviewer get passed on at the final round
- Lack of production experience. "I trained a model in a Jupyter notebook" without any mention of deployment, monitoring, or iteration signals junior-level thinking for mid-senior roles

What to do after a rejection:

- Ask for feedback. Not all companies provide it, but some do, and the feedback is gold
- Identify the weakest round. If you struggled in statistics, spend the next two weeks on StatQuest and practice problems. If case studies were the issue, practice with the company DS blog posts
- Keep interviewing. Interview skill is perishable. A two-month gap between interviews means you lose sharpness
- Build something. If you were weak on experimentation, design and run an A/B test on a side project. If ML depth was the issue, build and deploy a model end-to-end


## Handling Offers

Do not rush into agreeing immediately. If you have interviews with other companies, finish them first. Once you get the first offer, tell other companies about it to speed up their process. Having multiple offers is the ideal situation for negotiating salary and benefits.

Things to evaluate beyond compensation:

- Team and manager. Who will you work with? What is the team's analytical maturity? Do they have a proper experimentation platform or are you building from scratch?
- Scope and impact. Will you work on high-visibility problems or supporting dashboards? Is there a path from analysis to decision-making influence?
- Data infrastructure. Does the company have clean data pipelines and accessible data warehouses, or will you spend 60% of your time cleaning data and fighting tooling?
- Growth trajectory. Where are people on this team in 2-3 years? Are senior DS roles filled internally or externally?
- Remote vs in-office. DS work can be done remotely, but cross-functional collaboration (product, engineering) is harder without some in-person presence


## Salary Negotiation

If you already named a salary number in the initial recruiter call and they offer that exact number, it is very hard to negotiate upward. Two approaches to the initial salary question:

- Say the number upfront - works well when you already know the market and have experience negotiating
- Postpone the conversation - works when entering a new field, relocating, or when you do not know the market yet. "I would like to learn more about the role and scope before discussing compensation"

Regardless, do research and have a number in mind. Recruiters can be pushy and may not accept "let's talk later" as an answer.

Key negotiation principles for DS roles:

- Your strongest negotiation move is a competing offer. Direct all leverage toward the equity grant size, not base salary, since base bands at each level are relatively narrow
- Always benchmark by total compensation, not just base pay. Equity, bonuses, and signing bonuses can add 30-50% to your real annual package
- Negotiate the signing bonus separately. Companies often have more flexibility here than on base salary
- Ask about refresher grants. Some companies grant additional equity each year (refreshers), which can significantly change the 4-year compensation trajectory
- Request the offer in writing with all components broken out: base, equity (number of shares, vesting schedule, current stock price), signing bonus, annual bonus target, relocation package


## Compensation Ranges

Data Scientist compensation ranges (2025-2026 US market):

| Level | Big Tech Total Comp | Startup Range |
|---|---|---|
| Junior DS / New Grad | $120K-$180K | $90K-$140K + equity |
| Mid-level DS (3-5 YOE) | $180K-$300K | $140K-$220K + equity |
| Senior DS (5-8 YOE) | $280K-$420K | $200K-$350K + equity |
| Staff / Principal DS | $400K-$600K+ | $300K-$500K + equity |

These ranges are for the US market and vary significantly by company, location, and specialization. Candidates with experimentation or causal inference expertise tend to be at the higher end of each band. [^levels-fyi-ds] [^interviewquery-ds-salary]

Location adjustments:

- San Francisco / New York / Seattle: full range above
- Austin / Denver / Chicago: roughly 80-90% of Bay Area compensation
- Fully remote: varies widely, typically 75-95% depending on company policy
- International (London, Toronto, Singapore): roughly 60-80% of US compensation, but lower cost of living can make the net comparable

Equity considerations:

- Pre-IPO startups: equity is speculative. Evaluate the company like an investor - revenue growth, market size, competitive position. Ask about the latest 409A valuation and total shares outstanding to understand your ownership percentage
- Public companies: equity is liquid. Focus on total comp over 4 years including vesting schedule and refreshers
- Late-stage startups: often the best risk-adjusted compensation, combining near-public equity with startup-level grants


## The First 90 Days

Once you accept an offer, plan your first 90 days:

- Days 1-30: Learn the data. Understand the data warehouse, key tables, data pipelines, and data quality issues. Meet your cross-functional partners (PMs, engineers, analysts). Ship one quick analysis to build credibility
- Days 31-60: Ship a meaningful analysis. Pick a high-visibility project, define the question clearly, execute cleanly, and present findings to stakeholders. This establishes your reputation
- Days 61-90: Set your analytical agenda. Identify the 2-3 biggest unanswered questions for your product area. Propose a roadmap of analyses and experiments. This is what separates senior hires from junior ones


## Sources

[^levels-fyi-ds]: [Levels.fyi - Data Scientist Compensation](https://www.levels.fyi/t/data-scientist)
[^interviewquery-ds-salary]: [InterviewQuery - DS Salary Guide](https://www.interviewquery.com/p/data-scientist-salary-2025-guide)
