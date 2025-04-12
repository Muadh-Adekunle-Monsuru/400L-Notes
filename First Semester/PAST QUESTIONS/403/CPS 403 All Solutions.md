1. Error, fault and failure are often used interchangeably with a diffused meaning, discuss them
**1. Error:**
*   **Definition:** An *error* is a human action that results in a system containing a *fault*.
*   **Source:** Errors are made by people (developers, designers, testers, operators, etc.)
*   **Examples:**
    *   A programmer writing the wrong operator in a conditional statement (e.g., using `<` instead of `<=`).
*   **Key Characteristic:** It is the *cause* of the issue. The error *introduces* the problem into the system.

**2. Fault:**
*   **Definition:** A *fault* (also called a *defect* or a *bug*) is a static condition in a system that can cause a system to fail to perform its required function. It is an anomaly in the code, data, or documentation.
*   **Origin:** Faults are the *result* of errors.
*   **Examples:**
    *   Incorrect code in a software program.
    *   Missing or incorrect data in a database.
*   **Key Characteristic:** The fault is a *manifestation* of the error, representing the actual problem within the system. A fault does not always lead to failure.

**3. Failure:**
*   **Definition:** A *failure* occurs when the system deviates from its specified or expected behavior. This occurs when a *fault* is exercised under particular conditions.
*   **Origin:** Failures are the *result* of a *fault* being activated.
*   **Examples:**
    *   The system giving the wrong answer to a query.
    *   The system taking much longer to process a request than specified.
*   **Key Characteristic:** A failure is an *observable event*. It's what the user or operator experiences when the system isn't working correctly.

**Summary in a Table:**

| Term    | Definition                                                | Source          | Manifestation                    | Observable Event |
| ------- | --------------------------------------------------------- | --------------- | -------------------------------- | ---------------- |
| Error   | Human action resulting in a fault                         | Human           | N/A                              | NO               |
| Fault   | An anomaly in the system that can cause failure.          | Error           | Incorrect code, data, etc.       | Potentially      |
| Failure | Deviation from specified/expected behavior due to a fault | Fault Activated | System malfunction, wrong result | YES              |

---
![[403 TEST 2023.jpeg]]


**1. Agile Software Development & Deployment:**

*   **a) Agile Software Development Approach (4 marks):** The Agile approach is an iterative and incremental development methodology that emphasizes flexibility, collaboration, customer feedback, and rapid adaptation to change. It prioritizes delivering working software frequently, rather than focusing on extensive upfront planning and documentation. Key characteristics include short development cycles (sprints), close customer involvement, self-organizing teams, and continuous improvement.

*   **b) Accomplishing Development & Deployment with Agile Process (6 marks):**
    *   **Planning:** Break down the project into smaller, manageable user stories and prioritize them in a product backlog. 
    *   **Iterative Development:** Work on the stories within each sprint, focusing on delivering working, tested software at the end of the sprint.
    *   **Continuous Integration:** Integrate code frequently to detect and address integration issues early.
    *   **Customer Collaboration:** Regularly engage the Fountain Microfinance Bank to gather feedback, refine requirements, and validate the developed software.
    *   **Sprint Reviews:** Demonstrate the working software to stakeholders at the end of each sprint for feedback.
    *   **Incremental Deployment:** Deploy working software in increments, allowing the bank to start using parts of the system early on and provide ongoing feedback.

*   **i) Principles Underscoring Agile Development (4 marks):** The Agile Manifesto is based on key principles, some of which includes:
	- Customer Involvement
	- Incremental Delivery
	- People not process
	- Embrace change
	- Maintain simplicity
* **j) COTS vs. Scratch Development Recommendation :** I would advise carefully evaluating both options based on specific criteria.
    *   **COTS Benefits:** Faster implementation, lower initial cost (potentially), and proven functionality.
    *   **COTS Risks:** Potential lack of fit with specific bank needs, vendor dependency, ongoing licensing costs, customization limitations.
    *   **Scratch Development Benefits:** Full customization, ownership of the solution, potential for competitive advantage.
    *   **Scratch Development Risks:** Higher development cost, longer development time, risk of technical challenges.

**1) Agile Manifesto (4 marks):**
*   **l) State the Agile Manifesto**.
The Agile Manifesto is;
- *Individuals and interactions* over processes and tools
- *Working software* over comprehensive documentation
- *Customer collaboration* over contract negotiation
- *Responding to change* over following a plan

