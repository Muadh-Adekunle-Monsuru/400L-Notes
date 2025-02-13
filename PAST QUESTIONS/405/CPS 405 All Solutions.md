==Trust at your own risk, these pqs do not look like they were made by Dr A.😵☠️💀==

---

![[2025 Test.jpeg]]


**1. Six Classifications of Artificial Intelligence:**
- **AI tools**: 
	- Comprises of computer languages, models, database, management, decisions theory and cognitive programming. 
- **Learning & Induction**:
	- Includes heuristics, strategy to solve problems, reasoning and inferences. Most techniques used for developing AI falls into learning an induction category 
- **Perception & Data Acquisition:**
	- It comprises of the knowledge of visual and sound recognition by computer device.
- **Robotics:** 
	- These are machines that imitates human beings and can recognize objects, manipulates then and are usually mobile. 
- **Understanding & Communications:** 
	- This include knowledge, understanding written and oral languages. It also includes the act of learning and translation. 
- **Problem-solving & model building**: 
	- This class comprises of generation of solutions, analysis, searching and decision making. 

**2. Comparison between Natural and Artificial Intelligence:**

| Feature | Natural Intelligence (Human) | Artificial Intelligence |
|---|---|---|
| **Origin** | Biological | Man-made |
| **Learning** | Experience-based, slow | Data-driven, fast |
| **Creativity** | High, intuitive | Limited, based on algorithms |
| **Adaptability** | Flexible, broad | Specific, programmed |
| **Consciousness** | Present | Absent (currently) |
| **Processing** | Parallel, distributed | Sequential, centralized |

**3. Eight Specific Characteristics of Artificial Intelligence:**
1. **Learning from Experience:** AI systems can be programmed to learn from past data and experiences, similar to how humans learn from trial and error.  This allows them to improve performance over time.

2. **Handling Complex Situations:** AI aims to create systems capable of addressing intricate and challenging problems, even those involving incomplete or ambiguous information, much like human experts do.

3. **Applying Learned Knowledge:**  AI systems should be able to transfer and apply knowledge gained in one context to new and different situations, mirroring human adaptability.

4. **Problem-Solving with Incomplete Information:** AI can be designed to make decisions and solve problems even when crucial information is missing or uncertain, a common challenge in real-world scenarios.

5. **Identifying Important Information:** AI systems can be developed to filter out irrelevant data and recognize key pieces of information, enabling more effective decision-making.

6. **Human-Like Reasoning:** AI seeks to replicate human logical thinking and reasoning processes, allowing systems to draw valid conclusions from available information.

7. **Rapid Situational Assessment:** AI can be programmed to quickly and accurately analyze situations and react appropriately, similar to human reflexes and instincts.

8. **Visual Understanding and Perception:** AI aims to enable computers to interpret and understand visual inputs, allowing them to "see" and make sense of images and scenes, just as humans do.

**4. Knowledge-Based System Tools:**

* **i. Induction Systems:**
	These constitutes a simple way of creating a  limited knowledge based system.  The induction technology was derived from work aimed at getting systems to learn from examples. Specifically an induction system takes a set of examples and converts it into a decision tree or decision maker.
    * Example: Decision tree learning.

* **ii. Rule-Based Systems:**
	Uses facts, rules and a forward or backward chaining influence engine to infer knowledge about situations and make recommendations or decisions.
    * Example: Medical diagnosis systems.

* **iii. Hybrid Systems:**
	An HS adds objects, inheritance and message parsing to rule based system, the combination results in much more powerful tools and store elaborate problem decisions in object hierarchies and use rules to make influences as needed.
    * Example: Natural language processing systems.

**5. AI Techniques:**
 **i. Search:**
    * Exploring possible solutions to find the best one.
    * Algorithms like breadth-first search, depth-first search, A* search.
    * Used in game playing, route planning.

 **ii. Use of Knowledge:**
	AI provides a way of solving complex problems by exploiting the structure of the objects in which they are involved. 
    * Essential for expert systems, reasoning, and planning.

 **iii. Abstraction:**
	    AI systems separate critical information from irrelevant details, simplifying complex data. 
    * Used in planning, problem-solving, and machine learning.

