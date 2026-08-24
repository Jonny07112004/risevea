# **POSTORDER TRAVERSAL IN TREES**

**Postorder Traversal** is a type of **Depth-First Search (DFS)** used to visit every node of a Binary Tree in a specific order.

In Postorder Traversal, the **Left Subtree is visited first, then the Right Subtree, and finally the Root**.

The order is:

**Left → Right → Root**

The word **“Post”** helps us remember that the **Root is processed after its subtrees**.

---

## **HOW POSTORDER TRAVERSAL WORKS**

Postorder Traversal follows three basic steps:

1. **Traverse the Left Subtree using Postorder.**
2. **Traverse the Right Subtree using Postorder.**
3. **Visit the Root node.**

The same process is applied recursively to every subtree.

The important point is that the Root is processed **only after both its Left and Right Subtrees have been completely processed**.

---

## **THE ROOT-LAST RULE**

The most important property of Postorder Traversal is that the **Root is always processed after its children**.

For every node, the order is:

**Left Child → Right Child → Parent**

This makes Postorder particularly useful when a task requires the children to be processed before their Parent.

> **Postorder means: process the Left Subtree, process the Right Subtree, and process the current node last.**

---

## **RECURSIVE APPROACH**

Postorder Traversal is naturally implemented using **recursion**.

When the traversal reaches a node, it first makes a recursive call for the Left Subtree.

After the Left Subtree is completely processed, it makes a recursive call for the Right Subtree.

Only after both subtrees are finished does it process the current node.

The recursive pattern can be remembered as:

**Postorder(Left) → Postorder(Right) → Visit Node**

The base condition occurs when the current node is **NULL**.

---

## **HOW THE CALL STACK IS USED**

When recursion is used, the system's **Call Stack** stores information about the nodes whose processing has not yet been completed.

The traversal moves down toward the Leftmost part of the Tree.

After the Left Subtree is completed, the traversal returns to the Parent and processes its Right Subtree.

The Parent is processed only after both sides have been completed.

This is why Postorder is a **Depth-First Traversal**.

The traversal goes deep into the Tree and then works its way back toward the Root.

---

## **POSTORDER EXAMPLE**

Consider a Binary Tree where the Root has a Left Child and a Right Child.

The traversal does not process the Root immediately.

Instead, it follows this order:

**Left Subtree → Right Subtree → Root**

If the Left Subtree contains multiple nodes, the entire Left Subtree is completed before moving to the Right Subtree.

Only after both are completed is the Root processed.

This gives Postorder its characteristic **Root-last** behavior.

---

## **ITERATIVE POSTORDER TRAVERSAL**

Postorder can also be implemented without recursion using a **Stack**.

The iterative approach is more complicated than Preorder and Inorder because the Parent cannot be processed until **both of its subtrees have been processed**.

A common approach uses **two Stacks**.

The first Stack is used to process the nodes, while the second Stack stores them in an order that can later be reversed to produce:

**Left → Right → Root**

Another approach uses a **single Stack** along with a pointer to keep track of the previously processed node.

The main challenge is determining when a node's Right Subtree has already been processed so that the node itself can safely be visited.

---

## **WHY IS POSTORDER A DFS TRAVERSAL?**

Postorder is classified as **Depth-First Search** because it explores the Tree deeply before returning to process Parent nodes.

The algorithm goes down through the Left and Right branches before returning to the Root.

This is different from **Level Order Traversal**, where nodes are processed level by level using a Queue.

Postorder relies on the behavior of **recursion or a Stack**.

---

## **APPLICATIONS OF POSTORDER TRAVERSAL**

### **1. DELETING A TREE**

Postorder is useful when deleting all nodes of a Tree.

The Children are deleted before the Parent.

This is important because deleting a Parent first could make it difficult to access its Children.

Therefore:

**Delete Left Subtree → Delete Right Subtree → Delete Root**

---

### **2. EXPRESSION TREES**

Postorder Traversal of an Expression Tree produces a **Postfix Expression**.

For example, an expression such as:

**A + B**

can be represented in Postfix form as:

**A B +**

Postfix expressions are useful in expression evaluation and compiler-related applications.

---

### **3. CALCULATING DIRECTORY SIZE**

In hierarchical structures such as file systems, Postorder can be used when the total size of a Parent directory depends on the sizes of its subdirectories.

The child directories can be processed first, and then the Parent directory can be calculated.

---

### **4. TREE-BASED COMPUTATIONS**

Postorder is useful when the result of a Parent depends on the results calculated from its Children.

The Children are processed first, allowing their results to be combined when processing the Parent.

This is a common pattern in **Dynamic Programming on Trees**.

---

## **TIME COMPLEXITY**

Every node in the Tree is visited exactly once.

For a Tree containing **n nodes**:

**Time Complexity: O(n)**

The Tree may be balanced or skewed, but every node still needs to be processed.

---

## **SPACE COMPLEXITY**

The space complexity depends on the **height of the Tree**.

For a balanced Binary Tree:

**Space Complexity: O(log n)**

For a completely skewed Tree:

**Space Complexity: O(n)**

The space is required by the **recursion stack** or the explicit Stack used in an iterative implementation.

---

## **KEY IDEA**

The most important rule to remember for Postorder Traversal is:

> **First visit the Left Subtree, then the Right Subtree, and finally visit the Root.**

Therefore:

**Postorder = Left → Right → Root**

It is a **Depth-First Traversal** and is commonly implemented using **recursion or a Stack**.

The three major DFS Tree traversals can be remembered as:

**Preorder → Root → Left → Right**

**Inorder → Left → Root → Right**

**Postorder → Left → Right → Root**

The key characteristic of Postorder is:

> **The Parent is processed only after both of its Children have been processed.**
