Onboarding Tickets taking longer time:
    https://powerschoolgroup.atlassian.net/browse/UIHN-46346
    Customer is UAE customer. SIS DB not found. District Code not there. Several Issues. 

Rollover Process
    After Azure to AWS Migration have work to stabilize this in Q3. 

Cron not picking up jobs: 
    https://powerschoolgroup.atlassian.net/browse/UIHN-50271

Data type (null not null) mismatch in ETL vs Source
    Production : Olap refresh error for lrsc
    https://powerschoolgroup.atlassian.net/browse/UIHN-49620
    https://powerschoolgroup.atlassian.net/browse/UIHN-49952

    Why we have fields in ETL that are mandatory while in source these are not mandatory. 
    Do we have a mechanism to send these records to error records and report to customers via some reports ? Or can we make these nullable in ETLs as well. 

Spaces and special characters in source:
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
- How to get to know if Attunity is working or not. 
- Revise latency for Attunity tasks 18000
- Create a document on how to access new relic dashboard for attunity failures / latency 
- Horizontal scaling 
