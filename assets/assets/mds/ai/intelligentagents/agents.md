# **AGENTS AND ENVIRONMENTS IN AI**

An **Agent** is anything that can **perceive its environment through sensors and act upon it through actuators**.

The basic interaction is:

**Environment → Sensors → Agent → Actuators → Environment**

---

## **AGENT**

An Agent receives information from its environment and chooses an appropriate action.

**Example:** A self-driving car observes roads and vehicles using sensors and controls steering, brakes, and acceleration using actuators.

### **Sensors**

Sensors allow the Agent to **perceive** the environment.

Examples: Camera, GPS, microphone, radar.

### **Actuators**

Actuators allow the Agent to **perform actions**.

Examples: Wheels, motors, robotic arms, brakes.

---

## **RATIONAL AGENT**

A **Rational Agent** chooses the action that is expected to give the **best performance** based on its available information.

Rationality does not mean the Agent always makes the perfect decision. It means it chooses the best action based on what it currently knows.

---

## **PEAS**

PEAS is used to describe an Agent's **Task Environment**.

**P → Performance Measure** — How success is measured.

**E → Environment** — Where the Agent operates.

**A → Actuators** — How the Agent acts.

**S → Sensors** — How the Agent perceives.

For a self-driving car:

**Performance:** Safety, speed, comfort

**Environment:** Roads, vehicles, pedestrians

**Actuators:** Steering, brakes, accelerator

**Sensors:** Cameras, GPS, radar

---

## **TYPES OF ENVIRONMENTS**

AI environments can be classified as:

**Fully Observable / Partially Observable** — Whether the Agent can observe the complete relevant state.

**Single-Agent / Multi-Agent** — Whether one or multiple Agents are involved.

**Deterministic / Stochastic** — Whether actions have predictable or uncertain outcomes.

**Episodic / Sequential** — Whether the current action affects future situations.

**Static / Dynamic** — Whether the environment changes while the Agent is deciding.

**Discrete / Continuous** — Whether states and actions are separate/countable or continuously varying.

**Known / Unknown** — Whether the Agent knows the rules of the environment.

---

## **TYPES OF AGENTS**

### **Simple Reflex Agent**

Acts only according to the **current percept**.

**Condition → Action**

### **Model-Based Agent**

Maintains an **internal state** to handle partially observable environments.

### **Goal-Based Agent**

Chooses actions that help achieve a specific **goal**.

### **Utility-Based Agent**

Chooses the action that provides the **best utility or outcome**.

### **Learning Agent**

Learns from **experience and feedback** and improves its performance over time.

---

## **KEY IDEA**

The most important concept is:

> **An intelligent Agent perceives its environment, makes a decision, and performs an action to achieve its objective.**

Remember:

**Sensors → Perception**

**Agent → Decision**

**Actuators → Action**

**PEAS → Task Environment**

**Rational Agent → Best expected action**
