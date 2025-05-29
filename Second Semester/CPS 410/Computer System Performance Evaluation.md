**Instructor**: Dr. Sanni Abubakar O. Ogirima
**Credit Load**: 2 Units

---

## **1. What is Computer System Performance Evaluation (CSP)?**

CSP is the process of assessing how well a computer system operates under various conditions. It focuses on **efficiency**, **responsiveness**, **scalability**, and **capacity**. Its goal is to help organizations understand the behavior and performance of systems and make informed decisions for improvements.

---

## **2. Importance of Performance Evaluation**

Performance evaluation provides insight into:

* **System Capacity** – Determines the maximum workload a system can handle.
* **Bottlenecks** – Identifies system components that slow down performance.
* **Scalability** – Assesses how the system performs with increased workload.
* **Optimization Opportunities** – Reveals areas for performance tuning.
* **Future Planning** – Helps forecast performance under anticipated growth.

---

## **3. Types of Performance Evaluation Techniques**

### 1. **Model-Based Evaluation**

* **Definition**: Uses abstract, mathematical models (e.g., queuing theory).
* **Examples**: M/M/1 model, Jackson Networks.
* **Advantages**: Fast, cost-effective, great for early design and "what-if" analysis.
* **Limitations**: Assumptions may reduce accuracy; complex behavior may not be captured.

### 2. **Simulation-Based Evaluation**

* **Definition**: Mimics system behavior via software simulations.
* **Types**: Discrete Event Simulation (DES), Monte Carlo.
* **Tools**: SimPy, MATLAB, OMNeT++, GPSS.
* **Advantages**: High realism, handles complex systems, supports visualization.
* **Limitations**: Time-consuming, requires detailed knowledge, input accuracy dependent.

### 3. **Measurement-Based Evaluation**

* **Definition**: Collects real-world data from a live system.
* **Tools**: Monitoring tools (top, iostat), Profilers (gprof), Benchmarks (SPEC, TPC).
* **Advantages**: Realistic data, useful for comparing system configurations.
* **Limitations**: Time-consuming, costly, restricted to existing setup.

---

## **4. Steps in System Performance Evaluation**

1. **Define Objectives**: Determine what to evaluate (e.g., response time, throughput).
2. **Select Performance Metrics**: Choose specific measurable indicators.
3. **Characterize the Workload**: Identify tasks and how they are processed.
4. **Develop Model or Setup Tools**: Build analytical/simulation models or use monitoring tools.
5. **Conduct Experiments or Simulations**: Run tests to collect data.
6. **Analyze Results**: Use tools like SPSS or Excel to interpret data.
7. **Validate and Refine**: Confirm results and refine techniques.
8. **Report Findings**: Document insights and recommendations.

---

## **5. Performance Metrics**

Key metrics include:

* **Response Time**: Delay between request and response.
* **Throughput**: Number of tasks processed per time unit.
* **CPU Utilization**: How busy the CPU is.
* **Memory Usage**: Amount of memory used.
* **Turnaround Time**: Time from job submission to completion.
* **Availability**: Percentage of time the system is operational.
* **Scalability**: System's ability to maintain performance as load increases.
* **Fairness**: Resource sharing in multi-user systems.
* **Disk I/O Rate**, **Queue Length**, **Error Rate**

---

## **6. Workload Characterization**

### **Definition**: Understanding the nature of system tasks to model performance accurately.

### **Types of Workloads**:

* **Batch**: No user interaction, e.g., payroll.
* **Interactive**: User-driven, e.g., web browsing.
* **Transactional**: Many small requests, e.g., ATM.
* **Real-Time**: Time-sensitive, e.g., navigation systems.
* **Mixed**: Combination of the above.

### **Techniques**:

* **Empirical Analysis**: Monitor real system behavior.
* **Statistical Modeling**: Fit observed data to distributions (e.g., Poisson).
* **Synthetic Workload Generation**: Create artificial workloads.
* **Benchmarking**: Use standard programs to test systems.
* **Trace-Driven Analysis**: Replay real usage data.
* **Scenario-Based Analysis**: Hypothetical workload cases.

---

## **7. Queuing Theory and Network Models**

### **Definition**: The study of waiting lines to predict system behavior under load.

