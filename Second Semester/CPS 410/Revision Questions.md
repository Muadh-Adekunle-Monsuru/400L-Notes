### Revision Questions Set 1

**1a) What is Computer System Performance Evaluation (CSP)?** Computer System Performance Evaluation (CSP) is the process of assessing how well a computer system operates under various conditions. Its primary focus is on efficiency, responsiveness, scalability, and capacity. The goal of CSP is to help organizations comprehend system behavior and performance, enabling them to make informed decisions for improvements.

**1b) Highlight and explain the types of performance evaluation that you know.** There are three main types of performance evaluation techniques:

- **Model-Based Evaluation:** This technique utilizes abstract, mathematical models, such as queuing theory, to predict system behavior. It is advantageous for its speed, cost-effectiveness, and suitability for early design phases and "what-if" analyses. However, its accuracy can be limited by simplifying assumptions and it may not capture complex system behaviors.
    
- **Simulation-Based Evaluation:** This method involves mimicking system behavior through software simulations, including types like Discrete Event Simulation (DES) and Monte Carlo. Its benefits include high realism, the ability to handle complex systems, and support for visualization. The drawbacks are that it can be time-consuming to develop and run, requires detailed knowledge, and its results are dependent on the accuracy of input data.
    
- **Measurement-Based Evaluation:** This technique collects real-world data directly from a live system using tools like monitoring software, profilers, and benchmarks. It offers realistic data and is valuable for comparing different system configurations. Its limitations include being time-consuming, costly, and restricted to the existing system setup.
    

**1c) What are the insights being provided by computer performance evaluation?** Computer performance evaluation provides several key insights:

- **System Capacity:** It helps determine the maximum workload a system can effectively handle.
    
- **Bottlenecks:** It identifies specific system components that are slowing down overall performance.
    
- **Scalability:** It assesses how well the system performs as the workload increases.
    
- **Optimization Opportunities:** It uncovers areas where performance tuning can lead to improvements.
    
- **Future Planning:** It aids in forecasting system performance under anticipated growth or changes.
    

**1d) Draw system performance evaluation process flow and explain the steps involved.** The system performance evaluation process typically follows an 8-step structured methodology:

1. **Define Objectives:** Clearly determine what aspects of system performance need to be evaluated (e.g., response time, throughput, resource utilization).
    
2. **Select Performance Metrics:** Choose specific, measurable indicators to quantify performance.
    
3. **Characterize the Workload:** Identify and model the types of tasks, requests, or operations the system processes.
    
4. **Develop Model or Setup Tools:** Construct analytical or simulation models, or configure monitoring tools, depending on the chosen evaluation method.
    
5. **Conduct Experiments or Simulations:** Execute tests or simulations under various workloads and configurations to gather data.
    
6. **Analyze Results:** Interpret the collected data to identify trends, performance issues, and potential improvements.
    
7. **Validate and Refine:** Cross-validate the results with other techniques or real-world observations, refining models or measurement techniques as necessary.
    
8. **Report Findings:** Document the evaluation process, key insights, and recommendations for stakeholders.
    

**2a) What are the performance evaluation metrics and explain those metrics?** Key performance evaluation metrics include:

- **Response Time:** The delay between a request being made and the system's response. It is crucial for interactive systems where user experience depends on quick feedback.
    
- **Throughput:** The number of tasks or requests a system can process per unit of time, reflecting its capacity.
    
- **CPU Utilization:** The percentage of time the CPU is actively busy. High utilization can indicate efficient use but excessive levels might suggest an overload risk.
    
- **Memory Usage:** The amount of physical and virtual memory currently in use. Insufficient memory can lead to swapping and degraded performance.
    
- **Turnaround Time:** The total time taken for a job from submission to completion, encompassing waiting, execution, and completion times.
    
- **Availability:** The proportion of time a system is operational and accessible, usually expressed as a percentage.
    
- **Scalability:** The system's ability to maintain or improve performance as the workload or system size increases.
    
- **Fairness:** In multi-user systems, this measures how equitably resources are shared among users or processes.
    
