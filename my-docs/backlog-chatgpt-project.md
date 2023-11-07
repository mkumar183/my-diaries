How to measure and improve performance of the team: 
- productivity and business impact are two different things. 
- productivity is measured more as velocity of the team divided into bugs and user stories 
- Business impact is where this work is making the impact. 
- e.g. if user stories then which epics are getting completed. 
- if bugs then are these customer issues. if customer issues how many of these are having code changes
- are there internal issues being fixed by team 
- is team able to take ownership of specific components and deliver these issues 
- what % of tickets are having git checkins is also one way to look at it 
- what are the cycle times of the tickets resolved by team 
- which tickets are taking too much time in development vs overall cycle times 
- Are story points correlated with effort as in dev in progress times vs git checkins ? 
- how much team is contributing in confluence improving the components that team owns 



Pending:

Assign components automatically to new tickets 
Get last comment in jira extn table 

Metrics (Dashboard with Team and Sprint filters):
- Completions vs planned by EPIC. <Contribution by EPIC>
- Velocity by Sprint stacked by EPICs (avg, change over sprints)
- Velocity by User Stories and Bugs <Divide bugs by components>
- Velocity by Sprint stacked by Capex/Opex 
- Velocity by Sprint stacked by Releases  
- Velocity by tickets with Git checkin and without git checkin 
- Velocity by assignee

- Avg ticket size <by sprint>
- Completion % (User Stories Only): Bugs keep bandwidth

- Avg Dev cycle time by Story Points : Research anomaly 
- Total cycle time Anomalies 

Exceptions: 
- Outliers by Dev Cycle Time per story point 
- Outliers by Total Cycle Time per story point 
- Outliers by 

Dashboard for Maintenance:
- % of story points / count team spends on maintenance issues 
- % of story points /count team spends on customer issues vs internal issues 
- Components where team spends effort 
- Exception: Issues with a release but no git commit or checkin 
- Team backlog : By component , By Age 
- Avg dev cycle time spent by team per story point of issue, Outliers, Buckets  
- Avg cycle time of issues resolved by this team. Outliers, Buckets 
- Inflow Analysis By Component and Department  monthly - Is it trending up or down



No Fix Version: 
- Count and story points of No Fix Version Tickets by each month 
- By components and team and other filters 
- Filters production issues, internal issues


Filters by Bugs / User story / Production vs internal defects / Team / Department logged 
- Release dashboards / Analysis: 
  - count of defects / user stories delivered in a release
  - story points delivered in a release 
  - Epics delivered in release 
  - count of git merges 
  - count of lines of code delivered by repo 
  - number of confluence documents developed in release time line   

- tickets for Platform Optimization vs Operations work by data ninja 
- Individual contribution: Story Points, MRs, Confluence, MR Reviews 
- Cycle time overall and Dev Cycle time 
- Discuss and enhance system to capture timesheet hours if needed 
- PRs by repo -> Set goals for having some MRs to DW ETL from each team 
- EPIC or Initiative wise dashboards ? 

- Sprint performance metrics
  - Add confluence and MR Contributions within context of the sprint 
  - Add sprint column to planned vs complete widget 
  - Add no fix version filter and analysis 
  - Team assignments updates 
  - scorecard by team members <stretch goal> 

- Release dashboard with release filter 
  - release completion dashboards 

- Add ftp download logs to snowflake instead of json file
- EPIC/Initiative Statistics - dashboard  

 
Done:
- added age to issues in sprint and snowflake blocked issues 
- Snowflake team add department to distinguish snowflake issues: Done
- Flagged Time not getting populated correctly
- Make jira ql reusable with comments and status being optional. 
- refactor get_jira_issues_from_jql to get_jira_issues_details to avoid confusion - done 
- add two new parameters to get_jira_issues_details with default values - done 
- add conditions to not get comments and status history when not needed - done 
-> call get_jira_issues_details with list of your issues and comments and status being false 
-> separate out processes for identifying components and other classifications 
-> arrive at jql where components should be updated <issues logged > 5 days ago ? or issues triaged>
-> update components only when components are not null 
-> arrive at jql to update summary impact. before updating ensure issue already doesn't have summary comment 
-> write method to summarize issue and resolution
- Add updated_at to fact_merge_requests - done 
- Add varchar column to temp table - done
- Add date column to fact table - done 
- add to extract updated at 
- Insert into temp table string 
- Convert to timestamp and add to fact table 
- created at and merged at
- modify column in fact to timestamp
- or add new columns and delete existing
- modify merge statement to conver to timestamp 
- Establish on AWS Batch and hourly refresh : Done 