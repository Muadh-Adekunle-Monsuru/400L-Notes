![[CPS 412 1.jpeg]]

#### **Question 5a**  
**Estimating Approach for a Startup Software Project:**  
**Agile (e.g., Poker Planning or Time Boxing)**  
- Startups face uncertainty and changing requirements. Agile allows iterative adjustments, quick feedback, and prioritization of high-value features.  

#### **Question 5b**  
**Five Ways to Gather User Requirements:**  
1. **Interviews** (1-on-1 with stakeholders).  
2. **Surveys/Questionnaires** (for large user groups).  
3. **Workshops** (collaborative brainstorming sessions).  
4. **Prototyping** (visual mockups for feedback).  
5. **User Stories/Use Cases** (narratives of user needs).  

#### **Question 5c**  

| **Testing Phase**            | **Purpose**                       | **User Role**              | **Documentation/Products**  |     |
| ---------------------------- | --------------------------------- | -------------------------- | --------------------------- | --- |
| **Unit Testing**             | Test individual code components.  | Minimal (developers only). | Test cases, code modules.   |     |
| **System Testing**           | Validate full system integration. | QA team (not end-users).   | Test plans, bug reports.    |     |
| **Acceptance Testing (UAT)** | Confirm business readiness.       | End-users execute tests.   | UAT scripts, sign-off form. |     |
|                              |                                   |                            |                             |     |

#### **Question 6**  
**RFP Response Outline:**  
1. **Introduction**  
   - Briefly state your company’s expertise (e.g., "5+ years in scalable SaaS solutions").  
2. **Understanding of Requirements**  
   - Paraphrase key RFP needs (e.g., "The RFP seeks a CRM for healthcare providers").  
3. **Proposed Solution**  
   - Highlight methodology (Agile), timeline, and deliverables.  
4. **Budget & Timeline**  
   - Provide estimates (e.g., "$50K, 6 months").  
5. **Conclusion**  
   - Invite further discussion (e.g., "We welcome a discovery call").  
![[CPS 412 2.jpeg]]

### **Question 1 (Continued)**  
**d) Critical Path & Network Diagram**  
- **Critical Path**: Longest task sequence determining project duration. Highlight tasks with **zero slack** (e.g., A→B→D→F = 14 days). *(5 marks)*  
### **Question 2**  
**2a) Project Manager’s Role**  
1. Define scope, schedule, budget.  
2. Lead teams/stakeholders.  
3. Manage risks/issues.  
4. Monitor progress (KPIs).  
5. Deliver project on time, within budget.   

**2b) Importance of Project Definition**  
- Aligns team/stakeholders.  
- Sets clear objectives/MOV.  
- Prevents scope creep.  
- Guides resource allocation. *(4 marks)*  

**2c) Measuring Project Success**  
- Deliverables meet MOV.  
- On time/budget.  
- Stakeholder sign-off. *(3 marks)*  

**2d) Measuring IT Project Benefits**  
- ROI: return on investment (e.g., cost savings).  
- User adoption rates.  
- Performance metrics (e.g., reduced system downtime). 

### **Question 3**  
**3a) Milestone-Focused Planning**  
**Preference**: Yes.  
**Why**: Clarifies priorities, tracks progress, and motivates teams with clear targets.

**3b) Automated vs. Manual Scheduling**  

| **Automated** (e.g., MS Project) | **Manual** (e.g., Excel) |  
|----------------------------------|--------------------------|  
| Faster updates, handles complexity. | Time-consuming, error-prone. |  
| Real-time dependencies. | Flexible for simple projects. |  


**3c) Expert Judgment Disadvantages**  
1. Bias (optimism/pessimism).  
2. Varies by expert experience.  
3. No data backing.  

**3d) Productivity Drivers**  
1. Team skill level.  
2. Tooling/technology efficiency. 


### **Question 4**  
**a) Cost Monitoring Terms**  
- **PV**: Budgeted cost for planned work. 
- **AC**: Actual spend to date.  
- **SPI**: EV/PV (schedule efficiency).  
- **EV**: Budgeted cost of completed work.   

**b) Function Point Analysis (FPA)**  
1. Count inputs/outputs/files.  
2. Weight by complexity.  
3. Adjust for environmental factors.  
4. Convert to effort (e.g., person-hours).  



![[CPS 412 22-23.jpeg]]

#### **Question 1**  

**a) Work Breakdown Structure (WBS) vs. Product Breakdown Structure (PBS)**  

