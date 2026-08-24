# **PREORDER TRAVERSAL IN TREES**

**Preorder Traversal** is a type of **Depth-First Search (DFS)** used to visit every node of a Binary Tree in a specific order.

In Preorder Traversal, the **Root node is always visited first**, followed by the Left Subtree and then the Right Subtree.

The order is:

**Root → Left → Right**

The word **“Pre”** helps us remember that the **Root is processed before its subtrees**.

---

## **HOW PREORDER TRAVERSAL WORKS**

Preorder Traversal follows three basic steps:

1. **Visit the Root node.**
2. **Traverse the Left Subtree using Preorder.**
3. **Traverse the Right Subtree using Preorder.**

The same rule is applied recursively to every node in the Tree.

This recursive behavior works naturally because every subtree can itself be treated as a smaller Tree.

---

## **THE ROOT-FIRST RULE**

The most important property of Preorder Traversal is that the **Root is always processed before its children**.

Whenever we reach a node, we first visit that node before exploring anything below it.

Therefore, for every subtree:

**Parent → Left Child → Right Child**

This is different from **Inorder Traversal**, where the Root is processed between the Left and Right Subtrees, and **Postorder Traversal**, where the Root is processed last.

> **Preorder means process the current node first, then explore its descendants.**

---

## **RECURSIVE APPROACH**

Preorder Traversal is naturally implemented using **recursion**.

When the traversal reaches a node, it first processes the node. It then makes a recursive call for the Left Subtree and another recursive call for the Right Subtree.

The base condition occurs when the current node is **NULL**.

At that point, there is nothing left to visit, so the recursive call simply returns.

The recursive pattern can be remembered as:

**Visit Node → Preorder(Left) → Preorder(Right)**

---

## **HOW THE CALL STACK IS USED**

Although the recursive implementation does not explicitly create a Stack, recursion internally uses the **Call Stack**.

When the traversal moves into the Left Subtree, the current node's execution state is temporarily stored in the Call Stack.

After the Left Subtree has been completely processed, the algorithm returns to the previous node and begins exploring its Right Subtree.

This continues until every node has been visited.

Therefore, Preorder Traversal is considered a **Depth-First Traversal** because it explores one branch deeply before returning to explore another branch.

---

## **ITERATIVE PREORDER TRAVERSAL**

Preorder Traversal can also be implemented without recursion by using an **explicit Stack**.

The Root is first placed into the Stack.

Then repeatedly:

1. Remove the top node from the Stack.
2. Visit that node.
3. Push its **Right Child** into the Stack.
4. Push its **Left Child** into the Stack.

The Right Child is pushed first because a Stack follows **LIFO (Last In, First Out)**.

By pushing the Left Child after the Right Child, the Left Child remains on top and is processed first.

This maintains the required:

**Root → Left → Right**

order.

---

## **WHY IS PREORDER A DFS TRAVERSAL?**

Preorder is classified as **Depth-First Search** because it explores the Tree by moving downward through one branch before returning to another branch.

It does not process all nodes at the same level first.

That behavior would be **Level Order Traversal**, which uses a Queue.

Preorder instead uses **recursion or a Stack**, allowing it to go deeper into the Tree before backtracking.

---

## **APPLICATIONS OF PREORDER TRAVERSAL**

### **1. COPYING A TREE**

Preorder Traversal is useful when creating a copy of a Tree because the Parent node is processed before its children.

This makes it possible to create the parent structure before creating the corresponding child nodes.

### **2. SERIALIZATION OF TREES**

Preorder Traversal can be used to convert a Tree into a sequence that can later be stored or transmitted.

When combined with markers for NULL children, the Tree can be reconstructed from the serialized representation.

### **3. PREFIX EXPRESSIONS**

Expression Trees can use Preorder Traversal to generate **Prefix Expressions**.

In a Prefix Expression, the operator appears before its operands.

### **4. HIERARCHICAL DATA**

Preorder is useful when a parent must be processed before all of its descendants, such as traversing certain directory or organizational structures.

---

## **TIME COMPLEXITY**

In Preorder Traversal, every node of the Tree is visited exactly once.

Therefore, for a Tree containing **n nodes**:

**Time Complexity: O(n)**

It does not matter whether the Tree is balanced or skewed; every node still needs to be processed.

---

## **SPACE COMPLEXITY**

The space complexity depends on the **height of the Tree** because recursion uses the Call Stack.

For a balanced Binary Tree:

**Space Complexity: O(log n)**

For a completely skewed Tree:

**Space Complexity: O(n)**

The iterative version has similar worst-case auxiliary space requirements because it explicitly uses a Stack.

---

## **KEY IDEA**

The most important rule to remember for Preorder Traversal is:

> **Visit the Root first, then recursively visit the Left Subtree, and finally recursively visit the Right Subtree.**

Therefore:

**Preorder = Root → Left → Right**

It is a **Depth-First Traversal** and is commonly implemented using **recursion or a Stack**.

A simple way to distinguish the three major DFS Tree traversals is:

**Preorder → Root, Left, Right**

**Inorder → Left, Root, Right**

**Postorder → Left, Right, Root**
