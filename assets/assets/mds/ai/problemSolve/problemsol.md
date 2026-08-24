# **PROBLEM-SOLVING AGENTS**

A **Problem-Solving Agent** is a type of **Goal-Based Agent** that first thinks about a problem, creates a plan using **search**, and then executes that plan.

The basic idea is:

**Formulate → Search → Plan → Execute**

The Agent normally assumes a **Fully Observable, Deterministic, and Static** environment. 

---

## **PROBLEM FORMULATION**

Before searching for a solution, the problem must be formally defined using **5 components**:

### **1. INITIAL STATE**

The state where the Agent starts.

**Example:**
Agent is currently in **Mumbai**.

### **2. ACTIONS**

The actions available to the Agent from a particular state.

**Example:**
Move to Delhi, Pune, or Bangalore.

### **3. TRANSITION MODEL**

Describes what happens when the Agent performs an action.

**Example:**
**Mumbai + Drive to Pune → Pune**

### **4. GOAL TEST**

Checks whether the current state satisfies the goal.

**Example:**
**Current location = Delhi → Goal Reached**

### **5. PATH COST**

Measures the total cost of a sequence of actions.

Cost can represent:

**Distance, Time, Money, Energy**, etc.

These five components formally define the search problem. 

---

## **SEARCH SPACE**

The **State Space** contains all possible states that the Agent can reach.

The Agent searches through these states to find a path from:

**Initial State → Goal State**

The possible actions create different branches, producing a **Search Tree**.

As the number of available actions increases, the number of possible paths can grow extremely quickly.

---

## **FRONTIER**

The **Frontier**, also called the **Open List**, contains states that have been discovered but **have not yet been expanded**.

It represents the current boundary of the Agent's search.

**Frontier → States waiting to be explored**

Different search algorithms use the Frontier differently.

For example:

**BFS → Queue**

**DFS → Stack**

**Uniform-Cost Search → Priority Queue**

---

## **EXPLORED SET**

The **Explored Set**, also called the **Closed List**, stores states that the Agent has already visited.

Its purpose is to prevent the Agent from repeatedly exploring the same states.

For example, in a maze:

**Move Left → Move Right → Move Left → Move Right**

Without memory, the Agent could continue forever.

The Explored Set allows the Agent to recognize:

> **"I have already visited this state."**

and avoid unnecessary repetition. 

---

## **TREE SEARCH VS GRAPH SEARCH**

### **TREE SEARCH**

Tree Search does not maintain an Explored Set.

This can cause repeated exploration and even infinite loops when cycles exist.

### **GRAPH SEARCH**

Graph Search maintains an **Explored Set** to remember previously visited states.

Therefore, Graph Search is generally safer for environments containing **cycles or reversible actions**. 

---

## **PATH COST**

Finding a solution is not always enough.

The Agent may need to find the **cheapest or best solution**.

For example:

**Path A → 3 steps → Cost = ₹100**

**Path B → 5 steps → Cost = ₹20**

BFS might prefer Path A because it has fewer steps, but a cost-aware algorithm may prefer Path B because its **total path cost is lower**.

Therefore:

> **Fewest steps ≠ Lowest cost**

Path Cost is essential when actions have different costs. 

---

## **OFFLINE PLANNING**

A Problem-Solving Agent generally **thinks before it acts**.

It creates a plan by simulating possible actions internally.

Only after finding a solution does it execute the sequence of actions.

The basic process is:

**Current State → Search Possible Actions → Find Plan → Execute Plan**

This is called **offline planning**. 

---

## **OPEN-LOOP EXECUTION**

Problem-Solving Agents generally execute their plans **open-loop**.

This means that after creating the plan, the Agent follows the planned sequence without continuously changing it based on new sensor information.

The assumption is that the environment behaves as expected.

This can become a problem if the environment changes while the Agent is executing the plan. 

---

## **COMPLETENESS AND OPTIMALITY**

A good Problem-Solving Agent can have two important properties:

**Completeness** → Finds a solution if a solution exists within the relevant search space.

**Optimality** → Finds the best solution according to the defined path cost.

Whether an algorithm actually provides these guarantees depends on the **specific search algorithm and problem conditions**. 

---

## **COMPLEXITY**

The general search space can grow very quickly.

If:

**b = Number of possible actions per state**

**d = Depth of the goal**

then the search can have approximately:

**Time Complexity → O(b^d)**

The Frontier and Explored Set can also require substantial memory:

**Space Complexity → O(b^d)** 

This rapid growth is known as the **combinatorial explosion** of the search space.

---

## **KEY IDEA**

Remember the complete structure:

**Problem-Solving Agent → Goal-Based Agent**

**Problem Formulation → 5 Components**

**Initial State**

**Actions**

**Transition Model**

**Goal Test**

**Path Cost**

Then:

**Formulate → Search → Find Plan → Execute**

And during search:

**Frontier → What remains to be explored**

**Explored Set → What has already been explored**

> **The main purpose of a Problem-Solving Agent is to find a sequence of actions that transforms the Initial State into a Goal State, preferably with the lowest possible Path Cost.**