**2. Software Engineering:**

*   **a) Understanding of Software Engineering (4 marks):** Software engineering is concerned with the theories, methods, techniques and tools of producing cost effective software which meets the needs of the end-users (stakeholder). Software Engineering is the systematic, disciplined, and quantifiable approach to the development, operation, and maintenance of software. It emphasizes quality, reliability, efficiency, and maintainability throughout the software lifecycle.

*   **b) Software Process Activities (4 marks):** Software development typically involves these key process activities:
    *   *Requirements Engineering:* Gathering, analyzing, and documenting the needs of the client.
    *   *Design:* Creating the software architecture, components, and interfaces.
    *   *Implementation:* Writing the code.
    *   *Testing:* Verifying and validating that the software meets its requirements.
    *   *Deployment:* Releasing and installing the software in the production environment.
    *   *Maintenance:* Fixing bugs, adding new features, and adapting the software to changing needs.

---
![[403_1 2023.jpeg]]

### **Question 1**  

#### **(a) Software Development Approach**  
i. **Suggested Software Development Approach**  
   - The best approach for this contract is the **Agile Software Development Methodology** because it allows flexibility, iterative development, and continuous feedback from stakeholders.

ii. **Explanation of the Agile Approach**  
   - Agile focuses on delivering software in small, incremental releases.  
   - It involves close collaboration with stakeholders and continuous adaptation based on feedback.  
   - Agile methodologies include Scrum, Kanban, and Extreme Programming (XP).

iii. **Accomplishing Development and Deployment**  
   - Gather requirements through meetings with stakeholders.  
   - Form a development team and define user stories.  
   - Implement an iterative development cycle (Sprint Planning, Development, Testing, Review).  
   - Perform rigorous testing after each sprint and refine features based on feedback.  
   - Deploy a Minimum Viable Product (MVP) and progressively enhance it.  
   - Ensure continuous maintenance and updates post-deployment.

iv. **Five Suggested Modules**  
   - **User Authentication Module**: Handles login, registration, and access control.  
   - **Financial Transactions Module**: Manages payments, transfers, and transaction history.  
   - **Reporting & Analytics Module**: Provides insights, reports, and data visualization.  
   - **Customer Support Module**: Enables communication with employees and clients.  
   - **Security & Compliance Module**: Ensures data protection and regulatory compliance.

v. **Principles Underlying Agile Development**  
   - **Customer Collaboration**: Engaging users frequently for feedback.  
   - **Incremental Delivery**: Developing in small, workable pieces.  
   - **Adaptive Planning**: Allowing flexibility in requirements and solutions.  
   - **Continuous Improvement**: Regularly refining processes and features.  

#### **(b) Commercial Off-The-Shelf (COTS) vs. Custom Software**  
- **Advising the Client**: COTS is recommended if cost and time are constraints, as it is pre-built and ready for deployment.  
- **Wisdom of the Decision**:  
  - **Pros**: Faster implementation, lower cost, vendor support, reliability.  
  - **Cons**: Limited customization, potential licensing issues, dependency on vendor updates.  

#### **(c) Agile Manifesto**  
- **Individuals and interactions** over processes and tools.  
- **Working software** over comprehensive documentation.  
- **Customer collaboration** over contract negotiation.  
- **Responding to change** over following a plan.  

---

### **Question 2**  
#### **(a) Understanding Software Engineering**  
- Software Engineering is the systematic application of engineering principles to software development.  
- It involves planning, designing, building, testing, and maintaining software systems to ensure reliability and efficiency.  

#### **(b) Software Development Process Activities**  
1. **Requirements Engineering** – Gathering and analyzing software needs.  
2. **System Design** – Structuring the architecture of the software.  
3. **Implementation** – Writing code and integrating components.  
4. **Testing & Debugging** – Ensuring software functions correctly.  
5. **Deployment** – Releasing the product for use.  
6. **Maintenance** – Providing updates and bug fixes post-deployment.  

#### **(c) Use Case Diagram for a University System**  
- **Actors**: Student, Researcher, Instructor, Administrator, Registrar.  
- **Use Cases**:  
  - Student: Register courses, submit assignments.  
  - Researcher: Upload publications, access research data.  
  - Instructor: Grade students, upload lectures.  
  - Administrator: Manage student records, schedule exams.  
  - Registrar: Approve admissions, process results.  

