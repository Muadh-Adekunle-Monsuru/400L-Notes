### What is optimization:
It is the act of obtaining the best result under any give circumstance.

In most engineering design activities the design objective could be simply to minimize the cost of production or to maximize the efficiency of production. 

For example, optimization required in designing of aircraft structures for minimum weight, finding the optimal trajectory of space vehicles, designing of civil engineering structures such as frames, bridges and obtaining the optimum designing of the control system.

#### Constraints
These represent some functional relationship among the design variables and other design parameters satisfying certain physical phenomenon and certain resource limitation.

Constraint that represent limitation on the *behavior* or *performance* of the systems are termed **behavioral** or **functional** constraints. While constraints that represent *physical* limitations on design variables such as availability, transportability are known as **geometric** or **side-constraints**. 
### Type of optimization problem:
- **Constraint optimization problem**: problems which exhibits the presence of a number of constraints 
- **Unconstrained optimization problem:** These are problems which do not involve any form of constraint

### Optimization Algorithms
- Traditional method
- Non-traditional method

##### Traditional Method
These are helpful in finding the optimum solution of continuous and differentiable functions, these methods are analytical and make use of the techniques of differential calculus. It provides a good understanding of the properties of the minimum and maximum points in a functions. An example is the Newton-Raphlson method
	
**Advantages of the traditional method:**
- The convergence to an optimal solution depends on a chosen optimal solution
- Most algorithms tend to get stuck to a suboptimal solution
- The algorithms cannot be efficiently used on parallel machine
- Algorithms are not efficient in handling problems having discrete variables
- An algorithm efficient in solving one optimization problem may not be efficient in solving a different optimization problem. 

##### Non-traditional Method
This is quite a new method with rising popularity, it involves two algorithms, namely 
- Genetic algorithm
- Simulate algorithm

Genetic algorithm vs Traditional method:
- Genetic algorithms work with the coding of the parameter set not the parameters themselves
- Genetic algorithms search from a population of points and not a single point
- Genetic algorithm uses probabilistic tradition rules and not deterministic rules
- Genetic algorithms use objective based information and not derivative or other form of auxiliary knowledge. 

## **Genetic Algorithm (GA)**  
A non-traditional optimization method inspired by natural genetics and selection. It is widely used for solving complex, non-linear engineering optimization problems due to its precise search capabilities.  

---

### **Basic Steps/Terms in GA**  
1. **Working Principles**:  
   - GA uses probabilistic transition rules to guide the search, not simple random searches.  
   - It uses random choices to explore regions of the search space likely to yield improvements.  

2. **Initialization**:  
   - For maximization problems, binary strings representing variables ($x_i$) are generated randomly to create the initial population.  
   - In GA, strings correspond to chromosomes, and bits in a string are analogous to genes.  

3. **Fitness Function**:  
   - Evaluates each string in the population based on its fitness value.  
   - GA follows the "survival of the fittest" principle, making it naturally suited for maximization problems.  
   - Maximization problems can be transformed into minimization problems via suitable transformations.  

4. **Genetic Operators**:  
   - **Reproduction**:  
     Selects strings based on their fitness values to form a mating pool. Higher fitness increases the probability of producing offspring.  
   - **Crossover**:  
     Creates new strings by exchanging portions of strings in the mating pool. Two strings are selected at random, and parts are swapped to form new strings.  
   - **Mutation**:  
     Alters bits (1 → 0 or 0 → 1) with a small mutation probability ($P_m$). This introduces diversity and performs a local search around the current solution.  

   These operations iteratively produce new populations. A single cycle of operations and evaluation is called a **generation**.  

---

### **Advantages of GA**  
- Works with coded variables, enabling effective exploration of the search space, whether the function is discrete or continuous.  
- Requires only function values, making it applicable to various problems without additional costs.  
- Operators leverage string similarities for efficient searches.  

---

## **Modified GA**  
To improve efficiency, some natural genetic phenomena are emulated:  

1. **Aging of Individuals**:  
   - In conventional GA, fitter solutions dominate reproduction, reducing diversity. Aging introduces mechanisms to limit repeated reproduction of highly fit individuals, preserving diversity.  

2. **Incorporation of Ancestors' Influence**:  
   - Fitness evaluation considers not just current generation performance but also ancestral influences, enhancing performance.  
   - Genotypic and phenotypic similarities are used to determine crossover pairs.  

---

## **Simulated Annealing (SA)**  
A non-traditional search and optimization technique inspired by the annealing process of molten metals.  

- At high temperatures, atoms move freely; as the temperature decreases, their movement is restricted, forming an ordered crystal with minimal energy.  
- SA mimics this cooling process to solve combinatorial optimization problems efficiently.  

