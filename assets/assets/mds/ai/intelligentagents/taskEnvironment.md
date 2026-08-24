# **PROPERTIES OF TASK ENVIRONMENTS**

Not all AI problems have the same type of environment. Before designing an AI Agent, we need to understand the **Task Environment** because its properties determine what kind of Agent architecture and algorithms will work effectively.

The main properties are:

**Fully Observable / Partially Observable**

**Single-Agent / Multi-Agent**

**Deterministic / Stochastic**

**Episodic / Sequential**

**Static / Dynamic**

**Discrete / Continuous**

**Known / Unknown**

---

## **1. FULLY OBSERVABLE VS PARTIALLY OBSERVABLE**

A **Fully Observable** environment is one where the Agent can access all the relevant information about the current state.

A **Partially Observable** environment is one where the Agent's sensors cannot provide the complete state.

For example, in **Poker**, the Agent cannot see the opponent's cards, so it is **Partially Observable**.

In a partially observable environment, the Agent may need **internal memory or a belief state** to estimate what is happening.

> **Fully Observable → Agent can see the relevant state**

> **Partially Observable → Agent must reason about hidden information**

---

## **2. SINGLE-AGENT VS MULTI-AGENT**

A **Single-Agent** environment contains one Agent whose actions determine the outcome.

A **Multi-Agent** environment contains multiple Agents that can affect the outcome.

**Chess** is a Multi-Agent environment because the Agent must consider the opponent's actions.

Multi-Agent environments can be:

**Cooperative** — Agents work toward a common objective.

**Competitive** — Agents have conflicting objectives.

> **Multi-Agent does not automatically mean Stochastic.**

For example, Chess is Multi-Agent but can still be **Deterministic**, because there is no random dice roll involved. 

---

## **3. DETERMINISTIC VS STOCHASTIC**

A **Deterministic** environment produces a predictable result when the current state and action are known.

A **Stochastic** environment involves **randomness or uncertainty** in the outcome.

For example:

**Chess → Deterministic**

**Poker → Stochastic**

In a stochastic environment, the Agent may need to consider **multiple possible outcomes and their probabilities**.

This connects directly to **Expected Utility**, where the Agent evaluates possible future outcomes rather than assuming one guaranteed result.

---

## **4. EPISODIC VS SEQUENTIAL**

An **Episodic** environment consists of independent decisions.

The current decision does not significantly affect future decisions.

For example, an AI inspecting bottles on an assembly line can examine each bottle independently.

A **Sequential** environment is one where the current action affects future situations.

**Chess** is Sequential because a move made now changes the possible moves later.

> **Episodic → Decisions are independent**

> **Sequential → Current actions affect the future**

Sequential environments therefore require **planning and consideration of future consequences**.

---

## **5. STATIC VS DYNAMIC**

A **Static** environment does not change while the Agent is deciding what to do.

A **Dynamic** environment can change while the Agent is thinking.

For example:

**Crossword Puzzle → Static**

**Self-Driving Car → Dynamic**

In a Dynamic environment, taking too long to calculate an action can itself create problems because the environment continues to change.

There is also a **Semi-Dynamic** environment, where the environment does not change but the Agent's performance can change with time.

For example, **Chess with a game clock** becomes Semi-Dynamic because the board may remain unchanged while the passage of time affects the Agent's performance. 

---

## **6. DISCRETE VS CONTINUOUS**

A **Discrete** environment has distinct and countable states or actions.

**Chess** is largely Discrete because it has a fixed board and a specific set of legal moves.

A **Continuous** environment has values that can vary smoothly over a range.

A **Self-Driving Car** is Continuous because variables such as:

**Speed**

**Position**

**Steering angle**

can vary continuously.

> **Discrete → Separate, countable possibilities**

> **Continuous → Smoothly varying possibilities**

---

## **7. KNOWN VS UNKNOWN**

A **Known** environment is one where the Agent knows the rules governing how the environment works.

An **Unknown** environment is one where the Agent does not initially know the rules and may need to **learn them through experience**.

This is different from observability.

> **Partially Observable → Agent cannot see everything.**

> **Unknown → Agent does not know how the environment works.**

For example, an Agent could see everything happening in a new game but still not know the rules.

---

# **EXAMPLE: POKER**

Poker can be classified as:

**Partially Observable** — The Agent cannot see the opponent's cards.

**Stochastic** — Cards are randomly dealt.

**Multi-Agent** — Other players are involved.

**Sequential** — Current decisions affect future decisions.

This combination makes Poker significantly more challenging than a simple, fully observable deterministic environment.

---

# **EXAMPLE: SELF-DRIVING CAR**

A self-driving car operates in an environment that is generally:

**Partially Observable**

**Stochastic**

**Sequential**

**Dynamic**

**Continuous**

**Multi-Agent**

This is considered difficult because the physical world combines many of the challenging environment properties.

---

## **WHY THESE PROPERTIES MATTER**

Classifying the environment helps determine what kind of **AI architecture and algorithms** are appropriate.

For example:

**Partially Observable → Internal memory / belief state**

**Stochastic → Probability and Expected Utility**

**Sequential → Planning and Search**

**Dynamic → Fast decision-making**

**Continuous → Algorithms capable of handling continuous values**

The environment classification therefore acts as an **architectural roadmap** for designing an Agent.

---

## **KEY IDEA**

The most important thing to remember is:

> **Before building an AI Agent, classify its Task Environment. The environment's properties determine how the Agent needs to perceive, reason, learn, and act.**

Remember the seven dimensions:

**Observable → Fully / Partially**

**Agents → Single / Multi**

**Outcome → Deterministic / Stochastic**

**Decisions → Episodic / Sequential**

**Change → Static / Dynamic**

**Values → Discrete / Continuous**

**Knowledge → Known / Unknown**

These properties help us understand **how difficult an AI problem is and what type of Agent or algorithm is appropriate for solving it**.
