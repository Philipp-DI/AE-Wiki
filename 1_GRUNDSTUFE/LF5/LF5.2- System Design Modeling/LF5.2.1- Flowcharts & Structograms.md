# LF5.2.1: Flowcharts & Structograms

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Developer,  
> I want to visualize algorithms using flowcharts (PAP) and structograms (Nassi-Shneiderman),  
> so that I can plan logical sequences without worrying about programming syntax.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can define** the standard symbols used in Flowcharts and Structograms. (K1)
- **I know how to translate** an everyday process into a structured logical diagram. (K3)
- **I can differentiate** between the structural freedom of a PAP and the strict blocks of a Structogram. (K2)

## 🧠 Knowledge Briefing

Algorithms are step-by-step instructions. Before coding, we visualize them to prevent logical errors.

### **Flowchart / Programmablaufplan (PAP - DIN 66001)**

Uses distinct shapes connected by arrows.

- Rectangle: Process / Action
- Diamond/Rhombus: Decision (If/Else)
- Parallelogram: Input / Output
- Oval: Start / End

### Nassi-Shneiderman Structogram (DIN 66261)

Forces "Structured Programming" (no spaghetti code). It uses nested blocks instead of arrows. You read it strictly from top to bottom. It enforces clear loops (while/for) and branching.

## ⚠️ Common Pitfalls

- Getting lost in arrows in a PAP ("Spaghetti Code"). This is why Structograms are often preferred for complex algorithms, as they force you to nest blocks cleanly.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Draw and label the 4 standard PAP symbols (Start/End, Process, Decision, In/Output). (K1)
2. Explain in your own words why Nassi-Shneiderman structograms prevent "spaghetti code" compared to free-flowing PAPs. (K2)
3. Draw a simple analog PAP for the process of "Making a cup of tea" (including a decision like "Add sugar?"). (K3)
4. Convert your "Making a cup of tea" PAP into a strict Nassi-Shneiderman structogram. (K3)
5. Draw and describe the specific symbol/block used to represent a "Loop" (while/for) in a Nassi-Shneiderman diagram. (K1)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze a highly complex PAP with multiple nested loops and identify potential logical dead-ends. (K4)
2. Design a structogram for a sorting algorithm (e.g., Bubble Sort) to sort a list of numbers. (K6)
3. Evaluate the modern relevance of drawing PAPs compared to writing plain-text pseudo-code. (K5)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Programmablaufplan | Studyflix / YouTube | "PAP Programmablaufplan erstellen Studyflix" |
| Nassi-Shneiderman | Studyflix / YouTube | "Nassi Shneiderman Struktogramm einfach erklärt" |

</details>

:::warning
➕ Your analytical breakdown of the "Status" leak in the nested loop structure is exemplary.

➕ The Bubble Sort structogram is structurally and logically flawless.

➖ Mandatory Task 3 explicitly required you to _"Draw a simple analog PAP"_. You submitted a digitally generated diagram instead. Because you did not draw this by hand on paper or a whiteboard, this task is evaluated as **not fulfilled**
:::

### M1: Draw and label the 4 standard PAP symbols (Start/End, Process, Decision, In/Output). (K1)

![diagram.drawio.svg](files/019dd36b-744b-7538-8a32-a7338845ec20/diagram.drawio.svg?t=1777368528037)

---

### M2: Explain in your own words why Nassi-Shneiderman structograms ([**DIN**](https://de.wikipedia.org/wiki/DIN-Norm) **66261)** prevent "spaghetti code" compared to free-flowing PAPs. (K2)

**Free-Flow PAP:** Uses arrows to connect its symbols - which means arrows can be drawn from anywhere to anywhere. In large programmes and/or code you can quickly see how this can get out of hand and form the entangled “spaghetti code”.

**Nassi-Shneiderman Structogram:** Replaces arrows entirely with nested blocks. Every structure (sequence, branch, loop) must fully contain its sub-steps inside a clearly bounded rectangle. There is no way to "jump out" of a block mid-way - you read **strictly from top to bottom**, and every branching or looping construct has a defined beginning and end. The structure of the diagram itself enforces the structure of the algorithm.

**Analogy:** A PAP is like a city map where you can take any route. A structogram is like a building's floor plan - each room is fully enclosed, you cannot walk through walls and the layout is always clear.

