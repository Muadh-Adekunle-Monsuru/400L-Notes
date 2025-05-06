
Features of modelling a system
- System 
- Event
- Entity
- State
- Input 
- Output


---

### **Module Overview**
The module consists of six units:
1. Basics of Modelling and Simulation
2. Random Numbers
3. Random Number Generation
4. Monte Carlo Method
5. Statistical Distribution Functions
6. Common Probability Distributions

---

### **Unit 1: Basics of Modelling and Simulation**

#### **1. Introduction**
- Human decision-making is often clouded by uncertainty and imprecision.
- **Simulation** helps in evaluating and optimizing alternatives when direct testing is impractical or expensive.
- It's especially valuable for systems with complex interactions or delayed consequences.

#### **2. Intended Learning Outcomes**
After studying this unit, students should be able to:
- Define "model" and "modelling"
- Understand when and why models are used
- Describe the modelling process
- Identify different types of models

#### **3. Main Content**

##### **Definitions**
- **Modelling:** Creating abstract representations of systems to understand or predict behavior.
- **Model:** A representation (physical, conceptual, or mathematical) of a real-world entity or process.
- **Simulation:** Using a model to study the behavior of a system over time.
- **Computer model:** A model simulated on a computer with adjustable parameters.

##### **What is Modelling and Simulation?**
- It involves understanding systems and their interactions through iterative development and testing.
- It's both a science and an art—best learned by practice.

##### **Types of Models**
1. **Physical Models:** Tangible representations (e.g., model airplanes).
2. **Mathematical Models:** Use equations to describe relationships.
3. **Analogue Models:** Use physical or electrical analogs (e.g., gauges).
4. **Simulation Models:** Use sequences of random numbers to emulate real systems.
5. **Heuristic Models:** Rule-of-thumb-based, often intuitive.
6. **Deterministic Models:** Fixed inputs, no randomness.
7. **Stochastic Models:** Include variables subject to probability.

##### **Advantages of Using Models**
- Safer and cheaper than real-world testing
- Easier to control and manipulate
- Useful for training (e.g., flight simulators)

##### **Applications**
- Used in various fields from concept development to analysis and training.

##### **Modelling Procedure**
1. Examine the real-world situation.
2. Extract essential features.
3. Construct a model.
4. Solve and experiment.
5. Draw conclusions.
6. Refine if necessary.
7. Implement the model.

---

#### **4. Self-Assessment Questions**
- Define and differentiate between model, modelling, simulation, and computer model.
- List the steps in the modelling process.
- Explain the reasons for using models.

---

#### **5. Conclusion**
The unit offers an overview of fundamental modelling concepts to prepare students for deeper exploration into simulation techniques.


---

Congrumental
INT(RND x N + 1 - P) + P

Generate a random number between 1-6
INT(RND x 6) +1

1. Uniform Distribution as nearly as possible



---

## ✅ **Unit 3: Congruential Random Number Generator**

---

### 🧩 **1. Introduction**

* Random number generation is essential in simulations.
* When no built-in RNG is available, developers must implement one manually.
* Classical RNGs have short periods and low uniformity.
* Modern congruential generators offer longer periods and better uniformity.

---

### 🎯 **2. Intended Learning Outcomes**

By the end of this unit, you should be able to:

* Explain the Congruential Method of random number generation.
* Select suitable parameters (`a`, `c`, `m`) for implementation.
* Translate the methods into working code.
* Understand alternative methods: Mid-square, Mid-product, and Fibonacci.

---

### 📚 **3. Main Content**

#### ✅ 3.1 **Congruential Method**

* Based on **modulo arithmetic**:
  `Xn+1 = (aXn + c) mod m`

  * `X0`: Seed (initial value)
  * `a, c, m`: Carefully selected constants
* Types:

  * **Mixed Congruential Method**: `c ≠ 0`
  * **Multiplicative Method**: `c = 0`

**Example:**
Using `a=5`, `c=7`, `m=8`, `X0=4`:

```
X1 = (5×4 + 7) mod 8 = 3
X2 = (5×3 + 7) mod 8 = 6
...
X8 = 4 → cycle repeats
```

