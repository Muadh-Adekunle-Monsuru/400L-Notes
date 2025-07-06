# Comprehensive Notes on Modelling and Simulation  

## 1. Random Number Generation  
### Key Concepts:  
- **Pseudo-Random Numbers**: Generated algorithmically (not truly random).  
- **Congruential Methods**:  
  - **Mixed Congruential**:  $X_{n+1} = (aX_n + c) \mod m$  
  - **Multiplicative**: $X_{n+1} = aX_n \mod m$ (c = 0).  
- **Parameters**:  
  - $a$: Multiplier (must be carefully chosen).  
  - $c$: Increment (0 for multiplicative).  
  - $m$: Modulus (large prime for longer periods).  

### Example (Mixed Congruential):  
Given $a=5, c=7, m=8, X_0=4$:  
- $X_1 = (5×4 + 7) \mod 8 = 3$  
- $X_2 = (5×3 + 7) \mod 8 = 6$  
- Cycle repeats every 8 numbers.  

### Practice Questions:  
1. Generate 5 numbers using $a=3, c=5, m=16, X_0=2$.  
## 2. Modeling: Types, Processes, and Classifications  
### Types of Models:  
| **Type**         | **Description**                          | **Example**                     |  
|------------------|------------------------------------------|---------------------------------|  
| **Discrete**     | Changes at specific points (e.g., integers). | Queueing systems (customer arrivals). |  
| **Continuous**   | Changes smoothly (real numbers).         | Fluid flow in pipes.            |  
| **Deterministic**| No randomness (fixed outputs).           | Projectile motion.              |  
| **Stochastic**   | Incorporates randomness.                 | Stock price prediction.         |  
### Modeling Process:  
1. **Problem Definition** → 2. **Data Collection** → 3. **Model Construction** → 4. **Validation** → 5. **Implementation**.  
### Practice Questions:  
1. Differentiate between static and dynamic models with examples.  
2. List 3 advantages of using simulation models.  

## 3. Modeling with Difference & Differential Equations  
### Difference Equations (Discrete Time):  
- **General Form**: $P_{n+1} = aP_n + b$  
- **Example (Trout Population)**:  
  $P_{n+1} = 1.15P_n - 30,000$ → Solved as $P_n = -50,000(1.15)^n + 200,000$.  
### Differential Equations (Continuous Time):  
- **Newton’s Law of Cooling**:  
  $\frac{dT}{dt} = K(T - T_s)$ → Solution: $T(t) = T_s + (T_0 - T_s)e^{Kt}$.  
### Practice Questions:  
1. Solve: $y_{n+1} = 0.8y_n + 100$, $y_0 = 500$.  
2. A cup of coffee cools from 90°C to 80°C in 5 minutes (ambient=20°C). Find $K$.  

---
## 4. Queuing Theory  
### Key Formulas:  
- **Arrival Rate ($\lambda$)**: Customers per unit time.  
- **Service Rate ($\mu$)**: Customers served per unit time.  
- **Utilization ($\rho$)**: $\rho = \frac{\lambda}{\mu}$.  
- **Average Queue Length**: $L_q = \frac{\rho^2}{1-\rho}$ (M/M/1 model).  
### Example:  
If $\lambda = 4$/hour, $\mu = 5$/hour:  
- $\rho = \frac{4}{5} = 0.8$.  
- $L_q = \frac{0.8^2}{1-0.8} = 3.2$ customers.  

### Practice Questions:  
1. Calculate $L_q$ if $\lambda = 3$, $\mu = 4$.  
2. Why must $\lambda < \mu$ for a stable queue?  

---

## 5. Assignment-Style Problems  
### Example (From Assignment 2):  
**Problem**: A fishery has $P_0 = 150,000$ trout, grows at 15%/year, harvests 30,000/year.  
- **(a)**: Solve $P_{n+1} = 1.15P_n - 30,000$.  
- **(b)**: When does $P_n = 0$? *(Answer: ~9.92 years)*.  

### Practice Questions:  
1. Modify the harvest rate to ensure trout survive 20 years *(Hint: Use $P_{20} > 0$)*.  
2. Solve the cache hits problem: $H(n) = 0.9H(n-1) + 200$, $H(0) = 800$.  
