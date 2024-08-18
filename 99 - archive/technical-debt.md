https://www.productplan.com/glossary/technical-debt/

##Technical Debt
### What is Technical Debt?
Technical debt (also known as tech debt or code debt) describes what results when development teams take actions to expedite the delivery of a piece of functionality or a project which later needs to be refactored. In other words, it’s the result of prioritizing speedy delivery over perfect code.

If you’ve been in the software industry for any period of time, chances are you’ve heard the term “technical debt”. Also known as design debt or code debt, the phrase (or more accurately, the metaphor) is widely used in the technology space. It is referred to as a catchall that covers everything from bugs to legacy code, to missing documentation. But what exactly is technical debt anyway? And why do we call it that?

Technical debt is a phrase originally coined by software developer, Ward Cunningham, who in addition to being one of 17 authors of the Agile Manifesto, is also credited with inventing the wiki. He first used the metaphor to explain to non-technical stakeholders at WyCash why resources needed to be budgeted for refactoring.

He didn’t realize at the time, but he had coined a new buzzword in the software community. Later, it would become the subject of countless academic studies, debates, and panel discussions.

Years later, Cunningham described how he initially came up with the technical debt metaphor:

“With borrowed money, you can do something sooner than you might otherwise, but then until you pay back that money you’ll be paying interest. I thought borrowing money was a good idea, I thought that rushing software out the door to get some experience with it was a good idea, but that of course, you would eventually go back and as you learned things about that software you would repay that loan by refactoring the program to reflect your experience as you acquired it.”

For an in-depth look at technical debt, watch this video:



 

### Is There a Simplified Definition of Technical Debt?
Since metaphors are inherently abstract, the true definition of technical debt is up to interpretation. Various people have developed their own personal definitions for it over the years. Over time, several highly-nuanced explanations have evolved but at a high level. We can see several themes that can help us build a concrete definition for technical debt.

### It is a Tool
Much like someone may take out a loan on a property as a means of getting into a booming real estate market before being priced out, technical debt is often used as a tool for “getting ahead.” Trey Huffine, founder of gitconnected explains the role of technical debt through the lens of a startup. His definition is straightforward, “technical debt is any code added now that will take more work to fix at a later time—typically with the purpose of achieving rapid gains.”

### It Has Consequences
Shaun McCormick’s definition of technical debt focuses more on the consequences in the long term, “I view technical debt as any code that decreases agility as the project matures. Note how I didn’t say bad code (as that is often subjective) or broken code.” He suggests that true technical debt is always intentional and not accidental.

Gaminer’s explanation of what they call the fallacy of technical debt focuses heavily on the concept of paying interest later. “Technical debt happens when you take shortcuts in writing your code so that you achieve your goal faster, but at the cost of uglier, harder to maintain code. It’s called technical debt because it’s like taking out a loan. You can accomplish more today than you normally could, but you end up paying a higher cost later,” they write in a Hackernoon article.

### It is NOT a Mess
Sometimes when trying to define a somewhat abstract concept it can be useful to understand what it is NOT.

In an impassioned post, a long-time software development consultant, Uncle Bob writes “A mess is not a technical debt. A mess is just a mess. Technical debt decisions are made based on real project constraints. They are risky, but they can be beneficial. The decision to make a mess is never rational. It’s always based on laziness and unprofessionalism and has no chance of paying off in the future. A mess is always a loss.”

By his definition, taking on technical debt is always intentional and strategic. His explanation supports McCormick’s claim that bad code does not qualify as technical debt. Later, when we address the various ways to classify technical debt, you’ll see that not every instance of technical debt falls into this category.

### An Academic Definition for Technical Debt
With the wide array of opinionated definitions for technical debt, several academic works have attempted to present an unbiased, concrete definition for this abstract concept. For example, an article in the Information and Software Technology Journal defines technical debt in very specific terms:

“Technical debt describes the consequences of software development actions that intentionally or unintentionally prioritize client value and/or project constraints such as delivery deadlines, over more technical implementation, and design considerations…”

The same article expands on the metaphor for technical debt, “Conceptually, technical debt is an analog of financial debt, with associated concepts such as levels of debt, debt accrual over time and its likely consequences, and the pressure to pay back the debt at some point in time.”

### Are There Different Types of Technical Debt?
For as many definitions of technical debt that there are out there, there are just as many types of technical debt. For years, software development practitioners have sought new ways to classify and communicate technical debt.

In 2007, Steve McConnell suggested that there are 2 types of technical debt: intentional and unintentional. According to him, intentional technical debt is technical debt that one takes on consciously as a strategic tool. As opposed to unintentional debt, which he calls “the non-strategic result of doing a poor job.”

A few years later, Martin Fowler took McConnell’s concept a step further and published what he calls the “Technical Debt Quadrant.” This quadrant attempts to categorize technical debt into 4 categories based on both intent and context. Fowler says technical debt can be classified based first on intent: is it deliberate or inadvertent? And then even further distinguished by whether it is prudent or reckless debt.

Martin Fowler's 4 Categories of Technical Debt

![tech debt](../../images/techDebtQuadrant.png)

In 2014, a group of academics noted the existing frameworks for categorizing technical debt didn’t directly address the specific nature of the debt. They dismissed the categories proposed by McConnell and Fowler and proposed classifying technical debt by its nature rather than whether it was strategic or not.

According to the resulting paper, which was published by the Software Engineering Institute as “Towards an Ontology of Terms on Technical Debt,” there are 13 distinct types of technical debt and a set of key indicators for each.

- Architecture Debt
- Build Debt
- Code Debt
- Defect Debt
- Design Debt
- Documentation Debt
- Infrastructure Debt
- People Debt
- Process Debt
- Requirement Debt
- Service Debt
- Test Automation Debt
- Test Debt

### Is Tech Debt Bad?
If you want a simple answer: technical debt is neither good nor bad, it’s debt. And just like financial debt, there are several schools of thought around whether technical debt is a good or bad thing. So rather than searching for an objective answer, we will address a few of the different perspectives here.

Most software companies today are under pressure from the market and competitive forces to develop and ship fast. Startups especially feel this “ship or sink” pressure. This need for speed leads many product and software development teams to make the trade-off between taking on technical debt or launching later.

This is why the general consensus from most agile teams is that technical debt is not inherently bad. In fact, most, if not all software products have some degree of technical debt. When you consider how much code teams ship every day (especially in agile environments where working software is the primary measure of progress) this is not a surprising claim.

Download the Agile Product Manager's Guide to Building Better Products ➜

On the other hand, many software development teams working strictly within the Waterfall software development methodology and other documentation-driven frameworks do not share this perspective.

As Steve McConnell points out, attitudes toward technical debt vary greatly based on not only company philosophy but also across departments and roles.

“I’ve found that business staff generally seems to have a higher tolerance for technical debt than technical staff does. Business executives tend to want to understand the tradeoffs involved, whereas some technical staff seems to believe that the only correct amount of technical debt is zero.” McConnell writes, explaining that he attributes this aversion to technical debt to the communication challenges it will inevitably create down the line.

Technical staff, he says, often are tasked with trying to explain technical debt to business staff, who may not immediately see the implications. “The main issue seems to be that, unlike financial debt, technical debt is much less visible, and so people have an easier time ignoring it,” he suggests.

So the takeaway here is, context matters when determining whether technical debt is good or bad. In general, you can think of technical debt in the same way you do financial debt: it’s not problematic until it is.