**6. Three Steps to Build a System to Solve a Problem:**
1. **Define the problem**: Clearly specify the initial and desired final situations.  
2. **Analyze the problem**: Identify key features that influence solution techniques.  
3. **Choose and apply a technique**: Select the best approach and implement it.  



---

![[PAST QUESTIONS/405/2024_1.jpeg]]
---

### **Question 1**  
#### **(a) Define a notation for the state of this agent. How many distinct non-terminal states are there?**  

**Understanding the Problem**

The agent starts at position 2 (S). The goal is to reach all three positions 1, 3, and 4 (containing G1, G2, and G3 respectively). The search ends when all three goals are reached. We need to find the number of distinct *non-terminal* states. A non-terminal state is one where the agent hasn't yet reached all three goals.

**Defining the State**

The solution defines a state as a pair (P, G):

* **P:** Represents the current position of the agent (1, 2, 3, or 4).
* **G:** Represents the set of goals that have been reached so far. This can be any combination of G1, G2, and G3, including the empty set (∅) if no goals have been reached yet.

**Counting the States**

The solution uses a clever way to count the possible states:

1. **Starting Point (No Goals Reached):**
   - The agent starts at position 2, and no goals are reached (G = ∅). This gives us 1 state: (2, ∅).

2. **After Reaching G1:**
   - The agent can be at position 1 (G1 reached) or back at position 2 (still only G1 reached). 
   - So, we have 2 possible positions: 1 and 2. 
   - For each position, the reached goals are {G1}.
   - This gives us 2 states: (1, {G1}) and (2, {G1}).

3. **After Reaching G1 and G2:**
   - The agent can be at positions 1, 2, or 3. 
   - The reached goals are {G1, G2}.
   - This gives us 3 states: (1, {G1, G2}), (2, {G1, G2}), and (3, {G1, G2}).

4. **Generalizing the Pattern**
   - The solution observes a pattern:
     - When no goals are reached, there's only 1 possible position (2).
     - When G1 is reached, there are 2 possible positions (1 and 2).
     - When G1 and G2 are reached, there are 3 possible positions (1, 2, and 3).

   - This can be generalized as:
     - For reaching 0 goals, there is 1 reachable position.
     - For reaching 1 goal, there are 2 reachable positions.
     - For reaching 2 goals, there are 3 reachable positions.

5. **Calculating the Total Non-Terminal States**
   - The solution uses combinations to calculate the number of states for each stage:
     - 0 goals reached: 1 position (1 way to choose 0 goals out of 3) = 1 * 1 = 1 state
     - 1 goal reached: 2 positions (3 ways to choose 1 goal out of 3) = 2 * 3 = 6 states
     - 2 goals reached: 3 positions (3 ways to choose 2 goals out of 3) = 3 * 3 = 9 states

   - Total non-terminal states = 1 + 6 + 9 = 16

**Therefore, there are 16 distinct non-terminal states.**


#### **(b) Draw a search tree out to a depth of 3 moves, including repeated states. Circle repeated states.**  
**Understanding the Search Tree**

A search tree represents the exploration of possible paths in a problem space. In this case:

* **Nodes:** Each node in the tree represents a state (P, G), where P is the agent's position and G is the set of goals reached.
* **Branches:**  Each branch represents a move the agent makes from one position to another.
* **Depth:** The depth of the tree represents the number of moves made.

**Building the Search Tree (Depth 3)**

1. **Root Node (Start):** The root of the tree is the initial state (2, ∅) - position 2, no goals reached.

2. **Depth 1 (First Move):**
   - From position 2, the agent can move to 1, 3, or 4.
   - This leads to three branches and three new states:
     - (1, {G1}) - Moved to 1, G1 is reached.
     - (3, {G2}) - Moved to 3, G2 is reached.
     - (4, {G3}) - Moved to 4, G3 is reached.

