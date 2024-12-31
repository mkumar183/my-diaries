Advantages of TDD: 
1. Requirements are converted to Tests first (This takes you to clear requirements extreme quality to the left). Now if your software does not meet requirements its very obvious on the top. 
2. Forces you to separate writing to disk from business logic upfront (since it doesn't make lot of sense to test something that has no logic but is simply writing input and output to disks, files or databases). Typical structure of a function that deals with disks would be. GetInputs -> BusinessLogic -> WriteOutput 
	1. In above case getInputs -> get data from disk. which can be called 
3. It helps you model your program in a modular object oriented way from beginning. 
4. It make refactoring your code very simple without having to re-test everything. 
5. It promotes iterative way of writing and improving the code without worrying about something that's already done in past. 


Guidance:
1. Focus on writing test cases for business logic. Since this is most important. 
2. Keep reading from disks, apis or any other persistent storage as separate and do not unnecessarily write test cases for these since these make your tests complex and sometime redundant since these really do not test anything. they simply mock it. 
3. This will help you keep structure of the program also like reading and writing from external sources separate from core business logic. 