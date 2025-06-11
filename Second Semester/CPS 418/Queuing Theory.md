## **Operations Research – Unit 5: Queuing Theory**

---

### **Introduction**

Queuing theory studies waiting lines, aiming to balance:

* **Service cost** and
* **Customer waiting time**

It is widely applied in banks, hospitals, telecom, and computer networks.

---

### **Components of a Queuing System**

1. **Input Source**:

   * Can be **finite** or **infinite**
   * Arrival process usually follows a **Poisson distribution**
   * Inter-arrival time: **Exponential distribution**

2. **Queue Discipline**:

   * Order in which customers are served:

     * FIFO (First In First Out)
     * SIRO (Service in Random Order)
     * Priority, etc.

3. **Service Mechanism**:

   * One or more **service channels**
   * Service time typically follows **Exponential**, **Deterministic**, **General**, or **Erlang** distribution

---

### **Kendall’s Notation**

Queuing models are represented as:

$$
a / b / c : d / e
$$

Where:

* $a$: Inter-arrival time distribution
* $b$: Service time distribution
* $c$: Number of servers
* $d$: Capacity of the system
* $e$: Queue discipline

**Common Notations**:

* $M$: Exponential (Markovian)
* $D$: Deterministic
* $G$: General
* $E_k$: Erlang (k phases)

---

### **Standard Models**

| Model | Notation                             | Description                             |
| ----- | ------------------------------------ | --------------------------------------- |
| I     | $M / M / 1 : \infty / \text{FCFS}$   | Basic infinite queue with single server |
| II    | $M / M / 1 : N / \text{FCFS}$        | Finite queue capacity                   |
| III   | $M / M / 1 : \infty / \text{SIRO}$   | Random service                          |
| IV    | $M / D / 1 : \infty / \text{FCFS}$   | Deterministic service time              |
| V     | $M / G / 1 : \infty / \text{FCFS}$   | General service time                    |
| VI    | $M / E_k / 1 : \infty / \text{FCFS}$ | Erlang service distribution             |
| VII   | $M / M / K : \infty / \text{FCFS}$   | Multiple servers                        |
| VIII  | $M / M / K : N / \text{FCFS}$        | Multiple servers, finite capacity       |

---

### **Key Formulas (Model I: M/M/1)**

Let:

* $\lambda$: Arrival rate
* $\mu$: Service rate
* $\rho = \frac{\lambda}{\mu}$: Utilization (must be $< 1$)

1. **Utilization**:

   $$
   \rho = \frac{\lambda}{\mu}
   $$

2. **Probability of 0 units in system**:

   $$
   P_0 = 1 - \rho
   $$

3. **Probability of exactly $n$ units**:

   $$
   P_n = (1 - \rho) \cdot \rho^n
   $$

4. **Probability of $n$ or more units**:

   $$
   P_{\geq n} = \rho^{n+1}
   $$

5. **Expected number in queue**:

   $$
   L_q = \frac{\lambda^2}{\mu(\mu - \lambda)}
   $$

6. **Expected waiting time in queue**:

   $$
   W_q = \frac{L_q}{\lambda}
   $$

7. **Expected number in system**:

   $$
   L = L_q + \frac{\lambda}{\mu}
   $$

8. **Expected waiting time in system**:

   $$
   W = W_q + \frac{1}{\mu}
   $$

9. **Average non-empty queue size**:

   $$
   D = \frac{\lambda}{\mu - \lambda}
   $$

10. **Probability of waiting**:

$$
P_{\text{wait}} = 1 - P_0 = \rho
$$

11. **Probability wait in queue > $w$**:

$$
P(W_q > w) = \rho \cdot e^{-(\mu - \lambda)w}
$$

12. **Probability wait in system > $v$**:

$$
P(W > v) = e^{-(\mu - \lambda)v}
$$

---

### **Worked Example (Model I)**

**Given**:

* Mean inter-arrival time = 8 min → $\lambda = \frac{60}{8} = 7.5 \, \text{per hour}$
* Mean service time = 4 min → $\mu = \frac{60}{4} = 15 \, \text{per hour}$

**Solution**:

* a) Utilization:

  $$
  \rho = \frac{7.5}{15} = 0.5
  $$

* b) $L_q = \frac{(7.5)^2}{15(15 - 7.5)} = 0.5$

* c) $W_q = \frac{0.5}{7.5} = 0.0667 \, \text{hr} = 4 \, \text{min}$

* d) $L = 0.5 + \frac{7.5}{15} = 1$

* e) $W = 0.0667 + \frac{1}{15} = 0.1333 \, \text{hr} = 8 \, \text{min}$

* f) $D = \frac{7.5}{15 - 7.5} = 1$

* g) $P_{\text{wait}} = 1 - P_0 = 0.5$

