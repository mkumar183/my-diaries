
Ops Tasks vs Engg Tasks. 
- One way to differentiate is anything that requires writing code and following SDLC is better managed under engineering since engineering has right processes around it. Any work that does not require coding can be moved out of engineering. Coding is high value add work. Code goes to all 5000 customers and so one line of code impacts millions of users. Other work may or may not be that high impact. This way, its ensured that engineering is focused on delivering high value work. 

Difference between Engg and Cloudops
- Cloudops is organized by shifts and these roles are predominantly for monitoring and observing what's happening in production. 
- If there are thousands of pods active in production, cloudops should be trained to monitor these pods and raise issues or fix issues 

What is Ops Work ? 
- A work that happens in shifts and which is pure play monitoring work. This monitoring could be pods coming up or down. Peaking their CPUs. Disks going out of memory. Jobs failing. Sessions timing out. 
- Operations collects such phenomena happening in production and for scaled out teams registered JIRA work to automate e.g. cloudops can raise a jira ticket for automation of scaling of pods. The coding work required to get this done could be taken up by engineering which will write code, test on internal instances and finally deliver to production. 
- In our case tenant manager is an application which is code written by engineering team. This makes more sense to be owned by engineering. But cloudops should be trained on monitoring kubernetes and report any issues. 


How its applicable to Tenant Manager: 
- In UIHN we write code for managing pod configurations and managing application configurations via tenant manager. All this work should remain within engineering. 
- Certain teams may not manage Infrastructure as a code. e.g. an OLTP application that requires EC2s and ALBs it may not be automated and setup manually in cloud. In case its a manual setup in cloud which is one time hopefully, this can be executed by cloudops. However, in case team is able to automate it by writing code then this automation becomes engineering work. Since its code and why should it be different from writing any other type of code. 