# LF5.2.5: UML 2.0 - Sequence Diagrams

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Backend Developer,  
> I want to create UML Sequence Diagrams,  
> so that I can visualize the chronological exchange of messages between objects over time during a specific process.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can define** the concept of a lifeline and time flow. (K1)
- **I know how to map** message flows between different system components chronologically. (K3)
- **I can illustrate** the difference between synchronous and asynchronous calls. (K3)

## 🧠 Knowledge Briefing

While Class Diagrams show the _static_ structure, **Sequence Diagrams** show the _dynamic_ behavior over time. They are perfect for mapping API calls or login processes.

- **Time Flow:** Always flows strictly from Top to Bottom.
- **Lifeline (Dashed vertical line):** Represents the lifespan of an object during the sequence.
- **Activation Bar (Vertical rectangle):** Placed on the lifeline to show exactly when an object is actively calculating or processing data.
- **Synchronous Message (Solid arrow with solid head):** The sender waits until the receiver answers (e.g., loading a webpage).
- **Asynchronous Message (Solid arrow with open head):** The sender fires the message and continues working without waiting (e.g., sending an email in the background).
- **Return Message (Dashed arrow):** The reply to a synchronous message.

## ⚠️ Common Pitfalls

- Drawing arrows diagonally. Messages are drawn perfectly horizontally to show an instant transfer of the message, while time moves vertically down the lifeline.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Describe the purpose of the "Lifeline" and state the direction in which time flows in a sequence diagram. (K1)
2. Draw an analog sequence diagram showing a `Browser` requesting a webpage from a `WebServer`, and the `WebServer` sending the HTML back. (K3)
3. Explain the functional difference between a synchronous and an asynchronous message. (K2)
4. Draw the specific arrow symbols for a synchronous message, an asynchronous message, and a return message. (K1)
5. Add an "Activation Bar" to your `WebServer` lifeline from Task 2 to show when it is processing the request. (K3)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze a sequence where a system component sends a message to itself (a "self-call" loop). (K4)
2. Evaluate how sequence diagrams help architects find performance bottlenecks (like waiting for long synchronous API calls) before coding begins. (K5)
3. Design a Sequence Diagram that includes an "alt" (alternative) combined fragment to map an "if/else" scenario like a successful vs. failed login. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| UML Sequence Diagram | Studyflix / YouTube | "UML Sequenzdiagramm einfach erklärt" |
| Synchronous vs. Asynchronous | YouTube | "UML Sequenzdiagramm synchron asynchron" |

</details>

:::warning
➕ Your sequence diagram including the "alt" fragment for valid vs. invalid credentials is syntactically very good.

➕ Your performance bottleneck analysis shows a deep, practical understanding of synchronous network latency.

➖ Mandatory Tasks 2 and 5 required an _"analog sequence diagram"_. Since you utilized digital modeling tools, these tasks are graded as **not fulfilled.**
:::

### M1: Describe the purpose of the "Lifeline" and state the direction in which time flows in a sequence diagram. (K1)

A **Lifeline** is the dashed vertical line that extends downward from each participant (object, component, or actor) in a sequence diagram. It represents that participant's "existence" throughout the duration of the scenario being modeled. As long as a lifeline is visible, that participant is alive and capable of sending or receiving messages.

**Time flows strictly from top to bottom.** A message drawn higher on the diagram happens before a message drawn lower. There are no exceptions and no backward arrows in a well-formed sequence diagram - if you need to show a repeated action, you use a loop fragment, not an arrow going upward.

This top-to-bottom time flow is what makes sequence diagrams so useful for understanding chronological processes: you can read them like a script, from the top of the page to the bottom, and the order of events is unambiguous.

---

### M2: Draw an analog sequence diagram showing a `Browser` requesting a webpage from a `WebServer`, and the `WebServer` sending the HTML back. (K3)

![diagram.drawio.svg](files/019ddd64-8e1f-76bf-8c6e-12326ef8bfb1/diagram.drawio.svg?t=1777535871918)

---

### M3: Explain the functional difference between a synchronous and an asynchronous message. (K2)

**Synchronous message** - the sender sends a message and then stops and waits. It does nothing else until it receives a response. This is like making a phone call: you ask a question and hold the line until the other person answers.