- **WBS Diagram** (Hierarchical task-oriented breakdown):  
  ```
  1.0 Computer Equipment & Network Cabling Project  
    1.1 Planning  
    1.2 Procurement  
    1.3 Installation  
      1.3.1 Equipment Setup (Tasks A, B, C, E, F, H)  
      1.3.2 Cabling (Tasks D, G, I)  
    1.4 Testing & Handover (Task J)  
  ```  

- **PBS Diagram** (Deliverable-oriented breakdown):  
  ```
  1.0 New IT Infrastructure  
    1.1 Hardware (Computers, Servers)  
    1.2 Network Components (Cables, Routers)  
    1.3 Documentation (User Manuals)  
  ```  

**Key Differences**:  
- **WBS** focuses on **tasks/activities** (e.g., "Install equipment").  
- **PBS** focuses on **physical deliverables** (e.g., "Server racks").  

**b) Gantt Chart with Critical Path**  

| Task | Week 1-5 | Week 6-13 | Week 14-16 | Week 17-21 | Week 22-28 | Week 29-34 | Week 35-40 |     |
| ---- | -------- | --------- | ---------- | ---------- | ---------- | ---------- | ---------- | --- |
| A    | █████    |           |            |            |            |            |            |     |
| B    |          | ████████  |            |            |            |            |            |     |
| C    |          |           | ███        |            |            |            |            |     |
| D    |          | ████      |            |            |            |            |            |     |
| E    |          |           |            | █████      |            |            |            |     |
| F    |          |           |            |            | ███████    |            |            |     |
| G    |          |           |            |            | ██████     |            |            |     |
| H    |          |           |            |            |            | ████████   |            |     |
| I    |          |           |            |            |            | ██████     |            |     |
| J    |          |           |            |            |            |            | █████      |     |

**Critical Path**: A → B → C → F → H → J (40 weeks).  
**Free Float**: Tasks D, E, G, I have float (non-critical).  

---

**c) Updated Gantt Chart (Week 24 Progress)**  

- **Completed**: A (W1-5), B (W6-13), C (W14-16), D (W6-9), H (W22-29), I (W22-27).  
- **In Progress**: E (W17-21, on track).  
- **Revised Task F**: Now 4 weeks (W28-31).  

| Task | Week 1-5 | Week 6-13 | Week 14-16 | Week 17-21 | Week 22-28 | Week 28-31 | Week 32-36 |  
|------|----------|-----------|------------|------------|------------|------------|------------|  
| A    | █████    |           |            |            |            |            |            |  
| B    |          | ████████  |            |            |            |            |            |  
| C    |          |           | ███        |            |            |            |            |  
| D    |          | ████      |            |            |            |            |            |  
| E    |          |           |            | █████      |            |            |            |  
| F    |          |           |            |            |            | ████       |            |  
| G    |          |           |            |            | ██████     |            |            |  
| H    |          |           |            |            | ████████   |            |            |  
| I    |          |           |            |            | ██████     |            |            |  
| J    |          |           |            |            |            |            | █████      |  

**New Critical Path**: A → B → C → F → J (36 weeks).  

---

1. As an upcoming projects manager recently, you are asked to jump in a rescue, a small infrastructure project that was headed for disaster. What will you do? 

2. An upcoming University intends to introduce a compulsory laptop for all students on campus and attempts to improve the academic performance and enhance the students employability in the ever-competitive global markets. The university has consulted you as an it projects manager to relate the effects of this policy on: technology, business, and organization. You're expected to assist University in recent serveral questions that needs to be addressed in order to decide either the university should proceed on the implementing of the policy or not 

3. Organizations are operated based on four different frames. Provide brief explanation on these four frames 

4. Write two reasons why project schedules are important

#### **1. Rescuing a Failing Infrastructure Project**  
**Steps to Take:**  
1. **Assess the Situation** – Review project scope, timeline, budget, and team performance to identify root causes of failure (e.g., scope creep, poor communication).  
2. **Stakeholder Realignment** – Hold an emergency meeting to reset expectations and prioritize deliverables.  
3. **Revise the Plan** – Adjust timelines, reallocate resources, or fast-track critical tasks.  
4. **Monitor Closely** – Implement daily stand-ups and progress dashboards for transparency.  
5. **Mitigate Risks** – Address bottlenecks (e.g., contractor delays) with contingency plans.  

**Key Focus**: Stabilize the project, then optimize for recovery.  

#### **2. University Laptop Policy Analysis**  
**Effects & Key Questions:**  