- **Disk I/O Rate:** The number of input/output operations per second (IOPS) performed on disk storage, essential for disk-bound systems.
    
- **Queue Length:** The number of jobs waiting to be serviced by a resource. Long queues often indicate resource contention.
    
- **Error Rates:** The number of failed operations or transactions, useful for gauging reliability and robustness.
    

**2b) Highlight the types of workloads and explain 3.** Workloads can be categorized in various ways:

- **Batch Workload:** Consists of jobs submitted for processing without user interaction (e.g., payroll processing, end-of-day bank reconciliations). It is time-insensitive but resource-intensive.
    
- **Interactive Workload:** Involves direct user interaction with the system (e.g., web Browse, online banking). The emphasis is on minimizing response time to enhance user experience.
    
- **Transactional Workload:** Characterized by a large number of small, short-duration operations (e.g., ATM transactions, shopping cart updates). These workloads focus on maintaining high throughput and data integrity.
    
- **Real-Time Workload:** Involves time-critical operations where delays can lead to unacceptable outcomes (e.g., industrial control systems, flight navigation). Strict timing constraints are involved.
    
- **Mixed Workload:** A combination of the above types. Many modern systems, like cloud servers, handle mixed workloads with varying priorities.
    

**2c) Explain the techniques involved in workload characterization.** Workload characterization involves understanding and describing the nature of tasks a computer system processes. Common techniques include:

- **Empirical Analysis:** Collecting data from the system in operation by analyzing logs, performance counters, or audit trails using monitoring tools.
    
- **Statistical Modeling:** Fitting collected data into probability distributions. Commonly used distributions include Poisson (for arrival rates) and Exponential (for service times).
    
- **Synthetic Workload Generation:** Artificially creating workload patterns that mimic real system behavior, typically used in simulation or benchmarking when real data is unavailable.
    
- **Benchmarking:** Using standardized programs to evaluate system performance under specific workloads (e.g., SPEC CPU, TPC benchmarks).
    
- **Trace-Driven Analysis:** Replaying actual recorded workload traces to evaluate system performance, which provides highly realistic modeling.
    
- **Scenario-Based Analysis:** Defining hypothetical use cases or operational scenarios, useful for capacity planning or stress testing.
    

**2d) What do you understand by queuing theory and explain its types?** **Queuing Theory:** Queuing theory is the mathematical study of waiting lines or queues. In computer systems, queues form when multiple requests compete for limited resources such as processors, memory, disks, or network bandwidth. This theory provides tools to analyze these systems and predict their behavior under different workloads.

**Types of Queuing Networks:**

- **M/M/1 (Single-Queue, Single-Server):** This fundamental model represents a single queue served by a single server, where job arrivals follow a Poisson process and service times are exponentially distributed.
    
- **M/M/c (Single-Queue, Multiple-Servers):** This type features one queue with multiple identical servers. It is useful for modeling systems like bank tellers or cloud servers.
    
- **M/M/1/K (Finite-Capacity Queues):** Similar to M/M/1, but with a defined limit on the number of jobs that can wait in the queue. New arrivals are lost or blocked when the queue is full.
    
- **Priority Queues:** In these queues, jobs are assigned different priorities. Higher-priority jobs are serviced first, either by preempting lower-priority jobs or by being inserted ahead in the queue.
    
- **Closed Queuing Networks:** These networks involve a fixed number of jobs circulating among service centers. They are useful for modeling systems like operating systems or multi-programmed workloads.
    
- **Open Queuing Networks:** In contrast to closed networks, jobs can enter and exit the system freely, without a fixed population. These are commonly used in web applications or transaction processing systems.
    

**3a) How can we use queuing theory to solve a network model to find the average number in the system (L), average time in the system(W) and utilization(p)?** For simple queuing systems like M/M/1, analytical methods derived from queuing theory can be used to calculate these metrics, provided the system is stable (i.e., the arrival rate is less than the service rate):

- **Utilization (ρ):** This is calculated as the ratio of the arrival rate (λ) to the service rate (μ).
    
    - Formula: ρ = λ / μ
        
