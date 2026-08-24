# **BALANCED BRACKETS USING STACK**

The **Balanced Brackets** problem is one of the most common applications of a **Stack** in DSA. The goal is to determine whether brackets in an expression are correctly opened and closed.

For example:

**`{[()]}`** is balanced because every opening bracket has a matching closing bracket in the correct order.

But **`{[(])}`** is not balanced because the brackets are closed in the wrong order.

The three common types of brackets are:

* **Parentheses:** `()`
* **Square brackets:** `[]`
* **Curly brackets:** `{}`

A **Stack** is perfect for this problem because it follows **LIFO (Last In, First Out)**. The most recently opened bracket must be the first bracket to be closed.

---

## **STEP 1: SCAN THE EXPRESSION**

We process the expression **from left to right**, one character at a time.

For every character:

* If it is an **opening bracket**, push it into the Stack.
* If it is a **closing bracket**, check the top element of the Stack.
* The closing bracket must match the opening bracket at the top.

For example:

**`{[()]}`**

We process each bracket:

`{` → Push

`[` → Push

`(` → Push

`)` → Matches `(`, so Pop

`]` → Matches `[`, so Pop

`}` → Matches `{`, so Pop

At the end, the Stack is empty, so the brackets are **balanced**.

---

## **STEP 2: PUSH OPENING BRACKETS**

Whenever we encounter an opening bracket, we simply **push it onto the Stack**.

For:

**`{[(]`**

The Stack changes like this:

After `{`:

**Stack: `{`**

After `[`:

**Stack: `{ [`**

After `(`:

**Stack: `{ [ (`**

The Stack always remembers the most recently opened bracket.

---

## **STEP 3: CHECK CLOSING BRACKETS**

When a closing bracket appears, we look at the **top of the Stack**.

For example:

**`{[()]}`**

When we encounter `)`, the top of the Stack is `(`.

Since `(` matches `)`, we **pop** `(` from the Stack.

Then the next closing bracket `]` is checked against `[`, and finally `}` is checked against `{`.

This is where the **LIFO property of Stack** becomes important.

> **The last bracket opened must be the first bracket closed.**

---

## **STEP 4: DETECTING UNBALANCED BRACKETS**

There are several situations where brackets are considered unbalanced.

### **Case 1: Wrong Closing Bracket**

Consider:

**`{[)}`**

When `)` is encountered, the top of the Stack is `[`.

But `[` does not match `)`.

Therefore, the expression is **not balanced**.

---

### **Case 2: Closing Bracket Without Opening Bracket**

Consider:

**`())`**

After processing the first two brackets, the Stack becomes empty.

When the second `)` is encountered, there is no opening bracket available to match it.

Therefore, the expression is **not balanced**.

---

### **Case 3: Opening Bracket Left Unclosed**

Consider:

**`{[()]`**

After processing the expression, `{` is still present in the Stack.

Since the Stack is not empty, there is an unmatched opening bracket.

Therefore, the expression is **not balanced**.

---

## **STEP 5: THE COMPLETE LOGIC**

The general algorithm is:

1. Create an empty Stack.
2. Traverse the expression from left to right.
3. If the character is an opening bracket, **push it** into the Stack.
4. If the character is a closing bracket:

   * Check whether the Stack is empty.
   * If it is empty, the expression is not balanced.
   * Otherwise, check whether the top bracket matches the current closing bracket.
   * If it does not match, the expression is not balanced.
   * If it matches, **pop** the opening bracket.
5. After processing the entire expression, check the Stack.
6. If the Stack is empty, the brackets are **balanced**.
7. If the Stack is not empty, the brackets are **not balanced**.

---

## **EXAMPLE**

Consider:

**`{[()]}`**

Start with an empty Stack.

`{` → Push `{`

Stack: **`{`**

`[` → Push `[`

Stack: **`{ [`**

`(` → Push `(`

Stack: **`{ [ (`**

`)` → Matches `(` → Pop

Stack: **`{ [`**

`]` → Matches `[` → Pop

Stack: **`{`**

`}` → Matches `{` → Pop

Stack: **Empty**

Since the Stack is empty at the end:

**`{[()]}` is balanced.**

---

## **WHY DO WE USE A STACK?**

The main reason is the **LIFO principle**.

Suppose we have:

**`{ [ (`**

The last bracket opened is `(`.

Therefore, `(` must be closed first.

After that, `[` must be closed, and finally `{`.

The required closing order is:

**`) ] }`**

This exactly matches the behavior of a Stack.

> **Stack naturally remembers the most recently opened bracket, making it the ideal data structure for balanced bracket problems.**

---

## **TIME AND SPACE COMPLEXITY**

If the expression contains **n characters**:

**Time Complexity: O(n)**

We scan every character only once.

**Space Complexity: O(n)**

In the worst case, all characters could be opening brackets and therefore stored in the Stack.

For example:

{% raw %} **{{{{{{{{** {% endraw %}

All of them would remain inside the Stack.

---

## **REAL-WORLD APPLICATIONS**

Balanced bracket checking is useful in many areas of computer science.

### **1. Compiler Design**

Compilers use similar logic to check whether brackets and other symbols in source code are properly structured.

### **2. Code Editors**

Code editors can identify unmatched brackets and highlight errors while programmers write code.

### **3. Expression Parsing**

Stacks are used to process mathematical expressions containing parentheses and other symbols.

### **4. Syntax Validation**

Programming languages use bracket structures such as:

**`if (condition) { ... }`**

Correctly matching these symbols is important for valid syntax.

---

## **KEY IDEA**

The entire problem can be remembered with one simple rule:

> **Push every opening bracket. When a closing bracket appears, it must match the bracket at the top of the Stack. Pop it if it matches. At the end, the Stack must be empty.**

Therefore:

**Balanced → Stack is empty at the end**

**Unbalanced → Wrong match, empty Stack during closing, or remaining brackets in Stack**