3. **Depth 2 (Second Move):**
   - From each of the states at depth 1, the agent has new move options:
     - From (1, {G1}): Can move to 2, leading to (2, {G1}).
     - From (3, {G2}): Can move to 2, leading to (2, {G2}).
     - From (4, {G3}): Can move to 2, leading to (2, {G3}).

4. **Depth 3 (Third Move):**
   - Again, from each state at depth 2, the agent explores possible moves:
     - From (2, {G1}): Can move to 1, 3, or 4, leading to (1, {G1}), (3, {G1, G2}), (4, {G1, G3}).
     - From (2, {G2}): Can move to 1, 3, or 4, leading to (1, {G1, G2}), (3, {G2}), (4, {G2, G3}).
     - From (2, {G3}): Can move to 1, 3, or 4, leading to (1, {G1, G3}), (3, {G2, G3}), (4, {G3}).

**Identifying Repeated States**

The solution correctly identifies the following repeated states at depth 3:

* **(1, {G1})** - This state was already reached at depth 1.
* **(3, {G2})** - This state was already reached at depth 1.
* **(4, {G3})** - This state was already reached at depth 1.

**Why are these states repeated?**

The search tree shows the different *paths* to reach certain states, not just the states themselves. Even though the agent might reach the same "state" (position and goals achieved) through different sequences of moves, the search tree explicitly shows these different paths.


#### **(ii) Give the meaning of the acronym IDLE and Discuss it.**  
**IDLE (Integrated Development and Learning Environment)** is the default **Python IDE**. It features:
  - Interactive shell for testing code snippets.
  - Code editor with syntax highlighting and indentation support.
  - Debugger for identifying and resolving errors.
  - File handling for creating and managing scripts.
  - Autocomplete and code suggestions help documentation access.
  - Help and Documentation: IDLE allows users to access Python documentation and help directly from the interface
### **Question 2**  
#### **(i) Discuss planning.**  
Planning is a fundamental process in **Artificial Intelligence (AI)** used to determine a **sequence of actions** that lead to a desired goal. It involves:  
- **Goal Formulation**: Defining what needs to be achieved.  
- **State Space Representation**: Defining states and actions.  
- **Plan Generation**: Finding the best sequence of actions.  
- **Execution & Monitoring**: Applying and modifying plans as needed.  

Planning is essential for **robotics, logistics, game AI, and decision-making systems**.

#### **(ii) What are the features of an ideal planner?**  
An ideal planner should have:  
1. **Completeness** – It should find a solution if one exists.  
2. **Optimality** – It should find the best solution.  
3. **Efficiency** – It should minimize computational cost.  
4. **Flexibility** – It should adapt to dynamic environments.  
5. **Scalability** – It should handle large problem spaces.  

#### **(iii) What are the different types of planning?**  
1. **Classical Planning** – Assumes a fully known environment.  
2. **Hierarchical Planning** – Breaks tasks into sub-tasks.  
3. **Conditional Planning** – Plans for uncertainties with different contingencies.  
4. **Probabilistic Planning** – Handles probabilistic outcomes.  
5. **Real-time Planning** – Used in dynamic environments (e.g., robotics).  

### **Question 3**  
#### **(i) What is the difference between NLP and NLU?**  
- **Natural Language Processing (NLP)** refers to techniques for processing human language (e.g., translation, speech recognition).  
- **Natural Language Understanding (NLU)** focuses on **comprehension**—extracting meaning, sentiment, and intent from text.  
- **NLP includes both NLU and Natural Language Generation (NLG).**

#### **(ii) What are the components of NLP?**  
1. **Lexical Analysis** – Tokenization, stemming.  
2. **Syntactic Analysis** – Parsing, sentence structure.  
3. **Semantic Analysis** – Understanding meaning.  
4. **Pragmatic Analysis** – Understanding context.  
5. **Morphological Analysis** – Word structure analysis.  
6. **Discourse Integration** – Coherence in multiple sentences.  