* h) $P_3 = 0.5 \cdot (0.5)^3 = 0.0625$

* i) $P_0 = 1 - \rho = 0.5$

* j) $P_{\geq 3} = \rho^4 = (0.5)^4 = 0.0625$

* k) $P(W_q > 6\, \text{min}) = 0.5 \cdot e^{-(15 - 7.5) \cdot \frac{6}{60}} \approx 0.236$

* l) $P_{\geq 6} = \rho^7 = (0.5)^7 = 0.0078125 \approx 0.008$

* m) $P(W > 8\, \text{min}) = e^{-(15 - 7.5) \cdot \frac{8}{60}} \approx 0.367$

* n) To justify a second booth for Wq ≤ 6 min = 0.1 hr:

  $$
  W_q = \frac{\lambda}{\mu(\mu - \lambda)} = 0.1 \Rightarrow \lambda \approx 9
  $$

---

## 📘 **Multiple Server Model: M/M/K (∞/FCFS)**

### 📌 **Notations**

* **λ (lambda)**: Average arrival rate (customers/hour)
* **μ (mu)**: Average service rate per server (customers/hour)
* **K**: Number of servers
* **Pn**: Probability of having *n* customers in the system
* **P₀**: Probability that there are 0 customers in the system (system is idle)
* **L**: Average number of customers in the system
* **Lq**: Average number of customers in the queue
* **W**: Average time a customer spends in the system
* **Wq**: Average time a customer spends waiting in the queue
* **ρ (rho)**: Traffic intensity per server = λ / (Kμ)

---

### 📐 **Formulas**

**1. Probability that there are 0 customers in the system (P₀):**

$$
P_0 = \left[ \sum_{n=0}^{K-1} \frac{1}{n!} \left( \frac{\lambda}{\mu} \right)^n + \frac{1}{K!} \left( \frac{\lambda}{\mu} \right)^K \frac{K\mu}{K\mu - \lambda} \right]^{-1}
$$

---

**2. Probability of having *n* customers in the system (n ≥ 0):**

$$
P_n = 
\begin{cases} 
\frac{1}{n!} \left( \frac{\lambda}{\mu} \right)^n P_0 & \text{if } n < K \\
\frac{1}{K!} \left( \frac{\lambda}{\mu} \right)^n \frac{1}{K^{n-K}} P_0 & \text{if } n \geq K
\end{cases}
$$

---

**3. Average number of customers in the queue (Lq):**

$$
L_q = \frac{P_0 \cdot \left( \frac{\lambda}{\mu} \right)^K \cdot \frac{\lambda \mu}{(K-1)!}}{(K\mu - \lambda)^2}
$$

---

**4. Average number in the system (L):**

$$
L = L_q + \frac{\lambda}{\mu}
$$

---

**5. Average waiting time in the queue (Wq):**

$$
W_q = \frac{L_q}{\lambda}
$$

---

**6. Average time in the system (W):**

$$
W = W_q + \frac{1}{\mu}
$$

---

**7. Server utilization (ρ):**

$$
\rho = \frac{\lambda}{K\mu}
$$

---

## **Example 1: Commercial Bank with 3 Cashiers**

### **Problem Statement:**

A bank has **3 cashiers (servers)**. Customers arrive in a **Poisson process** at an average rate of **6 per hour (λ = 6/hr)**. The service time follows an **exponential distribution** with a mean of **18 minutes per customer (μ = 3.33/hr)**. The bank operates on a **First-Come-First-Served (FCFS)** basis.

**Calculate:**

1. **Average number of customers in the system (L).**
2. **Average time a customer spends in the system (W).**
3. **Average queue length (L\_q).**
4. **How many hours per week a cashier spends serving customers.**

---

### **Solution Steps:**

#### **1. Compute $P_0$ (Probability of Zero Customers in the System)**

The formula for $P_0$ in an M/M/K system is:

$$
P_0 = \frac{1}{\left[ \sum_{n=0}^{K-1} \frac{1}{n!} \left( \frac{\lambda}{\mu} \right)^n \right] + \frac{1}{K!} \left( \frac{\lambda}{\mu} \right)^K \frac{K\mu}{(K\mu - \lambda)}}
$$

* $K = 3$, $\lambda = 6$, $\mu = 3.33$.
* Compute the sum for $n = 0, 1, 2$:

  $$
  \sum_{n=0}^{2} \frac{1}{n!} \left( \frac{6}{3.33} \right)^n = 1 + 1.8 + \frac{1.8^2}{2} = 1 + 1.8 + 1.62 = 4.42
  $$
* Compute the last term:

  $$
  \frac{1}{3!} \left( \frac{6}{3.33} \right)^3 \frac{3 \times 3.33}{3 \times 3.33 - 6} = \frac{1}{6} (1.8)^3 \frac{10}{4} = 2.43
  $$
