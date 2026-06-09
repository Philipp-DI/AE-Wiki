# LF5.2.2: Entity-Relationship Modeling (ERM)

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Database Designer,  
> I want to create Entity-Relationship Models,  
> so that I can logically structure data and define relationships before creating physical database tables.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can identify** entities, attributes, and primary keys from a text. (K1)
- **I know how to construct** relationship cardinalities between entities. (K3)
- **I can define** the purpose of an ERM in the software design phase. (K1)

## 🧠 Knowledge Briefing

An ERM (often using Chen Notation) is the architectural blueprint of a relational database.

- **Entity (Rectangle):** A real-world object or concept (e.g., `Customer`, `Product`).
- **Attribute (Oval):** A property of an entity (e.g., `Name`, `Price`).
- **Primary Key (Underlined Oval):** A unique identifier for an entity instance (e.g., `CustomerID`).
- **Relationship (Diamond):** How entities interact (e.g., `Customer` - _buys_ - `Product`).
- **Cardinality:** Defines the quantity of the relationship:
  - **1:1** (One-to-One): One manager manages one department.
  - **1:n** (One-to-Many): One customer places many orders.
  - **m:n** (Many-to-Many): Many students attend many courses.

## ⚠️ Common Pitfalls

- Forgetting to assign a Primary Key. Every entity _must_ have a unique identifier, otherwise, the database cannot distinguish between two customers with the name "John Doe".

## 🛠️ Mandatory Tasks (Bloom K1 - K3)

1. Define the terms "Entity", "Attribute", and "Primary Key". (K1)
2. Draw the standard Chen Notation symbols for an Entity, an Attribute, and a Relationship. (K1)
3. Identify a suitable Primary Key for an entity named "Car" from this list: Color, Brand, License_Plate, Top_Speed. Justify your choice. (K2)
4. Draw an analog ERM showing a `Customer` who `Orders` a `Package`. Assign at least 2 attributes to each entity and set a **1:n** cardinality. (K3)
5. Explain the concept of an **m:n** (many-to-many) relationship using the entities `Authors` and `Books`. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze how relational databases resolve an **m:n** relationship technically (hint: linking table / association entity). (K4)
2. Evaluate the visual differences and benefits of using Crow's Foot notation instead of classic Chen notation. (K5)
3. Design an ERM for a school system including Teachers, Students, Classes, and Classrooms with exact cardinalities. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| ER Model Basics | Studyflix / YouTube | "ER Modell Chen Notation Grundlagen" |
| ERM Cardinalities | YouTube | "Datenbank Kardinalitäten 1:n m:n erklärt" |

</details>

:::warning
➕ Your database blueprint for the school system is very good normalized.

➕ Your comparison of Chen and Crow's Foot is highly professional.

➖ Mandatory Task 4 explicitly demanded an _"analog ERM"_. Your submission is completely digital. Consequently, this task is evaluated as **not fulfilled.**
:::

### M1: Define the terms "Entity", "Attribute", and "Primary Key". (K1)

**Entity:** Any real-world object or concept that is distinct enough to be stored in a database on its own. It represents a category of things, such as: `Customer`, `Product`, `Order`. An entity would be the **table heading**.

**Attribute:** A specific property or characteristic that describes an entity. For `Customer`, attributes might be `Name`, `Email` and `Date of Birth`. These become the **columns** in a database table.

**Primary Key:** The one attribute (or minimal combination of attributes) that **uniquely** identifies every single instance of an entity. No two rows may share the same primary key value, and it can never be empty. For `Customer`, `CustomerID` is a clean primary key - two customers can share a name, but never an ID.

---

### M2: Draw the standard Chen Notation symbols for an Entity, an Attribute, and a Relationship. (K1)

![diagram.drawio.svg](files/019dd40b-07b6-71c9-8188-be82cfd14178/diagram.drawio.svg?t=1777378986751)

---

