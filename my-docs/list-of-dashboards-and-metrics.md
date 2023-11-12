Staff Meeting Long one with Shemeem, Vaidehi, Veda, Nitin and Megha:
Metrics Discussion 
Meeting Effectivness 
1-1 
Customer Focus / Competitive Analysis 
Goals and Focus for 2024 

https://powerschool.domo.com/page/733042854
Getting Data in Snowflake: 

Customer Focus: 
-> Usage of our product (Gainsight/New Relic) 

What happened in last x days? 
1. How many new tickets came in 
2. How many tickets were resolved 
3. How many git merges happened 
4. How many content changes were done 
5. How many confluence pages were created / updated 
6. Who all logged how much time ? 


Usage and Monitoring
-> New Relic Metrics  

Tenant Data in Snowflake
-> Versions, Student Counts, Modules Enabled

Employee Data: 
-> Skills (List of Skills) Inventory 
-> Employeeid, Month, Skill
-> Forecasting what skills we will need (in next 6 month) 
-> Prepping up for it 
-> Component ownership by Teams


ETL Status: Vedantham/Shemeem 
-> Already we have. Testing and how to use 

GitPrime Metrics: Vedantham 

-> Velocity (By Team and By Engineer) 
-> % of Velocity on Maintenance  
-> Completion % (Planned vs Complete) 

By Engineer: 
-> JIRA, Confluence and Git 
-> Comparison across Engineers 

Bugs in Bronze: QA Logged: Internal Regressions: 
-> Trend over month, Teams, Components 

Dev Cycle Times: 
-> To understand where engineers are spending more time. what kind of tickets are getting blocked. What can we do to reduce 
-> 

Current Sprint Dashboard: 
-> Avg Dev Cycle Time per ticket and or per story point: 
   Dev in Progress to Ready to Accept 

TimeSpent vs Story Points
-> Avg Timespent per story point 
-> Collaboration: Number of people spending time on a JIRA 
-> Timespent vs Estimate on an EPIC 

Total Cycle Time 
-> 

Fix Version %: No Fix Version
-> Configuration or Data Issues. % 
-> Only for Bugs. % of issues closed with No Fix Version. 
-> By component, Team, Department logged 
-> Trend over sprints 
-> Audit. Ticket with Fix Version but not having Git Merge / Checkin 
 
Capex % 
-> Across Stories/Bugs. % of story points contributing to Capex. 
-> By Team
-> Trend over sprints 
-> (Are we making money): % of capex work going towards existing content ? How are these feedbacks coming from customers.

** Take STORY POINTS Seriously ** 
Customer Issues 
-> EDV: Salesforce cases. Trend. If its going up or down. 
-> Total Cycle Time 
-> Ageing 

% Automation Coverage:
-> Pass percentage 

EPIC: 
-> Total Stories, Completed, Expected End Date, Completed (Planner) 
-> EPIC Ownership by Team 


Audit Reports:
- Git merges missing Ticket number 
- Worklogs missing 
- Git missing reviews and comments 
- Fix version missing git link 
- Support logged tickets missing components: send automated email if possible to Sudhi 
- x story point tickets exceeding x days in dev in progress 
- tickets blocked beyond 3 days 
- Tickets with x age not triaged and put in BRB 
- Tickets in team backlog not addressed 
- Tickets spilled over beyond 3 sprints for a team 





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

