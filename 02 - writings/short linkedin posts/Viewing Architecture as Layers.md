
Software becomes an art form. Just like you understand a painting by understanding its layers and how layer by layer it was built reveals. A software is best understood by its layers. 

A good architect views a software in terms of its layers. 

Each layer can then be divided in boxes that separate certain part of that layer from the rest. 

now you have a picture to represent a software in form of layers of boxes that interact with each other. 

Architecture is the pattern across these boxes. 

Scalable architecture is when you can easily add more boxes to each layer without disturbing the architecture. Its like you have architecture of a building and now you can add another block into it that follows exactly the same pattern as the rest. 

You look at a software application and start asking these questions: 
- What are the layers . common layers are client, business logic and storage layer. 
- how is the software deployed. is it in some VMs, EC2s, database servers etc. How do these hardware interact with each other ? 
- How do different layers and boxes interact and communicate with each other. 
- Are responsibility of each layer and boxes clearly defined such that when a problem arise an engineer can pin point that problem to a single box ? 
- would there be kind of changes that will distrub all boxes or the changes that come in application end up constraint to few of these boxes ? 