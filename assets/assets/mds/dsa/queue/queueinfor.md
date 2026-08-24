# **QUEUE IN DSA**

A **Queue** is a linear data structure that follows the **FIFO (First In, First Out)** principle. Think of it like a line of people waiting at a ticket counter: the person who enters the line first is the person who gets served first.

Unlike a **Stack**, where insertion and deletion happen from the same end, a Queue uses two different ends. New elements are added from the **Rear**, while existing elements are removed from the **Front**. This makes Queues useful whenever data needs to be processed in the exact order in which it arrives.

---

## **STEP 1: ENQUEUE**

The first fundamental operation of a Queue is **Enqueue**, which means **adding a new element**.

1. A new element is inserted at the **Rear** of the Queue.
2. The Rear moves to the newly inserted element.
3. The existing elements remain in their original order.

For example, if the Queue contains **10, 20, and 30**, and we enqueue **40**, the Queue becomes **10, 20, 30, 40**.

The important rule is:

> **Insertion always happens at the Rear.**

---

## **STEP 2: DEQUEUE**

The second fundamental operation is **Dequeue**, which means **removing an element**.

1. The element at the **Front** is selected.
2. That element is removed from the Queue.
3. The Front moves to the next element.

For example, if the Queue contains **10, 20, 30, and 40**, performing dequeue removes **10**.

The remaining Queue becomes:

**20, 30, 40**

This demonstrates the **FIFO rule**. Since **10 entered the Queue first, it must leave first**.

---

## **STEP 3: FRONT AND REAR**

A Queue normally maintains two important positions: **Front** and **Rear**.

The **Front** represents the element that will be removed next.

The **Rear** represents the position where the next element will be inserted.

For example, in a Queue containing **10, 20, 30, and 40**, **10** is at the Front and **40** is at the Rear.

This separation between insertion and deletion is what makes a Queue different from a Stack.

---

## **STEP 4: CIRCULAR QUEUE**

When a Queue is implemented using an **Array**, a common problem is **wasted space**.

Suppose an Array has a fixed size of 5. Initially, it contains **10, 20, 30, 40, and 50**.

If we remove **10, 20, and 30**, the first three positions become empty.

Even though there is free space at the beginning, the Rear may already be at the end of the Array.

A **Circular Queue** solves this problem.

In a Circular Queue, when the Rear reaches the last position, it can move back to the first available position. The Array is treated as if the last position is connected to the first position.

This allows the available memory to be **reused efficiently**.

---

## **STEP 5: QUEUE USING LINKED LIST**

A Queue can also be implemented using a **Linked List**.

Two pointers are generally maintained:

* **Front** — points to the first node.
* **Rear** — points to the last node.

When a new element is inserted, it is added after the **Rear**.

When an element is removed, the **Front** node is removed.

With both Front and Rear pointers, **Enqueue and Dequeue can be performed in O(1) time**.

---

## **REAL-WORLD APPLICATIONS**

### **1. CPU Scheduling**

Operating systems use Queues to manage processes waiting for CPU execution. **Round Robin scheduling** uses a circular queue-like structure.

### **2. Breadth-First Search**

Queues are heavily used in **Breadth-First Search (BFS)**. BFS processes nodes level by level and uses a Queue to maintain the order in which nodes should be processed.

### **3. Printer Scheduling**

When multiple documents are sent to a printer, they can be placed into a Queue. The document that arrives first is normally **printed first**.

### **4. Network Data Processing**

Routers and servers use Queues to temporarily store network packets when data arrives faster than it can be processed.

### **5. Task Scheduling**

Queues can be used to manage tasks waiting to be executed. Tasks can be processed according to their **arrival order**.

---

## **TIME COMPLEXITY**

For a properly implemented Queue:

* **Enqueue:** O(1)
* **Dequeue:** O(1)
* **Peek:** O(1)
* **isEmpty:** O(1)

The main idea to remember is simple:

> **A Queue follows FIFO — First In, First Out.**

Elements are **inserted from the Rear** and **removed from the Front**. This makes Queues especially useful for **scheduling, BFS, buffering, networking, and situations where data must be processed in the order it arrives**.
