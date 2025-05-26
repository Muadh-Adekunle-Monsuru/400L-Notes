All equations are models, but not all models are equations
`y` is the dependent variable
`x` is the independent variable
`t` can also be an independent variable

### **Temperature Model – Newton's Law of Cooling**

Newton's Law of Cooling states that:

> *The rate of change of the temperature of an object is proportional to the difference between the object's temperature and the surrounding temperature.*

---

#### **Definitions and Variables**

* Let **$t$** = time (independent variable)
* Let **$T$** = temperature of the object at time $t$ (dependent variable)
* Let **$T_s$** = constant surrounding temperature
* Let **$K$** = proportionality constant

---

#### **Mathematical Formulation**

$$
\frac{dT}{dt} \propto (T - T_s)
$$

$$
\frac{dT}{dt} = K(T - T_s)
$$

---

#### **Solving the Differential Equation**

Separate the variables:

$$
\frac{dT}{T - T_s} = K\,dt
$$

Integrate both sides:

$$
\int \frac{1}{T - T_s} \, dT = \int K \, dt
$$

$$
\ln |T - T_s| = Kt + C
$$

Where $C$ is the constant of integration.
Take the exponential of both sides to eliminate the logarithm:

$$
|T - T_s| = e^{Kt + C}
$$

$$
T - T_s = \pm e^{Kt + C}
$$

Since $e^{Kt + C} = e^{Kt} \cdot e^C$, we can simplify by absorbing the sign and constant into a new constant $K_1$:

$$
T - T_s = K_1 e^{Kt}, \quad \text{where } K_1 = \pm e^C
$$

Solve for $T$:

$$
T = T_s + K_1 e^{Kt}
$$

---


$$
\boxed{T(t) = T_s + K_1 e^{Kt}}
$$
This is the **general solution** to the temperature model based on Newton's Law of Cooling.

### **Finding the Particular Solution**

To determine the **particular solution**, we apply an initial condition:

Let:

* $t_0 = 0$ (initial time)
* $T(0) = T_0$ (initial temperature of the object)

Start with the general solution:

$$
T(t) = T_s + K_1 e^{Kt}
$$

Apply the initial condition $T(0) = T_0$:

$$
T_0 = T_s + K_1 e^{K \cdot 0}
$$

$$
T_0 = T_s + K_1 \cdot 1
$$

$$
K_1 = T_0 - T_s
$$

---

### ✅ **Particular Solution**

Substitute $K_1 = T_0 - T_s$ into the general solution:

$$
\boxed{T(t) = T_s + (T_0 - T_s) e^{Kt}}
$$

---

This equation models how the temperature $T(t)$ of an object changes over time $t$, given its initial temperature $T_0$ and the constant surrounding temperature $T_s$.


--- 
### **Mixing Problem Models**

In mixing problems:

> **The rate of change of a substance in a system is equal to the rate at which it enters the system minus the rate at which it exits the system.**

---
#### **Mathematical Formulation**
Let:
* $y(t)$ = amount of the substance in the system at time $t$
* $\frac{dy}{dt}$ = rate of change of the substance over time

Then the model is:

$$
\frac{dy}{dt} = \text{Rate In} - \text{Rate Out}
$$

This differential equation forms the basis for solving mixing problems involving inflow and outflow of substances like salt, chemicals, etc.


---
### **Difference Equation**

A **difference equation** is used to predict the future value of a variable based on its previous values. It expresses the value of a quantity $Q$ at a given time in terms of its past values.

* If the model depends on time, it is called a **dynamic model**.
* If the model is independent of time, it is called a **static model**.

---

#### **Example: Malthusian Population Model**

Let:

* $P$ = population
* $f$ = birth rate
* $d$ = death rate
* $\Delta P$ = change in population

$$
\Delta P = fP - dP = (f - d)P
$$

Define $r = f - d$ (net growth rate), then:

$$
\Delta P = rP
$$

In difference form:

$$
P_{t+1} = P_t + rP_t = (1 + f-d)P_t
$$

This equation model time steps.

