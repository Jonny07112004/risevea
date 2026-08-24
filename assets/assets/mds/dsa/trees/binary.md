# **BINARY TREE IN DSA**

A **Binary Tree** is a special type of **Tree data structure** in which every node can have **at most two children**.

These two children are called the **Left Child** and the **Right Child**.

The word **Binary** refers to the fact that each node can have a maximum of **two branches**.

A node may have:

* **No children**
* **One child**
* **Two children**

But it can never have more than two children.

---

## **BASIC STRUCTURE OF A BINARY TREE**

A Binary Tree consists of **nodes and edges**, just like a general Tree.

Each node generally contains:

* **Data**
* **Reference to the Left Child**
* **Reference to the Right Child**

The Root is the starting point of the Binary Tree.

Every node below the Root belongs to either the **Left Subtree** or the **Right Subtree** of another node.

The important rule is:

> **Every node can have at most one Left Child and at most one Right Child.**

---

## **ROOT, PARENT, AND CHILD**

The **Root** is the topmost node of the Binary Tree.

A node directly connected above another node is its **Parent**.

A node connected below another node is its **Child**.

In a Binary Tree, a Parent can have:

**0 children**

**1 child**

or

**2 children**

The children are specifically identified as:

**Left Child**

and

**Right Child**

The position of a child matters. A Left Child and Right Child are not considered interchangeable.

---

## **LEAF NODE**

A node that has **no children** is called a **Leaf Node**.

Leaf nodes are the endpoints of the Binary Tree.

For example, if a node does not have either a Left Child or a Right Child, it is a Leaf.

Leaf nodes are important in many Tree algorithms because they represent the points where a path terminates.

---

## **INTERNAL NODE**

A node that has at least one child is called an **Internal Node**.

For example, if a node has only a Left Child, it is still an Internal Node.

Therefore:

**Leaf Node → 0 children**

**Internal Node → 1 or 2 children**

---

## **HEIGHT OF A BINARY TREE**

The **Height** of a Binary Tree is the length of the longest path from the Root to a Leaf.

The height determines how many levels the Tree can contain.

A Binary Tree with a small height is generally more efficient for operations such as searching when the Tree follows appropriate ordering or balancing properties.

A highly unbalanced Binary Tree can become similar to a Linked List, increasing the time required for many operations.

---

## **DEPTH AND LEVEL**

The **Depth** of a node represents its distance from the Root.

The Root is generally considered to have depth **0**.

Its children have depth **1**.

Their children have depth **2**, and so on.

The nodes at the same depth are considered to be on the same **Level**.

These concepts are particularly important in **BFS and Level Order Traversal**.

---

## **TYPES OF BINARY TREES**

There are several important types of Binary Trees.

### **1. FULL BINARY TREE**

A **Full Binary Tree** is a Binary Tree in which every node has either:

**0 children**

or

**2 children**

No node has exactly one child.

---

### **2. COMPLETE BINARY TREE**

A **Complete Binary Tree** is a Binary Tree in which:

* All levels are completely filled except possibly the last level.
* The last level is filled from **left to right**.

Complete Binary Trees are particularly important for implementing **Heaps**.

---

### **3. PERFECT BINARY TREE**

A **Perfect Binary Tree** is a Binary Tree in which:

* Every internal node has exactly two children.
* All Leaf Nodes are at the same level.

If the height is **h**, the number of nodes is:

**2^(h + 1) - 1**

---

### **4. BALANCED BINARY TREE**

A Binary Tree is considered balanced when the heights of its subtrees remain reasonably close to each other.

Balanced Trees prevent the structure from becoming heavily skewed.

Examples include:

**AVL Tree**

and certain forms of **Red-Black Trees**.

Balanced structures help maintain efficient operations.

---

### **5. SKEWED BINARY TREE**

A **Skewed Binary Tree** is a Tree where most nodes have only one child.