![[Pasted image 20250211105304.png]]


---

### **Question 3**  
#### **(a) Project Management in Software Engineering**  
**Software Project Management** involves planning, executing, monitoring, and closing software development projects to ensure they are completed successfully within budget and on time. 
#### **(b) Key Phases of Software Project Management (CAF - Common Activity Framework)**  
1. **Initiation** – Identifying project scope, feasibility, and key objectives.  
2. **Planning** – Defining tasks, schedules, resources, and risks.  
3. **Execution** – Developing the software, ensuring adherence to plans.  
4. **Monitoring & Control** – Tracking progress, making adjustments.  
5. **Closure** – Finalizing deliverables, client approval, maintenance planning.  

#### **(c) Challenges in Software Project Management**  
1. **Changeability of Software**: Requirements often evolve during the project.  
2. **Technical Uncertainty**: Unanticipated challenges with new technologies.  
3. **Team Dynamics**: Communication breakdowns and skill mismatches can disrupt progress.  
4. **Client Involvement**: Managing expectations and priorities effectively.  
5. **Resource Constraints**: Balancing limited budgets, time, and personnel.  
6. **Defining Success**: Establishing clear metrics for success beyond basic functionality.  

#### **(d) Critical Success Factors in Managing Projects**  
1. **Clear Objectives**: Well-defined and measurable goals (SMART framework).  
2. **Detailed Requirements**: Clearly document functional and non-functional requirements.  
3. **Realistic Schedule and Budget**: Plan with accurate estimates and buffers for issues.  
4. **Effective Project Management**: A strong leader to manage risks, communication, and issues.  
5. **User-Centric Development**: Involve users and gather feedback during development.  
6. **Skilled Team**: Ensure a qualified and motivated team is in place.  
7. **Continuous Monitoring**: Regularly track progress, report status, and adjust as needed.  
8. **Adaptability**: Adjust plans based on changing requirements or unforeseen challenges.  

---
![[403_1 2020.jpeg]]


### **Question 1**  

#### **(a) Step-by-Step Approach to Implement a Tourism Management System**
1. **Requirement Gathering & Analysis**  
   - Engage stakeholders (government officials, tourism operators, end-users).  
   - Define system requirements and expected functionalities.  

2. **System Design**  
   - Develop a system architecture outlining key modules:  
     - Tourist Registration  
     - Attractions Management  
     - Accommodation Management  
     - Food & Drinks Management  
     - Transport & Logistics  
     - Payment & Billing  

3. **Technology Selection**  
   - Choose an appropriate tech stack (e.g., React, Node.js, PostgreSQL).  

4. **Prototype Development**  
   - Build wireframes and mockups for user interfaces.  
   - Validate designs with stakeholders.  

5. **Agile Development Process (Sprint-Based)**
   - Break tasks into sprints (e.g., 2-week cycles).  
   - Implement and test individual modules iteratively.  

6. **Testing & Quality Assurance**  
   - Conduct unit testing, integration testing, and user acceptance testing.  

7. **Deployment & Training**  
   - Deploy the system on cloud-based servers.  
   - Train government officials and tourism operators.  

8. **Maintenance & Continuous Improvement**  
   - Gather user feedback and update features accordingly.  

#### **(b) Agile Development Methodology**  
- Agile is an iterative and incremental development approach that prioritizes flexibility and customer collaboration.  
- **Reasons for Choosing Agile:**  
  1. Allows continuous feedback and improvement.  
  2. Enhances flexibility in handling changing requirements.  
  3. Delivers functional software in short cycles.  
  4. Encourages stakeholder involvement throughout the process.  
  5. Improves risk management by addressing issues early.  

- **Principles of Agile:**  
1. Customer involvement
2. Incremental delivery
3. People not process
4. Embrace change
5. Maintain simplicity
#### **(c) Likely Issues That May Affect Timely Completion**  
1. **Changing Requirements** – Government policies may shift, requiring adjustments.  
2. **Technical Challenges** – Integration with existing infrastructure may be difficult.  
3. **Budget Constraints** – Insufficient funding could slow development.  
4. **Skill Shortage** – Limited expertise may delay implementation.  
5. **User Adoption Issues** – Resistance from end-users could cause delays.  