- **Average time in the system (W):** This represents the average time a job spends waiting and being serviced in the system.
    
    - Formula: W = 1 / (μ - λ)
        
- **Average number of jobs in the system (L):** This is the average number of jobs present in the queue and being served.
    
    - Formula: L = λ * W or L = ρ / (1 - ρ)
        

These formulas are valid when the system is stable, meaning the arrival rate (λ) is less than the service rate (μ).

**3b) What are the advantage and disadvantage of simulation based performance evaluation on the idea of Monte Carlo simulation?** **Advantages of Simulation-Based Evaluation (including Monte Carlo):**

- **High Realism:** It can realistically model complex systems with intricate logic and dependencies.
    
- **Visualization:** It allows for the visualization of system behavior over time.
    

**Disadvantages of Simulation-Based Evaluation:**

- **Time-Consuming:** It requires significant time for both development and execution.
    
- **Detailed Knowledge Requirement:** It demands detailed knowledge of the system being simulated.
    
- **Input Accuracy Dependent:** The accuracy of the simulation results heavily relies on the accuracy of the input data.
    

**3c) Highlight the techniques involved in measuring based performance evaluation under a real operating condition, using monitoring tools and log.** Measurement-based performance evaluation under real operating conditions involves:

- **Benchmarking:** Using standardized programs or workloads (e.g., SPEC CPU, TPC benchmarks) to assess system performance.
    
- **Profiling:** Analyzing system performance at a granular level, such as function calls, memory usage, and CPU cycles, using tools like `gprof` or `perf`.
    
- **System Monitoring:** Tracking real-time performance metrics like CPU usage, memory, I/O, and network activity with tools like `top`, `htop`, or Windows Task Manager.
    
- **Log Analysis:** Examining historical event records to identify trends, errors, and performance degradation.
    

**3d) What are the steps involved in discrete event simulation?** Discrete-Event Simulation (DES) models a system as a sequence of events occurring at discrete points in time. The steps involved are:

1. Define system components
2. Create event list
3. Initialize simulation
4. Process events in chronological order
5. Collect statistics
6. Analyze results
    

**4a) What are performance measuring tools and highlight the tools with examples?** Performance measuring tools are essential utilities used to observe, monitor, and analyze a computer system's behavior in real-time or over time. They help detect bottlenecks, optimize resource usage, and ensure efficient system operation.

Examples of these tools include:

- **Monitoring Tools (for real-time data):**
    
    - **Unix/Linux:** `top`, `htop`, `vmstat`, `iostat`, `netstat`, `sar`.
        
    - **Windows:** Task Manager, Performance Monitor (perfmon), Resource Monitor, Windows Event Viewer.
        
- **Profiling Tools (for in-depth application analysis):**
    
    - **Unix/Linux:** `gprof`, `perf`, `strace`.
        
    - **Windows:** Visual Studio Profiler, Windows Performance Toolkit (WPT), Process Explorer.
        
- **Benchmarking Tools (for comparing system performance):**
    
    - **CPU Benchmarking:** `sysbench`, `stress-ng` (Unix/Linux); Cinebench, PassMark PerformanceTest (Windows).
        
    - **Disk Benchmarking:** `hdparm`, `dd`, `fio` (Unix/Linux); CrystalDiskMark (Windows).
        
    - **Network Benchmarking:** `iperf`, `netperf` (Unix/Linux and Windows).
        

**4b) Why do we need profiling tools in performance evaluation?** Profiling tools are essential in performance evaluation because they enable developers and administrators to perform an in-depth analysis of individual applications or system components. They provide granular details such as execution time per function, memory allocations, and CPU cycles, which are crucial for identifying and isolating inefficiencies or performance bottlenecks within programs and services.

**4c) How can we carry out web performance evaluation?** To conduct web performance evaluation, one would integrate various performance evaluation techniques and tools:

- **Workload Characterization:** Identify and model typical user interactions, requests, and data traffic relevant to the web application (e.g., interactive, transactional workloads).
    
- **Performance Metrics Selection:** Monitor key web-specific metrics such as response time, throughput (e.g., requests per second), CPU utilization, memory usage, and error rates.
    
