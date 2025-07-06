![[CPS 418 a.jpeg]]
![[CPS 418 b.jpeg]]

### Question 1: Queuing Model Terms and Calculations

**(a) Explain the following terms as related to Queuing Model and indicate the type of queue in which each can happen.**

* **(i) Balking:** A customer decides not to join the queue because it is too long. This can happen in any type of queue where customers can observe the queue length before deciding to join.
* **(ii) Reneging:** A customer joins the queue but leaves before being served because the wait is too long. This can happen in any type of queue where customers are already in line but abandon the process.
* **(iii) Jockeying:** A customer moves from one queue to another in a multi-queue system if they perceive the other queue is moving faster. This specifically occurs in systems with multiple parallel queues.

**(b) The time spent by a repairman on his job has an exponential distribution with mean of 10 minutes. If he repairs phones in the order in which they come in and if the arrival of phones is approximately Poisson with an average rate of 5 per hour. Consider the model as M/M/1.**

**Calculate the following:**

* **(i) The traffic intensity**
    * **Arrival rate ($\lambda$):** 5 phones per hour.
    * **Service time:** Mean of 10 minutes. To convert to service rate ($\mu$) in phones per hour: 60 minutes/hour / 10 minutes/phone = 6 phones per hour.
    * **Traffic intensity ($\rho$):** $\rho = \frac{\lambda}{\mu}$
        $\rho = \frac{5 \text{ phones/hour}}{6 \text{ phones/hour}} = 0.8333$

* **(ii) Probability that there is no phone to repair**
    * This is $P_0 = 1 - \rho$.
    * $P_0 = 1 - 0.8333 = 0.1667$

* **(iii) Probability that there are five phones with the repairman**
    * This means there are 5 phones in the system. For an M/M/1 queue, $P_n = \rho^n P_0$.
    * $P_5 = (0.8333)^5 \times 0.1667$
    * $P_5 \approx 0.40187 \times 0.1667 \approx 0.06698$

* **(iv) Probability that there are at least two phones with the repairman**
    * This is $P(n \ge 2) = 1 - P(n=0) - P(n=1)$.
    * $P(n=1) = \rho^1 P_0 = 0.8333 \times 0.1667 \approx 0.1389$
    * $P(n \ge 2) = 1 - 0.1667 - 0.1389 = 1 - 0.3056 = 0.6944$
    * Alternatively, $P(n \ge k) = \rho^k$. So $P(n \ge 2) = \rho^2 = (0.8333)^2 \approx 0.6944$.

* **(v) Number of phones with the repairman ($L_s$)**
    * $L_s = \frac{\lambda}{\mu - \lambda}$
    * $L_s = \frac{5}{6 - 5} = \frac{5}{1} = 5$ phones

* **(vi) Number of phones waiting for repair ($L_q$)**
    * $L_q = \frac{\lambda^2}{\mu(\mu - \lambda)}$
    * $L_q = \frac{5^2}{6(6 - 5)} = \frac{25}{6(1)} = \frac{25}{6} \approx 4.1667$ phones

* **(vii) Waiting time in the system ($W_s$)**
    * $W_s = \frac{L_s}{\lambda}$
    * $W_s = \frac{5 \text{ phones}}{5 \text{ phones/hour}} = 1 \text{ hour}$ or 60 minutes.

* **(viii) Waiting time in the queue ($W_q$)**
    * $W_q = \frac{L_q}{\lambda}$
    * $W_q = \frac{4.1667 \text{ phones}}{5 \text{ phones/hour}} \approx 0.8333 \text{ hours}$ or 50 minutes.

### Question 2: Classification of Models and Simulation Circumstances

**(a) Explain the following classification of models:**

* **(i) Static vs. Dynamic Models** 
    * **Static Model:** Represents a system at a single point in time, without considering time dependency. It's used for equilibrium analysis or snapshots. 
        * **Example:** An economic supply-demand equilibrium model. 
    * **Dynamic Model:** Represents a system over time, where variables change with time. It's used for studying evolution and transient behavior. 
        * **Example:** A population growth model that tracks changes yearly. 

