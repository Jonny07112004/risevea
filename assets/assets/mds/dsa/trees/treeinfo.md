# **TREES IN DSA**

A **Tree** is a non-linear data structure used to represent data in a **hierarchical relationship**. Unlike arrays, linked lists, stacks, and queues, which are generally linear structures, a Tree organizes data in multiple levels.

A Tree consists of **nodes connected by edges**. The topmost node is called the **Root**, and the nodes below it represent different levels of the hierarchy.

Trees are widely used in **file systems, databases, compilers, searching algorithms, artificial intelligence, and many other areas of computer science**.

---

## **BASIC STRUCTURE OF A TREE**

A Tree consists of two fundamental components:

* **Node** — Represents the actual data.
* **Edge** — Represents the connection between two nodes.

The topmost node is called the **Root**.

Every node can have zero or more child nodes, depending on the type of Tree.

The structure of a Tree naturally represents relationships such as:

**Parent → Child**

This makes Trees particularly useful for representing hierarchical information.

---

## **ROOT, PARENT, AND CHILD**

The **Root** is the starting point of a Tree. It does not have a parent.

A node directly connected above another node is called its **Parent**, while the node below it is called its **Child**.

For example, if node A is connected to nodes B and C, then:

**A is the Parent**

**B and C are Children**

A node can have multiple children, but each node generally has only one parent in a standard Tree.

---

## **LEAF NODE**

A node that does not have any children is called a **Leaf Node** or **Terminal Node**.

Leaf nodes represent the endpoints of the Tree.

For example, if a Tree contains nodes A, B, C, D, and E, and D and E have no children, then:

**D and E are Leaf Nodes.**

Leaf nodes are particularly important in algorithms involving **Tree traversal, searching, and decision-making**.

---

## **INTERNAL NODE**

A node that has at least one child is called an **Internal Node** or **Non-Leaf Node**.

For example, if A has children B and C, then A is an internal node.

Therefore:

**Leaf Node → No children**

**Internal Node → Has at least one child**

---

## **EDGE**

An **Edge** is the connection between two nodes.

If one node is connected directly to another node, the connection between them represents an edge.

For a Tree containing **N nodes**, there are always:

**N - 1 edges**

This is an important property of Trees.

---

## **DEPTH AND LEVEL**

The **Depth** of a node represents its distance from the Root.

The Root has depth **0**.

Its children have depth **1**.

Their children have depth **2**, and so on.

Therefore, as we move downward from the Root, the depth increases.

The concept of **Levels** is closely related to depth and is commonly used when discussing Tree traversal and Tree height.

---

## **HEIGHT OF A TREE**

The **Height** of a Tree represents the length of the longest path from the Root to a Leaf.

Similarly, the **height of a node** represents the longest path from that node down to one of its descendant leaf nodes.

Height is an important concept because the efficiency of many Tree operations depends on the Tree's height.

A shorter Tree generally allows faster searching and insertion.

---

## **SUBTREE**

A **Subtree** is a smaller Tree formed from a particular node and all of its descendants.

Every node in a Tree can be considered the root of its own subtree.

This recursive nature is one of the most important properties of Trees and is why **recursion is frequently used in Tree algorithms**.

---

## **TREE TRAVERSAL**

Tree Traversal means **visiting every node of a Tree according to a specific order**.

The main Tree traversal techniques are:

### **1. Preorder Traversal**

The order is:

**Root → Left Subtree → Right Subtree**

Preorder is useful when we need to process the Root before its children.

---

### **2. Inorder Traversal**

The order is:

**Left Subtree → Root → Right Subtree**

In a **Binary Search Tree**, inorder traversal produces the elements in **sorted order**.

This makes inorder traversal particularly important in BST-related problems.

---

### **3. Postorder Traversal**

The order is:

**Left Subtree → Right Subtree → Root**

Here, the Root is processed after its children.

Postorder is useful in situations where children need to be processed before their parent.

---

### **4. Level Order Traversal**

Level Order Traversal visits nodes **level by level**, starting from the Root.

It generally uses a **Queue** and is closely related to **Breadth-First Search (BFS)**.

---

## **TYPES OF TREES**

There are several important types of Trees in DSA.

### **GENERAL TREE**

