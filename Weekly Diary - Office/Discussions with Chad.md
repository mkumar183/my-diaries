- Architectural opportunities
	- CICD for ETLs. In case it can be broken by each functional component. 
	- Modularize upgrade such that each component can be upgraded indepednently 
	- Allowing frequent releases
	- Proper Feature flag usage for blue green deployments 
- QA: Improving upon Regression suite. 
	- Reducing manual QA Effort and increasing automation. What parts are we testing. 
- 
- Defining the boundaries 
	- Issues from Support 
		- Product for product improvements such as data quality issues 
		- Product to write required configurations clearly and communication. Right Documentation for setting up each module 
		- Configuration issues to be dealt with product and cloudops and not come to engineering
	- Cloudops 
		- ETL Issues 
			- Differentiation between functional configurations vs infrastructure configurations 
			- ETL Issues: Data issues to be fixed by Engineering. Cloudops to be able to detect any infrastructure issues. 
		- Infrastructure Monitoring 
			- To be owned by cloudops completely 
		- New customer onboarding
			- To be owned by cloudops completely 
	- Content work 
		- Content versioning is pending for a long time 
- TM: not an emergency but may be a long term strategy to take care of it.
- pscore 
- Individual people he is working with and feedback 