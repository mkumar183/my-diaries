## Insights Jobs
### Attunity Task Monitoring
> - Latency Issues > 5 hours there will be FS Ticket: **_Reload the tasks_**.  
> - Connection Issues -> Reloading or Connect with Networking Team 
> - **_Task Errors > FS Ticket in case of Task Error**_  
> - (All of this can be done from New Relic easily)  
> - In case of Task Errors or Latency Issues **_Reload The Tasks_**
> _TODO: Understand if same challenge will remain post snowflake. And if yes, how can this process be further automated._
 - _After 12 In case any ETL has started or not can be time consuming_

### Insight ETL
> Info: For Tenants where there was replication delay or error Insight ETL will run automatically. 
> Info: For Insights ETL that fail there will be an FS Tickets logged   
> Action: For tenants where Insight ETL failed then log JIRA Ticket and Inform Engineering
> Action: For tenants where Insight ETL is not triggered check if SIS job run or not 
> Action: If SIS Job not run then create a support ticket 

### DW ETL
> **Info**: As Insight ETLs are completing DW ETLs will start triggered and complete based on tenant size  
> **Info**: This happens via manifest file in FTP and a poller on FTP folder via Insight ETL   
> **Action**: In case any DW ETL fails there will be an Email to SRT Team  
> **Info**: For every success also there is a mail. Subject of the email has Success or Failure so its easy to filter emails that need attention  
> **Action**: In case there is an DW ETL Failed:   
> > In case there is a custom task failure SRT to inform Services Team  
> > In case there is core task failure then SRT to log bug   
> > For task failure SRT need to look into Audit table and put that information in an email and report to Engg   
> Improvement/Question: Sometimes SRT has to Retry <Need to fill this up>  
> **Improvement**: In these cases communication is not happening to customers. We can add in portal last ETL Success Time.   
> **Improvement**: Create an API that takes tenant code, cluster id and task name and provides audit log

## Before 10-11 pm if there are FS Tickets Insight ETL Checks:
> FS Tickets are automatically logged for late running Tasks.  
> (4-5 average, outlier some days > 20 once a month)  
> Remove these from nightly  
> Delete the index (replicated DB Indexes)
> Reload LS tasks (log stream tasks)  
> Once LS tasks are complete: Reload other replication tasks.  
> execute pipeline (new tenant pipelines) step: replication db migration: insight pipelines. These will run db migration and create indexes.  
> Add tenant back to nightly (update K8S secret)  
> These ETLs may trigger after 10 AM IST  

2.0 Now check Insight ETL Status: (Azure)
2.0 In case insight ETLs are not triggerred (all logs are in centralized metadata DB) (change query to NOT RUN)
(this is to be run at 10:30 or 11:00): In case # of tenants is too high investigate in case there is an abnormal issue.
(> 30 tenants every day are not run due to various reasons)
Another check is at 12 and only after 12 if ETLs are still not run then following steps are to be followed.
- check if latency is fine or not. if latency is not good then create a ticket for SRT and reload tasks as in previous step.
- if latency is fine then check if these are added to nightly or not
- check vpn connection for on-prem customers. in case vpn not okay then log network ticket
- if not there in nightly then add to nightly.
- if there in night then check if SIS jobs ran for these or not
- if SIS job did not run then log a support ticket (salesforce ticket)
- if SIS job ran then reload views control table or trigger on demand pipeline. (on demand should not be triggerred) 