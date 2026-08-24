# **STATE REPRESENTATION IN AI**

A **State Representation** is the way an AI Agent internally describes the current state of its environment. Russell and Norvig describe three levels of representation:

**Atomic → Factored → Structured**

---

## **1. ATOMIC REPRESENTATION**

An **Atomic representation** treats each state as a single, indivisible unit.

The Agent knows that two states are different, but does not know the internal details of those states.

**Example:**

Mumbai, Delhi, and Bangalore can simply be represented as three different states.

**Key Point:**
**Atomic = State treated as a single black box**

**Used For:**
Basic search and pathfinding problems.

**Advantage:** Simple and fast.

**Limitation:** The Agent cannot reason about the internal properties of a state.

---

## **2. FACTORED REPRESENTATION**

A **Factored representation** divides a state into multiple **variables or attributes**.

**Example:**

Location = Mumbai
Traffic = High
Raining = Yes
Battery = 85%

Now the Agent can reason about individual properties of the state.

**Key Point:**
**Factored = State represented using variables**

**Used For:**
Problems involving constraints and variables, such as **Sudoku**.

### **State Space**

If there are **N Boolean variables**, each variable has 2 possible values.

Therefore:

**Number of possible states = 2^N**

For 10 Boolean variables:

**2^10 = 1,024 states**

---

## **3. STRUCTURED REPRESENTATION**

A **Structured representation** represents the environment using **objects, attributes, and relationships**.

**Example:**

**Block A is ON TOP OF Block B**

Here, the Agent understands both the objects and the relationship between them.

**Key Point:**
**Structured = Objects + Properties + Relationships**

**Used For:**
Complex knowledge involving relationships, language, and knowledge representation.

---

## **QUICK COMPARISON**

**Atomic**
→ Single black-box state
→ Simple
→ Low information

**Factored**
→ Variables and attributes
→ More reasoning
→ State space can grow rapidly

**Structured**
→ Objects and relationships
→ Most expressive
→ More computationally expensive

---

## **REMEMBER IT LIKE THIS**

**Atomic → What state am I in?**

**Factored → What properties does the state have?**

**Structured → What objects exist and how are they related?**

> **More detailed representation gives the Agent more reasoning ability, but also increases computational complexity.**