- **Measurement-Based Evaluation:**
    
    - **System Monitoring:** Use tools (e.g., `top`, Task Manager) to track resource usage on web servers (CPU, memory, network I/O, disk I/O).
        
    - **Profiling:** Analyze specific web application components or code for performance bottlenecks.
        
    - **Benchmarking:** Employ benchmarking concepts or create synthetic workloads to simulate user traffic and measure performance under load.
        
    - **Log Analysis:** Examine web server access and application logs to identify performance trends, errors, and user behavior.
        
- **Simulation-Based Evaluation:** For complex web architectures, build simulation models to mimic user traffic and server responses to predict behavior under various loads.
    
- **Queuing Theory:** Apply queuing models, such as Open Queuing Networks, to understand how requests are processed and queued at different stages (e.g., load balancer, application server, database).
    

**4d) What are the needed metrics that can be used for web server evaluation?** For web server evaluation, the critical performance metrics are:

- **Response Time:** The time taken for the web server to respond to a client request. This is crucial for user experience.
    
- **Throughput:** The number of requests (e.g., HTTP requests) the web server can handle per second, indicating its processing capacity.
    
- **CPU Utilization:** The percentage of CPU time consumed by web server processes. High utilization can point to a bottleneck.
    
- **Memory Usage:** The amount of RAM used by the web server and its associated processes. Excessive memory usage can lead to swapping and performance degradation.
    
- **Network I/O Rate:** The volume of data being sent and received by the web server, indicating network activity.
    
- **Disk I/O Rate:** For web servers handling static content or interacting with databases, this measures read/write operations per second on disk.
    
- **Error Rates:** The number of failed requests or errors generated by the web server, reflecting reliability.
    
- **Availability:** The percentage of time the web server is accessible and operational. Downtime directly impacts user access and business continuity.
    
- **Queue Length:** The number of pending requests awaiting processing by the web server. Long queues often signal an overloaded server.
    

**5a) E-commerce sites are more complex than static web servers. What are those things involved for the site evaluation: user session, third-party?** 
*  Dynamic content rendering
    
- User sessions management
    
- Database interactions
    
- Third-party integrations (payment gateways)


**5b) What are the e-commerce performance metrics you know and explain 3?** :

- **Response Time:** For an e-commerce site, this is the delay from a user action (e.g., clicking "Add to Cart," loading a product page) to the site's response. Rapid response times are vital for positive user experience and conversion rates.
    
- **Throughput:** This refers to the number of transactions (e.g., completed purchases, product page views) an e-commerce site can handle per second or minute. High throughput signifies the site's capacity to manage a large volume of user activity, especially during peak periods.
    
- **Availability:** This is the percentage of time the e-commerce site is operational and accessible to users. Downtime directly results in lost sales and customer dissatisfaction, making high availability paramount.
    


**5c) What are the best practices for web and e-commerce performance evaluation?** 

- **Define Clear Objectives:** Explicitly determine the performance aspects to be evaluated (e.g., response time for product pages, checkout process throughput).
    
- **Accurately Characterize Workload:** Understand typical user interactions, traffic patterns (e.g., peak hours, transactional behavior), and resource demands on the e-commerce platform using techniques like empirical analysis or scenario-based analysis.
    
- **Select Appropriate Metrics:** Choose relevant metrics (response time, throughput, utilization, error rates) that are critical for user experience and business goals on an e-commerce site.
    
- **Combine Evaluation Techniques:** Utilize a mix of model-based, simulation-based, and measurement-based approaches for a comprehensive evaluation. For example, real-world measurements can validate models, and simulations can explore "what-if" scenarios.
    
- **Utilize Performance Measuring Tools:** Employ monitoring tools (e.g., Task Manager, `top`), profiling tools (e.g., `gprof`), and benchmarking tools (e.g., `iperf`) to gather data and identify bottlenecks.
    
- **Analyze and Validate Results:** Thoroughly interpret collected data to identify trends and performance issues, and validate findings against expected behavior or using other techniques.
    
