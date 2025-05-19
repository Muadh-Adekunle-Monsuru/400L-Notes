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

Difference Equation
Predict the outcome of a variable using a previsouly given variable. If model is  time dependent it is called dynamic, while if a model is independent of time it is called a static model. 

A difference equation is an equation expressing the value of a quantity Q, in terms of previous values of Q