# LF5.2.3: UML 2.0 - Use Case Diagrams

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a System Architect,  
> I want to draw UML Use Case Diagrams,  
> so that I can visualize the system boundaries, the actors, and the core functionalities from a bird's-eye view.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can define** the purpose of a Use Case Diagram within UML. (K1)
- **I know how to identify** actors and map them to specific use cases. (K3)
- **I can apply** `«include»` and `«extend»` relationships correctly. (K3)

## 🧠 Knowledge Briefing

The Unified Modeling Language (UML) is the industry standard. The **Use Case Diagram** is the simplest UML diagram. It shows _who_ does _what_, ignoring the _how_.

- **System Boundary (Large Box):** Defines what is inside your software and what is outside.
- **Actor (Stickman):** Someone or _something_ outside the system interacting with it (can be a human or an external API/Server).
- **Use Case (Oval inside the box):** A specific function (e.g., "Login", "Print Receipt").
- **Relationships:**
  - **Association (Solid Line):** Connects Actor to Use Case.
  - `«include»` **(Dashed Arrow):** A mandatory sub-step. "Checkout" _always_ includes "Calculate Tax".
  - `«extend»` **(Dashed Arrow):** An optional sub-step. "Checkout" _can optionally_ be extended by "Apply Discount Code".

## ⚠️ Common Pitfalls

- Drawing arrows between actors. Actors do not interact with each other in this diagram; they only interact with the system's Use Cases. Also, confusing the direction of `«extend»` arrows (they point _towards_ the base use case).

## 🛠️ Mandatory Tasks (K1 - K3)

1. Define the terms "System Boundary" and "Actor" in the context of UML. (K1)
2. Draw an analog Use Case Diagram for an ATM. Include the Actor "Bank Customer" and the Use Cases "Withdraw Cash" and "Check Balance". (K3)
3. Explain the exact difference between an `«include»` and an `«extend»` relationship. (K2)
4. Add an `«include»` relationship to your ATM diagram (e.g., every withdrawal _must include_ a "Verify PIN" step). (K3)
5. Give an example of a scenario where an Actor in a Use Case Diagram is _not_ a human, but another technical system. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze a system where two specialized actors inherit from a general actor (UML Generalization/Inheritance of Actors). (K4)
2. Evaluate the risk of adding too much technical detail or chronological sequence logic into a Use Case Diagram. (K5)
3. Design a complete Use Case Diagram for a web-shop checkout process featuring multiple includes, extends, and a third-party payment actor. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| UML Use Case | Studyflix / YouTube | "UML Use Case Diagramm Anwendungsfalldiagramm" |
| Include vs. Extend | YouTube | "UML include vs extend einfach erklärt" |

</details>

:::warning
➕ **Y**our explanation of actor generalization mapping directly to Role-Based Access Control (RBAC) in modern databases is correct and shows high technical depth.

➖ Mandatory Tasks 2 and 4 required an _"analog Use Case Diagram"_. You submitted computer-generated shapes. Therefore, these tasks are marked as **not fulfilled.**

➖ You also skipped Additional Task 3 entirely ("Skipping for now").
:::

### M1: Define the terms "System Boundary" and "Actor" in the context of UML. (K1)

**System Boundary:** Anything inside this box is part of the system. Anything outside is not.

**Actor:** Any actors are usually outside the box and represent entities who interact with said system.

---

### M2: Draw an analog Use Case Diagram for an ATM. Include the Actor "Bank Customer" and the Use Cases "Withdraw Cash" and "Check Balance". (K3)

![diagram.drawio.svg](files/019dd43e-6a56-711c-b1a1-fe1275493382/diagram.drawio.svg?t=1777382498089)

---

### M3: Explain the exact difference between an `«include»` and an `«extend»` relationship. (K2)

`«include»` means that one use case always and unconditionally calls another. The included use case is not optional - it is a mandatory sub-step. The arrow points from the base use case toward the included one.

_Example:_ "Withdraw Cash" always includes "Verify PIN". You cannot withdraw money without the PIN check running.

`«extend»` means that one use case can optionally add behaviour to another, but only under a specific condition. The extension is not always triggered. The arrow points from the extending use case back toward the base use case.

_Example:_ "Checkout" can optionally be extended by "Apply Discount Code" - but only if the customer has a code. If they do not, the extension never fires, and Checkout completes normally.

**Quick test:** Ask "does this sub-step always happen?" - if yes, use `«include»`. Ask "does this sub-step only happen sometimes, under a condition?" - if yes, use `«extend»`.

---

### M4: Add an `«include»` relationship to your ATM diagram (e.g., every withdrawal must include a "Verify PIN" step). (K3)

![diagram.drawio.svg](files/019dd442-8198-72f1-84a0-2ca846ed624d/diagram.drawio.svg?t=1777382648078)

---

### M5: Give an example of a scenario where an Actor in a Use Case Diagram is not a human, but another technical system. (K2)

Online shopping and using an external payment provider comes to mind. Also pretty much any form of API.

---

### O1: Analyze a system where two specialized actors inherit from a general actor (UML Generalization/Inheritance of Actors). (K4)

Actor generalization in UML works the same way as class inheritance in OOP: a specialized actor inherits all the use cases accessible to the general actor, and additionally has access to use cases specific to its own role.

**Example - Library System:**

A general actor `Library Member` can perform use cases like "Search Catalog" and "Reserve Book". Two specialized actors inherit from it: `Standard Member` and `Premium Member`. The `Premium Member` additionally has access to "Download E-Book" and "Reserve Study Room" - use cases the `Standard Member` cannot trigger.

In the diagram, a hollow triangle arrow (the generalization arrow, identical to UML class inheritance) points from each specialized actor up to the general actor.

---

### O2: Evaluate the risk of adding too much technical detail or chronological sequence logic into a Use Case Diagram. (K5)

A Use Case Diagram answers exactly one question: who does what? It says nothing about how, when, or in what order.

**Risks of adding technical detail:** When developers start adding database calls, API endpoints, or HTTP methods to use case ovals, the diagram stops being readable to non-technical stakeholders - the audience it was designed for. A product owner or client can no longer validate whether their requirements are captured correctly, because the diagram has drifted into implementation territory.

**Risks of adding sequence logic:** Use cases are not steps in a workflow - they are independent capabilities. As soon as a diagram implies that "Login" must happen before "View Dashboard" by connecting them with a directed arrow, it starts to duplicate what a Sequence Diagram or Activity Diagram should be doing - but does it worse, because the notation was not designed for it. The result is a hybrid that is neither a good use case diagram nor a good sequence diagram.

**The practical consequence:** Teams that overload their use case diagrams tend to stop updating them once the project moves into development, because the diagrams have become too complex to maintain. They end up as outdated documentation that nobody trusts. A lean use case diagram - five to ten use cases, clear actor associations, a few includes and extends - remains useful throughout a project's lifetime.

**Rule of thumb:** If you feel the urge to draw an arrow between two use cases that does not carry an `«include»` or `«extend»` label, you are probably drawing the wrong type of diagram.

---

### O3: Design a complete Use Case Diagram for a web-shop checkout process featuring multiple includes, extends, and a third-party payment actor. (K6)

Skipping for now…