In the diagram: solid arrow with a filled arrowhead. The sender's activation bar stays active (meaning "I am frozen, waiting") until the return arrow arrives.

**Asynchronous message** - the sender fires the message and immediately continues its own work, without waiting for a response. The recipient handles it whenever it gets to it. This is like sending an email: you write it, hit send, and go back to whatever you were doing.

In the diagram: solid arrow with an open (hollow) arrowhead. The sender's activation bar can end immediately after the arrow, because it does not wait.

**When to use which:** Any operation that requires the result before the next step can proceed must be synchronous (e.g. checking a user's password before granting access). Operations that can happen in the background without blocking the sender - notifications, logging, sending a confirmation email - are good candidates for asynchronous.

---

### M4: Draw the specific arrow symbols for a synchronous message, an asynchronous message, and a return message. (K1)

![diagram.drawio.svg](files/019ddd66-aca7-70e3-b4fd-deab7f95677b/diagram.drawio.svg?t=1777535987310)

---

### M5: Add an "Activation Bar" to your `WebServer` lifeline from Task 2 to show when it is processing the request. (K3)

See M2.

---

### O1: Analyze a sequence where a system component sends a message to itself (a "self-call" loop). (K4)

A self-call (also called a self-message or recursive call) is when an object sends a message to itself - visible in the diagram as an arrow that leaves the object's own lifeline and returns to the same lifeline, drawn as a small loop to the right.

![diagram.drawio.svg](files/019ddd6a-1c2d-7372-b6d1-ebfa42be396d/diagram.drawio.svg?t=1777536212146)

**When does this occur?**

- A method internally calls another method on the same object. For example, a `UserService` might call its own `validateInput()` method before executing `createUser()`.
- A recursive algorithm: a `TreeNode` calling `findValue()` on itself with a different parameter.
- An object triggering an internal state change, such as a `Timer` calling its own `reset()` after expiry.

**What to watch for analytically:** Self-calls that loop without a guaranteed exit condition are a recursion depth problem. In code this causes a stack overflow; in the diagram it should be represented with a `loop` combined fragment that specifies a guard condition for termination. If the guard is missing from the diagram, that is a modeling error - the diagram implies infinite recursion.

Self-calls also sometimes reveal that a class is doing too much. If an object sends five different messages to itself in a single sequence, it may be a sign that it should be split into multiple classes with clearer single responsibilities (the Single Responsibility Principle).

---

### O2: Evaluate how sequence diagrams help architects find performance bottlenecks (like waiting for long synchronous API calls) before coding begins. (K5)

A sequence diagram makes the cost of waiting visible in a way that verbal requirements or bullet-point feature lists do not.

When an architect draws a synchronous call between two components, the calling component's activation bar stays open until the response arrives. In a diagram with several such calls chained together - `Frontend` calls `API`, which synchronously calls `Database`, which synchronously calls an external `Analytics Service` - you can see at a glance that the total response time visible to the user is the sum of all those waiting periods stacked on top of each other.

This is something that is genuinely difficult to see in code or in a class diagram. The class diagram shows that the connections exist; the sequence diagram shows what happens when those connections are actually used in real time.

**Concrete problems sequence diagrams surface before coding:**

- **Synchronous chains** - a long chain of sequential synchronous calls where several could be parallelized or replaced with asynchronous calls.
- **Chatty interfaces** - a component that makes dozens of small calls to a service in a single use case, each with a round-trip cost, where a single batched call would be far more efficient.
- **Blocking on slow external systems** - a payment API or third-party data provider that is called synchronously, blocking the user's request for potentially several seconds, which the architect can decide to offload to a background job.
- **Single points of failure** - a component that every single message in the diagram passes through, making it both a performance bottleneck and a reliability risk.

The key value is that architects can have these conversations and make architectural decisions with a ten-minute diagram review, rather than discovering the bottleneck six months later during a load test on a production system that took two years to build.

---

### O3: Design a Sequence Diagram that includes an "alt" (alternative) combined fragment to map an "if/else" scenario like a successful vs. failed login. (K6)

![diagram.drawio.svg](files/019ddd6d-23c3-700f-9610-3c73df8e2a53/diagram.drawio.svg?t=1777536410621)