| **Aspect**      | **Effects**                                                                 | **Questions to Address** |  
|-----------------|-----------------------------------------------------------------------------|--------------------------|  
| **Technology**  | - Increased demand for campus Wi-Fi/IT support. <br> - Cybersecurity risks. | - Is infrastructure scalable? <br> - How to maintain device security? |  
| **Business**    | - Higher upfront costs (subsidies/loans). <br> - Potential ROI via digital learning. | - What’s the budget? <br> - Will it attract more students? |  
| **Organization**| - Faculty training needed. <br> - Digital divide concerns.                   | - How to ensure equity for low-income students? <br> - Is faculty prepared? |  

**Recommendation**: Pilot the policy with a focus on infrastructure readiness and financial aid options.  


#### **3. Four Organizational Frames**  
1. **Structural Frame** – Focuses on roles, hierarchy, and processes (e.g., reporting lines).  
2. **Human Resource Frame** – Emphasizes employee needs, motivation, and teamwork.  
3. **Political Frame** – Addresses power dynamics, conflicts, and stakeholder influence.  
4. **Symbolic Frame** – Centers on culture, values, and shared vision (e.g., branding).  

**Application**: Projects succeed when all frames are balanced (e.g., clear structure + team morale).  

#### **4. Importance of Project Schedules**  
1. **Resource Optimization** – Ensures efficient use of time, budget, and personnel.  
2. **Accountability** – Provides milestones to track progress and avoid delays.  

**Example**: A Gantt chart prevents overlapping tasks and identifies critical paths.  

---
![[CPS 412 c.jpeg]]

### Question 2
**2a) Project Manager's Role (4 marks)**
1. Define project scope, objectives and deliverables
2. Develop project plans and schedules
3. Lead and motivate project teams
4. Monitor progress and manage risks
5. Communicate with stakeholders
6. Ensure quality control

**2b) Importance of Project Definition (2 marks)**
- Provides clear direction and boundaries
- Aligns stakeholders on expectations
- Forms basis for planning and control
- Prevents scope creep

**2c) Measuring IT Project Success (3 marks)**
1. Deliverables meet requirements/MOV
2. Completed within budget and timeline
3. Stakeholder acceptance/sign-off
4. Delivers expected business value

**2d) Measuring IT Project Benefits (3 marks)**
1. Quantitative metrics (ROI, cost savings)
2. User adoption/engagement rates
3. Performance improvements (speed, uptime)
4. Strategic alignment assessment

### Question 3
**3a) Milestone-Focused Planning (3 marks)**
Preferred because:
- Provides clear progress checkpoints
- Helps prioritize critical deliverables
- Motivates teams with achievable targets
- Enables better progress tracking

**3b) Automated vs Manual Scheduling (3+3 marks)**
Differences:
- Speed (automated is faster)
- Complexity handling (automated better)
- Flexibility (manual more adaptable)

Benefits/Problems:
- Automated: More accurate but rigid
- Manual: Simple but error-prone

**3c) Expert Judgment Disadvantages (3 marks)**
1. Subjectivity/bias in estimates
2. Varies by individual experience
3. No empirical data support
4. May overlook technical constraints

**3d) Productivity Drivers (3 marks)**
1. Team skill/experience levels
2. Development tools/technology stack
3. Process maturity/methodology
4. Work environment factors

### Question 4
**4a) Cost Monitoring Terms**
i) PV: Budgeted cost for planned work
ii) AC: Actual costs incurred
iii) SPI: Schedule efficiency (EV/PV)
iv) EV: Budgeted cost of completed work

**4b) Function Point Analysis (4 marks)**
1. Count logical user functions
2. Weight by complexity
3. Adjust for environmental factors
4. Convert to effort estimates

### Question 5
**5a) Startup Estimation Approach (3 marks)**
Agile (e.g., story points) because:
- Accommodates changing requirements
- Works with limited initial information
- Supports iterative development

**5b) User Requirements Gathering (5 marks)**
1. Stakeholder interviews
2. Surveys/questionnaires
3. Workshops/focus groups
4. Use case analysis
5. Prototyping

**5c) Testing Phases (4 marks)**
System Testing:
- Purpose: Validate full system
- User role: Minimal (QA team leads)
- Docs: Test plans, defect reports

Acceptance Testing:
- Purpose: Verify business readiness
- User role: Active participation
- Docs: UAT scripts, sign-off forms

### Question 6
**RFP Response Structure:**
1. Executive Summary
2. Understanding of Requirements
3. Proposed Solution/Methodology
4. Project Approach/Timeline
5. Budget/Cost Breakdown
6. Company Qualifications
7. Next Steps/Contact

---

![[CPS 412 d.jpeg]]