- **Report Findings:** Document the evaluation, insights, and recommendations for stakeholders to facilitate informed decisions for improvements.
    

**5d) Performance-driven design ensures that system architecture and device choices are made with performance objectives in mind. What are those objectives?** 

- **Achieve Target Response Times:** Designing for optimal user experience, particularly in interactive systems, by ensuring requests are processed within acceptable timeframes.
    
- **Maximize Throughput:** Ensuring the system can efficiently handle the expected volume of tasks or transactions, especially during peak loads.
    
- **Optimize Resource Utilization:** Designing systems to efficiently use resources like CPU, memory, and I/O, avoiding underutilization or overspending.
    
- **Ensure Scalability:** Building systems that can maintain or improve performance as the workload or system size increases, accommodating future growth without degradation.
    
- **Maintain High Availability:** Designing for system uptime and accessibility, minimizing downtime to ensure continuous operation.
    
- **Minimize Bottlenecks:** Identifying and addressing potential performance bottlenecks in the architecture to prevent slowdowns.
    

**6a) What are the types of tests involved in continuous performance testing?** 
- Load Testing: Simulates expected user traffic to test response times and behavior under normal load.
- Stress Testing: Determines the system's robustness by pushing it beyond normal operational capacity. 
- Endurance Testing: Evaluates performance over an extended period to detect memory leaks or degradation. 
- Spike Testing: Measures the system’s ability to handle sudden increases in load.

**6b) What are the benefits of software performance engineering?** 
- Early detection of performance bottlenecks
- Reduction in cost and time associated with late-stage performance fixes 
- Better user experience and satisfaction 
- Improved scalability and maintainability 
- Competitive advantage due to better system responsiveness

**6c) Draw and explain the SPE life-cycle embedded in SDLC.** 
![[Pasted image 20250701153449.png]]

**6d) Why do we need performance modeling in SPE (Software Performance Engineering)?** Performance modeling is crucial in Software Performance Engineering (SPE) because it enables the prediction and analysis of system behavior under various conditions without the need to build the actual system.:

- **Early Design Analysis:** Performance modeling, as part of model-based evaluation, is fast, cost-effective, and excellent for analyzing designs and conducting "what-if" scenarios early in the system development lifecycle. This helps identify and address performance issues before significant development efforts are invested.
    
- **Understanding System Behavior Under Load:** Analytical models, such as those from queuing theory, help predict how systems will perform as workloads increase and how resources will be utilized. This predictive capability is vital for designing robust and scalable software.
    
- **Identifying Bottlenecks:** Models can help detect which parts of the system (e.g., CPU, memory, disk, network) are likely to cause slowdowns or delays before they become real-world problems.
    
- **Supporting Performance Planning and Optimization:** Performance models allow engineers to evaluate how system performance can be improved by adjusting resource allocation, scheduling, or scaling, thereby guiding optimization efforts effectively.
    
- **Capacity Planning and System Design:** A well-characterized workload, often achieved through modeling techniques, enables accurate capacity planning and informed system design decisions.
    

### Revision Questions Set 2

**1. Briefly describe the performance evaluation method and briefly describe one advantage and limitation.** Here are the performance evaluation methods with one advantage and one limitation for each:

- **Analytical Modeling (Model-Based Evaluation):** This method uses mathematical models to predict system performance.
    
    - **Advantage:** It is fast and cost-effective, making it suitable for early system design and "what-if" analyses.
        
    - **Limitation:** Its accuracy depends on the assumptions made and it may not fully capture complex system behaviors.
        
- **Simulation-Based Evaluation:** This involves building a software model to mimic system behavior under various scenarios.
    
    - **Advantage:** Offers high realism and can effectively handle complex systems.
        
    - **Limitation:** It is time-consuming to develop and run, and requires detailed system knowledge.
        
- **Measurement-Based Evaluation:** This technique involves collecting real-world performance data directly from a live system.
    
    - **Advantage:** Provides realistic performance data and is useful for comparing different system configurations.
        
    - **Limitation:** It can be expensive and time-consuming, and its application is restricted to the existing system setup.
        