### M3: Identify a suitable Primary Key for an entity named "Car" from this list: Color, Brand, License_Plate, Top_Speed. Justify your choice. (K2)

The primary key would be **License_Plate**.

All other attributes wouldn’t be unique, not even in any combination. The License Plate though is different for every car. (Anecdote: There might be real-world exceptions to this. That’s the VIN would be a better choice.)

---

### M4: Draw an analog ERM showing a `Customer` who `Orders` a `Package`. Assign at least 2 attributes to each entity and set a 1:n cardinality. (K3)

![diagram.drawio.svg](files/019dd416-bb03-74be-bce3-8cba40bdeafc/diagram.drawio.svg?t=1777379943209)

---

### M5: Explain the concept of an m:n (many-to-many) relationship using the entities `Authors` and `Books`. (K2)

A many-to-many relationship means that instances on both sides of the relationship can be linked to multiple instances on the other side. With `Authors` and `Books`: one author can write many books and one book can also be written by many authors.

In a relational database, an m:n relationship cannot be stored directly in two tables alone - it requires a third linking table (→ Associative Entity).

---

### O1: Analyze how relational databases resolve an m:n relationship technically (hint: linking table / association entity). (K4)

As briefly mentioned above, we need a linking table / associative entity to model the DB.

For `Authors` and `Books`:

| Author_ID (FK) | Book_ID (FK) |
| --- | --- |
| 1   | 101 |
| 1   | 102 |
| 2   | 101 |
| 3   | 103 |

This table combines the primary keys of their “parents”: Author 1 wrote Books 101 and 102. Book 101 was written by Authors 1 and 2. The m:n relationship is now represented as two 1:n relationships - one from `Authors` to this linking table, and one from `Books` to this linking table.

The combination of `(AuthorID, BookID)` typically forms a **composite primary key** for the linking table, ensuring the same author-book pairing cannot appear twice.

---

### O2: Evaluate the visual differences and benefits of using Crow's Foot notation instead of classic Chen notation. (K5)

Auto-generated answer:

> Chen notation was designed in 1976 as an academic modeling tool, and it shows. The diamond shapes for relationships and separate ovals for every attribute produce diagrams that expand rapidly - a simple three-entity model can fill an A3 sheet. Chen is expressive and precise, but it is not compact.
> 
> **Crow's Foot notation** (also called IE notation, developed by Gordon Everest) takes a different approach: relationships are shown directly on the connecting lines between entity rectangles, and attributes are listed inside the entity box as rows - exactly like a database table. The "crow's foot" symbol (three lines fanning out, like a bird's foot) appears on the line's end to indicate "many", while a single line indicates "one". A circle indicates "zero" (optional), a vertical bar indicates "one" (mandatory).
> 
> **Practical benefits of Crow's Foot:**
> 
> - Much more compact - attributes live inside the entity box, not floating around it as separate ovals
> - The cardinality notation is directly on the line, so you read it in one glance without tracing back to a diamond
> - Industry tools (MySQL Workbench, Lucidchart, [draw.io](http://draw.io), [dbdiagram.io](http://dbdiagram.io)) default to Crow's Foot because it maps directly to what a database table looks like
> - Better suited for large schemas with many entities - a Chen diagram with 15 entities becomes unreadable, a Crow's Foot version remains navigable
> 
> **Where Chen still wins:** For teaching and early conceptual modeling, Chen's explicit diamonds for relationships make the model's logic more visible. The separation of "what exists" (entities) and "how they relate" (diamonds) aids understanding when students are still building the concept. Crow's Foot collapses this distinction in favor of compactness.
> 
> In professional practice today, Crow's Foot is the dominant standard.

---

### O3: Design an ERM for a school system including Teachers, Students, Classes, and Classrooms with exact cardinalities. (K6)

![diagram.drawio.svg](files/019dd42e-87a4-721a-8dfa-1d518b10460f/diagram.drawio.svg?t=1777381772202)