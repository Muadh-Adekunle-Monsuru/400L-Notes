Here's the answer to the past questions, with explanations and solutions based on the provided notes.

### Question 1: Queuing Model Terms and Calculations

**(a) Explain the following terms as related to Queuing Model and indicate the type of queue in which each can happen.**

* **(i) Balking:** A customer decides not to join the queue because it is too long. This can happen in any type of queue where customers can observe the queue length before deciding to join.
* **(ii) Reneging:** A customer joins the queue but leaves before being served because the wait is too long. This can happen in any type of queue where customers are already in line but abandon the process.
* **(iii) Jockeying:** A customer moves from one queue to another in a multi-queue system if they perceive the other queue is moving faster. This specifically occurs in systems with multiple parallel queues.

**(b) The time spent by a repairman on his job has an exponential distribution with mean of 10 minutes. If he repairs phones in the order in which they come in and if the arrival of phones is approximately Poisson with an average rate of 5 per hour. Consider the model as M/M/1.**

**Calculate the following:**

* **(i) The traffic intensity**
    * Arrival rate ($\lambda$): 5 phones per hour.
    * Service time: Mean of 10 minutes. To convert to service rate ($\mu$) in phones per hour: 60 minutes/hour / 10 minutes/phone = 6 phones per hour.
    * Traffic intensity ($\rho$): $\rho = \frac{\lambda}{\mu}$
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
    * Alternatively, for an M/M/1 queue, $P(n \ge k) = \rho^k$. So $P(n \ge 2) = (0.8333)^2 \approx 0.6944$.
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
    * **Static Model:** Represents a system at a single point in time, without considering time dependency. [cite_start]It's used for equilibrium analysis or snapshots. [cite: 298] [cite_start]Example: An economic supply-demand equilibrium model. [cite: 298]
    * [cite_start]**Dynamic Model:** Represents a system over time, where variables change with time. [cite: 298] [cite_start]It's used for studying evolution and transient behavior. [cite: 298] [cite_start]Example: A population growth model (tracking changes yearly). [cite: 298]
* **(ii) Deterministic vs. Stochastic Models**
    * [cite_start]**Deterministic Model:** No randomness involved; the same inputs always produce the same outputs. [cite: 302] [cite_start]Used when system behavior is fully predictable. [cite: 303] [cite_start]Example: Projectile motion (physics equations with no randomness). [cite: 303]
    * [cite_start]**Stochastic Model:** Incorporates randomness (probabilistic elements). [cite: 302] [cite_start]Used for real-world uncertainty (e.g., failures, random arrivals). [cite: 303] [cite_start]Example: A Monte Carlo simulation (stock price prediction with random variations). [cite: 303]
* **(iii) Continuous vs. Discrete Models**
    * [cite_start]**Continuous Model:** Represents systems where changes occur smoothly over time or space. [cite: 296] [cite_start]Uses real numbers (infinite possible values). [cite: 296] [cite_start]Example: Fluid flow in a pipe (pressure changes continuously). [cite: 296]
    * [cite_start]**Discrete Model:** Represents systems where changes occur at specific, separate points in time or space. [cite: 296] [cite_start]Uses distinct, countable values (e.g., integers). [cite: 296] [cite_start]Example: Queueing system (customers arrive at discrete times). [cite: 296]

**(b) Explain three (3) circumstances where simulation should be used and not be used as appropriate tool for studying and analyzing system.**

**Circumstances where simulation should be used:**
1.  [cite_start]**When direct experimentation is impractical, expensive, or dangerous:** Simulation helps in evaluating and optimizing alternatives when direct testing is impractical or expensive. [cite: 20]
2.  [cite_start]**When a system has complex interactions or delayed consequences:** It's especially valuable for systems with complex interactions or delayed consequences. [cite: 21]
3.  [cite_start]**For training purposes:** Models are useful for training (e.g., flight simulators). [cite: 48]

**Circumstances where simulation should NOT be used (or might not be the most appropriate tool):**
1.  **When an analytical solution exists:** If a system can be accurately described and solved using mathematical equations, an analytical solution is usually faster, cheaper, and provides exact results, making simulation unnecessary.
2.  **When the problem is too simple or too complex:** For very simple problems, setting up a simulation might be overkill. For extremely complex problems with too many unknown variables or intractable relationships, building a valid and verifiable simulation model might be impossible or require excessive resources.
3.  **When data is insufficient or unreliable:** Simulations require accurate input data to produce meaningful results. If there's insufficient historical data or the available data is unreliable, the simulation output will also be unreliable.

### Question 3: Key Characteristics of a Queuing Model and Kendall Notation

**(a) What are the key characteristics of the queuing model? Explain them.**

The key characteristics of a queuing model define its structure and behavior:
1.  **Arrival Process:** Describes how customers enter the system, including the pattern of arrivals and the arrival rate.
2.  **Service Process:** Describes how customers are served, including the distribution of service times and the service rate.
3.  **Number of Servers (Channels):** The number of service facilities available to process customers.
4.  **Queue Discipline:** The rule by which customers are selected from the queue for service (e.g., FIFO, LIFO).
5.  **System Capacity:** The maximum number of customers allowed in the system.
6.  **Customer Behavior:** How customers react to the queue, including balking, reneging, and jockeying.

**(b) What is Kendall notation? Explain each parameter in it.**

Kendall notation is a shorthand method for classifying and describing queuing systems, typically in the format A/B/C.
* **A: Arrival Distribution:** Describes the probability distribution of customer inter-arrival times.
    * **M (Markovian / Poisson):** Inter-arrival times follow an exponential distribution (arrivals follow a Poisson process).
    * **D (Deterministic):** Inter-arrival times are fixed.
    * **G (General):** Inter-arrival times follow any arbitrary statistical distribution.
* **B: Service Time Distribution:** Describes the probability distribution of time it takes to serve a customer.
    * **M (Markovian / Exponential):** Service times follow an exponential distribution.
    * **D (Deterministic):** Service times are fixed.
    * **G (General):** Service times follow any arbitrary statistical distribution.
* **C: Number of Servers:** An integer representing the number of parallel servers in the system.