In computer system, queueing form when multiple request compete for limited resources such as Processor, Memory, Disks, or Network Bandwidth.
### **Key Concepts**:

* **Arrival Rate (λ)**: Rate at which jobs arrive.
* **Service Rate (μ)**: Rate at which jobs are serviced.
* **Utilization (ρ = λ/μ)**

### **Types of Queuing Networks**:

1. **M/M/1**: Single queue, single server.
2. **M/M/c**: Single queue, multiple servers.
3. **M/M/1/K**: Limited/Finite capacity queue.
4. **Priority Queues**: Jobs have service priority.
5. **Closed Network**: Fixed number of circulating jobs.
6. **Open Network**: Jobs can enter/exit freely.

### **Importance of Queuing Theory in Computer System Performance Evaluation**

1. **Provides a Strong Foundation for System Modeling**  
    Queuing theory offers a mathematical framework for modeling and analyzing how computer systems handle workloads and waiting lines (queues).
    
2. **Helps Understand System Behavior Under Load**  
    It enables engineers and system administrators to predict how systems perform as the workload increases—revealing how different resources are utilized.
    
3. **Identifies Performance Bottlenecks**  
    Through queuing models, it becomes easier to detect which parts of the system (e.g., CPU, memory, disk, network) are causing slowdowns or delays.
    
4. **Supports Performance Planning and Optimization**  
    Queuing theory allows professionals to evaluate how system performance can be improved by adjusting resource allocation, scheduling, or scaling.
---

## **8. Solving Queuing Network Models**

### **Analytical Methods**:

* Used for simple models like M/M/1.
* Key formulas:
$L = \frac{\lambda}{\mu - \lambda}$ $\rho = \frac{\lambda}{\mu}$ $W = \frac{1}{\mu - \lambda}$

  * **L**: Avg. number of jobs in system.
  * **W**: Avg. time a job spends in system.
  * **ρ**: Server utilization.

### **Advanced Methods**:

* **Jackson Networks**: For open networks; uses decomposition.
* **Mean Value Analysis (MVA)**: For closed systems with fixed jobs.
* **Simulation**: For complex systems not suited to math models.

---

## **9. Summary of Advantages and Disadvantages**

| Technique             | Advantages                        | Limitations                     |
| --------------------- | --------------------------------- | ------------------------------- |
| **Model-Based**       | Fast, good for early design       | Depends on assumptions          |
| **Simulation-Based**  | Realistic, supports complex logic | Time-consuming, needs expertise |
| **Measurement-Based** | Real-world data, comparison-ready | Expensive, setup-specific       |

---

## **10. Assignment Guide**

**a. List and explain queuing models.**
**b. Explain analytical solution formulas (L, W, ρ).**
**c. State where formulas apply (e.g., M/M/1 systems).**
**d. Benefits of queuing models**:

* Simplifies complex systems.
* Helps predict system performance.
* Identifies bottlenecks for optimization.

---
## **Performance Measuring Tools for Operating Systems**

### **5.1 Introduction to Performance Measuring Tools**

Performance measuring tools are vital for:

* Observing system behavior in real-time or over time
* Detecting bottlenecks
* Optimizing resource usage
* Ensuring efficient system operation

These tools are available as both built-in and third-party utilities for Unix/Linux and Windows platforms. They are used to:

* Monitor CPU, memory, disk, and network usage
* Profile application performance
* Benchmark systems under various workloads

---

### **5.2 Monitoring Tools**

Monitoring tools provide **real-time data** on the system’s current state.

#### **a) Unix/Linux Monitoring Tools**

* **top** – Displays active processes and resource usage
* **htop** – Enhanced version of top with better UI
* **vmstat** – Reports on memory, processes, and CPU
* **iostat** – Monitors I/O device load
* **netstat** – Shows network connections and statistics
* **sar** – Collects/report system activity over time

#### **b) Windows Monitoring Tools**

* **Task Manager** – Overview of processes and performance
* **Performance Monitor (perfmon)** – Customizable performance tracking
* **Resource Monitor** – Detailed resource usage
* **Event Viewer** – Logs system events and errors

---

### **5.3 Profiling Tools**

Profiling tools provide in-depth analysis of application performance.