**2. Give the 8 steps methodology evaluating system performance, outline and describe it.** The 8-step methodology for evaluating system performance is outlined and described as follows:

1. **Define Objectives:** Determine what aspects of system performance need to be evaluated, such as response time, throughput, or resource utilization.
    
2. **Select Performance Metrics:** Choose the specific metrics that will quantify performance.
    
3. **Characterize the Workload:** Identify and model the types of tasks, requests, or operations the system handles.
    
4. **Develop a Performance Model or Measurement Setup:** Depending on the chosen evaluation method, either construct an analytical/simulation model or set up tools to monitor the system.
    
5. **Conduct Experiments or Simulations:** Run the model or system under various workloads and configurations to gather data.
    
6. **Analyze Results:** Interpret the collected data to identify trends, performance issues, and potential improvements.
    
7. **Validate and Refine:** Cross-validate the results with other techniques or real-world observations. Refine models or measurement techniques as needed.
    
8. **Report Findings:** Document the evaluation process, key insights, and recommendations for stakeholders.
    

**3. Computation analysis of M/M/1 queue, if the arrival rate (λ) is 15 requests/second and service rate (μ) is 25 requests per second:** Given: λ = 15 requests/second, μ = 25 requests/second. **a. Calculate system utilization (ρ):**

ρ = λ / μ

ρ = 15 / 25 = 0.6 or 60%

**b. Average number of jobs in the system (L):** First, calculate the Average time in the system (W):

W = 1 / (

μ - λ)

W = 1 / (25 - 15) = 1 / 10 = 0.1 seconds Then, calculate L: L =

λ * W

L = 15 * 0.1 = 1.5 jobs

**c. State the condition required for the system stability:** The condition required for system stability in a queuing system is that the arrival rate (λ) must be less than the service rate (μ). In this case, 15 < 25, so the system is stable.

**4. Describe all the queuing network types, provide a practical computer system example for each type.**

- **M/M/1 (Single-Queue, Single-Server):** This model represents a single queue served by one server.
    
    - **Example:** A single-core CPU processing jobs sequentially.
        
- **M/M/c (Single-Queue, Multiple-Servers):** This type features one queue with multiple identical servers.
    
    - **Example:** A web server farm with multiple identical servers handling requests from a single load balancer.
        
- **M/M/1/K (Finite-Capacity Queues):** Similar to M/M/1, but with a limited capacity for the queue.
    
    - **Example:** A print server with a limited print queue size, where new print jobs are rejected if the queue is full.
        
- **Priority Queues:** Jobs are assigned different priorities, with higher-priority jobs being serviced first.
    
    - **Example:** An operating system's CPU scheduler giving preference to interactive user processes over background batch jobs.
        
- **Closed Queuing Networks:** A fixed number of jobs circulates among service centers within the network.
    
    - **Example:** An operating system with a fixed number of active processes, where processes move between CPU and I/O service centers.
        
- **Open Queuing Networks:** Jobs can freely enter and exit the system; there is no fixed population of jobs.
    
    - **Example:** A web application where users continuously arrive, make requests, and then leave the system.
        

**5. T&I development company designed a mobile payment application to serve millions of users in Nigeria daily. They ensured that the system met the performance goals from the design phase through deployment. As a software engineer, identify how you can integrate SPE into the development life cycle.** the principles of performance evaluation emphasize embedding performance considerations from design through deployment. As a software engineer, integrating SPE would involve:

 ![[Pasted image 20250701153449.png]]   

**6. Identify and discuss the three key phases where SPE should be applied.** 
- Requirements (set goals) 
- Design (architecture choices)
- Implementation (efficient coding)
    

**7. Discuss the measurement-based approach focusing on profiling and system monitoring.** The measurement-based approach in performance evaluation involves directly collecting real-world data from a live system. This method is valuable for identifying actual bottlenecks and provides realistic performance data, particularly for comparing system configurations. However, it can be time-consuming, costly, and limited to the existing setup.