---
### **Difference Equation for an Organism with a Rigid Lifecycle**

Suppose an organism has a **rigid lifecycle** where:

* Each **female lays 200 eggs**, and then all **adults die**.
* After the eggs hatch, **only 3%** survive to become **adult females** (the rest die or are males).

---

#### **Step 1: Define Rates**

* **Death rate** $d = 1$ (since all adults die)
* **Survival (birth) rate** $f = 0.03 \times 200 = 6$

---

#### **Step 2: Write the Difference Equation**

We use the general form:

$$
P_{t+1} = (1 + f - d)P_t
$$

Substitute $f = 6$ and $d = 1$:

$$
P_{t+1} = (1 + 6 - 1)P_t = 6P_t
$$

---

#### **Step 3: Initial Conditions and First Iterations**

Let the initial population be:

$$
P_0 = 6
$$

Then:

$$
P_1 = 6P_0 = 6 \times 6 = 36
$$
---

### **Modelling Loans with a Difference Equation**

When modeling loan repayment using a difference equation, the following elements must be known:

* The **interest rate** (per repayment period)
* The **loan term** (number of repayment periods)
* The **repayment amount and frequency**

---

#### **Key Variables**

* $U_n$: Amount owing after $n$ repayments
* $k$: Interest rate multiplier (e.g., 2% monthly → $k = 0.02$)
* $c$: Fixed repayment amount per period

---

#### **Difference Equation for Loan Repayment**

$$
U_n = U_{n-1} + kU_{n-1} - c = (1 + k)U_{n-1} - c
$$

This recurrence relation reflects the fact that interest is added to the loan balance before a repayment is made.

---

#### **General Solution**

$$
U_n = k^n U_0 + \frac{c(k^n - 1)}{k - 1}
$$


---

### ✅ **Example: Solve a Loan Repayment Problem**

**Problem**: Find the monthly repayment on a **\$500 loan** at **24% interest per annum**, repaid over **18 months**.

---

#### **Step 1: Convert Annual Interest to Monthly**

$$
\text{Annual interest rate} = 24\% \Rightarrow \text{Monthly rate} = \frac{24}{12} = 2\%
\Rightarrow k = 0.02
$$

$$
\text{So, } 1 + k = 1.02
$$

---

#### **Step 2: Use Present Value of an Annuity Formula**

To find the monthly repayment $c$, we use the annuity formula:

$$
U_0 = c \cdot \frac{1 - (1 + k)^{-n}}{k}
$$

Where:

* $U_0 = 500$
* $k = 0.02$
* $n = 18$

$$
500 = c \cdot \frac{1 - (1.02)^{-18}}{0.02}
$$

$$
500 = c \cdot \frac{1 - 0.6982}{0.02}
= c \cdot \frac{0.3018}{0.02}
= c \cdot 15.09
$$

$$
c = \frac{500}{15.09} \approx \boxed{33.14}
$$

---

### ✅ **Answer:**

The monthly repayment is approximately **\$33.14**


---

## First Order difference equation

$$
U_n =   KU_{n-1} + c
$$
$$
U_{n+1} =   KU_n + c
$$
general solution

if k != 1
$$
U_n = k^n U_0 + \frac{c(k^n - 1)}{k - 1}
$$

if k = 1
$$
U_n =   U_0 + nc
$$


---
**Problem**: Find the monthly repayment on a **\$500 loan** at **24% interest per annum**, repaid over **18 months**.

Let Un be the amount owing after n months, U0 is = 500

Un = Un-1 + 2%Un-1
    = Un-1 + 0.02Un-1 - C
	= 1.02Un-1 - C

Solution
$$
U_n = k^n U_0 + \frac{c(k^n - 1)}{k - 1}
$$
$$
U_n = 1.02^n 500 - \frac{c(1.02^n - 1)}{0.02}
$$
$$
U_n = 1.02^n 500 - 50c(1.02^n - 1)
$$
at n = 18, U18 = 0 
$$
0 = 1.02^{18} 500 - 50c(1.02^{18} - 1)
$$
c = 33.35
ooo