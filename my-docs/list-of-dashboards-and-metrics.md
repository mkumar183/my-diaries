Productivity, Product Improvements and Business impact 

-> Current Sprint and Backlog 
-> Inflow / Outflow - Component, Teams, Department Logged 
-> Outstanding Backlog bucketed by Age / Components / Teams / Logged Department / Salesforce ID 
-> Issues Trend By Department (QA, CloudOps, Support, Engineering, Product)
-> No Fix Version: Going up or Down by Teams 
-> Capex Contribution -> Going up or down by Teams 
-> Timespent by story points 
-> Story point audit: Avg Story points across Teams for Bugs and User Stories 
-> No Fix Version Audit: Issues with Release but no Git Checkin / Commit 
-> Sprint performance: Velocity, % Complete 
-> Sprint Effectiveness: Impact to Customer Backlog, Impact to EPICs, Capex %, Fix Version %  
-> Dev Cycle Times Outliers 
-> Cycle Time Outliers for Production Issues 
-> TimeSpent to Story Points 
-> Content only work 
-> Total Contributions by Engineers: JIRA, Confluence and Git: Team Filter 
-> Ongoing EPICs view with % Complete ? 

-> GitPrime metrics 
-> Knowledge Sharing + Reviews 
-> Kickboard Metrics 

Productivity/Work Focus
- How much work was done ? Story points, Number of Tickets pushed in each sprint. 
- Where did the team struggle with ? <High dev cycle times>
  Metric: Avg Dev Effort per story point for tickets closed in sprint, quarter
  Metric: Avg Overall Cycle Time on production issues 
- How quickly is team able to push user stories. 
  <Avg Cycle Times from dev in progress onward per ticket per story point>
- What % of issues (Bugs and User Stories) Team fixes involve a code change ? 
- 

Ownership Focus: 
- Which EPICs does the team own ? How much backlog is present in these epics.
- Which components does the team own. What is inflow/outflow on these components. What is outstanding backlog ? 
- What improvements are done to these components 

Product Focus: 


Customer Focus: 
- How quickly are we able to resolve production issues <P0s, P1s, P2s>
  Metric: Avg Dev Effort per story point for tickets closed in sprint, quarter

Delivery Focus 
- EPIC Effectiveness: 
  EPIC Estimate, Start Date, End Date, % Complete 
  Which EPICs Teams are working currently. 
  What is their % Complete. 
  What is their expected end date

Metrics: 
- Velocity (# of tickets per person, story points per person per sprint): Measures consistency of team and each person in the team over a period of time. 
- % Completion: Tells us how well team plans 


- % of bugs with code changes: 
- Capex % 
- EPIC Impact: 
- Backlog Impact 


Current Sprint and Backlog Dashboard:
- This dashboard will show whats being done in current sprint. 
- How much is the progress. Day Remaining. 
- What is the upcoming backlog. 
- Who are the players doing best. 
- Time logs 
- How much backlog team has (User Stories/EPICs and Customer issues)
- Components that backlog belongs to 
- EPICs that backlog belongs to 
- Avg velocity from past 6 sprints and current sprint planned work 


Quarterly Dashboards: Focused on Quarterly Goals 
- Key metrics to be measured quarterly 
  -- Avg Velocity per sprint - by story points 
  -- Avg Velocity per sprint - by # of tickets 
  -- Avg story points per issue - compare with previous qtr 
  -- Avg Completion % Till date compared to previous qtr 
  -- Capex % (By Story points)
  -- % of issues going in release vs no fix version (Story points)
  -- % of issues with git checkin or git merge (Story points)
  -- # of EPICs completed in Quarter 
  -- New Feature EPICs % Complete where team is working on <Exclude internal defect and customer defect ones>
  -- In Progress EPICs and their expected completion dates 
  -- # of bugs fixed by Team. Out of these production issues vs internal issues. 
  -- # of bugs fixed by Team. % of issues with valid code changes 
  -- Issues fixed by team by components 
  -- Component ownership and respective backlog 
  -- Number of spike tickets done by team in quarter 
  -- Number of confluence documents updated by team in quarter - contribution by each person 


Release Dashboards:




Engineer Dashboard: (Quarterly)
- Contribution to JIRA, Confluence and GIT by myself 
- Tickets completed by me taken high dev cycle times and cycle times 
- Components and EPICs where I contributed to 
- Story points pushed per sprint 
- count of MRs / git checkins raised per sprint 
- For a team look across last 6 sprints (Q2)
- Look for under which EPICs work is performed by team 
- How much of this work is for new enhancements vs bug fixes


Analysis for bug fixes: 
- in bug fixes, how much work went under no fix version
- in bug fixes, under which components team fixed issues
- what is the patter of these issues, what are the CAPA for such issues such that these issues do not occur again 
- which components team can own end to end in coming quarter. which training is needed 
- set goals for owning components, calculate inflow and bring about improvement in this inflow 

Analysis for User Stories 


Individual Analysis 


### Metrics that should matter: 
1. in a period lets say 6 months. for a team. Total story points done. 
2. Divide story points in user stories and bugs 
3. Slice that work into bugs solved for production customers and within that how many have code changes 
4. For user stories, categorize under which EPICs these belong to and what business impact these stories are able to create. (how much epics are able to move forward)
5. Correlate this with dev cycle time effort. and that with story points and git checkins