#### a) Precedence Diagram
The precedence diagram is constructed based on the given activities and their dependencies. Here is the representation:

- **Start** → **A** (2) → **B** (4) → **D** (2) → **G** (4) → **I** (6) → **K** (4) → **End**
- **A** → **C** (2) → **E** (4) → **H** (2) → **I** or **J** (6) → **K**
- **B** → **E** (4) → **H** (2) → **J** (6) → **K**
- **A** → **F** (6) → **H** (2) → **J** (6) → **K**
- **D** → **H** (2) → **J** (6) → **K**
- **E** → **F** (6) → **H** (2) → **J** (6) → **K**
- **H** → **I** (6) → **K**
- **F** → **J** (6) → **K**

#### b) Project Duration
To determine the project duration, we calculate the longest path (critical path) through the network:

1. **Path 1**: A → B → D → G → I → K  
   Duration: 2 + 4 + 2 + 4 + 6 + 4 = 22 months  
2. **Path 2**: A → B → E → H → I → K  
   Duration: 2 + 4 + 4 + 2 + 6 + 4 = 22 months  
3. **Path 3**: A → C → E → H → I → K  
   Duration: 2 + 2 + 4 + 2 + 6 + 4 = 20 months  
4. **Path 4**: A → B → E → H → J → K  
   Duration: 2 + 4 + 4 + 2 + 6 + 4 = 22 months  
5. **Path 5**: A → F → H → J → K  
   Duration: 2 + 6 + 2 + 6 + 4 = 20 months  

The longest paths are 22 months. Therefore, the **project duration is 22 months**.

#### c) Critical Activities
Critical activities are those on the longest path(s) with no slack. From the paths above, the critical activities are:  
**A, B, E, H, I, K** and **A, B, D, G, I, K** and **A, B, E, H, J, K**.

#### d) Critical Path on Diagram
The critical paths are:  
1. **A → B → D → G → I → K**  
2. **A → B → E → H → I → K**  
3. **A → B → E → H → J → K**  

These paths should be highlighted on the precedence diagram.

#### e) Latest Completion Time for Activity G
Activity G is on the critical path **A → B → D → G → I → K**. The latest time G must be completed to avoid delaying the project is the latest start time of I (which is 22 - 6 - 4 = 12 months). Therefore, **G must be completed by month 12**.

#### f) Earliest Completion Time for Activity D
Activity D depends on B, which depends on A. The earliest completion time for D is:  
Earliest start of A (0) + duration of A (2) + duration of B (4) + duration of D (2) = **8 months**.

#### g) Free Float for Activity E with Respect to Activity H
Free float is the time activity E can be delayed without delaying the early start of H.  
- Early finish of E: 2 (A) + 4 (B) + 4 (E) = 10 months  
- Early start of H: Max(early finish of D, E, F)  
  - Early finish of D: 8 months  
  - Early finish of F: 2 (A) + 6 (F) = 8 months  
  - Therefore, early start of H = 10 months (from E)  
- Free float of E = early start of H - early finish of E = 10 - 10 = **0 months**.

---
![[CPS 412 j.jpeg]]

### **Question 2**  
**d) Why is the project definition important?**  
(2 marks)  
- **Clarity and Direction**: It provides a clear understanding of the project's goals, scope, and deliverables, ensuring all stakeholders are aligned.  
- **Foundation for Planning**: It serves as the basis for creating schedules, budgets, and resource plans, reducing ambiguity and miscommunication.  

### **Question 3**  
**a) As a project manager, how do you practically assess the risks in an IT project?**  
(4 marks)  
1. **Risk Identification**: Brainstorm with the team, review historical data, and consult experts to list potential risks.  
2. **Risk Analysis**: Evaluate the likelihood and impact of each risk using qualitative (e.g., High/Medium/Low) or quantitative (e.g., numerical scoring) methods.  
3. **Prioritization**: Rank risks based on severity to focus on the most critical ones.  
4. **Mitigation Planning**: Develop strategies such as avoidance, transfer, mitigation, or acceptance for high-priority risks.  

**b) Keys to the success of Issue Management Process?**  
(5 marks)  
- **Early Detection**: Identify issues as soon as they arise to prevent escalation.  
- **Clear Ownership**: Assign responsibility for resolving each issue to a specific team member.  
- **Documentation**: Maintain a log to track issues, actions, and resolutions.  
- **Communication**: Regularly update stakeholders on issue status and resolutions.  
- **Proactive Resolution**: Address root causes to prevent recurrence.  

