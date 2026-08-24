# **INORDER TRAVERSAL IN TREES**

**Inorder Traversal** is a type of **Depth-First Search (DFS)** used to visit every node of a Binary Tree in a specific order.

In Inorder Traversal, the **Left Subtree is visited first, then the Root, and finally the Right Subtree**.

The order is:

**Left → Root → Right**

The word **“In”** can help us remember that the **Root is processed in between the Left and Right Subtrees**.

---

## **HOW INORDER TRAVERSAL WORKS**

Inorder Traversal follows three basic steps:

1. **Traverse the Left Subtree using Inorder.**
2. **Visit the Root node.**
3. **Traverse the Right Subtree using Inorder.**

The same process is applied recursively to every subtree.

The important point is that the Root is **not processed immediately**. We first completely process the Left Subtree before visiting the Root.

---

## **THE LEFT-FIRST RULE**

The most important property of Inorder Traversal is that the **Left Subtree is always processed before the Root**.

For every node, the order is:

**Left Child → Parent → Right Child**

This makes Inorder Traversal particularly important for **Binary Search Trees**.

> **Inorder means: go Left first, process the current node, then go Right.**

---

## **RECURSIVE APPROACH**

Inorder Traversal is naturally implemented using **recursion**.

When the traversal reaches a node, it first makes a recursive call to its Left Subtree.

Only after the entire Left Subtree has been processed does it visit the current node.

Finally, it makes a recursive call to the Right Subtree.

The recursive pattern can be remembered as:

**Inorder(Left) → Visit Node → Inorder(Right)**

The base condition occurs when the current node is **NULL**.

---

## **HOW THE CALL STACK IS USED**

When recursion is used, the system's **Call Stack** keeps track of the nodes that have not yet been completely processed.

The traversal continues moving toward the Leftmost node.

Once it reaches a node with no Left Child, that node is processed.

Then the traversal moves back to its Parent and continues toward the Right Subtree.

This process is called **backtracking**, and it allows Inorder Traversal to systematically process the entire Tree.

Therefore, Inorder Traversal is a **Depth-First Traversal**.

---

## **INORDER IN A BINARY SEARCH TREE**

One of the most important properties of Inorder Traversal is its behavior on a **Binary Search Tree (BST)**.

A BST follows the rule:

**Left Subtree < Root < Right Subtree**

Because Inorder Traversal visits:

**Left → Root → Right**

the elements are visited in **ascending sorted order**.

For example, if a BST contains the values:

**50, 30, 70, 20, 40, 60, 80**

An Inorder Traversal produces:

**20 → 30 → 40 → 50 → 60 → 70 → 80**

Therefore:

> **Inorder Traversal of a Binary Search Tree produces the elements in sorted order.**

This is one of the most important concepts to remember for DSA interviews and coding problems.

---

## **ITERATIVE INORDER TRAVERSAL**

Inorder Traversal can also be implemented without recursion by using an explicit **Stack**.

The basic idea is to continuously move toward the **Leftmost node**, pushing each node onto the Stack.

When there is no more Left Child:

1. Pop a node from the Stack.
2. Visit that node.
3. Move to its Right Child.
4. Repeat the same process.

The Stack is necessary because after reaching the Leftmost node, we need to remember the Parent nodes so that we can return to them.

This allows the iterative approach to reproduce the behavior of recursive Inorder Traversal.

---

## **WHY IS INORDER A DFS TRAVERSAL?**

Inorder Traversal is classified as **Depth-First Search** because it follows a branch deeply before returning to process other nodes.

It does not visit the Tree level by level.

Instead, it explores the Left side as deeply as possible, processes the appropriate Parent node, and then explores the Right side.

This is different from **Level Order Traversal**, which uses a Queue and processes nodes according to their levels.

---

## **APPLICATIONS OF INORDER TRAVERSAL**

### **1. SORTED DATA FROM A BST**

The most important application is obtaining elements in **sorted order** from a Binary Search Tree.

### **2. SEARCH TREE OPERATIONS**

Inorder traversal can be used when processing the values of a BST in ascending order.

### **3. EXPRESSION TREES**

Inorder Traversal of an Expression Tree can be used to produce an **Infix Expression**, where operators appear between operands.

For example:

**A + B**

### **4. RANGE-BASED PROCESSING**

In a BST, Inorder Traversal can be used to process values within a particular range in sorted order.

---

## **TIME COMPLEXITY**

Every node is visited exactly once.

For a Tree containing **n nodes**:

**Time Complexity: O(n)**

Whether the Tree is balanced or skewed, every node must still be processed.

---

## **SPACE COMPLEXITY**

The space complexity depends on the **height of the Tree**.

For a balanced Binary Tree:

**Space Complexity: O(log n)**

For a completely skewed Tree:

**Space Complexity: O(n)**

This space is mainly required by the **recursion stack** or the explicit Stack used in the iterative approach.

---

## **KEY IDEA**

The most important rule to remember is:

> **First visit the Left Subtree, then the Root, and finally the Right Subtree.**

Therefore:

**Inorder = Left → Root → Right**

It is a **Depth-First Traversal** and can be implemented using **recursion or a Stack**.

The three major DFS Tree traversals can be remembered as:

**Preorder → Root → Left → Right**

**Inorder → Left → Root → Right**

**Postorder → Left → Right → Root**

And the most important special property is:

> **Inorder Traversal of a Binary Search Tree gives the elements in sorted order.**