---
![[PAST QUESTIONS/405/2024_2.jpeg]]

### **Question 4**  
#### **(i) What is the CSP search algorithm?**  
A **Constraint Satisfaction Problem (CSP) search algorithm** is a method used to find solutions to problems defined by variables, domains, and constraints. The algorithm explores possible variable assignments while ensuring all constraints are satisfied. Common CSP search techniques include:  
- **Backtracking Search**: A depth-first search that assigns values and backtracks when a conflict arises.  
- **Forward Checking**: Eliminates inconsistent values from domains before assigning variables.  
- **Arc Consistency (AC-3)**: Ensures that every variable in a binary constraint has consistent values.  
- **Constraint Propagation**: Uses inference to reduce the search space.  

#### **(ii) Why is it a good heuristic to choose the variable that is most constrained but the value that is the least constraining in a CSP search?**  
Using the **Most Constrained Variable (MCV) Heuristic**, also known as the **Minimum Remaining Values (MRV) heuristic**, helps reduce the search space by selecting the variable with the fewest legal values first. This reduces the likelihood of conflicts and failure early.  

Choosing the **Least Constraining Value (LCV)** means selecting a value that **leaves the most options open** for future variables. This helps in **avoiding dead-ends** and increases the chances of finding a solution faster.  

This combination improves efficiency by prioritizing decisions that maximize flexibility and minimize constraint violations.  

### **Question 5**  
#### **(i) Why is Python popular, and why does it matter?**  
Python's popularity stems from several factors:

- **Ease of Learning and Use**: Its straightforward and readable syntax allows developers to express ideas with fewer lines of code, minimizing errors and debugging time.
- **Versatility**: Python is a general-purpose language used in various fields, including web development, data science, artificial intelligence, and more.
- **Large Community**: A thriving community provides access to resources, libraries, and support through forums and tutorials.
- **High Job Demand**: Python is in demand due to its widespread adoption by tech companies and startups.
- **Adoption in Cutting-Edge Technologies**: Python powers innovations in AI, machine learning, and automation using libraries like TensorFlow and PyTorch.
#### **(ii) Write a program to display all duplicate items from the list given below:**  
**Given list:**  
```python
sample_list = [10, 20, 60, 30, 20, 40, 30, 60, 70, 80]
```
**Python Code:**  
```python
from collections import Counter

sample_list = [10, 20, 60, 30, 20, 40, 30, 60, 70, 80]
count_dict = Counter(sample_list)  

duplicates = [key for key, value in count_dict.items() if value > 1]
print(duplicates)
```
**Output:**  
```plaintext
[20, 60, 30]
```
This code uses `Counter` to count occurrences and filters items appearing more than once.


#### **(iii) Write a filter dictionary to contain keys present in the given list.**  
**Given dictionary:**  
```python
d1 = {'A': 65, 'B': 66, 'C': 67, 'D': 68, 'E': 69, 'F': 70}
l1 = ['A', 'C', 'F']
```
**Python Code:**  
```python
filtered_dict = {key: d1[key] for key in l1 if key in d1}
print(filtered_dict)
```
**Output:**  
```plaintext
{'A': 65, 'C': 67, 'F': 70}
```
This code **filters `d1`** to keep only keys present in `l1`.

---
![[405_1 2023.jpeg]]


**Question 1**

**1b) Scenarios**

**(i) Supervised Learning:**

* **Scenario:** A hospital wants to predict the likelihood of patients developing diabetes based on their medical history (age, BMI, blood pressure, etc.). They have a dataset of patients with known diagnoses (diabetes/no diabetes).
* **Application:** Use a classification algorithm (like logistic regression or a decision tree) to train a model on the labeled data. The model can then predict diabetes risk for new patients based on their features.

**(ii) Unsupervised Learning:**

