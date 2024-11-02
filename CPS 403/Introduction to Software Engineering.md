Books:
	- Software Engineering by Ian Sommerville 10th Edition

Software is a group of programs working together to perform a specific task.

Software engineering is concerned with the theories, methods, techniques and tools of producing cost effective software which meets the needs of the end-users (stakeholder)

Why: The economy of all developed nation are all developed on software. More and more systems are software controlled i.e (course registration, payment). The expenditure on software represents a significant fraction of the GNP (Gross National Product). Software cost often dominate computer system cost. 

Software can be divided into:
- **Generic Products:** Standalone systems that are marketed and sold to any customer who wishes to buy them. Also know as off-the-shelf software. E.g. Photoshop. The specification of what the software will do is owned by the developer.
- **Customized Product**: Tailor made products, software that is commissioned by a specific customer to meet their own specific needs. e.g. Embedded control system, air-traffic software system, traffic monitoring system, result computation. Bespoke. The specification of what the software will do and look like is owned by the customer. 

Attributes of a good software system:
1. Cost-effective 
2. Maintainable
3. Dependable  
4. Reliable
5. **Useable**: easy to navigate and use by the user. 
6. Security
7. Acceptability 

Key challenges facing software developer:
1. Increasing diversity, multiple language.
2. Staff retention: Keeping software engineer is costly 

---
21/10/2024

**Software process**: is a set of structured activities required to develop a working software system.

**Key components of software development:**
- **Specification**: defining what the system should do
- **Design and implementation**: Defining the organazation of the system and implementation of the system
- **Testing**: testing and validating the system built, and to make sure it meets the requirements of the specification.
- **Evolution**: Software deployment, changing the system in response to changing customers needs. 

**Model**: A representation of an abstract entity, simplified representation of a complex system or idea, it is an abstraction that helps to understand, analyze and predict the outcome of a phenomenon.

**Type of models**:
- **Physical Model**: a representation of objects or system. e.g architectural model of a building or estate
- **Mathematical Model**: represented inform of equations or algorithms. 
- **Conceptual models**: representation of ideas or concepts.
- Simulation model
- **Statistical model:** Data driven representation of patterns and trends

**Benefits of models:**
- **Insights**: Models provide understanding of complex system.
- **Efficiency**: Models streamline analysis of decision making
- **Accuracy:** Models improve prediction and forecasting
- **Innovation**: Models facilitate experimentation and scenario planning
- **Communication**: models facilitates knowledge sharing

**Software process model:** Software process model is an abstract representation of a process for developing a software. This represents a description of a process from some particular perspective. It includes the product, the roles of stakeholder, and the pre and post conditions.

**Types of process models:**
1. **Plan-driven model:** are processes where all the process activities are planned in advanced and progress is measured against this plan
	1.  Waterfall model
	2. Reusable components model
	3. Spiral model
1. **Agile Model**: Planning is incremental and it is easier to change the process to reflect changing customer requirement
	Variants of Agile:
	1. Scrum
	2. Extreme programming
	3. Kanban
There is no such thing as a good or bad model, in practice we have a fusion of process models.


---
28/10/24

**Waterfall Model**
Waterfall Model: often used in building large complex systems. It is a linear sequential approach to software development. Plan-driven model. Separate and distinct phases of specification and development.

- Specification
- Design
- Implementation
- Testing/Validation
- Integration & Deployment

**Tools used in specification:**
- Context diagram
- Architectural diagram
- Dataflow diagram
- Sequence diagram

Validation is checking if the program performs the action the user intended while verification is to ensure all expectations can be handled by the system

**Features of Waterfall Model**
- Linear progression
- Predictive: Project plan is fixed with clear deadline and deliverables.  
- Sequential

**Advantages of waterfall manage**:
- Easy to manage: A linear progression makes it easy to manage and track progress
- Clear deadline: the predictive nature of waterfall model provides a clear deadline.
- Well defined requirements
- Less risky
- Flexibility: Processes can be broken down and assigned to different teams to work on. 

**Disadvantages:**
- Inflexibility: The linear progression makes is difficult to accommodate changes in requirements 
- High risk of project failure: If requirement are not well defined
- Long development cycle
- Difficulty in accommodating changes

**Situations to use waterfall**
- Fixed deadline
- When all requirements are gathered
- Low risk project

**What will make it fail**
- Insufficient project requirement
- Poor project design
- Inadequate testing
- Lack of flexibility to add to changes

**Incremental Design Model**
After initiation all other phases are interleaved. This model allows amendments to be made at each phase

![[Pasted image 20241028152439.png]]
**Incremental development benefits**:
- The cost of accommodating changing customer requirements is reduced
- It is easier to get customer feedback on the development work that has been done.
- More rapid delivery and deployment of useful software to the customer is possible

**Incremental development problems**:
- The process is not visible
- System structure tends to degrade as new increments are added. 

**When will incremental design approach be suitable**:
- User isnt certain about the requirement