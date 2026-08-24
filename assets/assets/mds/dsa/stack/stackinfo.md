📚 Stacks: The LIFO Powerhouse

Imagine you are washing dishes and stacking the clean plates on the counter. When you add a new plate, you put it on the very top. When you need a plate to eat dinner, you take the one from the very top. You would never try to yank a plate out from the absolute bottom—the whole stack would crash!

This is the exact physical mechanic of a Stack data structure. It operates strictly on the LIFO principle: Last-In, First-Out.

⚙️ Core Operations (The Rule of the Top)

A Stack is an incredibly rigid structure. You are only allowed to interact with one single element: the Top. Because you never have to search through the underlying data or shift elements around in memory, the core operations operate in blazing-fast $O(1)$ constant time.

Push: Drop a new element onto the very top of the stack.

Pop: Remove and return the element currently sitting at the top.

Peek (or Top): Look at the top element without actually removing it.

⚠️ The Two Deadly Crashes

Because Stacks are so beautifully simple, there are really only two major ways they can break:

>Stack Underflow: You cannot take a plate from an empty table. If a Stack has 0 elements, and you blindly attempt to call Pop() or Peek(), the program will panic and throw an Underflow Exception. Good programmers always check isEmpty() before popping!

>Stack Overflow: If a Stack is built using a fixed-size array in memory (which is exactly how your computer's CPU is built), it has a physical limit. If you Push too many items and breach that limit, the Stack overflows, resulting in a catastrophic hard crash.

🌍 Real-World Applications

1. The "Undo" Button (Ctrl + Z)
Every time you type a word or delete a line in a text editor, that action is Pushed onto a history Stack. When you realize you made a mistake and hit Ctrl+Z, the computer Pops the most recent action off the top of the stack and reverses it.

2. The Browser "Back" Button
As you click links surfing the web, every page you leave behind is pushed onto a Stack. Hitting the "Back" arrow pops the top URL off the stack and loads it back to your screen.

3. The CPU Call Stack (Recursion)
When a function calls another function, the computer pauses the first function and pushes its current state onto the hardware's Call Stack. When the second function finishes, the CPU pops the first function back off the stack and resumes right where it left off. This is how recursive algorithms (like Quick Sort and Merge Sort) are physically tracked and executed by your computer!