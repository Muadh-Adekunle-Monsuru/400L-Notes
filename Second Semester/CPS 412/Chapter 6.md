### **Detailed Explanation of Chapter 6: Project Planning – The Schedule and Budget**  
*(Turning Scope into Actionable Plans)*  

---

## **1. Introduction to Scheduling & Budgeting**  
With scope defined (Chapter 5), we now:  
1. **Sequence tasks** (schedule)  
2. **Assign costs** (budget)  
**Goal**: Create a **realistic baseline plan** approved by stakeholders.  

**Key Inputs**:  
- WBS (Work Breakdown Structure)  
- Task durations/resource needs  
- Dependencies between tasks  

---

## **2. Scheduling Tools & Techniques**  

### **A. Gantt Charts**  
- **What**: Visual timeline of tasks (bars = duration).  
- **Pros**: Easy to read; shows progress.  
- **Cons**: Doesn’t show dependencies clearly.  

**Example**:  
| Task          | Week 1 | Week 2 | Week 3 |  
|---------------|--------|--------|--------|  
| Design UI     | █████  |        |        |  
| Develop Login |        | █████  | ███    |  

**Uses**:  
- **Planning**: Assign start/end dates.  
- **Tracking**: Shade completed work.  

---

### **B. Network Diagrams (AON – Activity on Node)**  
- **What**: Maps task **dependencies** (arrows show relationships).  
- **Critical Path**: Longest path; determines project duration.  

**Example**:  
```
A (2 days) → B (5 days) → C (4 days) → F (4 days) → H (2 days) → J (1 day)  
              ↘ D (3 days) → G (3 days) → I (5 days) → J  
                ↘ E (1 day) → G  
```  
**Paths**:  
1. A→B→C→F→H→J = 18 days *(Critical Path)*  
2. A→B→D→G→I→J = 19 days  

**Key Terms**:  
- **Slack/Float**: Time a task can be delayed without delaying the project.  
- **Fast-Tracking**: Do tasks in parallel (risky if dependencies exist).  
- **Crashing**: Add resources to shorten duration (costly).  

---

### **C. PERT (Program Evaluation Review Technique)**  
- **What**: Estimates task durations using probabilities.  
- **Formula**:  
  `Expected Time = (Optimistic + 4×Most Likely + Pessimistic) / 6`  

**Example**:  
| Task | Optimistic (a) | Most Likely (b) | Pessimistic (c) | Expected Time |  
|------|----------------|------------------|------------------|---------------|  
| A    | 1 day          | 2 days           | 4 days           | 2.2 days      |  

**Use Case**: High-uncertainty projects (e.g., R&D).  

---

### **D. Precedence Diagramming (PDM)**  
Defines **4 dependency types**:  
1. **Finish-to-Start (FS)**: B can’t start until A finishes.  
   - *Example*: "Paint walls (A) before laying carpet (B)."  
2. **Start-to-Start (SS)**: B can start once A starts.  
   - *Example*: "Code development (A) and testing (B) start simultaneously."  
3. **Finish-to-Finish (FF)**: B can’t finish until A finishes.  
   - *Example*: "Editing (A) must finish when printing (B) finishes."  
4. **Start-to-Finish (SF)**: Rare; B can’t finish until A starts.  
   - *Example*: "Night shift (B) ends when day shift (A) starts."  

**Lead/Lag Times**:  
- **Lead**: Overlap (e.g., start testing 2 days before coding finishes).  
- **Lag**: Delay (e.g., wait 1 day after painting before sanding).  

---

## **3. Critical Chain Project Management (CCPM)**  
- **Problem**: Teams inflate estimates ("student syndrome").  
- **Solution**:  
  1. Use **50% probability estimates** (aggressive but realistic).  
  2. Add **buffers**:  
     - **Feeding Buffers**: Protect critical path from delays.  
     - **Project Buffer**: Extra time at the end.  

**Before CCPM**:  
```
A (10 days) → B (10 days) → C (10 days)  
```  
**After CCPM**:  
```
A (5 days) → B (5 days) → C (5 days) → [2.5-day Buffer]  
```  

**Benefits**:  
- Reduces procrastination.  
- Focuses on **resource contention** (avoid multitasking).  

---

## **4. Budget Development**  
### **Cost Categories**  
| **Type**          | **Description**                     | **Example**                |  
|--------------------|-------------------------------------|----------------------------|  
| **Direct Costs**   | Labor, materials.                   | Developer salaries.        |  
| **Indirect Costs** | Overhead (rent, utilities).         | Office space.              |  
| **Sunk Costs**     | Irrecoverable past expenses.        | Failed prototype R&D.      |  
| **Reserves**       | Contingency funds for risks.        | 10% buffer for delays.     |  

### **Steps to Build a Budget**:  
1. **List Resources**: People, software, equipment.  
2. **Assign Costs**: Hourly rates, license fees.  
3. **Aggregate**: Sum costs per WBS task.  
4. **Validate**: Compare to historical data.  

**Tool**: **Resource Sheet in MS Project**  
| Resource    | Cost/Hour | Hours | Total Cost |  
|-------------|-----------|-------|------------|  
| Developer   | $50       | 100   | $5,000     |  
| Cloud Hosting | $200/month | 3    | $600       |  

---

## **5. Baselining & Approval**  
- **Baseline Plan**: Approved version of schedule/budget (used to track progress).  
- **Kickoff Meeting**: Formal start after baseline approval.  

**Key Checks**:  
- **Resource Leveling**: Avoid overallocation (e.g., one person on two tasks at once).  
- **Stakeholder Alignment**: Ensure MOV is still supported.  

---

## **6. Key Takeaways**  
1. **Scheduling**: Use Gantt charts for visuals, AON/PERT for dependencies.  
2. **Critical Path**: Longest path = project duration.  
3. **CCPM**: Buffers protect against delays; reduces padding.  
4. **Budgeting**: Include direct/indirect costs + reserves.  

**Link to Execution**: Approved baseline → **Chapter 7+ (Execution & Control)**.  

---

### **Final Summary**  
Chapter 6 transforms scope into **actionable plans**:  
- **Schedules**: Gantt, Critical Path, PERT.  
- **Budgets**: Direct/indirect costs, reserves.  
- **Optimization**: Fast-tracking, crashing, CCPM.  

**Next**: Execution phases (monitoring, risk management).  

Would you like a deep dive into **risk management (Chapter 7)**?