A General Tree is a Tree in which a node can have **any number of children**.

There is no fixed limit on the number of children a node can have.

---

### **BINARY TREE**

A **Binary Tree** is a Tree in which every node can have at most **two children**.

These children are generally referred to as:

**Left Child**

**Right Child**

Binary Trees are one of the most important Tree structures in DSA.

---

### **BINARY SEARCH TREE**

A **Binary Search Tree (BST)** is a special type of Binary Tree that maintains an ordering property.

For every node:

**Left subtree values < Node value < Right subtree values**

This property allows efficient searching when the Tree is properly balanced.

The average search, insertion, and deletion complexity can be **O(log n)** for a balanced BST.

However, in the worst case, a BST can become skewed and behave similarly to a Linked List, resulting in **O(n)** operations.

---

### **AVL TREE**

An **AVL Tree** is a self-balancing Binary Search Tree.

It automatically maintains its height balance after insertion and deletion.

The balance of the Tree ensures that searching, insertion, and deletion remain:

**O(log n)**

AVL Trees use **rotations** to restore balance when necessary.

---

### **HEAP**

A **Heap** is a specialized Tree-based data structure commonly used to implement **Priority Queues**.

There are two major types:

**Min Heap** — The smallest element is at the Root.

**Max Heap** — The largest element is at the Root.

Heaps are also fundamental to the **Heap Sort** algorithm.

---

### **TRIE**

A **Trie** is a Tree-based data structure used mainly for storing and searching **strings or words**.

It is particularly useful for:

* Autocomplete
* Dictionary implementations
* Prefix searching
* Spell checking

A Trie organizes strings according to their characters.

---

## **WHY ARE TREES IMPORTANT?**

Trees are important because many real-world problems naturally contain **hierarchical relationships**.

For example:

**File System**

Folder → Subfolder → Files

**Organization**

Company → Department → Team → Employee

**HTML**

HTML → Body → Div → Elements

**Database Indexing**

Databases use Tree-based structures such as **B-Trees and B+ Trees** to efficiently store and retrieve large amounts of data.

---

## **APPLICATIONS OF TREES**

### **1. File Systems**

Operating systems use hierarchical Trees to represent folders and files.

### **2. Databases**

Database systems use structures such as **B-Trees and B+ Trees** for efficient searching and indexing.

### **3. Compilers**

Compilers use **Syntax Trees** to represent the structure of source code.

### **4. Searching**

Binary Search Trees provide an efficient structure for searching, inserting, and deleting data.

### **5. Artificial Intelligence**

Decision Trees can be used to make decisions based on a series of conditions.

### **6. Networking**

Tree structures can represent hierarchical network relationships and routing structures.

---

## **TREE VS LINEAR DATA STRUCTURES**

A major difference between Trees and structures such as Arrays, Linked Lists, Stacks, and Queues is how data is organized.

A **linear data structure** stores elements sequentially.

A **Tree** stores elements hierarchically.

Linear structures generally follow a single sequence:

**A → B → C → D**

A Tree can branch:

**A → B, C**

**B → D, E**

This branching structure allows Trees to represent much more complex relationships.

---

## **TIME COMPLEXITY**

The time complexity of Tree operations depends heavily on the **height and type of Tree**.

For a balanced Binary Search Tree:

**Search → O(log n)**

**Insertion → O(log n)**

**Deletion → O(log n)**

For a highly skewed Binary Search Tree:

**Search → O(n)**

**Insertion → O(n)**

**Deletion → O(n)**

Tree traversal generally takes:

**O(n)**

because every node needs to be visited.

---

## **KEY IDEA**

The most important thing to understand about Trees is that they are **hierarchical, recursive, and non-linear data structures**.

A Tree is built from **nodes and edges**, starting from a **Root** and branching into **Children** and **Subtrees**.

The most important concepts to remember are:

**Root → Starting node**

**Parent → Node above another node**

**Child → Node below a parent**

**Leaf → Node with no children**

**Edge → Connection between nodes**

**Height → Longest downward path**

**Traversal → Process of visiting nodes**

Trees form the foundation for important DSA structures such as **Binary Trees, Binary Search Trees, AVL Trees, Heaps, Tries, B-Trees, and B+ Trees**.