A Left-Skewed Tree has nodes primarily connected through Left Children.

A Right-Skewed Tree has nodes primarily connected through Right Children.

A skewed Binary Tree can resemble a **Linked List**.

---

## **BINARY TREE TRAVERSALS**

Traversal means **visiting every node in a particular order**.

The major Binary Tree traversals are:

### **PREORDER**

**Root → Left → Right**

The Root is processed first.

---

### **INORDER**

**Left → Root → Right**

The Root is processed between the Left and Right Subtrees.

In a Binary Search Tree, Inorder Traversal produces values in **sorted order**.

---

### **POSTORDER**

**Left → Right → Root**

The Root is processed after both subtrees.

This is useful when child nodes need to be processed before their Parent.

---

### **LEVEL ORDER**

**Level by Level**

Level Order Traversal generally uses a **Queue** and follows the principles of **Breadth-First Search**.

---

## **BINARY TREE VS BINARY SEARCH TREE**

A very important distinction is that a **Binary Tree is not necessarily a Binary Search Tree**.

A Binary Tree only follows one main rule:

> **Each node can have at most two children.**

There is no requirement that values must be ordered.

A **Binary Search Tree (BST)** has an additional ordering rule:

**Left Subtree < Root < Right Subtree**

Therefore, every BST is a Binary Tree, but **not every Binary Tree is a BST**.

---

## **APPLICATIONS OF BINARY TREES**

### **1. EXPRESSION TREES**

Binary Trees can represent mathematical expressions.

Operators can be stored in internal nodes, while operands can be stored in Leaf Nodes.

This is useful for **expression evaluation and compilers**.

---

### **2. BINARY SEARCH TREES**

Binary Trees form the foundation of **Binary Search Trees**, which are used for efficient searching, insertion, and deletion.

---

### **3. HEAPS**

A Heap is commonly represented as a **Complete Binary Tree**.

Heaps are used in:

* Priority Queues
* Heap Sort
* Scheduling algorithms

---

### **4. DECISION TREES**

Binary Trees can represent decisions where each node leads to one of two possible choices.

For example:

**Condition → Yes / No**

This concept is widely used in decision-making algorithms and machine learning.

---

### **5. HIERARCHICAL DATA**

Binary Trees can represent hierarchical relationships where each element has at most two branches.

---

## **TIME COMPLEXITY**

The complexity depends on the operation and structure of the Binary Tree.

For simply traversing a Binary Tree containing **n nodes**:

**Preorder → O(n)**

**Inorder → O(n)**

**Postorder → O(n)**

**Level Order → O(n)**

Every node must be visited during a complete traversal.

For a general Binary Tree, searching for a particular value can take:

**O(n)**

because there is no guarantee that the values are ordered.

---

## **SPACE COMPLEXITY**

The space required for traversal depends on the **height of the Tree**.

For recursive DFS traversals:

**O(h)**

where **h** is the height of the Tree.

For a balanced Tree:

**O(log n)**

For a skewed Tree:

**O(n)**

Level Order Traversal uses a Queue, which can require **O(n)** space in the worst case.

---

## **KEY IDEA**

The most important thing to remember about a Binary Tree is:

> **A Binary Tree is a Tree in which every node can have at most two children: a Left Child and a Right Child.**

The major concepts are:

**Root → Topmost node**

**Parent → Node having children**

**Child → Node below a Parent**

**Leaf → Node with no children**

**Height → Longest path from Root to Leaf**

**Left Subtree → Nodes connected through the Left side**

**Right Subtree → Nodes connected through the Right side**

The four important traversal techniques are:

**Preorder → Root → Left → Right**

**Inorder → Left → Root → Right**

**Postorder → Left → Right → Root**

**Level Order → Level by Level**

Binary Trees are fundamental to DSA because they form the basis for important structures such as **Binary Search Trees, Heaps, AVL Trees, Expression Trees, and many hierarchical algorithms**.