* **(ii) Deterministic vs. Stochastic Models** 
    * **Deterministic Model:** No randomness involved; the same inputs always produce the same outputs. Used when system behavior is fully predictable. 
        * **Example:** Projectile motion described by physics equations with no randomness. 
    * **Stochastic Model:** Incorporates randomness or probabilistic elements.Used for real-world uncertainty like failures or random arrivals. 
        * **Example:** A Monte Carlo simulation for stock price prediction with random variations.

* **(iii) Continuous vs. Discrete Models**
    * **Continuous Model:** Represents systems where changes occur smoothly over time or space, using real numbers for values. 
        * **Example:** Fluid flow in a pipe, where pressure changes continuously. 
    * **Discrete Model:** Represents systems where changes occur at specific, separate points in time or space, using distinct, countable values (e.g., integers). 
        * **Example:** A queueing system where customers arrive at discrete times. 

**(b) Explain three (3) circumstances where simulation should be used and not be used as appropriate tool for studying and analyzing system.**

**Circumstances where simulation should be used:**
1.  **When direct experimentation is impractical, expensive, or dangerous:** For example, simulating a new aircraft design before building a physical prototype, or analyzing the impact of a pandemic on hospital capacity without risking patient lives.
2.  **When a system has complex interactions or delayed consequences:** Simulation allows you to observe how various components of a system interact over time and evaluate long-term effects that might not be immediately obvious. This is common in supply chain management or complex manufacturing processes.
3.  **For training purposes:** Simulation models provide a safe and controlled environment for training individuals in complex or high-risk scenarios, such as flight simulators for pilots or surgical simulators for medical students. 

**Circumstances where simulation should NOT be used (or might not be the most appropriate tool):**
1.  **When an analytical solution exists:** If a system can be accurately described and solved using mathematical equations (e.g., simple queuing formulas under specific assumptions), an analytical solution is usually faster, cheaper, and provides exact results, making simulation unnecessary.
2.  **When the problem is too simple or too complex:** For very simple problems, setting up a simulation might be overkill. For extremely complex problems with too many unknown variables or intractable relationships, building a valid and verifiable simulation model might be impossible or require excessive resources.
3.  **When data is insufficient or unreliable:** Simulations require accurate input data to produce meaningful results. If there's insufficient historical data or the available data is unreliable, the simulation output will also be unreliable ("garbage in, garbage out").

### Question 3: Key Characteristics of a Queuing Model and Kendall Notation

**(a) What are the key characteristics of the queuing model? Explain them.**

The key characteristics of a queuing model define its structure and behavior:
1.  **Arrival Process:** Describes how customers enter the system. This includes the pattern of arrivals (e.g., random arrivals following a Poisson distribution, or deterministic arrivals), the arrival rate, and the population size (finite or infinite).
2.  **Service Process:** Describes how customers are served. This involves the distribution of service times (e.g., exponential, deterministic, or general), and the service rate.
3.  **Number of Servers (Channels):** The number of service facilities available to process customers. This can be a single server or multiple servers working in parallel.
4.  **Queue Discipline:** The rule by which customers are selected from the queue for service. Common disciplines include:
    * **FIFO (First-In, First-Out) / FCFS (First-Come, First-Served):** Customers are served in the order they arrive.
    * **LIFO (Last-In, First-Out):** The last customer to arrive is served first (e.g., a stack of items).
    * **SIPT (Shortest Important Processing Time):** Customers with shorter service times are prioritized.
    * **Priority:** Customers are served based on their assigned priority level.
5.  **System Capacity:** The maximum number of customers (waiting in line and being served) that the system can accommodate. If the capacity is limited, customers may be turned away (balking) when the system is full.
6.  **Customer Behavior:** How customers react to the queue, including balking, reneging, and jockeying (as explained in Question 1a).

**(b) What is Kendall notation? Explain each parameter in it.**

Kendall notation is a shorthand method for classifying and describing queuing systems. It uses a series of letters and numbers, typically in the format A/B/C/D/E/F, though often simplified to A/B/C for common cases.

* **A: Arrival Distribution:** Describes the probability distribution of customer inter-arrival times.
    * **M (Markovian / Poisson):** Inter-arrival times follow an exponential distribution (arrivals follow a Poisson process). This implies random arrivals.
    * **D (Deterministic):** Inter-arrival times are fixed (constant).
    * **G (General):** Inter-arrival times follow any arbitrary statistical distribution.