To scale to a desired range `[p, m]`:
`Xn+1 = ((aXn + c) mod (m + 1 - p)) + p`

#### ⚙️ Example QBASIC Function:

```basic
FUNCTION RAND (SEED)
CONST M = 32767, A = 2743, C = 5923
IF SEED < 0 THEN SEED = SEED + M
SEED = (A * SEED + C) MOD M
RAND = SEED / M
END FUNCTION
```

#### 📌 Example Program: Generate 20 integers between 1–64

```basic
DECLARE FUNCTION RAND(X)
DIM SHARED SEED
SEED = TIMER
FOR K% = 1 TO 20
  SEED = RAND(SEED)
  PRINT SEED
NEXT K%
FUNCTION RAND (SEED)
CONST M = 64, A = 27, C = 13
IF SEED < 0 THEN SEED = SEED + M
SEED = (A * SEED + C) MOD M + 1
RAND = SEED
END FUNCTION
```

---

#### ⚙️ 3.2 **Choosing a, c, and m**

* Based on **Knuth’s Rules** for full period:

  * `a` and `c` must be carefully chosen.
  * For **m**:

    * If prime, `c` can be 0.
    * Conditions for full period:

      * `c` and `m` are relatively prime.
      * If `q` divides `m`, then `q` divides `a-1`.
      * If `4` divides `m`, then `4` divides `a-1`.

---

#### 🎲 3.3 **RANECU Generator (FORTRAN)**

* Combines 3 multiplicative congruential generators.
* Suitable for 16-bit computers.
* Period > 8×10¹²
* Uses 3 seed values with constraints.

**Core Algorithm Logic:**

```fortran
ISEED1 = 157*(ISEED1 - K*206) - K*21
ISEED2 = 146*(ISEED2 - K*217) - K*45
ISEED3 = 142*(ISEED3 - K*222) - K*133
...
IZ = (ISEED1 - ISEED2 + ISEED3) mod 32362
```

---

#### 🧮 3.4 **Other Random Number Generators**

| **Method**                 | **Formula**                   | **Comments**                   |
| -------------------------- | ----------------------------- | ------------------------------ |
| **Quadratic Congruential** | `Xn+1 = (dX² + cX + a) mod m` | `m` should be a power of 2     |
| **Mid-square**             | `Xn+1 = middle_digits(Xn²)`   | Tends to degenerate, slow      |
| **Mid-product**            | `Xn+1 = middle_digits(cXn)`   | Better than mid-square         |
| **Fibonacci**              | `Xn+1 = (Xn + Xn-1) mod m`    | Needs 2 seeds, poor randomness |

> ⚠️ These are mainly **of historical interest** and not suitable for modern simulation tasks.

---

### ✍️ **4. Self-Assessment Exercises**

1. Write a QBASIC program using **Quadratic Congruential Method** for 15 integers (1–50).
2. Use **Multiplicative Method** with `a=5`, `m=8`, `X0=4` and analyze the results.
3. Create a **Mixed Congruential QBASIC function** for random numbers between 30–100.
4. Generate the following sequences:

   * a. `Xn+1 ≡ (Xn + 3) mod 10`, `X0 = 2` (10 values)
   * b. `Xn+1 ≡ (5Xn + 1) mod 8`, `X0 = 4` (8 values)
   * c. `Xn+1 ≡ (61Xn + 27) mod 100`, `X0 = 40` (two-digit numbers)
   * d. `Xn+1 ≡ (21Xn + 53) mod 100`, `X0 = 33` (five-digit numbers)

---

### 📌 **Conclusion**

* Congruential methods form the backbone of many pseudo-random number generators.
* Careful selection of constants leads to long periods and good randomness.
* Understanding different methods helps in choosing the right one for simulations.

---

### 🧾 **Summary**

* **Congruential methods** are practical, mathematical ways to generate pseudo-random numbers.
* The **Mixed and Multiplicative** methods are most commonly used.
* **Parameter selection** is crucial for effectiveness.
* **Other methods** (mid-square, Fibonacci) are outdated and rarely used today.

---

Would you like this formatted as a printable PDF or a PowerPoint slide summary?
