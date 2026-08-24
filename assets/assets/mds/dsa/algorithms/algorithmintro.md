# ⚙️ Introduction to Algorithms & Complexity

A computer is a manmade machine that lacks innate decision-making capabilities. It cannot guess or magically deduce answers; it only executes the exact instructions handed to it by a user.

To solve any computational problem, you require two fundamental elements:

1. **Data** (the raw components needing manipulation).
2. **An Algorithm** (the clear instructions to manipulate that data).

An **algorithm** is defined as a finite collection of well-defined, step-by-step instructions designed to solve a specific problem.

> [What is an Algorithm?] A finite, well-defined set of step-by-step instructions designed to solve a specific problem by transforming input data into desired output.

---

## 💎 The 5 Core Characteristics of an Algorithm

Every valid algorithm must satisfy five distinct structural criteria to ensure a computer can process it correctly:

* **📥 Input:** It must receive initial values or parameters required to begin the solution.
* **⚙️ Process:** It must perform clear, concrete actions and operations on the incoming data.
* **📤 Output:** It must produce a finished result or solution after running its calculations.
* **🛑 Finiteness:** It must terminate. An algorithm cannot run forever; it must finish its work after a specific, finite number of steps.
* **🎯 Effectiveness:** Every single instruction must play a crucial role in solving the problem. Furthermore, each step must be **feasible** (doable by the machine) and completely **unambiguous** (with absolutely no room for interpretation).

> [Key Principle] An algorithm is not optional—these five characteristics are fundamental and non-negotiable for any valid algorithm.

---

## 🎛️ Choosing Your Algorithm: The Complexity Trade-off

When multiple algorithms can solve the same problem, we choose the most optimal one by looking at its **Complexity**. Complexity is a measure of the resources an algorithm demands. We break this down into two categories:

### 1. Space Complexity (Memory Requirements)

Space requirements dictate how much hardware storage your routine consumes. This footprint is split into two halves:

* **Fixed Space:** The memory required to hold constants, static variables, and the literal **instruction sets** (code blocks) themselves. This space remains completely unchanged during runtime.
* **Dynamic Space:** The fluid memory allocated at runtime as data structures grow and shrink.

> [Space Complexity] The memory required to hold constants, static variables, instruction sets, and dynamic data structures allocated at runtime.

> [💡 Pro Tip] In modern computing, physical memory is highly accessible and available at a very low cost. Because of this, space complexity is generally considered a secondary factor when evaluating performance.

### 2. Time Complexity (Execution Requirements)

Time is the most critical asset in computing. We study time requirements so we can predict if a program will execute within acceptable limits before we deploy it.

However, you cannot measure an algorithm's efficiency by simply using a stopwatch. Physical execution times vary wildly depending on the processor speed, machine architecture, and current CPU load.

To evaluate performance objectively regardless of the hardware, **Time Complexity is measured exclusively in terms of the Input Size ($n$).**

* If the input size ($n$) is massive, resource requirements scale up.
* If the input size ($n$) is small, resource requirements remain low.

> [⚠️ Important Note] Time complexity is measured in terms of input size (n), not absolute time. This makes performance evaluation hardware-independent and truly objective.

