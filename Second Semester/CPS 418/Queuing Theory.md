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