Profiling tools help developers and administrators analyze the performance of individual applications or system components. They provide details such as execution time per function, memory allocations, and CPU cycles
#### **a) Unix/Linux Profilers**

* **gprof** – Profiles C/C++ applications (function call graphs)
* **perf** – Powerful kernel and application profiler
* **strace** – Traces system calls for debugging

#### **b) Windows Profilers**

* **Visual Studio Profiler** – Built into IDE for .NET/C++
* **Windows Performance Toolkit (WPT)** – Includes WPR and WPA for deep tracing
* **Process Explorer** – Detailed view of processes, threads, and handles

---

### **5.4 Benchmarking Tools**

Benchmarking tools test system performance under controlled conditions.

#### **a) CPU Benchmarking**

* **Unix/Linux**: `sysbench`, `stress-ng`
* **Windows**: `Cinebench`, `PassMark PerformanceTest`

#### **b) Disk Benchmarking**

* **Unix/Linux**: `hdparm`, `dd`, `fio`
* **Windows**: `CrystalDiskMark`

#### **c) Network Benchmarking**

* **Cross-platform**: `iperf`, `netperf`
* 

---

### **Conclusion**

* **Monitoring tools** provide real-time/historical system insights.
* **Profiling tools** identify inefficiencies in code and system processes.
* **Benchmarking tools** evaluate and compare system performance.

Mastery of these tools enables efficient system analysis, optimization, and maintenance.

---

## **CHAPTER SIX: Case Studies – Web Server and E-commerce Site Performance**

### **6.1 Introduction to Web Server Performance Evaluation**

Web servers handle requests for web content (HTML, images, data). Performance evaluation is essential to:

* Ensure **fast page loads**, **high availability**, and **scalability**
* Detect **bottlenecks**, forecast demand, optimize resource use
* Support decisions on caching, load balancing, and upgrades

---

### **6.2 Key Web Server Performance Metrics**
It is used to check the evaluation and performances of the websites designed in order to check the factors that is needed for upgrading those sites. Web server performance is influenced by multiple factors, including server hardware, software configuration, network speed, and client behavior. 

* **Throughput:** HTTP requests per second (higher is better)
* **Response Time:** Includes DNS, connection, request, and delivery times
* **Latency:** Delay to receive first byte of response (lower improves UX)
* **Error Rate:** Percentage of failed requests (e.g., 404, 500)
* **Concurrency Handling:** Number of simultaneous users supported
* **CPU/Memory Utilization:** Measures resource efficiency
* **Cache Hit Ratio:** Proportion of cached responses (higher is better)

---

### **6.3 E-commerce Site Performance Evaluation**

E-commerce systems are more complex:

* Involve dynamic content, user sessions, databases, and third-party APIs
* Require evaluation across frontend, backend, and network layers

---

### **6.4 E-commerce Performance Metrics**

* **Page Load Time:** Total time to fully load a page
* **Time to First Byte (TTFB):** Time until first byte received
* **Transaction Response Time:** Duration of actions like login, search, checkout
* **Conversion Rate vs Performance:** Correlate speed with purchase behavior
* **Cart Abandonment Rate:** Can reflect performance issues
* **Database Query Time:** Critical for optimizing dynamic operations
* **Server Uptime:** Downtime affects revenue and trust
- User sessions
- Third-party

---

### **6.5 Performance Testing Tools**

* **Apache JMeter:** Load testing with user simulation
* **Google Lighthouse:** Page speed, SEO, accessibility testing
* **GTmetrix / Pingdom / WebPageTest:** Load analysis and suggestions
* **New Relic / Datadog:** Real-time monitoring and dashboards
* **Selenium + JMeter:** Browser automation + stress testing

---

### **6.6 Best Practices**

1. Use **CDNs** to reduce latency
2. Implement **multi-layer caching**
3. Optimize images, scripts, and styles
4. Minimize HTTP requests (e.g., bundling, lazy loading)
5. Optimize **database queries and indexing**
6. Apply **load balancing and horizontal scaling**
7. Monitor performance regularly and set alerts

> Continuous optimization is essential for delivering scalable, reliable, and responsive web services.

---

## **CHAPTER SEVEN: Software Performance Engineering (SPE)**

### **7.1 Overview of SPE**

