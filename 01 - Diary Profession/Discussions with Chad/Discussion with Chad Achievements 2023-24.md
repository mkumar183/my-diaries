### Our Achievements in 2023-24
1. We cut down on [signature work](https://powerschoolgroup.atlassian.net/wiki/spaces/UI/pages/64839974913/Tech+Design+Automation+of+Assessment+Signature+Generation), freeing up 12 engineers. This was a big win, though 2 engineers still handle some of this work. We made the process more efficient through automation.
2. Growing operations: India team took charge of Tenant Manager and made it better. We grown in tenant count 2.5x and student count rapidly in last year. We could scale it without causing an increase in our backlog. 
3. We reorganized teams by parts they work on. We trained each team on their area and set up talks with support teams to help them fix issues. We reduced our inflow and kept it contained with increased number of customers and students on our platform. 
4. Build [Migration Guide](https://git.versifit.com/docker-ci/hoonuit_delivery_platform/-/blob/ansible-dev-ca/Instructions/MigrationInstruction%20from%20Azure%20to%20AWS.md?ref_type=heads). Step by Step. Finished moving to Snowflake. We moved over 250 Tenants. The system is now more stable. Our India Team led and completed this project.
5. Better system tracking: We can now see Tenant APIs and setup data in Snowflake. Usage data is there too.
6. We did well with new ideas like TMA, Intervention Analytics, and working with Kickboard and Kinvolve. Our India Teams handled all of this.

### Areas for Improvement:
1. Scaling challenges. These are ongoing challenges with LAUSD and Montana. Alabama is our premium customer and there are things that can be made better with Alabama. 
2. Give Cloudops more power. We're working on removing engineering access from TM production. We need to clearly state what each team does (like managing costs and performance) and let Cloudops handle more of the system monitoring, support, and upgrades.
3. Cut down on ETL Failures. It's better with AWS, but we can do more. We still see 20-30+ failures daily. Help Cloudops tell the difference between system and app issues. Engineering should fix app problems for good, looking into why they happen. Cloudops should work on system failures or ask engineering to make the system better.
4. The way we handle custom work isn't set up well. I don't know much about this, but we could look at how it's built. We should try to make it so services can work without needing engineering, and support teams can easily spot their issues.
5. Make a better way for support to know if a problem is with the product or with setup/data that they should handle. Create better tools to check data quality so support can see these issues without asking engineering. The Product team should look at what support often asks for and try to fix it by giving more info or making the product better.
6. Some parts of the product could be better, like the YET Rollover process (we've made it better, but it can improve more, even though it only happens once a year). Also, the Dev Tenant setup and what it needs (right now, we have a dev tenant that can't have separate releases, but we're getting requests for setups that don't fit the usual mold).
7. Assessment Requests: We still get some of these. Also, we have a big team in services loading assessments. I'm not sure if we can make this work cheaper or easier.

Other Improvements (Not current pain):
- CICD. More frequent maintenance releases with better automation. Improved automation/regression suite that allows us to push changes incrementally to production esp bug fixes. 
- Better use of feature flags and build features while deliver in production but open up slowly and steadily. 
- Reduce number of jobs during ETL which can bring more stability to ETLs. 
- Portal re-architecture and convert MTSS into microservices. Introduce reference framework and enable dashboards from UIHN over to my powerschool hub 
- Current performance. alternate architecture of moving queries to RDS.