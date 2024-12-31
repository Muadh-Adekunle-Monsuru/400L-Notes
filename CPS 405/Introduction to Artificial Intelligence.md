**Intelligence:**
Intelligence implies to choose and form an opinion, make a choice and understanding a phenomenon beyond ordinary.

**Artificial Intelligence:**
It is the art of creating a machine that performs human functions that requires knowledge and intelligence. 

**Importance of Artificial Intelligence:**
- **Search**: It provides a way of solving problems for which no more approach is available, as well as a framework into which any other direct technique that are available can be embedded and used. 
- **Use of knowledge:** AI provides a way of solving complex problems by exploiting the structure of the objects in which they are involved. 
- **Abstraction:** AI provides a way of separating important features and variations from the many unimportant ones that will otherwise overwhelm any process.

**Classification of Artificial Intelligence:**
- **AI tools**: Comprises of computer languages, models, database, management, decisions theory and cognitive programming. 
- **Learning & Induction**: Includes heuristics, strategy to solve problems, reasoning and inferences. Most techniques used for developing AI falls into learning an induction category 
- **Perception & Data Acquisition:** It comprises of the knowledge of visual and sound recognition by computer device.
- **Robotics:** These are machines that imitates human beings and can recognize objects, manipulates then and are usually mobile. 
- **Understanding & Communications:** This include knowledge, understanding written and oral languages. It also includes the act of learning and translation. 
- **Problem-solving & model building**: This class comprises of generation of solutions, analysis, searching and decision making. 


---
30-10-20
## Characteristics of AI

- **Learn from experience**: 
	Being able to learn from past situations and events is a key component of intelligent behavior, and it is a natural ability for humans who learn from trials and error. The ability must be carefully programmed into the system. For instance some artificial intelligence programs such as computerized chess games are able to play with human competitors successfully
- **Handle complex and perplexing situations**: 
	Humans are always involved in regarding difficult, global economic conditions, starvation and natural disasters in a business setting. Top-level managers and executives are usually faced with computer difficulties and challenging situation. To develop a computer system that can handle perplexing situations require careful planning and elaborate intelligence in computer programming
- **Applied knowledge acquired from experience:**
	In addition to learning from experience, people apply what they have learned to new settings or circumstance. In a number of cases industries have taken the intelligence they have learned from an existing industry and apply in other to solve their own challenge. 
- **Solve problem when important information is missing**:
	We all have to make decisions when we have missing or inaccurate information, there are a number of cases in which computers have to respond to human commands which does not compute due to insufficient information. AI systems can make important calculations, comparison and decision under condition of missing information. 
- **Determining what is important**:
	Knowing what is truly important is a mark of a good decision maker, for instance in the analysis of data, filtering out what is unnecessary, determining which items are crucial and important can make the difference between good decisions and those that will ultimately lead to problems or failures. Developing programs and approaches to allow computer machines and systems to identify important information is not a simple task, because computers do not have this natural ability.  
- **Ability to reason and think like a human**: 
	Although people do not always use a logical approach developing computer systems that can reach logical conclusions from information available is a much complex task. For example assembling a block of puzzle can be extremely difficult even for sophisticated computers without artificial intelligence. 
- **Reading quickly and correctly to a situation:** A small child for example can look over a edge or a drop off and knows not to move too close doing so the child is reacting quickly and correctly to a situation. Computers on the other-hand do not naturally have this ability without complex programming in artificial intelligence.
- **Understanding visual images and perceptive systems:** Interpreting visual images can be extremely difficult even for sophisticated computers without AI, unlike when human can look at an object  and understand what exactly is going on. For example, we can see a man sitting on a table and know that he has legs and hands which computers cannot do without intelligence. 

#### Knowledge-Based System Tools:
- **Induction system**: These constitutes a simple way of creating a  limited knowledge based system.  The induction technology was derived from work aimed at getting systems to learn from examples. Specifically an induction system takes a set of examples and converts it into a decision tree or decision maker.
- **Rule-based system**: Uses facts, rules and a forward or backward chaining influence engine to infer knowledge about situations and make recommendations or decisions.
- **Hybrid System**: An HS adds objects, inheritance and message parsing to rule based system, the combination results in much more powerful tools and store elaborate problem decisions in object hierarchies and use rules to make influences as needed.

---
20/11/2024
### Intelligent Agents

An **intelligent agent** perceives its environment using sensors and acts upon it through effectors or actuators. For humans, intelligent agents include body parts like eyes, ears, nose, legs, and mouth. In robotics, examples of agents are cameras, infrared sensors, and motors.

---

### Structure of an Intelligent Agent

The structure of an intelligent agent is defined as:  
**Agent = Architecture + Program**  

- **Agent Program**: A function that maps perceptions to actions. AI focuses on designing this program.  
- **Architecture**: Can be a standard computer or specialized hardware, possibly with software layers insulating the raw hardware from the agent program.  

---

### Steps to Build an Intelligent System

1. **Define the problem**: Clearly specify the initial and desired final situations.  
2. **Analyze the problem**: Identify key features that influence solution techniques.  
3. **Choose and apply a technique**: Select the best approach and implement it.  

---

### Problem Formulation

Problem formulation involves defining the actions and states needed to achieve a goal. Steps include:  
1. Define a **state space** of all possible configurations of the objects involved.  
2. Specify an **initial state**, the starting point of the problem-solving process.  
3. Define a **goal state**, representing the desired solution.  
4. Develop a set of **rules** for valid actions within the system.

---

Here’s an expanded and detailed version with explanations and examples:

---

### Route-Finding Problem