#### **(d) Five Critical Success Factors for 100% Success**  
1. **Clear and Well-Defined Requirements** – Avoid ambiguity in system needs.  
2. **Effective Communication** – Ensure all stakeholders are aligned.  
3. **Strong Project Management** – Maintain realistic schedules and milestones.  
4. **Continuous Testing & Feedback** – Identify and fix issues early.  
5. **Proper Training & Documentation** – Ensure users can effectively operate the system.  

#### **(e) COTS vs. Custom Development**  
- **Recommendation:** Custom development by Fountain Consult is preferable for flexibility and scalability.  

- **Reasons:**  
  1. **Tailored to Local Needs** – Custom software can address Osun’s unique tourism dynamics.  
  2. **Better Integration** – Seamless connectivity with local databases and services.  
  3. **Long-Term Cost Savings** – Avoiding expensive licensing fees for COTS solutions.  

### **Question 2**  

#### **(a) Concept of Software Reuse (Component-Based Software Engineering)**  
- **Software reuse** involves leveraging pre-existing software components to build new applications.  
- **Component-Based Software Engineering (CBSE)** focuses on creating modular, reusable components to reduce development effort.  

#### **(b) Different Ways of Implementing Software Reuse**  
1. **Library Reuse** – Using pre-written code libraries (e.g., React, Bootstrap).  
2. **Framework Reuse** – Employing software frameworks like Django or Angular.  
3. **API Reuse** – Integrating third-party APIs (e.g., Google Maps API).  
4. **Service-Oriented Architecture (SOA)** – Developing reusable web services (e.g., REST APIs).  

#### **(c) Benefits of the Reusable Components Model**  
- **Increased Development Speed** – Saves time by using prebuilt modules.  
- **Reduced Costs** – Minimizes redundant work, lowering expenses.  
- **Improved Software Quality** – Reused components are well-tested and reliable.  
- **Enhanced Maintainability** – Modular components simplify updates and debugging.  

---
![[403_2 2023.jpeg]]


**4. Short Notes (3 marks each):**

*   **a) Functional Requirement:**
    *   Description: A functional requirement specifies what the system *should do*. It defines a specific function or behavior of the system. These requirements are directly related to the core functionality of the software.
    *   Example: The system should allow users to log in with a valid username and password.

*   **b) Non-Functional Requirement:**
    *   Description: A non-functional requirement specifies *how* the system should be or perform. It describes attributes like performance, security, usability, reliability, and maintainability. These requirements influence the overall quality and user experience of the software.
    *   Example: The system should load a webpage in under 3 seconds for 95% of users.

*   **c) Model-View-Controller (MVC):**
    *   Description: An architectural pattern used to separate the application's data (Model), user interface (View), and control logic (Controller). The Model manages data, the View displays data to the user, and the Controller handles user input and updates the Model and View.
    *   Benefits: Improved code organization, testability, and maintainability.
     *    Components work independently.
    *   Example: A web application where user input is handled by the Controller, which updates the Model (database), and the View (web page) displays the updated information.

*   **d) Attributes of Good Software:**
    *   Description: Characteristics that contribute to high-quality software.
    *   Examples:
        *   *Reliability:* Consistent and predictable performance.
        *   *Usability:* Easy to learn and use.
        *   *Maintainability:* Easy to modify and fix.
        *   *Efficiency:* Optimized use of resources (time, memory).
        *   *Testability:* Easy to verify functionality through testing.
        *   *Portability:* Able to run on different platforms/environments.

**5. Architectural Design:**

*   **a) Understanding of Architectural Design (4 marks):** Architectural Design is the process of defining the high-level structure of a software system. It involves identifying the main components, their relationships, and the overall organization of the system. It defines the blueprint of the system, guiding subsequent design and development efforts.

*   **b) Key Phases of Architectural Design (4 marks):**
    1.  *Requirements Analysis:* Understanding the functional and non-functional requirements to inform architectural decisions.
    2.  *System Decomposition:* Breaking down the system into smaller, manageable components or modules.
    3.  *Architectural Pattern Selection:* Choosing appropriate architectural patterns (e.g., layered, microservices, MVC) to address specific needs.
    4.  *Interface Design:* Defining how components interact and communicate.
    5.  *Documentation and Review:* Documenting the architecture and reviewing it with stakeholders.
    6.  *Evaluation:* Examining the architecture for usability, functionality and overall efficiency.

