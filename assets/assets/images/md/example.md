### 🔍 Real-World Analogy
Imagine you are looking for a specific book on a giant library shelf. You don't know where it is, so you start at the very first book and check them one by one until you find the right one. That is **Linear Search**.

---

### 📊 Complexity Scorecard

| Metric | Complexity | Description |
| :--- | :--- | :--- |
| **Best Case** | O(1) | The item is the very first one in the array. |
| **Worst Case** | O(n) | The item is at the very end, or doesn't exist. |
| **Space** | O(1) | No extra memory is needed. |

**✅ Pros:**
* Incredibly simple to write and understand.
* Works on **unsorted** data (unlike Binary Search).

**❌ Cons:**
* Very slow for large datasets.

---

### 🚨 Common Pitfalls
* **Off-by-One Errors:** Remember that arrays are 0-indexed! Your loop should typically run `i < arr.length`, not `i <= arr.length`.
* **Returning too early:** Don't return `-1` (Not Found) inside the loop just because the *current* item isn't a match. Wait until the loop finishes completely before deciding the item doesn't exist!

---

### 💻 Production Implementation

```java
public int linearSearch(int[] arr, int target) {
    // Traverse the array from start to finish
    for (int i = 0; i < arr.length; i++) {
        // If we find a match, return the exact index
        if (arr[i] == target) {
            return i;
        }
    }
    // Loop finished without a match
    return -1; 
}