SPE is a **proactive, quantitative approach** to integrating performance into every stage of software development—from requirements to deployment.

* Prevents costly redesigns and late-stage performance failures
* Ensures alignment with SLAs, user expectations, and business needs

---

### **7.2 Performance-Driven Design**

Key strategies include:

* Setting measurable **performance goals** (e.g., response time, throughput)
* Designing for **scalability** (vertical & horizontal)
* Selecting appropriate architectures (e.g., microservices, cloud-native)
* Avoiding anti-patterns (e.g., excessive remote calls, tight coupling)
* Optimizing **data access**, caching, and query design

---

### **7.3 Performance-Oriented Development**

Encourages developers to write efficient, performance-aware code:

* **Code Optimization:** Reduce loops, reuse objects
* **Memory Management:** Avoid leaks and excessive allocation
* **Concurrency & Parallelism:** Use threads, async, non-blocking I/O. Occurs in a multiuser environment, 
* **Efficient Resource Handling:** Manage file handles, DB connections efficiently

---

### **7.4 Continuous Performance Testing**

Performance testing should be integrated into the SDLC:

* **Load Testing:** Normal expected traffic
* **Stress Testing:** Beyond normal capacity
* **Endurance Testing:** Long-term performance stability
* **Spike Testing:** Sudden traffic surges

**Automation Tools:**

* JMeter, Gatling, Locust, k6 integrated with Jenkins, etc.

**Monitoring:** Use dashboards to track CPU, memory, I/O, and network usage

---

### **7.5 Performance Modeling in SPE**

* **Analytical Models:** Based on queuing theory to predict bottlenecks
* **Simulation Models:** Use tools like Simulink, OPNET, or Python scripts

---

### **7.6 Integration into SDLC**

Embed performance at all development phases:

* **Requirements:** Define performance expectations
* **Design Reviews:** Assess architectural impact
* **Code Reviews:** Check for inefficiencies
* **Testing:** Include performance tests in QA plans
* **Deployment:** Monitor real-world performance and iterate

---

### **7.7 Benefits of SPE**

* Early detection of issues
* Lower cost/time than fixing late-stage problems
* Better user experience
* Scalability and maintainability
* Competitive edge through superior performance

> SPE transforms performance from an afterthought to a central pillar of system design and development.

---

Likely Examination Questions
1a)  What is computer system performance Evaluation
1b) Highlight and explain the types of performance evaluation that you know
1c) What are the insights being provided by computer performance evaluation
1d) Draw system performance evaluation process flow and explain the steps involved

2a) What are the performance evaluation metrics and explain those metrics,
2b) Highlight the types of workloads and explain 3
2c) Explain the techniques involved in workload characterization
2d) What do you understand by queuing theory and explain its types

3a) How can we use queuing theory to solve a network model to find the average number in the system (W), average time in the system(L) and utilization(p). (hint: )
3b) What are the advantage and disadvantage of simulation based performance evaluation on the idea of monte carlos simulation
3c) Highlight the techniques involved in measuring based performance evaluation under a real operating condition, using monitoring tools and log
3d) What are the steps involved in discrete event simulation

4a) What are performance measuring tools and highlight the tools with examples
4b) Why do we need profiling tools in performance evaluation
4c) How can we carry out web performance evaluation
4d) What are the needed metrics that can be used for web server evaluation


5a) Ecommerce site are more complex that static web servers, What are those things involved for the site evaluation: <mark style="background: #ABF7F7A6;">user session, thirdpart</mark>
5b) What are the eccomerce performance metrics you know and explain 3
5c) What are the best practice for web and ecommerce performance evaluation
5d) Performance-driven design ensure that system architecture and device choices are made with perfocmance objectives in mind, what are those objectives

6a) What are the type of test that are involved in continuous performance testing
6b) What are the benefit of software performance engineering
6c) Draw and explain the SPE life-cycle embded in sdlc
6d) Why do we need performance modeling in spe, (software performance engineering)

---
## Software Performance Metrics
SPE: Is a method or procedure in building system software that will meet performance metrics or objectives

Performance driven design is an architecture being used to:
- highlight the certain performances goals, then 
- consider the design and scalability




Types of backups:
- Full Backup
- Incremental Backup
- Continous backup