*   **c) UML for Weather Station (4 marks):** A class diagram is appropriate here:

    *   **WeatherStation** (Class):
        *   *Attributes:* stationID, location, lastReportTime
        *   *Operations:* reportWeather(), reportStatus(), powerSave(), restart(), shutdown(), remoteControl(), reconfigure()
        *   It is a system to determine how to report the weather of multiple locations.
    *   Relationships to other classes (if relevant, but not specified in this question, assuming it's a single-system focus).

![[Pasted image 20250211112838.png|500]]

**6. UML Diagrams (3 marks each):**

*   **a) i) Context Diagram:**
    *   Description: Shows the system and its interactions with external entities (users, other systems, hardware). Depicts the boundaries of the system and its relationship to the outside world.
    *   Use: To define system scope, identify external dependencies, and communicate system context.

*   **a) ii) Activity Diagram:**
    *   Description: A flowchart that illustrates the flow of activities within a process or system. Shows the sequence of actions, decisions, and parallel activities.
    *   Use: To model workflows, business processes, and use cases.

*   **a) iii) Sequence Diagram:**
    *   Description: Shows the interactions between objects or components over time. Emphasizes the temporal order of messages exchanged between objects.
    *   Use: To model scenarios, understand object interactions, and identify potential bottlenecks.

*   **b) Challenges for Software Professionals (3 marks):**
    *   *Keeping Up with Technology:* The software landscape is constantly evolving.
    *   *Managing Complexity:* Software projects are becoming increasingly complex.
    *   *Meeting Requirements:* Accurately understanding and fulfilling client needs.
    *   *Working in Teams:* Collaborating effectively with diverse individuals.
    *   *Maintaining Quality:* Ensuring software is reliable, secure, and performs as expected.
    *   *Ethical Conduct:* Adhering to software standards that are unbiased, equitable and promotes good conduct.

---

![[Pasted image 20250211165557.png]]
1. **Gathering requirements:** Visually capture user interactions to define system scope and features.
2. **Communication:** Provide a common language for stakeholders to discuss and validate functionality.
3. **Test case design:**  Serve as a basis for creating tests to ensure all functionalities are covered.

---
![[Pasted image 20250211170052.png]]


**3. a) Software Process & Generic Activities:**

A software process is a structured set of activities for developing and maintaining software. Generic activities include:

- **Specification:** Defining what the software should do.
- **Design & Implementation:** Creating the software's architecture and code.
- **Validation:** Testing to ensure requirements are met.
- **Evolution:** Modifying the software after deployment.

**3. b) Adapting Waterfall & Hybrid Models:**

Waterfall, though inflexible, can be adapted for short-term projects with stable requirements. Two hybrid models:

1. b) Adapting Waterfall and Hybrid Models
 While Waterfall is simple to understand, it's inflexible. Changes late in the process are difficult and costly.  For short-term projects like a payroll system for a small organization like Fountain University, where requirements are relatively stable and well-understood, some aspects of Waterfall can be useful.
	1. Incremental Model with Waterfall Phases:
	- Divide the payroll system into increments (e.g., basic pay calculation, tax deductions, reporting).
	- Apply the Waterfall phases (requirements, design, implementation, testing) to each increment.
	- **Benefit**: Delivers working parts of the system early, allowing for feedback and reducing risk.
	2. Prototyping with a Final Waterfall Phase:
	- Develop a prototype of the payroll system to clarify and validate requirements.
	- Once the prototype is approved, use the Waterfall model to develop the final production system.
	- **Benefit**: Reduces the risk of building the wrong system by ensuring a clear understanding of user needs before full-scale development.
	_Benefit of Hybrids:_ Reduced risk, early feedback, better requirements.

**3. c) Professional Responsibilities:**

Software engineers must consider:
- Confidentiality
- Competence
- Intellectual Property
- Computer Misuse
- Data Protection
- Integrity
- Professional Development

---
![[Pasted image 20250211171446.png]]

**5. a) Spiral Model**
The Spiral Model is a risk-driven software development process that helps manage risks in complex projects. It's iterative and cyclical, with each cycle representing a phase of the software process.

**Illustrative Diagram:**
![[Pasted image 20250211173919.png]]
**How it Works:**

1. **Planning:** Define objectives, scope, and constraints.
2. **Risk Analysis:** Identify and assess potential risks.
3. **Engineering:** Develop and test the software increment.
4. **Evaluation:** Review the results and plan for the next iteration.

