Pending:
- Establish on AWS Batch and hourly refresh 
- Sprint performance metrics
  - Populate sprint dimension - Done 
  - tickets completed - Done 
  - story points completed - Done 
  - tickets with no fix version or tickets with having some commit part of it - Done 
  - bugs vs user stories - Done 
  - summary by epics how many epics how many stories are done in the sprint - Done 
  - Add a column which states if this ticket has any commit mentions or not 
  = Add a column that give associated PR and its url 
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