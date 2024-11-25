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
- The process is not visible: Managers need regular deliverables to measure progress. If systems are developed quickly, it is not cost-effective to produce documents that reflect every version of the system. 
- System structure tends to degrade as new increments are added. 

**When will incremental design approach be suitable**:
- User isnt certain about the requirement

---
04/11/2024

## Reusable Component Model

This is based on systematic reuse where systems are integrated from existing components or COTS(Commercial-off-the-shelf) systems.

**Process stages:**
- Requirements specification
- Component analysis
- Requirements modification
- System design with reuse
- Development and integration
- System Validation
![[Pasted image 20241104144217.png]]

**Types of software component**:
- Web services that are developed according to service standards and which are available for remote invocation. 
- Collections of objects that are developed as a package to be integrated with a component framework such as .NET or J2EE.
- Stand-alone software systems (COTS) that are configured for use in a particular environment.



## Specification

This is the process of establishing what services are required and the constraints on the system's operation and development.

**Process of requirement engineering (specification):**
- **Feasibility study**: Is it technically and financially feasible
- **Requirements elicitation and analysis**: what exactly do the system stakeholders require or expect from the system.
- **Requirements specification**: Defining the requirements in detail
- **Requirements validation**: Checking the validity of the requirement. 

![[Pasted image 20241104150826.png]]

**Software design**: This is the process of converting the system specification into an executable system. 

**Implementation:** Translate this structure into an executable program;

**functional requirements** define what the system should do. They specify the core functionality and features of a system, describing the tasks it must perform. Examples include user authentication, data processing, and reporting.

**Non-functional requirements** define how the system should perform those tasks. These are quality attributes, like performance, scalability, usability, reliability, and security, which influence the system's operational standards.


![[Pasted image 20241104151541.png]]

|              | Context Diagram                                                                                                                           | Architectural Diagram                                                                                                       |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Purpose      | Shows the system's interaction with external entities (like users, other systems, or data sources) but does not go into internal details. | Provides a detailed view of the system’s internal structure and components, including how they interact with each other.    |
| Focus        | Only on high-level relationships, data flow, and the boundaries of the system.                                                            | Internal organization of the system, including layers, components, modules, databases, servers, and network configurations. |
| Detail Level | High-level, providing a broad overview of inputs and outputs.                                                                             | More detailed than a context diagram, often technical, aimed at developers and engineers.                                   |
| Usage        | Useful for stakeholders who need to understand the system's overall context without technical detail.                                     | Used for technical planning and development, showing how components work together within the system.                        |


In summary, a context diagram is more about the external perspective (what interacts with the system), while an architectural diagram dives into the internal workings and structure of the system.

List reasons why software development could fail:
- Lack of clear understanding of the requirement
- Faulty software design
- Bad implementation
- Improper testing
- Bad documentation


---
## Agile

The agile manifesto
![[Pasted image 20241111144637.png]]

## Principles of agile method

| Principle               | Description                                                                                                                                                                 |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Customer Involvement    | Customers should be closely involved throughout the development process. <br>                                                                                               |
| Incremental Delivery    | The software is developed in increments with the customer specifying the requirements to be included in each increment.<br>                                                 |
| People not process      | The skills of the development team should be recognized and exploited. Team members should be left to develop their own ways of working without prescriptive processes.<br> |
| Embrace change<br>      | Expect the system requirements to change and so design the system to accommodate these changes.<br>                                                                         |
| Maintain simplicity<br> | Focus on simplicity in both the software being developed and in the development process. Wherever possible, actively work to eliminate complexity from the system.<br>      |

**Areas where agile method is applicable**:
- Product development where a software company is developing a **small** or **medium-sized** product for sale. 
- Custom system development within an organization, where there is a *clear commitment* from the customer to become involved in the development process and where there are not a lot of external rules and regulations that affect the software.

Problems with the agile method
- It can be difficult to keep the interest of customers who are involved in the process.
- Team members may be unsuited to the intense involvement that characterises agile methods.
- Prioritising changes can be difficult where there are multiple stakeholders.
- Maintaining simplicity requires extra work.
- Contracts may be a problem as with other approaches to iterative development: Scope of contract can be elongated by the customer


Agile vs Plan Driven Method:

