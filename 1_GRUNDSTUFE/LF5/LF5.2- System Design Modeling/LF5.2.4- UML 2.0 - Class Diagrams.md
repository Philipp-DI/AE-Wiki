# LF5.2.4: UML 2.0 - Class Diagrams

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Software Engineer,  
> I want to model UML Class Diagrams,  
> so that I can define the static structure of an Object-Oriented system, including properties, methods, and inheritances.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can define** the three-part "../LF5.2_ System Design Modeling"structure of a UML Class. (K1)
- **I know how to assign** visibility modifiers to encapsulate data. (K2)
- **I can model** OOP relationships like inheritance, aggregation, and composition. (K3)

## 🧠 Knowledge Briefing

Class Diagrams are the foundation of Object-Oriented Programming (OOP). They show the static blueprint of the code.

**1\. The Class Box:** Divided into three horizontal sections:

- Top: Class Name (e.g., `User`)
- Middle: Attributes / Variables (e.g., `email: String`)
- Bottom: Methods / Functions (e.g., `login(): void`)

**2\. Visibility Modifiers (Encapsulation):**

- `+` Public (Accessible from anywhere)
- `-` Private (Accessible only within the class)
- `#` Protected (Accessible to child classes)

**3\. Relationships:**

- **Association (Solid Line):** A standard connection.
- **Inheritance / Generalization (Hollow Triangle):** An "is-a" relationship (e.g., a `Dog` _is an_ `Animal`).
- **Aggregation (Hollow Diamond):** A "has-a" relationship, but parts can exist independently (e.g., `Team` has `Players`).
- **Composition (Filled Diamond):** A strict "owns-a" relationship. If the parent dies, the child dies (e.g., `House` owns `Room`).

## ⚠️ Common Pitfalls