- **System Monitoring:** This involves tracking real-time performance metrics to observe system behavior either in real-time or over time. It is crucial for detecting issues, measuring performance metrics, and making data-driven optimization decisions.
    
    - **Unix/Linux Tools:** Examples include `top` (displays live system processes and resource usage), `htop` (a user-friendly alternative to `top`), `vmstat` (reports on memory, processes, paging, and CPU activity), `iostat` (monitors I/O device load), `netstat` (shows network connections and statistics), and `sar` (collects and reports system activity data over time).
        
    - **Windows Tools:** Examples include Task Manager (provides an overview of processes and performance), Performance Monitor (an advanced tool for tracking custom counters), Resource Monitor (offers detailed breakdowns of resource usage), and Windows Event Viewer (logs system events, warnings, and errors).
        
- **Profiling:** This technique provides an in-depth analysis of application performance, focusing on granular details such as execution time per function, memory allocations, and CPU cycles. Profiling tools assist developers and administrators in pinpointing inefficiencies within individual applications or system components.
    
    - **Unix/Linux Profilers:** Examples include `gprof` (GNU profiler for C/C++ applications), `perf` (a powerful performance analysis tool), and `strace` (traces system calls made by a program).
        
    - **Windows Profilers:** Examples include Visual Studio Profiler, Windows Performance Toolkit (WPT), and Process Explorer from the Sysinternals suite.
        

**8. Propose a real-time action and one long-term strategy to solve Linux-based server stack.** 
- Realtime: Identify bottlenecks (top, vmstat)
- Long-term: Optimize configurations, upgrade hardware

**9. CPU usage is over 90% during the issue page. How will you select tools to confirm whether the bottleneck is of CPU-related or is due to memory on the usage stack?** If CPU usage is consistently over 90% during an "issue page," you would need to use specific performance measuring tools to determine if the bottleneck is truly CPU-related or if it's a symptom of a memory bottleneck (e.g., excessive swapping) leading to high CPU.

- **To confirm a CPU bottleneck:**
    
    - **Monitoring Tools (e.g., `top` or `htop` on Linux):** You would use these tools to observe real-time processes and their CPU utilization. Look for specific processes or applications consistently consuming a very high percentage of CPU.
        
        `vmstat` can also provide system-wide CPU activity reports.
        
    - **Profiling Tools (e.g., `perf`, `gprof` on Linux):** If a particular application or process is identified as a high CPU consumer, profiling tools can drill down into its code to pinpoint the specific functions or code sections that are most CPU-intensive.
        
- **To confirm a memory bottleneck:**
    
    - **Monitoring Tools (e.g., `free`, `vmstat` on Linux):** These tools show overall memory usage, including physical RAM and swap space. 
        
    - **Profiling Tools:** Some profiling tools can also track memory allocations and identify memory leaks within applications.
        

**10. Propose 5 best practices to optimize an e-commerce website, and explain their impact.** - CDN: Reduce latency
- Caching: Lower server load
- Image optimization: Faster loads
- Database indexing: Quicker queries
- Load balancing: Handle traffic spikes

**11. Why is performance evaluation crucial to the company?** Performance evaluation is crucial for a company for several compelling reasons:

- **Understanding System Behavior:** It helps organizations understand precisely how their computer systems operate under various conditions and how they will perform as the workload increases.
    
- **Informed Decision-Making:** It empowers organizations to make informed decisions for improvements, leading to optimized resource allocation, scheduling, and scaling.
    
- **Identifying Bottlenecks:** It effectively identifies specific system components or subsystems that are causing slowdowns, enabling targeted interventions to resolve these issues.
    
- **Capacity Planning and Scalability:** It helps determine the maximum workload a system can handle (system capacity) and assesses how the system performs with increased load (scalability). These insights are vital for accurate future planning and sustained growth.
    
- **Optimization Opportunities:** It uncovers areas ripe for performance tuning and efficient resource utilization, preventing both underutilization of resources and overspending on unnecessary upgrades.
    
- **Ensuring Efficiency and Meeting Expectations:** As organizational reliance on computer systems grows, performance evaluation ensures that these systems operate efficiently and meet predefined performance expectations and objectives, thereby preventing costly system failures under critical loads.