| **Consideration**                     | **Agile Development**                                                              | **Plan-Driven Development**                                                                           |
| ------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Detailed Specification and Design** | Not required initially; design evolves during development.                         | Required before implementation.                                                                       |
| **Incremental Delivery**              | Well-suited for incremental delivery with regular customer feedback.               | Not as flexible with incremental delivery; feedback is limited to set stages.                         |
| **System Size**                       | Works best for small to medium-sized systems with small, co-located teams.         | Suited for large systems that require extensive coordination among teams.                             |
| **System Type**                       | Works well for systems without complex requirements (e.g., business apps).         | Suitable for systems with complex requirements that need detailed analysis (e.g., real-time systems). |
| **System Lifetime**                   | May have less focus on long-term documentation.                                    | Emphasizes comprehensive documentation for long-term maintenance.                                     |
| **Supporting Technologies**           | Requires tools to support continuous integration and evolving design.              | May rely on fewer specialized tools, as the process is defined upfront.                               |
| **Team Organization**                 | Works best with small, co-located teams.                                           | Supports distributed or outsourced teams, where documentation is needed to maintain consistency.      |
| **Cultural and Organizational Fit**   | Suits modern, flexible, and tech-centric environments.                             | Preferred by traditional engineering organizations with a structured development culture.             |
| **Team Skill Level**                  | Requires skilled designers and programmers comfortable with evolving requirements. | Can accommodate less skilled developers, as they follow a well-defined design.                        |
| **External Regulation**               | May struggle with high regulatory requirements due to evolving documentation.      | Well-suited for regulated industries where detailed documentation is mandatory for compliance.        |
Flavor of agile development:
1. Scrum
2. Extreme Programming: r every build and the build is only accepted if tests run successfully.
3. Kanban 
4. Lean software development

**Extreme Programming**
takes an ‘extreme’ approach to iterative development. 
	New versions may be built several times per day;
	Increments are delivered to customers every 2 weeks;
	All tests must be run fo

Principles of extreme programming:
- Incremental Planning
- Small releases
- Simple design
- Test-first development
- Refactoring


---
159000
# Functional And Non Function
In software design requirements are divided into functional & non-functional

**Functional**: This describes the specific functions or behavior that a software system must perform. They define what the system should do, how it should behave and what it should provide.
Examples include:
1. The system can allow user to login with username and password
2. The system can display a list of products with their prices and descriptions. 
3. The system can enable users to add, edit and delete products.
4. The system shall generate invoices for orders

Non-functional : Describes the overall qualities or characteristics that a software system should posses, they define how the system should behave, perform  or used without specifying functions.
Examples of non-functional requirements:
1. Performance: the system should respond to a user request within a few second
2. Security: System shall ensure that all user data is encrypted and protected from unauthorized access
3. Usability: The system shall provide an intuitive and userfriendly interface
4. Reliabability: The system shall be available. 99.99% of the time, with the maximum downtime of one hour per month
5. Scalability: The system should be able to handle at least one thousand concurrent users without a significant decrease in performance
6. Portability: The system should be able to run on multiple platforms,
7. Maintainablity: The system shall be easy to update and maintain

---
## Architectural Design in SE

In software engineering, architectural design refers to the process of creating a high level structure and organization of software systems, It involves designing the overall architecture of the system, including the components relationships and interaction between them. The goal of architectural design is to create a blueprint or a framework that will guide the development of the software system, it helps to ensure that the system meets the required functional and non-functional requirements, such as performance, scalability, security and maintainability. 
The key elements of architectural design:
1. The components: These are the building blocks of the system, such as modules, services and subsystems
2. The interface: How components interact with each other, including apis, data format, and communication protocols.
3. The relationships: This describe how components are connected and how they interact with each other
4. Layers: Logical groupings of components, which performs specific functions, quality attributes, non-functional attributes 
5. Deployment: Refers to the physical infrastructure and environments which the system will be deployed.

==Read chapter 4==


--- 
## UML
refers to Unified Modelling Language diagram and they are a set of graphical representation used to model and design software system. They provide a standard way to visualize, specify and document software systems.  It makes it easier for developers, stakeholders, and users to understand and communicate about the system.

- Class diagram
- Object diagram
- Use-case diagram
- Sequence Diagram
- Activity Diagram