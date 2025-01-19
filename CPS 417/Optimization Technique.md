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


**Genetic Algorithm:**
It is a non-traditional optimization method based on the mechanics of natural genetics and natural selection. They are now mostly used in solving engineering optimization problems because of its wide range of precise search and capability of solving complex non-linear problems



Basic Steps/Term in GA
- Working Principles: Unlike many method GA use probabilistic transition rules to guide their search, the method is not a simple random search or is not a decision making tool depending on the simple probability act just like a toss of a coin. GA use random choice as a tool to guide a search toward regions of the search space with likely improvements 
- Initialization: Referring to the maximization problem a set of binary strings representing the variable $x_i$ are generated at random to make the initial population. The string in GA corresponds to chromosomes and bits in a string refers to genes in natural genetics
- Fitness Function: Every member string in a population is judged by the functional value of the fitness function. As GA follows the rule of survival of fittest candidate in nature to make a search process so the algorithm is naturally suitable for  solving maximization problems. Maximization problems are usually transformed into minimization problem by some suitable transformation.
- Genetic Operators: With an initial population of individuals of various fitness values the operators of GA begin to generate a new and improve population from the old one. A simple GA (SGA) consists of 3 basic operations
	- **Reproduction:** Usually the first operator applied on a population. This selects string according the fitness values in a population and forms a mating pool, selecting strings according to their fitness values means that  strings with a higher value have a higher probability of contributing one or more off-springs to the next generation
	- **Crossover:** In reproduction, good strings in a population are probabilistically assigned a larger number of couples and a mating pool is formed. But no new strings are formed in the reproduction phase. In the crossover operator, new strings are created by exchanging information among strings of the mating pool. Many crossover operators exist in the GA literature. In most crossover operators two strings are picked from the mating pool at random and some portions of the strings are exchanged between the string. 
	- **Mutation**: A crossover operator is mainly responsible for the search of new strings even though a mutation operator is also used for this purpose. The mutation operator changes 1 to 0 and vice versa in a bit position with a small mutation probability $P_m$ . Changing bits with probability $Pm$ can be simulated by choosing a number between 0 to 1 at random if the random number is smaller than $P_m$ the randomly selected bit is altered otherwise the bit is kept unchanged. The need for mutation is to create a point in the neighborhood of the current point, thereby achieving a local search around the current solution.
	Through these operation a new population of point is evaluated. the population is iteratively operated by the above be those three operations. One cycle of these operations and subsequent evaluation procedure is known as **generation** in GA

Advantages of GA:
As seen from the above description of the working principles of genetic algorithms they are radically different from most of the traditional optimization methods.
GA work with a string coding of variables instead of the variables. The advantage of working with a coding of variables is that the coding dispitices  the search space, even though the function may be continuous. On the other hand since GA require only function values at various discreet points a discreet or continuous function can be handled with no extra cost. This allows GA to be applied to a wide variety of problems. Another advantage is that GA operators exploits the similarities in string structures to make an effective search.


Modified GA:
Some phenomena in the natural genetic system are emulated in fitness function evaluation and crossover operation in other to improve the efficiency of conventional GA. This includes the concept of aging of individuals and ancestors influence for computing the fitness value of individuals and genotypic and phenotypic similarity for determining pairs undergoing crossover operation

**Aging of individuals**:
In the conventional GA once a particular solution becomes more fit it goes on getting chances to produce offspring until the end of the algorithm, if a proportional payoff is used thereby increasing the chance of generating similar type of offspring and loosing diversity very fast more fit individuals do not normally die, but only the less fit ones die.

**Incorporation on ancestors influence**
As it is well known in GA in each generation or iteration the objective function determines the suitability of each individuals based on this some of them, called parent individuals are selected for reproduction, number of copies reproduced by an individual parent is expected to be directly proportional to its fitness value, hence the performance of a GA depends on the fitness evaluation to a large extent

Simulated Annealing (SA)
This is another non-traditional search and optimization technique which is becoming popular in engineering optimization problem. But the solution of combinatorial optimization problem SA is very suitable and powerful search technique. The SA resembles the cooling process of molten metals through annealing as the high temperature the atoms of the molten metals can move freely with respect to each other but as the temperature is being reduced the movement of the atoms get restricted, the atoms start to get ordered and finally form crystals having the minimum possible energy. 