* **Scenario:** A marketing company wants to segment its customers into different groups based on their purchasing behavior. They have data on customer purchases but no pre-defined labels for the segments.
* **Application:** Use a clustering algorithm (like k-means) to group customers based on similarities in their purchase patterns. This allows the company to target each segment with personalized marketing campaigns.

**(iii) Reinforcement Learning:**

* **Scenario:** A game developer wants to create an AI agent that can play a new video game. The agent needs to learn the game's rules and strategy through trial and error.
* **Application:** Use reinforcement learning where the agent receives rewards for making progress in the game (e.g., scoring points) and penalties for mistakes. Over time, the agent learns to maximize its rewards and improve its gameplay.

**1c) AI in the Computer Industry in Nigeria**

1. **Cybersecurity:** AI can be used to detect and prevent cyberattacks by analyzing network traffic and identifying suspicious patterns. This is crucial for protecting sensitive data and infrastructure.
2. **Customer Service:** AI-powered chatbots can handle routine customer inquiries, freeing up human agents to deal with more complex issues. This can improve efficiency and customer satisfaction.
3. **Software Development:** AI can assist in code generation, bug detection, and testing, making the development process faster and more efficient. AI-driven tools can also help developers write higher-quality code.

**Question 2**

**2a) AI Agent Definition**

From an AI perspective, an **agent** is an entity that perceives its environment through sensors and acts upon that environment through actuators. The agent's actions are chosen to maximize its chances of achieving its goals.

**2b) Agent Types**

1. **Reflex Agent:** Acts based on pre-defined rules or reflexes, reacting to immediate stimuli without considering the past or future.
   * **Example:** A thermostat that turns on the heating when the temperature drops below a set point.
2. **Learning Agent:**  Improves its performance over time by learning from its experiences. It uses feedback to adjust its actions and make better decisions in the future.
   * **Example:** A spam filter that learns to identify spam emails based on user feedback (marking emails as spam or not spam).

**2c) Rational Agent Definition**

A **rational agent** is an agent that acts in a way that is expected to maximize its performance measure, given its percepts (observations), knowledge, and available actions. It chooses the best action among the available options, considering the potential consequences.

**2d) Rational Agent Scenarios**

1. **Medical Diagnosis:** A diagnostic system that uses AI to analyze patient symptoms and medical history to suggest the most likely diagnosis and treatment plan. It aims to maximize the chances of a correct diagnosis and effective treatment.
2. **Financial Trading:** A trading bot that uses AI to analyze market data and make trading decisions with the goal of maximizing profits while minimizing risk.

**Question 3**

**PEAS Analysis for Automated Taxi**

* **Performance Measure:**
    * Safety (minimize accidents)
    * Efficiency (fast travel time, optimal routes)
    * Passenger comfort
    * Profitability (maximize fares, minimize operating costs)
    * Adherence to traffic laws
* **Environment:**
    * Roads, traffic conditions
    * Weather conditions
    * Passengers (destinations, preferences)
    * Other vehicles and pedestrians
    * Traffic signals and signs
* **Actuators:**
    * Steering wheel
    * Accelerator and brakes
    * Communication systems (for interacting with passengers and traffic control)
    * Navigation system
* **Sensors:**
    * Cameras (for object detection and lane keeping)
    * GPS (for location and navigation)
    * Radar and lidar (for detecting obstacles)
    * Speedometers and odometers
    * Microphones (for passenger interaction)

**Question 4**

**4a) Conditions for Intelligent Action**

1. **Perception:** The ability to perceive and understand the environment through sensors.
2. **Learning:** The ability to learn from experience and improve performance over time.
3. **Reasoning:** The ability to reason about the world, make inferences, and solve problems.

**4b) Goals of AI**
- **Search & Problem Solving**: 
	-  AI can explore multiple solutions for problems that lack a straightforward answer,  often finding optimal paths quickly.. 