---

### M3: Draw a simple analog PAP for the process of "Making a cup of tea" (including a decision like "Add sugar?"). (K3)

![diagram.drawio.svg](files/019dd37a-505e-769b-90d1-305109b5cc80/diagram.drawio.svg?t=1777369501884)

---

### M4: Convert your "Making a cup of tea" PAP into a strict Nassi-Shneiderman structogram. (K3)

![diagram.drawio.svg](files/019dd386-9d94-711a-8357-553e510f2c2e/diagram.drawio.svg?t=1777370414923)

---

### M5: Draw and describe the specific symbol/block used to represent a "Loop" (while/for) in a Nassi-Shneiderman diagram. (K1)

![diagram.drawio.svg](files/019dd392-0856-7709-815b-c17a1c12fd02/diagram.drawio.svg?t=1777371056266)

---

### O1: Analyze a highly complex PAP with multiple nested loops and identify potential logical dead-ends. (K4)

#### **Common dead-end patterns:**

**1\. The infinite validation loop** - A while-loop checks `input valid?`. The No-branch loops back to "Read input" - but if the input source is fixed (e.g. reading from a file that never changes), the condition can never become true. The loop spins forever with no exit.

**2\. Missing else-branch** - A decision diamond has a Yes-branch leading forward, but the No-branch arrow simply... points nowhere, or back to a previous step without a clear termination condition. The analyst drew the happy path and forgot the error case.

**3\. Nested loop with shared counter** - An outer loop runs `i = 1 to n`, and inside it, an inner loop also modifies `i`. The inner loop's increment can push `i` past `n` before the outer loop's condition is checked, causing the outer loop to terminate early - or never terminate if `i` is reset inside the inner loop.

**4\. Unreachable code** - A decision diamond has both branches eventually merging, but one branch passes through another decision whose condition can logically never be true given the path taken to reach it. That sub-branch is structurally reachable in the diagram but logically dead.

**How to spot them systematically:** Trace every possible path from Start to End. For each loop, ask: "Is there guaranteed to be a state change inside this loop that will eventually make the exit condition true?" If the answer is "maybe" or "only if the user behaves correctly" - that's a risk. A well-formed PAP has exactly one answer to that question for every loop: yes, provably.

**From my experience (anecdote):** Modern IDEs (when configured correctly) are pretty good at catching these kinds of logical or structural errors. So in practice, it shouldn’t be too difficult to catch those. But of course, when writing Pseudo-Code and/or drafting ideas, structure, etc. you should keep the aforementioned patterns in mind.

---

### O2: Design a structogram for a sorting algorithm (e.g., Bubble Sort) to sort a list of numbers. (K6)

![diagram.drawio.svg](files/019dd3e1-5b13-75ae-b7c2-e27e61aee8e3/diagram.drawio.svg?t=1777376335868)

---

### O3: Evaluate the modern relevance of drawing PAPs compared to writing plain-text pseudo-code. (K5)

**Where PAPs win:** PAPs are better suited for audiences who aren’t programmers. A decision diamond is universally legible - a business analyst, a client, or a student in their first week of IT can follow the arrows without knowing what `while` or `if` means. For documentation that has to cross professional boundaries, a PAP communicates more broadly.

PAPs also force you to think about flow in a visual, spatial way. Drawing the diagram often reveals that a branch is missing, or that two decision points could be merged - things that are easier to overlook when writing sequential lines of text.

**Where Pseudo-Code wins:** Pseudo-Code scales far better. A PAP for Bubble Sort already fills a page; a PAP for a realistic sorting algorithm with edge cases, error handling and multiple data structures becomes unmanageable. Pseudo-code handles complexity gracefully, can be versioned in Git, copy-pasted into a chat, and of course, transformed into actual code with minimal friction.

Pseudo-Code is also closer to what we as developers actually write. The mental step from `for i = 0 to n-1` in pseudo-code to the equivalent in Python or Java is very small. The same step from a PAP requires re-reading a diagram and then translating it.

**Verdict:** PAPs remain useful as a communication and teaching tool, especially in early-stage planning or when the audience is mixed. For anything beyond a handful of steps, or in professional development workflows, pseudo-code is more practical. Many teams today skip both in favour of writing tests first and letting the implementation emerge - but that is a different conversation entirely.