# 🗑️ Linked List Deletion: A Short Note

Deleting a node in a Linked List is fundamentally different from deleting an item in an array. Instead of physically shifting elements over to fill the empty space, you simply re-route the pointers to bypass the unwanted node.

### ✂️ The Core Mechanism: The "Pointer Bypass"

Because linked list nodes are scattered in memory and connected by arrows (pointers), removing a node just means changing where the arrows point.

To delete a target node (let's call it **Node C**), you must:

1. Stop at the node exactly *before* it (**Node B**).
2. Take Node B's pointer, disconnect it from Node C, and plug it directly into **Node D**.

>Node C is now completely disconnected from the chain. In modern languages (like Python, Java, or JavaScript), the computer's Garbage Collector will notice Node C is floating away and automatically delete it to free up memory. (Note: In C or C++, you must manually delete it!)

---

### 🚦 The 3 Main Scenarios

When writing a deletion algorithm, you must account for three distinct scenarios:

* **1. Deleting the Head (First Node):** The Head node has no "previous" node to re-route. To delete it, you simply move the main Head pointer to point to the second node (Head = Head.next).
* **2. Deleting a Middle or Tail Node:** You must traverse the list using two pointers: a current pointer to find the target value, and a prev (previous) pointer trailing right behind it. Once found, execute the bypass: prev.next = current.next.
* **3. The Value Does Not Exist:** If your current pointer reaches the end of the list (null) and hasn't found the target, the algorithm should safely exit without changing anything or crashing.

---

### ⏱️ Time & Space Complexity

* **Time Complexity (Traversal): $O(n)$** Because linked lists do not have indexes, you must walk through the list one by one to find the node you want to delete. In the worst case, the node is at the very end.
* **Time Complexity (The Deletion itself): $O(1)$** Once you find the correct spot, swapping the pointers takes instant, constant time.
* **Space Complexity: $O(1)$** The operation is done entirely in-place without needing any extra memory structures.