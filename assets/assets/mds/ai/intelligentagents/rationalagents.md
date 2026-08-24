# **RATIONAL AGENTS AND EXPECTED UTILITY**

A **Rational Agent** is an AI Agent that chooses the action expected to **maximize its utility or performance measure**, based on the information currently available to it. This turns the idea of "being intelligent" into a mathematical decision-making problem. 

---

## **RATIONALITY**

A rational Agent does **not** necessarily make the correct decision every time.

It makes the **best possible decision based on what it currently knows**, including its percepts, knowledge, available actions, and the uncertainty of the environment.

> **Rationality ≠ Omniscience**

An **Omniscient Agent** would know the actual outcome of every action in advance.

A **Rational Agent** only uses the information available to it and chooses the action with the best expected outcome. 

---

## **EXPECTED UTILITY**

When outcomes are uncertain, a Rational Agent uses **Expected Utility (EU)** to compare actions.

The basic formula is:

**EU(a) = Σ P(s' | s, a) × U(s')**

Where:

**P(s' | s, a)** = Probability of reaching state s' after taking action a

**U(s')** = Utility or reward of that resulting state

The Agent calculates the expected utility of its available actions and chooses the one with the **highest Expected Utility**. 

---

## **EXAMPLE**

Suppose an Agent has two choices:

**Shortcut:**

80% chance of reward **10**

20% chance of reward **-50**

Expected Utility:

**(0.8 × 10) + (0.2 × -50) = -2**

**Highway:**

100% chance of reward **5**

Expected Utility:

**1.0 × 5 = 5**

Since **5 > -2**, the Rational Agent chooses the **Highway**.

The important idea is that the Agent does not simply choose the action with the highest probability of success. It considers both **probability and consequence**. 

---

## **AUTONOMY**

A truly **Autonomous Agent** can learn from its environment and improve its decisions instead of depending entirely on the knowledge provided by its programmer.

If the environment changes, an autonomous Agent should be able to **adapt its internal knowledge and behavior**.

Therefore:

**Experience → Learning → Better Decisions** 

---

## **EXPLORATION VS EXPLOITATION**

A Rational Agent must often balance two choices:

**Exploitation:** Choose the best action currently known.

**Exploration:** Try an action that may not currently seem optimal but could provide useful information.

Exploration can help the Agent learn more about an unknown environment and make better decisions in the future. 

---

## **VALUE ALIGNMENT PROBLEM**

The **Value Alignment Problem**, sometimes illustrated by the **King Midas Problem**, occurs when an Agent is given a poorly defined goal.

A highly capable Rational Agent will aggressively optimize the **Performance Measure it is given**, even if the result has harmful unintended consequences.

Therefore:

> **A powerful Agent with a badly specified objective can produce disastrous results.** 

---

## **BOUNDED RATIONALITY**

In the real world, an Agent cannot calculate every possible future outcome because the number of possible states can become enormous.

Therefore, instead of calculating the absolute perfect decision, Agents often use:

**Heuristics**

**Approximations**

**Monte Carlo methods**

and other techniques to find a **good enough decision within available computational resources**. 

---

## **KEY IDEA**

The main concept is:

> **A Rational Agent chooses the action that maximizes Expected Utility based on the information currently available.**

Remember:

**Rationality → Best expected decision**

**Expected Utility → Probability × Utility**

**Omniscience → Perfect knowledge of actual outcomes**

**Autonomy → Learning and adapting from experience**

**Exploration → Learning more**

**Exploitation → Using the best-known option**

**Value Alignment → Correctly defining the Agent's objective**

**Bounded Rationality → Making good decisions despite limited computation**