- Confusing Aggregation and Composition. Ask yourself: "If I delete the main object, do the connected objects still make sense existing on their own?" If yes -> Aggregation. If no -> Composition.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Draw a standard 3-part "../LF5.2_ System Design Modeling"UML Class box for a `User` class. Add private attributes for name and email, and a public method for `logout()`. (K3)
2. Explain the meaning of the visibility modifiers `+`, `-`, and `#`. (K2)
3. Define the Object-Oriented concept of "Inheritance" (Vererbung). (K1)
4. Model a parent class `Vehicle` and a child class `Bicycle` showing the correct UML symbol for inheritance. (K3)
5. Describe the difference between Aggregation and Composition using the real-world metaphor of a "Car and its Engine" vs. a "Car and its Passengers". (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze how declaring an attribute as `-` (Private) improves software security and stability (Encapsulation). (K4)
2. Evaluate how an **m:n** association from an ERM is mapped and resolved inside a UML Class Diagram. (K5)
3. Design a complex Class Diagram for a library system including books, digital media, members, and a strict composition relationship. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| UML Class Diagram | Studyflix / YouTube | "UML Klassendiagramm erstellen Grundlagen" |
| OOP Inheritance | YouTube | "Objektorientierung Vererbung UML" |
| Aggregation vs. Composition | Google | "UML Aggregation Komposition Unterschied" |

</details>

### M1: Draw a standard 3-part "../LF5.2_ System Design Modeling"UML Class box for a `User` class. Add private attributes for name and email, and a public method for `logout()`. (K3)

![diagram.drawio.svg](files/019dd81b-3a43-73dd-8be3-43a1e25233d3/diagram.drawio.svg?t=1777447156449)

---

### M2: Explain the meaning of the visibility modifiers `+`, `-`, and `#`. (K2)

`+` **Public** - the attribute or method can be accessed from anywhere: other classes, external code, subclasses. It is fully exposed. In a well-designed class, only methods that are intentionally part of the public interface should carry this modifier.

`-` **Private** - access is restricted entirely to code within the same class. No other class can read or modify a private attribute directly, not even a subclass. This is the foundation of encapsulation: the class controls its own internal data.

`#` **Protected** - a middle ground. The attribute or method is hidden from unrelated external classes, but subclasses can access it. This is useful in inheritance hierarchies where a parent class wants to share something with its children without making it fully public.

---

### M3: Define the Object-Oriented concept of "Inheritance" (Vererbung). (K1)

Inheritance is the mechanism by which one class (the child or subclass) automatically receives all the attributes and methods of another class (the parent or superclass), and can then add its own or override the inherited ones.

It models an "is-a" relationship: a `Dog` is an `Animal`. A `SavingsAccount` is a `BankAccount`. The child class does not need to re-implement everything the parent already defines - it inherits it for free and only specifies what makes it different.

In UML, inheritance is drawn with a solid line and a hollow (unfilled) triangle arrowhead pointing from the child class toward the parent class.

---

### M4: Model a parent class `Vehicle` and a child class `Bicycle` showing the correct UML symbol for inheritance. (K3)

![diagram.drawio.svg](files/019ddd50-2eac-7732-baac-724d18133ac3/diagram.drawio.svg?t=1777534512954)

---

### M5: Describe the difference between Aggregation and Composition using the real-world metaphor of a "Car and its Engine" vs. a "Car and its Passengers". (K2)

**Composition - Car and its Engine:**

An engine is built into a car and belongs to it completely. If the car is destroyed (say, in an accident and sent to the scrapyard as a crushed cube), the engine does not meaningfully exist as a standalone object anymore either - it goes with the car. The engine's existence depends entirely on the car. This is Composition: a strict "owns-a" relationship where the child cannot survive without the parent. In UML, drawn with a **filled (solid) diamond** on the parent side.

**Aggregation - Car and its Passengers:**

Passengers are inside the car while the car exists and is in use - but they are entirely independent entities. If the car breaks down and gets towed away, the passengers get out and continue their lives. Deleting the car object does not delete the passenger objects. This is Aggregation: a "has-a" relationship where the parts can exist independently of the whole. In UML, drawn with a **hollow (empty) diamond** on the parent side.

**The test question from the course material:** "If I delete the main object, do the connected objects still make sense existing on their own?" Passengers: yes - Aggregation. Engine: no - Composition.

---

### O1: Analyze how declaring an attribute as `-` (Private) improves software security and stability (Encapsulation). (K4)

When an attribute is public, any piece of code anywhere in the application can read or overwrite it directly. There is nothing stopping a developer - or a bug in another class - from setting `user.balance = -99999` or `user.email = null`. The class has no say in how its own data is modified.

Making the attribute private forces all access through the class's own methods (getters and setters). This creates a controlled gateway. The `setBalance()` method can check that the new value is not negative before accepting it. The `setEmail()` method can validate that the string contains an `@` symbol. The class enforces its own invariants - rules about what valid state looks like - and no external code can bypass them.

**Security benefit:** Private attributes prevent accidental or malicious manipulation of sensitive data. An attacker who manages to inject code into a different class cannot directly overwrite a private field - they would have to go through the public method, which can include authentication checks, logging, or rate limiting.

**Stability benefit:** If the internal representation of data ever needs to change (e.g. splitting a `name` attribute into `firstName` and `lastName`), only the class itself needs to be updated. All external code was already talking to the public method, not the field directly - so nothing outside the class breaks. This property is called "loose coupling" and it is one of the main reasons large codebases remain maintainable.

---

### O2: Evaluate how an m:n association from an ERM is mapped and resolved inside a UML Class Diagram. (K5)

In an ERM, an m:n relationship is acceptable as a modelling shorthand - the ERM is a conceptual tool and does not need to reflect implementable database structures. A diamond labeled "attends" between `Student` and `Class` cleanly expresses the real-world situation.

A UML Class Diagram is closer to the actual code. Object-oriented languages cannot directly represent m:n associations between two classes without a container - a `Student` object cannot hold a variable-length list of `Class` references AND a `Class` object cannot simultaneously hold a variable-length list of `Student` references in a flat structure without redundancy and synchronization problems.

The standard resolution is to introduce an **association class** - a third class that represents the relationship itself and holds both foreign keys as attributes. For `Student` and `Class`, this becomes an `Enrollment` class with attributes like `enrollmentDate` and `grade`. It relates to `Student` with a 1:n relationship (one student has many enrollments) and to `Class` with a 1:n relationship (one class has many enrollments). The m:n is fully resolved.

This mirrors exactly what happens at the database level with the linking table - which makes sense, because both the UML class diagram and the relational schema are trying to represent the same reality in implementable form. The ERM is the why; the class diagram and the schema are the how.

---

### O3: Design a complex Class Diagram for a library system including books, digital media, members, and a strict composition relationship. (K6)

![diagram.drawio.svg](files/019ddd5f-9f77-761e-b49b-94ee4866da3a/diagram.drawio.svg?t=1777535524801)