**Reference:** [Lecture Notes on Search Strategies](https://users.sussex.ac.uk/~christ/crs/kr-ist/lec01b.html)

---

### **Search Strategies**  

Route-finding problems are common in fields like artificial intelligence and computer science, where the goal is to navigate from a starting point to a destination efficiently. Two fundamental search strategies used in such problems are **Depth-First Search (DFS)** and **Breadth-First Search (BFS)**.

---

#### **1. Depth-First Search (DFS)**  
DFS explores as deeply as possible into the search tree before backtracking to explore other branches.  

**Key Characteristics:**  
- Prioritizes depth over breadth.  
- Uses a **stack** (either explicitly or via recursion) to keep track of the current path.  

**Advantages:**  
- Low memory usage compared to BFS (space complexity depends on the maximum depth, not the breadth).  
- May find a solution faster in problems where solutions are located deeper in the tree.  

**Disadvantages:**  
- May get stuck in infinite loops if the search space is infinite and no mechanisms (like visited states) are used.  
- Not guaranteed to find the shortest path in unweighted graphs.  

**Performance:**  
- **Time Complexity:** $O(b^d)$, where $b$ is the branching factor (average number of children per node) and $d$ is the depth of the solution.  
- **Space Complexity:** $O(b \cdot m)$, where $m$ is the maximum depth of the tree.

**Example:**  
Suppose we want to find a path from **A** to **F** in the following graph:

```
         A
        / \
       B   C
      / \   \
     D   E   F
```

Using DFS:  
1. Start at \( A \).  
2. Explore \( B \) → \( D \) (depth-first).  
3. Backtrack to \( B \) and explore \( E \).  
4. Backtrack to \( A \), then explore \( C \) → \( F \).  

DFS Path: $A \to B \to D \to E \to C \to F$.  
The solution $A \to C \to F$ is found, but not necessarily in the shortest path order.

---

#### **2. Breadth-First Search (BFS)**  
BFS explores all nodes at the current level of the tree before moving to deeper levels.  

**Key Characteristics:**  
- Prioritizes breadth over depth.  
- Uses a **queue** to track the order of nodes to be explored.  

**Advantages:**  
- Guarantees finding the shortest path in unweighted graphs.  
- Avoids infinite loops in graphs with infinite branching (with proper handling of visited states).  

**Disadvantages:**  
- High memory usage, as it stores all nodes at the current level (space complexity grows exponentially with depth).  
- Can be slower than DFS for deep solutions.

**Performance:**  
- **Time Complexity:** $O(b^d)$, where $b$ is the branching factor and $d$ is the depth of the solution.  
- **Space Complexity:** $O(b^d)$, as all nodes at the current level are stored in memory.

**Example:**  
Using the same graph as above:

```
         A
        / \
       B   C
      / \   \
     D   E   F
```

Using BFS:  
1. Start at \( A \).  
2. Explore \( B \) and \( C \) (current level).  
3. Explore \( D \), \( E \), and \( F \) (next level).  

BFS Path: $A \to B \to C \to D \to E \to F$.  
The solution $A \to C \to F$ is found and is the shortest path.

---

### **Comparison Table**

| Feature                 | Depth-First Search (DFS) | Breadth-First Search (BFS) |
| ----------------------- | ------------------------ | -------------------------- |
| **Exploration**         | Depth-first              | Breadth-first              |
| **Data Structure**      | Stack (or recursion)     | Queue                      |
| **Shortest Path**       | No                       | Yes                        |
| **Memory Usage**        | Low ($O(b \cdot m)$)     | High ($O(b^d)$)            |
| **Infinite Loops Risk** | Yes (without safeguards) | No (with visited tracking) |
| **Use Case**            | Deep solutions           | Shallow solutions          |

---

### **Real-World Applications**

1. **DFS Applications:**  
   - Solving puzzles like mazes, where the solution may require deep exploration.  
   - Pathfinding in scenarios with limited memory resources.  

2. **BFS Applications:**  
   - Finding the shortest route in navigation systems like Google Maps.  
   - Social network analysis (e.g., finding the shortest connection between two people).

----
# **Games**
#### **Emergent Behavior**  
- **Definition:** Complex behaviors that arise from simple individual actions or rules without a central controller.  
- **Example:** In games, crowds or groups of agents dynamically form patterns (e.g., swarming or dispersing) based on local interactions.  

---

### **Flocking**  
- **Definition:** A coordinated movement pattern among agents, inspired by natural phenomena like birds flying in formation.  
- **Key Rules:**  
  1. Separation: Avoid crowding neighbors.  
  2. Alignment: Move in the same direction as neighbors.  
  3. Cohesion: Stay close to the group.  

---

### **Influence Mapping**  
- **Definition:** A method of representing and analyzing the influence of different factors (like enemy strength or terrain) on a game map.  
- **Use Case:** Helps AI decide strategic positions for attacks or defense.  

---

### **Only Computer Details Path for Visible Agents**  
- **Definition:** AI agents compute paths or make decisions only for entities visible in their environment.  
- **Benefit:** Optimizes performance by reducing unnecessary calculations for unseen or irrelevant agents.  

---

### **Manage Task Assignment**  
- **Definition:** The process of efficiently allocating tasks to agents or units based on their capabilities, availability, or proximity.  
- **Example:** Assigning roles in a real-time strategy game, such as gathering resources or defending a base.  

---

### **Obstacle Avoidance**  
- **Definition:** Techniques used by AI agents to navigate around physical barriers while moving toward a goal.  
- **Example:** In pathfinding, agents adjust their routes to avoid collisions with walls or other agents.  

---

### **Trigger System**  
- **Definition:** A mechanism to activate events or behaviors in response to specific conditions or stimuli.  
- **Example:** In games, opening a door when a player steps on a pressure plate.  

---
