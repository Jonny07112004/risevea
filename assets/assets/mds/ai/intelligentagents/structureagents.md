# **THE STRUCTURE OF AGENTS**

An AI Agent is defined by a simple relationship:

> **Agent = Architecture + Program**

The **Architecture** provides the Agent with its physical or virtual components, such as **sensors and actuators**. The **Program** contains the logic that decides what action the Agent should take based on its percepts.

Russell and Norvig describe several types of Agent Programs, ranging from simple rule-based Agents to Agents that can learn from experience.

---

## **1. SIMPLE REFLEX AGENT**

A **Simple Reflex Agent** chooses an action based only on the **current percept**.

It uses simple **Condition-Action rules**:

**Condition → Action**

For example:

**Obstacle detected → Brake**

**Red light → Stop**

The Agent does not remember the past or plan for the future.

> **Simple Reflex Agent → Current Percept → Immediate Action**

It is fast and simple, but it can fail in **Partially Observable environments** because it has no memory.

---

## **2. MODEL-BASED AGENT**

A **Model-Based Agent** adds an **Internal State** or memory.

This allows the Agent to remember information that is no longer directly visible through its sensors.

For example, if an object disappears behind a wall, a Model-Based Agent can use its previous observations and knowledge of the environment to estimate where the object might be.

Therefore:

**Percept + Previous State + Environment Model → New Internal State → Action**

> **Model-Based Agent = Reflex behavior + Memory**

This makes it much more suitable for **Partially Observable environments**.

---

## **3. GOAL-BASED AGENT**

A **Goal-Based Agent** does not simply react to the current situation. It considers **future actions** to achieve a specific goal.

For example, a navigation Agent may have the goal:

**Reach Mumbai**

It examines possible paths and chooses actions that move it toward that goal.

The basic idea is:

**Current State + Goal → Search/Planning → Action**

Goal-Based Agents commonly use **search and planning algorithms**.

The major advantage is that they can consider future consequences rather than simply reacting to current percepts.

---

## **4. UTILITY-BASED AGENT**

A **Utility-Based Agent** goes one step further than a Goal-Based Agent.

A Goal-Based Agent mainly asks:

> **Can I achieve the goal?**

A Utility-Based Agent asks:

> **Which possible outcome is the best?**

For example, several routes may all reach the destination, but one may be:

**Faster**

**Safer**

**Cheaper**

The Agent uses a **Utility Function** to assign a value to possible outcomes and chooses the action with the highest utility.

> **Goal-Based → Achieve the goal**

> **Utility-Based → Choose the best way to achieve it**

---

## **5. LEARNING AGENT**

A **Learning Agent** can **improve its behavior through experience**.

It does not need to be perfectly programmed from the beginning. It can learn from its interactions with the environment.

A Learning Agent has four important components:

### **Learning Element**

Improves the Agent's behavior based on experience.

### **Performance Element**

Selects the actions that the Agent performs.

### **Critic**

Evaluates how well the Agent is performing against an external performance standard.

### **Problem Generator**

Encourages exploration by suggesting actions that can provide useful new information.

The basic idea is:

**Action → Feedback → Learning → Improved Action**

---

## **COMPARISON OF AGENT TYPES**

**Simple Reflex Agent**

Uses **current percepts** and Condition-Action rules.

**Model-Based Agent**

Adds **internal memory** to handle information that may not currently be observable.

**Goal-Based Agent**

Uses **goals and planning** to determine future actions.

**Utility-Based Agent**

Uses a **Utility Function** to compare different possible outcomes.

**Learning Agent**

Uses **experience and feedback** to improve its behavior.

---

## **IMPORTANT DIFFERENCE: GOAL VS UTILITY**

This is an important concept.

A **Goal-Based Agent** has a binary idea of success:

**Goal achieved → Yes/No**

A **Utility-Based Agent** considers the **quality of the outcome**.

For example:

Two routes both reach the destination.

The Goal-Based Agent considers both successful.

The Utility-Based Agent can determine that one route is **safer, faster, or cheaper** and choose it because it has higher utility.

---

## **KEY IDEA**

The structure of Agents can be remembered as a progression:

**Simple Reflex → React**

**Model-Based → Remember**

**Goal-Based → Plan**

**Utility-Based → Compare**

**Learning → Improve**

And the fundamental equation is:

> **Agent = Architecture + Program**

As the environment becomes more complex, the Agent can require **memory, planning, utility evaluation, and learning** rather than simply reacting to the current percept.