**c) How do you maintain quality work in an IT project?**  
(6 marks)  
1. **Quality Planning**: Define standards and metrics upfront (e.g., code review criteria, testing protocols).  
2. **Regular Reviews**: Conduct peer reviews, testing (unit, integration, UAT), and audits.  
3. **Continuous Improvement**: Use feedback loops (e.g., retrospectives) to refine processes.  
4. **Tools and Automation**: Implement CI/CD pipelines and automated testing.  
5. **Training**: Ensure team members are skilled in quality best practices.  
6. **Stakeholder Involvement**: Engage clients/users in validation and feedback.  

**d) Functions of the project manager?**  
(7 marks)  
1. **Planning**: Define scope, schedule, budget, and resources.  
2. **Organizing**: Assemble and lead the project team.  
3. **Executing**: Oversee task completion and deliverables.  
4. **Monitoring**: Track progress using KPIs and adjust plans as needed.  
5. **Risk Management**: Identify and mitigate risks.  
6. **Communication**: Facilitate stakeholder updates and collaboration.  
7. **Closing**: Ensure deliverables are accepted and conduct post-project reviews.  

### **Question 4**  
**a) Do you prefer the Milestone-Focused planning approach? Why?**  
(8 marks)  
**Yes**, because:  
- **Clear Progress Tracking**: Milestones mark critical achievements, providing tangible checkpoints.  
- **Motivation**: Teams gain a sense of accomplishment at each milestone.  
- **Flexibility**: Allows adjustments between milestones without derailing the overall plan.  
- **Stakeholder Alignment**: Simplifies reporting by focusing on key outcomes rather than granular tasks.  

**b) Differences between automated and manual scheduling?**  
(9 marks)  

| **Automated Scheduling**                | **Manual Scheduling**                  |  
|-----------------------------------------|----------------------------------------|  
| Uses software (e.g., MS Project, Jira)  | Relies on spreadsheets/whiteboards     |  
| Dynamic updates (e.g., critical path)   | Static, requires manual adjustments    |  
| Scalable for complex projects           | Prone to errors in large projects      |  
| **Benefits**: Speed, accuracy, analytics | **Benefits**: Simplicity, low cost     |  
| **Problems**: Over-reliance on tools    | **Problems**: Time-consuming, inflexible |  

**c) THREE disadvantages of expert judgement estimation**  
(10 marks)  
1. **Bias**: Experts may over/underestimate based on personal experience.  
2. **Inconsistency**: Different experts may provide varying estimates.  
3. **Lack of Documentation**: Assumptions may not be recorded, leading to future confusion.  

**d) TWO productivity drivers for IT project effort estimation**  
(11 marks)  
1. **Team Skill Level**: Highly skilled teams complete tasks faster (e.g., familiarity with frameworks).  
2. **Tooling/Technology**: Modern tools (e.g., DevOps pipelines) reduce manual effort and errors.  


### **Question 5**  
**a) Top 3 items to audit as a Quality Auditor**  
(12 marks)  
1. **Process Compliance**: Verify adherence to defined methodologies (e.g., Agile/Waterfall).  
2. **Deliverable Quality**: Assess outputs against standards (e.g., code quality, test coverage).  
3. **Risk Management**: Check if risks are identified, tracked, and mitigated effectively.  

**b) Why do things need to change during a project?**  
(13 marks)  
- **New Requirements**: Stakeholder needs evolve.  
- **External Factors**: Market shifts, regulatory changes, or technology updates.  
- **Issues/Risks**: Unforeseen obstacles (e.g., resource shortages, technical failures).  

**c) TWO instances to reject a change**  
(14 marks)  
1. **Scope Creep**: Change derails core objectives without added value.  
2. **Resource Constraints**: Change requires unavailable budget/time/expertise.  

**d) Dealing with nervousness from organizational change**  
(15 marks)  
1. **Transparent Communication**: Explain reasons and benefits clearly.  
2. **Support Systems**: Offer training or counseling to ease transitions.  

**e) Control/reporting needed in a start-up IT project**  
(16 marks)  
- **Lightweight Agile Reporting**: Daily stand-ups, sprint reviews, and burn-down charts.  
- **Focus on Key Metrics**: Track progress, budget, and blockers without bureaucratic overhead.  


### **Question 6**  

**b) FIVE project stakeholders and their functions**  
(18 marks)  
1. **Sponsor**: Provides funding and strategic direction.  
2. **Client**: Defines requirements and approves deliverables.  
3. **Team Members**: Execute tasks (developers, testers).  
4. **End Users**: Utilize the final product.  
5. **Regulators**: Ensure compliance with standards (e.g., GDPR).  
