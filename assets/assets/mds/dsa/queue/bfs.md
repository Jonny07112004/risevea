# **QUEUE IN BREADTH-FIRST SEARCH (BFS)**

**Breadth-First Search (BFS)** is a graph traversal algorithm that explores a graph **level by level**. Instead of going as deep as possible into one path, BFS first visits all the immediate neighbors of a vertex before moving to the next level.

A **Queue** is the core data structure used in BFS because its **FIFO (First In, First Out)** property naturally maintains the order in which vertices are discovered.

---

## **WHY DOES BFS USE A QUEUE?**

When BFS visits a vertex, it discovers its neighboring vertices. These newly discovered vertices need to be processed later.

The problem is: **which discovered vertex should be processed first?**

BFS requires the vertex that was discovered **first** to be processed first.

This is exactly what a Queue provides.

The Queue maintains a waiting list of vertices:

**First discovered → First processed**

Therefore, the Queue ensures that BFS explores the graph **level by level**.

---

## **ROLE OF THE QUEUE IN BFS**

The Queue has two main responsibilities in BFS:

### **1. Store Discovered Vertices**

When BFS encounters an unvisited neighboring vertex, that vertex is added to the **Rear of the Queue**.

This means the vertex has been discovered but is waiting to be processed.

### **2. Process Vertices in Discovery Order**

BFS removes vertices from the **Front of the Queue**.

Since the Queue follows FIFO, vertices are processed in the same order in which they were discovered.

This maintains the required **breadth-first order**.

---

## **BASIC THEORY OF BFS**

BFS generally works according to the following process:

1. Select a starting vertex.
2. Mark the starting vertex as **visited**.
3. Insert the starting vertex into the **Queue**.
4. Remove a vertex from the Front of the Queue.
5. Examine all of its adjacent vertices.
6. Every unvisited adjacent vertex is marked as visited and inserted into the Queue.
7. Continue this process until the Queue becomes empty.

The Queue therefore acts as a **temporary storage structure for vertices waiting to be processed**.

---

## **WHY NOT USE A STACK?**

A Stack follows **LIFO (Last In, First Out)**.

If a Stack were used, the most recently discovered vertex would be processed first. This naturally leads toward **Depth-First Search (DFS)** rather than BFS.

BFS requires:

**First discovered → First processed**

Therefore:

**BFS → Queue → FIFO**

While:

**DFS → Stack/Recursion → LIFO**

This is one of the most important differences between BFS and DFS.

---

## **QUEUE MAINTAINS LEVEL ORDER**

The Queue allows BFS to maintain the concept of **levels**.

Suppose a starting vertex is at Level 0.

Its direct neighbors are placed into the Queue and become Level 1.

After all Level 1 vertices are processed, their unvisited neighbors are added to the Queue and become Level 2.

This continues until all reachable vertices have been processed.

Therefore, the Queue ensures that a vertex at a particular level is processed before vertices at deeper levels.

> **The FIFO property of the Queue is what allows BFS to move through a graph level by level.**

---

## **VISITED ARRAY AND QUEUE**

In graph BFS, a **visited array or set** is normally used along with the Queue.

The visited structure prevents the same vertex from being repeatedly added to the Queue.

When a vertex is discovered:

**Mark it as visited → Insert it into the Queue**

This is important because graphs can contain **cycles**.

For example, if A is connected to B and B is connected back to A, without a visited structure BFS could keep adding the same vertices repeatedly.

---

## **BFS IN TREES**

In a tree, BFS is also called **Level Order Traversal**.

Consider a tree with several levels.

BFS first processes the **root**, then all nodes at the next level, then all nodes at the following level.

The Queue stores the nodes that belong to the upcoming levels.

This makes Queue one of the fundamental data structures behind **level-order traversal**.

---

## **BFS FOR SHORTEST PATH**

One of the important properties of BFS is that it can find the **shortest path in an unweighted graph**.

This works because BFS explores vertices according to their distance from the starting vertex.

It first visits vertices at distance:

**0**

Then:

**1**

Then:

**2**

Then:

**3**

And so on.

Because the Queue processes vertices in FIFO order, all vertices at distance **d** are processed before vertices at distance **d + 1**.

Therefore, when BFS first reaches a vertex in an unweighted graph, it has found the shortest path to that vertex.

---

## **TIME COMPLEXITY**

For a graph represented using an **adjacency list**, BFS has:

**Time Complexity: O(V + E)**

Where:

* **V** = Number of vertices
* **E** = Number of edges

Every vertex is processed once, and every edge is examined during the traversal.

The Queue operations themselves, such as **enqueue** and **dequeue**, take **O(1)** time.

---

## **SPACE COMPLEXITY**

BFS requires additional memory for:

* The **Queue**
* The **Visited Array/Set**

In the worst case, the Queue can contain a large number of vertices.

Therefore, the auxiliary space complexity is:

**O(V)**

---

## **KEY IDEA**

The Queue is not simply an implementation detail of BFS. It is what gives BFS its fundamental **breadth-first behavior**.

The relationship can be remembered as:

**BFS → Queue → FIFO → Level-by-Level Processing**

A vertex is **discovered**, placed into the Queue, and eventually **processed according to its discovery order**.

That FIFO behavior guarantees that BFS explores vertices closer to the starting point before moving farther away, which is why BFS is useful for **level-order traversal and shortest paths in unweighted graphs**.