* **B: Service Time Distribution:** Describes the probability distribution of time it takes to serve a customer.
    * **M (Markovian / Exponential):** Service times follow an exponential distribution.
    * **D (Deterministic):** Service times are fixed (constant).
    * **G (General):** Service times follow any arbitrary statistical distribution.

* **C: Number of Servers:** An integer representing the number of parallel servers in the system.
    * **Example:** 1 for a single server, 'c' or 'k' for multiple servers.

**(c) State Little's Law (Equation)**
Little's Law states a fundamental relationship between the average number of customers in a stable system (or part of a system), the average arrival rate, and the average time a customer spends in the system.
The equation is:
$L = \lambda W$
Where:
* $L$: Average number of customers in the system.
* $\lambda$: Average arrival rate of customers into the system.
* $W$: Average time a customer spends in the system.

**(d) Given an M/M/1 queue with traffic intensity of 90%, what is the mean number of customers in the queuing area?**
* Traffic intensity ($\rho$) = 90% = 0.90
* For an M/M/1 queue, the mean number of customers in the queuing area (queue length) is $L_q = \frac{\rho^2}{1-\rho}$ or $L_q = \frac{\lambda^2}{\mu(\mu-\lambda)}$.
    Using $L_q = \frac{\rho^2}{1-\rho}$:
    $L_q = \frac{(0.90)^2}{1 - 0.90} = \frac{0.81}{0.10} = 8.1$ customers.

### Question 4: Modelling with Differential Equations

**(a) The rate of change (per day) in the price P of a commodity is directly proportional to (P - 10). If the initial price of the commodity is N150 and three days later, the price increases to N175.**

* **(i) Set up a model (with differential equation) to solve for P.**
    Let P be the price of the commodity.
    The rate of change of price is $\frac{dP}{dt}$.
    "directly proportional to (P - 10)" means $\frac{dP}{dt} \propto (P - 10)$.
    Introducing a proportionality constant $k$:
    $\frac{dP}{dt} = k(P - 10)$

* **(ii) After how many days will the price of the commodity be doubled?**
    From the differential equation: $\frac{dP}{P-10} = k dt$
    Integrate both sides: $\int \frac{1}{P-10} dP = \int k dt$
    $\ln|P-10| [cite_start]= kt + C$ 
    $P-10 = e^{kt+C} = e^C e^{kt}$ 
    Let $A = e^C$.So, $P(t) = 10 + Ae^{kt}$. 

    Initial condition: At $t=0$, $P=150$.
    $150 = 10 + Ae^{k \cdot 0}$ 
    $150 = 10 + A$
    $A = 140$
    So, the particular solution is $P(t) = 10 + 140e^{kt}$. 

    Now, use the second condition: At $t=3$ days, $P=175$.
    $175 = 10 + 140e^{k \cdot 3}$
    $165 = 140e^{3k}$
    $e^{3k} = \frac{165}{140} = \frac{33}{28} \approx 1.17857$
    $3k = \ln(\frac{33}{28})$
    $k = \frac{1}{3} \ln(\frac{33}{28}) \approx \frac{1}{3} (0.1643) \approx 0.05477$

    The price will be doubled when $P = 2 \times 150 = 300$.
    $300 = 10 + 140e^{kt}$
    $290 = 140e^{kt}$
    $e^{kt} = \frac{290}{140} = \frac{29}{14} \approx 2.0714$
    $kt = \ln(\frac{29}{14})$
    $t = \frac{\ln(\frac{29}{14})}{k} = \frac{\ln(\frac{29}{14})}{0.05477}$
    $t \approx \frac{0.7285}{0.05477} \approx 13.29$ days.

* **(iii) What will be the price of the commodity 30 days after the initial price?**
    We need to find $P(30)$.
    $P(30) = 10 + 140e^{k \cdot 30}$
    We know $e^{3k} = \frac{33}{28}$. So $e^{30k} = (e^{3k})^{10} = (\frac{33}{28})^{10}$.
    $P(30) = 10 + 140 \times (\frac{33}{28})^{10}$
    $P(30) \approx 10 + 140 \times (1.17857)^{10}$
    $P(30) \approx 10 + 140 \times 4.908$
    $P(30) \approx 10 + 687.12 = 697.12$ Naira.