* Total denominator: $4.42 + 2.43 = 6.85$.
* Thus, $P_0 = \frac{1}{6.85} = 0.145$.

---

#### **2. Compute $L_q$ (Average Queue Length)**

$$
L_q = \frac{\lambda \mu \left( \frac{\lambda}{\mu} \right)^K}{(K-1)! (K\mu - \lambda)^2} \times P_0
$$

* Plugging in values:

  $$
  L_q = \frac{6 \times 3.33 \times (1.8)^3}{2! (10 - 6)^2} \times 0.145 = \frac{6 \times 3.33 \times 5.832}{2 \times 16} \times 0.145 = 0.532
  $$
* **Interpretation:** On average, **0.532 customers** are waiting in the queue.

---

#### **3. Compute $L$ (Average Customers in the System)**

$$
L = L_q + \frac{\lambda}{\mu} = 0.532 + \frac{6}{3.33} = 0.532 + 1.8 = 2.332
$$

* **Interpretation:** On average, **2.332 customers** are either in the queue or being served.

---

#### **4. Compute $W$ (Average Time in the System)**

$$
W = W_q + \frac{1}{\mu} = \frac{L_q}{\lambda} + \frac{1}{\mu} = \frac{0.532}{6} + \frac{1}{3.33} = 0.0887 + 0.3 = 0.388 \text{ hrs (≈ 23.3 mins)}
$$

* **Interpretation:** A customer spends **\~23.3 minutes** in the bank on average.

---

#### **5. Weekly Service Time per Cashier**

* **Utilization factor ($\rho$):**

  $$
  \rho = \frac{\lambda}{K \mu} = \frac{6}{3 \times 3.33} = 0.6
  $$
* **Weekly hours (assuming 5 days, 8 hours/day):**

  $$
  \text{Weekly service time} = \rho \times 5 \times 8 = 0.6 \times 40 = 24 \text{ hrs}
  $$
* **Interpretation:** Each cashier spends **24 hours per week** serving customers.

---

## **Example 2: Telephone Exchange with 2 Operators**

### **Problem Statement:**

A telephone exchange has **2 operators (servers)**. Calls arrive in a **Poisson process** at **15 per hour (λ = 15/hr)**. The average call duration is **5 minutes (μ = 12/hr)**.

**Calculate:**

1. **Probability that a subscriber must wait for an operator.**
2. **Average waiting time for customers ($W_q$).**

---

### **Solution Steps:**

#### **1. Compute $P_0$ (Probability of Zero Calls in the System)**

$$
P_0 = \frac{1}{\left[ 1 + \frac{15}{12} + \frac{1}{2} \left( \frac{15}{12} \right)^2 \frac{24}{24-15} \right]} = \frac{1}{1 + 1.25 + 1.5625 \times \frac{24}{9}} = \frac{1}{1 + 1.25 + 4.1667} = \frac{1}{6.4167} = 0.156
$$

*(Note: The document gives $P_0 = 0.230$, but the correct calculation should yield \~0.156. There may be an error in the original solution.)*

---

#### **2. Probability a Subscriber Must Wait ($P_{wait}$)**

This is the probability that **both operators are busy**:

$$
P_{wait} = 1 - P_0 - P_1
$$

* First, compute $P_1$:

  $$
  P_1 = \frac{1}{1!} \left( \frac{15}{12} \right)^1 \times 0.156 = 1.25 \times 0.156 = 0.195
  $$
* Then,

  $$
  P_{wait} = 1 - 0.156 - 0.195 = 0.649 \quad (\text{Document says } 0.48, \text{ likely due to } P_0 \text{ error})
  $$
* **Interpretation:** There is a **64.9% chance** a caller must wait.

---

#### **3. Compute $W_q$ (Average Waiting Time)**

$$
W_q = \frac{L_q}{\lambda} = \frac{\lambda \mu \left( \frac{\lambda}{\mu} \right)^K}{\lambda (K-1)! (K\mu - \lambda)^2} \times P_0
$$

$$
= \frac{15 \times 12 \times (1.25)^2}{1! (24 - 15)^2} \times 0.156 = \frac{15 \times 12 \times 1.5625}{81} \times 0.156 = 0.053 \text{ hrs (≈ 3.2 mins)}
$$

* **Interpretation:** Callers wait **\~3.2 minutes** on average before being served.

---

### **Key Takeaways:**

1. **M/M/K Model** helps analyze multi-server queues with Poisson arrivals and exponential service times.
2. **Key Metrics:**

   * $L_q$: Average queue length.
   * $W$: Total time in the system.
   * $\rho$: Server utilization.
3. **Real-world Applications:**

   * Banks, call centers, and service systems use these models to optimize staffing and reduce wait times.

---
