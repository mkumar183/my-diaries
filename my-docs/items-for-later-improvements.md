we get many tickets with request to change configurations on behavior side. How can we have a better process that these are not logged as JIRA tickets. 

https://powerschoolgroup.atlassian.net/browse/UIHN-50236 
Where is the documentation for these SSO process. Is this documentation or Automation that needs to be improved in order for such issue to not occur. 

How to build a culture of Prevention and not just Fixing. 
How to note down work that is done for prevention. Such as tickets logged and work done and reward this ? 

Production Checklist
- Have a static checklist that SRT Team runs every release 
- Fill this up with steps every release with specific changes that occur release to release 
- update production checklist in case any tenant is updated with a custom tag to remove part of release
- review release process and add this step there 


Ticket      Reason 
Attunity tasks issues: 
    UIHN-50317 Production - Users unable to log onto Unified Insights 
    https://powerschoolgroup.atlassian.net/browse/UIHN-50546 : similar issue. not sure if due to replication 
    

Onboarding Tickets taking longer time:
    https://powerschoolgroup.atlassian.net/browse/UIHN-46346
    Customer is UAE customer. SIS DB not found. District Code not there. Several Issues. 

Rollover Process
    After Azure to AWS Migration have work to stabilize this in Q3. 

cron not picking up jobs: 
    https://powerschoolgroup.atlassian.net/browse/UIHN-50271

data type (null not null) mismatch in ETL vs Source
    Production : Olap refresh error for lrsc
    https://powerschoolgroup.atlassian.net/browse/UIHN-49620
    https://powerschoolgroup.atlassian.net/browse/UIHN-49952

    Why we have fields in ETL that are mandatory while in source these are not mandatory. 
    Do we have a mechanism to send these records to error records and report to customers via some reports ? Or can we make these nullable in ETLs as well. 

spaces and special characters in source:
    https://powerschoolgroup.atlassian.net/browse/UIHN-50040
    what does it take for us to allow spaces in source and not let our ETL fail


Troubleshooting guide, how can we put it in a different tool for easy search and find. Add components to it. 

SSO Issues Troubleshooting: 
- Role mapping in SIS 
- Move document to support facing documents in Unified Insight Collab area 
- An enhancement to sync roles via a button in TM to run just this task
- School year should be mapped 
- YET Rollover should automatically happen from 
- Troubleshooting UIHN login error in production : Document 
- 

