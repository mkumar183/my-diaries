Roles and Responsibilities:

#### Core Team 
Consistes of Architect, Project Manager and Product Manager. Developers and testers can come and go. They will never hold the knowledge that is irreplaceable. 

#### Architect 
Technical Manager. Sees through design and implementation. Process. Sees that system is built incrementally over a period of time. later point of time conducts code reviews etc.  

#### Project Manager
Shields and encapsulates team from stakeholder noise. Provides status reports and progress on the project. 

#### Product Manager
shields and encapsulates team from customer noise. Later point of time conducts demos. 

#### Fuzzy front end 

#### Software Development Plan Review
SDP Review Meeting 
Feed Me/Kill Me Meeting 
Provide multiple options. Time, Cost & Risks 

#### Services and Developers
Assign Services to Developers in 1:1 Ratio 
However, you should never see a developer working on more than one service at a time or more than one developer working concurrently on the same service.

![tightly coupled team](../../images/tightly-coupled-system-and-team.jpeg) 

This assures even right communication between developers. Its isomorphic to service design. 

A good system design strives to reduce the number of interactions between the modules to their bare minimum—the exact opposite of what happens in Figure 7-2. A loosely coupled system design such as that in Figure 7-1 has minimized the number of interactions to the point that removing one interaction makes the system inoperable.

#### Service Dependency Graph and Task Continuity

*Take developer proclivities into consideration*

##### Two types of estimations
Estimation of each activity/developer/service
Estimation of entire project 
Both are unrelated.

##### Uncertainty is the cause. Reduce uncertainty. 

*Overestimation. Parkinson's Law. Gold Plating.* 
These (overestimation and underestimation) are not just common, classic mistakes—they are cardinal mistakes.

![probability of failure](../../images/prob-of-failure.jpeg)

#### Uncertainty vs Unknown
Example: Certainty of my demise vs knowing the exact date of the same. 

When asking people to estimate, you should help them overcome their fear of estimations.

Confronted with the uncertain, take these steps:

Ask first for the order of magnitude: Is the activity more like a day, a week, a month, or a year? With the magnitude known, narrow it down using factor of 2 to zoom in. For example, if the answer to the first question was a month as the type of unit, ask if it is more like two weeks, one month, two months, or four months. The first answer rules out eight months (since that is more like a year as an order of magnitude), and it cannot be one week because that was not provided in the first place as an order of magnitude.

Make an explicit effort to list the areas of uncertainty in the project and focus on estimating them. Always break down large activities into smaller, more manageable activities to greatly increase the accuracy of the estimations.

Invest in an exploratory discovery effort that will give insight into the nature of the problem and reduce the uncertainty. Review the history of the team or the organization, and learn from your own history how long things have taken in the past.

#### Activity Time 
Time required to complete this activity
Time required to reach this activity 


#### Critical Path Analysis
Most important analysis in coming up with timing for the project level. 
Requires list of activities, services, dependencies between activities and services, assumptions and effort estimates. 

Building blocks of the architecture and dependencies between these building blocks or architectural components. 

That longest path in the network is called the critical path

Because the critical path is the longest path in the network, it also represents **the shortest possible project duration**. *Any delay on the critical path delays the entire project and jeopardizes your commitments.*

![activities dependencies](../../images/activities-dependencies.jpeg)

#### Assigning Resources
During project design, *the architect assigns abstract resources (such as Developer 1)* to each of the project design options. Only after the decision makers have chosen a particular project design option can the *project manager assign actual resources*.

Assign your best developers to critical path first. 

#### staffing level
Based on the network diagram of the project, it should be critically thought as how many resources should be assigned to which project at which given point of time. 

![critical path](../../images/critical-path.jpeg)
#### Float based prioritization 
start with 1 which is highest priority. 
2 can float until its going to impact completion time of 16. 
6 and 7 can wait until backward tracking of 11 is impacted which impacts 15 
so at this point additional resources should first go on 3 and then on 5 and 10 so that time to complete of 8 is not impacted 
(based on critical path it can be assume time to 5 and 10 is less than time to complete 3)


