Specific Incidence. 
Time bound : Under Pressure Situation 
https://powerschoolgroup.atlassian.net/wiki/spaces/PESE/pages/39082558757/2021-06-13+-+PE-95183+PE-94541+PE-95363+-+Miami-Dade+Import+Slowness
https://powerschoolgroup.atlassian.net/wiki/spaces/PESE/pages/39082561790/SPIKE+Miami+Dade+Investigate+Error+Could+not+establish+a+connection+to+SFTP+Server

- Changing from php older version to newer version. Switching over to serverless technology. 
- Switching from MSSQL to Snowflake. Switching from Azure to AWS. 
- Monitoring of ETLs has become very challenging. So I got APIs developed for ETL Statuses and brought these over to a single system using python programs 
- Reporting functionality in Kickboard had to be developed and there were several challenges. We picked up AWS Batch for it and we made it success. 
- SIS Sync was very challenging. We planned it behind feature flags so we were able to control the deployment. 

I deal with systems where availability requirements are 99.9%. Any kind of outage of the system is reported as a P0. I have dealt with systems of different nature. E.g. Schoology is a multi-tenant system. Which means it uses single instances of servers across all its customers large, medium and small. Its a very complex system with 30+microservices and using many different types of technologies. Very heavy AWS based system. The core of this application is built in PHP Drupal. 

Integration Team was handed over to me to manage which deals mostly with data sync across different products. This product has two solutions. SiS Adapter which is based on SQS, Step Function and Lambda architecture. However, Auto Import system was old and it was for file based customers. (customers who upload their files to FTP location and from where we pick the data and load data into our system). 

For us Back to School situations are very critical. During these times huge data uploads come our way and any kind of delays in these loads. We deal with almost 1-2 P0 situations every month. We have a strong process around handling these P0s. Page Duty, Rosters, Training of Staff. Incident Commander, Each Team POC is on Rotation, Product Owner, QA and one Cloudops. Cloudops is available 24#7 and engineers have required access to the production system. 

This was for Miami-Dade School and I had just recently acquired this team. This customer became very very escalated and was identified as At Risk customer. Their imports were inconsistent and even a 30 minutes delay was not acceptable. This had repeated few times. A Daily Standup with Customer was created. Customer was very loud and team was not too happy about it. However, i had to steer the whole situation. It took us about 6-8 weeks to be able to completely reach a stage where imports were predictable there were proper logs, alerts and certain amount of predictability around it. 

There were issues at customer end as well. Their movements to files were not happening at right times. So we had to establish strong status update on the same. Which provides a clear indication of when the file uploads were done. There were also issues in those file uploads and data was inaccurate and we had to investigate those data issues and bring it to notice of customer. There was lot of blame game inside and it seems there was some politics where another vendor of ours was involved in dissuading the customer about stability of our system. 

Issues at our end: 
- Our jobs were not resilient. 
- There were connection failures to Mongo DB, Redis and FTP and there were not enough retries. SFTP, Redis and Mongo at different times were overloaded and proper monitoring and alerts were not in place. 
- Proper high alert monitoring was not available and so customer support, cloudops were not alerted on such failures and actions were not taken in time 
- Retry mechanism was missing resulting in more failures 
- There was shared infrastructure for these jobs and the volume of jobs across other customers had increased. We had to separate this out for this customer. 
- Sumologic was our logging system 

Team Explored various options such making jobs run in parallel. More emphasis on better logging of the data and jobs. 

Actions:
- Proactive alerts for jobs approaching breach
- Isolate the infrastructure to its own process
- Predictive alerting for early detection

Improve monitoring and alerts by:
- Reporting on elapsed time while the job is in progress
- Add monitoring and alerts for the last updated timestamp exceed x time