- **Use of knowledge:** 
	- AI provides a way of solving complex problems by exploiting the structure of the objects in which they are involved. 
- **Abstraction & focus:** 
	-  AI systems separate critical information from irrelevant details, simplifying complex data. 

**4c) Robot Movement Program (Conceptual)**

```
// Assuming basic movement commands: moveForward(), moveBackward(), turnLeft(), turnRight()

function moveToSpecificDirections(directions) {
  for (direction in directions) {
    if (direction == "forward") {
      moveForward();
    } else if (direction == "backward") {
      moveBackward();
    } else if (direction == "left") {
      turnLeft();
    } else if (direction == "right") {
      turnRight();
    }
  }
}

// Example usage:
let instructions = ["forward", "left", "forward", "right"];
moveToSpecificDirections(instructions);
```

**Question 5**

**5a) Controller Functions in an Agent**

* **Receiving Percepts:** Controllers receive sensory information from the agent's sensors.
* **Decision Making:** They process the sensory input and make decisions about which actions to take.
* **Executing Actions:** They send commands to the agent's actuators to carry out the chosen actions.

**5b) Components of a Learning Problem**

1. **Task:** The specific problem that the agent is trying to solve (e.g., playing a game, classifying images).
2. **Data:** The information that the agent uses to learn (e.g., labeled examples, sensor data).
3. **Model:** The representation that the agent learns to capture the patterns in the data (e.g., a decision tree, a neural network).
4. **Learning Algorithm:** The method that the agent uses to update its model based on the data (e.g., backpropagation, reinforcement learning algorithm).

**5c) AI from Industrial Revolution Perspective**

From the perspective of the Industrial Revolution, AI can be seen as the next major technological advancement that is automating not just physical labor but also cognitive tasks. Just as machines replaced manual labor in the Industrial Revolution, AI is poised to automate intellectual work, leading to increased efficiency and productivity.

**5d) Achievements of AI**

1. **Machine Learning:** Development of algorithms that allow computers to learn from data without explicit programming.
2. **Natural Language Processing:** Enabling computers to understand and generate human language.
3. **Computer Vision:** Enabling computers to "see" and interpret images and videos.
4. **Robotics:** Creating robots that can perform complex tasks in various environments.

---
![[405_1 2020.jpeg]]


**Question 1**

**(a) Intelligence in Drone Technology for War (10 marks)**

Improving drone intelligence can significantly reduce human casualties in warfare through:

* **Autonomous Target Recognition:** Drones can be equipped with AI-powered computer vision to automatically identify and classify targets (military vehicles, enemy combatants) with high accuracy, minimizing risks to civilians.
* **Precision Strikes:** AI algorithms can optimize flight paths and weapon deployment for precise targeting, reducing collateral damage.
* **Real-time Threat Assessment:** Drones can analyze battlefield data in real-time to assess threats and adapt their strategies, preventing human errors in judgment under pressure.
* **Reduced Human Involvement:** Removing soldiers from direct combat roles reduces their exposure to danger.
* **Ethical Considerations:**  While AI can improve accuracy, ethical programming is crucial to prevent unintended harm. Clear rules of engagement and human oversight are necessary.

**(d) Utility-Based Agent Diagram (10 marks)**
![[Pasted image 20250213182316.png]]

* **Percepts:** Sensory inputs from the environment.
* **Environment:** The world the agent interacts with.
* **Agent:** The AI system making decisions.
* **State Representation:** The agent's internal understanding of the current situation.
* **Goals:** The agent's objectives or desired outcomes.
* **Utility Function:**  A measure of how desirable different states are.
* **Actions:**  Steps the agent can take to change the environment.
* **Controller:** The component that selects actions based on percepts, state, goals, and utility.
* **Actuators:**  Mechanisms for executing actions on the environment.

**(b) Goals of AI (4 marks)**

* To understand human intelligence.
* To develop intelligent systems that can perform tasks that typically require human intelligence.

**(c) Architecture of a Learning Agent (9 marks)**