Each loop in the spiral represents a phase. The radius of the spiral represents the cost and schedule.

**5. b) Scenarios for Spiral Model Use**

1. **High-Risk Projects:** When there are significant technical, financial, or business risks.
2. **Complex Projects:** Large-scale projects with many components and integrations.
3. **Evolving Requirements:** Projects where requirements are likely to change significantly.
4. **Long-Term Projects:** Projects spanning a long duration, allowing for risk assessment and adaptation.
5. **Research-Oriented Projects:** Projects involving new technologies or approaches where risks are unknown.

**5. c) Benefits of Spiral Model**

6. **Risk Management:** Systematic risk assessment and mitigation throughout the process.
7. **Flexibility:** Accommodates changes in requirements and project scope.
8. **Good for Large Projects:** Well-suited for complex, large-scale applications.
9. **Early User Involvement:** Users can evaluate increments early and provide feedback.
10. **Continuous Improvement:** The iterative nature allows for learning and process improvement.

**6. Short Notes**

**a) Requirement Engineering:**

The process of discovering, analyzing, documenting, and validating the requirements for a software system. It involves understanding stakeholder needs and translating them into software specifications.

**b) Software Testing:**

The process of evaluating software to identify defects and ensure it meets requirements. It involves executing the software and comparing the results with expected behavior.

**c) Project Planning Process:**

The process of defining project scope, objectives, timelines, resources, and budget. It involves creating a roadmap for executing the project and managing risks.

**d) Extreme Programming (XP):**

An agile software development methodology that emphasizes frequent releases, close customer involvement, and continuous testing. It promotes practices like pair programming and test-driven development.

**e) Architectural Design in Software Engineering:**

The process of defining the overall structure and components of a software system, their relationships, and how they interact. It involves making high-level design decisions that guide the development process.

---
![[Pasted image 20250211174524.png]]


**5. a) Software Testing as an Important Activity**

Software testing is the process of evaluating a software product to identify defects and ensure it meets its intended requirements. It's crucial because it:

- **Improves Quality:** Finds and fixes bugs, leading to more reliable software.
- **Reduces Risk:** Minimizes the chances of software failure in real-world use.
- **Enhances User Satisfaction:** Delivers a better user experience by ensuring smooth operation.
- **Saves Money:** Fixing bugs early is cheaper than after release.
- **Validates Requirements:** Confirms that the software does what it's supposed to.

**5. b) Motivations Behind Software Testing**

- **Defect Detection:** Finding and removing errors before release.
- **Validation and Verification:** Ensuring the software meets specifications and user needs.
- **Reliability Assessment:** Measuring the software's ability to perform consistently.
- **Performance Evaluation:** Checking speed, responsiveness, and stability under load.
- **Security Analysis:** Identifying vulnerabilities to protect against attacks.
- **Compliance:** Meeting regulatory or industry standards.

**5. c) Major Methods for Testing a Newly Developed Software**

1. **Unit Testing:** Testing individual components or modules in isolation to ensure they function correctly.
2. **Integration Testing:** Combining tested units and verifying their interactions.
3. **System Testing:** Testing the entire software system as a whole to ensure it meets overall requirements.
4. **User Acceptance Testing (UAT):** Having end-users test the software in a real-world environment to validate that it meets their needs and expectations.
5. **Regression Testing:** Rerunning tests after code changes to ensure existing functionality hasn't been broken.

**6. Short Notes**

**a) Agile Unified Process (AUP):**

A lightweight, simplified version of the Rational Unified Process (RUP) that embraces agile principles. It emphasizes iterative development, continuous feedback, and close collaboration.

**b) Ethical Responsibilities in Software Engineering:**

- **Confidentiality:** Protecting sensitive information.
- **Competence:** Working within expertise and staying updated.
- **Intellectual Property:** Respecting copyrights and patents.
- **Integrity:** Being honest and ethical in work.
- **Professional Development:** Staying current with best practices.

**c) Spiral Software Development Method:**

A risk-driven process that iteratively cycles through planning, risk analysis, engineering, and evaluation. It's suitable for complex projects with high risk factors.

**d) Requirement Engineering:**

The process of discovering, analyzing, documenting, and validating software requirements. It involves understanding stakeholder needs and translating them into specifications.

**e) Software Process Model:**

A framework for organizing and managing the activities involved in software development. It provides a structured approach to building software systems. Examples include Waterfall, Agile, Spiral.