* **(iv) Describe the graph of the behavior of P.**
    The solution is $P(t) = 10 + 140e^{kt}$, where $k \approx 0.05477$ is positive.
    * **Starting Point:** At $t=0$, $P(0)=150$.
    * **Growth:** Since $k$ is positive, $e^{kt}$ is an increasing exponential function. Therefore, the price $P(t)$ will increase exponentially over time.
    * **Asymptotic Behavior:** As $t \rightarrow \infty$, $e^{kt} \rightarrow \infty$, so $P(t) \rightarrow \infty$. There is no upper limit to the price in this model.
    * **Minimum Price:** The function $P(t)$ approaches 10 as $t \rightarrow -\infty$. This means the "base" value for the price is 10.
    * **Shape:** The graph will be an upward-curving exponential curve starting from 150 and increasing without bound.

**(b) Explain the following components of a system**

* **(i) Event:** A discrete occurrence that triggers a change in the system's state at a specific time. Example: In a traffic simulation, a "car arrival" or "traffic light change" is an event. 
* **(ii) State:** The current condition of the system at any given time, defined by the values of key variables. Example: In a hospital simulation, the state could include "number of occupied beds" or "queue length in ER." 
* **(iii) Entity:** An individual object or component within the system that moves through processes and interacts with resources. Example: Customers in a bank queue, packets in a network, or products on an assembly line.

### Question 5: Probability Distribution Functions

**(a) Explain the following Probability Distribution Functions:**

* **(i) Binomial Distribution:**
    The Binomial distribution models the number of successes in a fixed number of independent Bernoulli trials. A Bernoulli trial is an experiment with only two possible outcomes: success or failure.
    * **Key characteristics:** Fixed number of trials, each trial is independent, only two outcomes per trial (success/failure), and the probability of success is constant.
    * **Formula:** $P(X=k) = \binom{n}{k} p^k (1-p)^{n-k}$
    * **Example:** The number of heads when flipping a coin 10 times.

* **(ii) Poisson Distribution:**
    The Poisson distribution models the number of events occurring in a fixed interval of time or space, given that these events occur with a known constant mean rate and independently of the time since the last event.
    * **Key characteristics:** Events occur independently, events occur at a constant average rate, and the number of events in one interval does not affect the number of events in other non-overlapping intervals.
    * **Formula:** $P(X=k) = \frac{e^{-\lambda} \lambda^k}{k!}$ where $\lambda$ is the average number of events in the interval.
    * **Example:** The number of calls received by a call center in an hour.

**(b) The number of typing mistakes made by a secretary has a Poisson distribution. The mistakes are made independently at an average rate of 1.55 per page. Find the probability that a four-page letter contains:**

* Average rate ($\lambda$) per page: 1.55 mistakes/page.
* For a **four-page letter**, the new average rate ($\lambda_{total}$) will be $1.55 \times 4 = 6.2$ mistakes.
* We use the Poisson probability formula: $P(X=k) = \frac{e^{-\lambda_{total}} \lambda_{total}^k}{k!}$

* **(i) exactly two mistakes**
    Here, $k=2$.
    $P(X=2) = \frac{e^{-6.2} (6.2)^2}{2!}$
    $e^{-6.2} \approx 0.00203$
    $P(X=2) = \frac{0.00203 \times 38.44}{2} = \frac{0.0780212}{2} \approx 0.03901$

* **(ii) at most two mistakes**
    This means $P(X \le 2) = P(X=0) + P(X=1) + P(X=2)$.
    * $P(X=0) = \frac{e^{-6.2} (6.2)^0}{0!} = \frac{e^{-6.2} \times 1}{1} \approx 0.00203$
    * $P(X=1) = \frac{e^{-6.2} (6.2)^1}{1!} = \frac{0.00203 \times 6.2}{1} \approx 0.01259$
    * $P(X=2) \approx 0.03901$ (calculated above)
    $P(X \le 2) = 0.00203 + 0.01259 + 0.03901 = 0.05363$