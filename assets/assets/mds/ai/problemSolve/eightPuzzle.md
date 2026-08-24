# **8-PUZZLE PROBLEM**

The **8-Puzzle** is a classic **Problem-Solving Agent** problem used to understand how AI performs **search and planning**.

It consists of a **3 × 3 grid** containing **8 numbered tiles and one blank space**.

The Agent's objective is to move the tiles and reach a specific **Goal State**.

The puzzle is useful because it is **Discrete, Fully Observable, and Deterministic**, making it ideal for studying classical search algorithms. 

---

## **PROBLEM FORMULATION**

The 8-Puzzle can be formally described using the five components of a search problem.

### **1. INITIAL STATE**

The arrangement of the tiles at the beginning.

**Example:**

**2 8 3**
**1 6 4**
**7 _ 5**

The blank space is usually represented by **0** when stored in code.

---

### **2. ACTIONS**

The Agent moves the **Blank Space**, rather than directly moving individual tiles.

The possible actions are:

**Up**

**Down**

**Left**

**Right**

The actual available actions depend on the position of the blank.

**Corner → 2 possible moves**

**Edge → 3 possible moves**

**Center → 4 possible moves**

Therefore, the maximum branching factor is:

**b = 4**

---

### **3. TRANSITION MODEL**

The Transition Model describes what happens after an action.

The Agent simply **swaps the blank space with the adjacent tile** in the chosen direction.

For example:

**1 2 3**
**4 _ 6**
**7 5 8**

Move **Down**:

**1 2 3**
**4 5 6**
**7 _ 8**

The blank and tile 5 have exchanged positions.

---

### **4. GOAL TEST**

The Goal Test checks whether the current board matches the required Goal State.

A standard goal configuration is:

**1 2 3**
**4 5 6**
**7 8 _**

If the current state matches this configuration:

**Goal = Reached**

---

### **5. PATH COST**

Each movement of the blank can be assigned a cost.

In the simplest version:

**Every move = Cost 1**

Therefore, the total Path Cost is simply the **number of moves** required to reach the Goal.

The objective can therefore be:

> **Find the solution with the minimum number of moves.**

---

# **STATE SPACE**

Every possible arrangement of the 8 tiles and blank space represents a possible **state**.

There are 9 positions containing 9 objects, so the total number of arrangements is:

**9! = 362,880**

However, only half of these arrangements are reachable from a particular starting state.

Therefore:

**Reachable states = 9! / 2 = 181,440**

This is why randomly generated puzzles can sometimes be **mathematically impossible to solve**.

---

## **SOLVABILITY AND INVERSIONS**

An **Inversion** occurs when a larger numbered tile appears before a smaller numbered tile when the board is read in sequence.

For the standard 8-Puzzle, a state is solvable when its number of inversions is **even**.

Therefore, before running an expensive search algorithm, the Agent can check the puzzle's **inversion parity**.

This prevents wasting resources searching for a solution that does not exist.

---

# **HEURISTICS**

The 8-Puzzle is especially useful for learning **Heuristic Search**.

A heuristic gives the Agent an estimate of how far the current state is from the Goal.

### **MISPLACED TILES**

Count how many tiles are not currently in their correct positions.

For example, if three tiles are in the wrong positions:

**h(n) = 3**

It provides a simple estimate of the remaining work.

---

### **MANHATTAN DISTANCE**

The **Manhattan Distance** measures how many horizontal and vertical moves each tile is away from its goal position.

For each tile:

**Distance = |Current Row − Goal Row| + |Current Column − Goal Column|**

The distances of all tiles are then added together.

The blank space is normally ignored.

Manhattan Distance gives a more informative estimate than simply counting misplaced tiles.

---

# **WHY DFS IS NOT IDEAL**

**Depth-First Search (DFS)** explores one path deeply before trying alternatives.

In the 8-Puzzle, this can cause DFS to explore a very long sequence of unnecessary moves before finding a solution.

It may find a solution, but that solution can be far from optimal.

For finding the **shortest solution**, **Breadth-First Search (BFS)** is more appropriate because it explores states level by level.

Heuristic methods such as **A*** can be much more efficient by using information about how close each state is to the Goal.

---

# **IMPORTANT PROPERTIES**

**Total states:**

**9! = 362,880**

**Reachable states:**

**181,440**

**Maximum branching factor:**

**4**

**Average branching factor:**

Approximately **3**

**Hardest solvable puzzle:**

**31 moves**

These properties make the 8-Puzzle a useful benchmark for comparing search algorithms.

---

# **KEY IDEA**

The 8-Puzzle converts a physical puzzle into a **mathematical search problem**.

Remember:

**State → Arrangement of 8 tiles + blank**

**Actions → Move blank Up, Down, Left, Right**

**Transition Model → Swap blank with adjacent tile**

**Goal Test → Check whether the board matches the Goal State**

**Path Cost → Number/cost of moves**

**Heuristic → Estimate distance to Goal**

The most important idea is:

> **The Agent does not need to think about moving eight different tiles. It only needs four possible actions for the Blank Space, and each action produces a new state that can be searched.**

This transforms the puzzle into a **Graph Search problem**, allowing algorithms such as **BFS and A*** to find a sequence of actions from the Initial State to the Goal State.