```
                                      Percepts (Sensors)
                                            |
                                            V
                                   +-----------------+
                                   |    Environment   |
                                   +--------+-------+
                                            |
                                            V
                                   +-----------------+
                                   |     Agent      |
                                   |  (Controller)  |
                                   +--------+-------+
                                            |
                           +-------------------------------------+
                           |                                     |
                           V                                     V
               +-----------+-----------+            +-----------+-----------+
               |    Learning     |            |    Performance  |
               |   Element     |            |   Element     |
               +-----------+-----------+            +-----------+-----------+
                           |                                     |
                           +-------------------------------------+
                                            |
                                            V
                                   +--------+-------+
                                   |   Actions    | (Actuators)
                                   +-----------------+
```

* **Learning Element:**  Modifies the performance element based on feedback.
* **Performance Element:** Selects actions based on percepts.
* **Feedback:** Information about the success or failure of actions.

---
![[405_1 2016.jpeg]]


**Question 4**

**(b) An agent interacts with the environment through its body. Explain (9 marks)**

The agent's "body" refers to its physical embodiment (if it's a robot) or its interface with the environment (if it's a software agent).  This interaction is crucial:

* **Sensors:** The agent uses sensors (e.g., cameras, microphones, GPS) to gather information from the environment. These sensors are the agent's "eyes and ears" on the world.
* **Actuators:** The agent uses actuators (e.g., motors, wheels, software commands) to act upon the environment. These are the agent's "hands and feet" for affecting the world.
* **Feedback Loop:**  The agent's actions change the environment, and these changes are perceived by the sensors, creating a feedback loop. This loop allows the agent to learn and adapt its actions over time.
* **Situatedness:** The agent is situated within its environment. Its actions and perceptions are grounded in the specific context it's in.


**Question 6**

**(a) An agent looks into the future in four ways; briefly explain these four ways (8 marks):**

1. **Planning:** Creating a sequence of actions to achieve a goal. This involves considering the possible consequences of different action sequences.
2. **Prediction:** Estimating what will happen in the future if certain actions are taken.
3. **Lookahead:**  Exploring possible future states to evaluate the potential outcomes of different actions.
4. **Anticipation:**  Predicting the behavior of other agents or the environment.

**(b) Explain the concept of Hierarchical Robotic System Architecture (9 marks):**

Hierarchical Robotic System Architecture organizes the control of a robot into multiple layers, each with different levels of abstraction and responsibility.  Common layers include:

1. **Reactive Layer:** The lowest layer, responsible for immediate reactions to sensory input. This layer handles basic motor control and obstacle avoidance.
2. **Deliberative Layer:** The middle layer, responsible for planning and decision-making. This layer works with higher-level goals and creates plans to achieve them.
3. **Executive Layer:** The highest layer, responsible for coordinating the reactive and deliberative layers. This layer manages the overall behavior of the robot.

**Benefits of this architecture:**

* **Modularity:** Each layer can be developed and tested independently.
* **Flexibility:**  The robot can handle both reactive and planned behaviors.
* **Robustness:**  The robot can still function even if one layer fails.
* **Efficiency:**  Different tasks can be assigned to the most appropriate layer.

---
![[405_4.jpeg]]
**2a. AI Applications in the Nigerian Computer Industry (3 ways)**

1. **Cybersecurity:** AI can be used to detect and prevent cyberattacks by analyzing network traffic and identifying suspicious patterns. This is crucial for protecting sensitive data and infrastructure in Nigeria's growing digital economy.
2. **Customer Service:** AI-powered chatbots can handle routine customer inquiries, freeing up human agents to deal with more complex issues. This can improve efficiency and customer satisfaction in various sectors like banking, telecommunications, and e-commerce.
3. **Software Development:** AI can assist in code generation, bug detection, and testing, making the development process faster and more efficient. AI-driven tools can also help Nigerian developers write higher-quality code and create more sophisticated software applications.
