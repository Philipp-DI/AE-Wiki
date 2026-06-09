# LF5.2: System Design Modeling

<details>
<summary>**Briefing**</summary>

## 👥 Epic User Story

> As IT Consultants,  
> we want to design the system architecture and logic visually before writing any code,  
> so that we can identify structural flaws early, align with stakeholders, and provide clear blueprints for the implementation phase.

## 🎉 Celebration Criteria (Core Competencies)

- **We can construct** an Entity-Relationship Model (ERM) to structure the chosen scenario's data logically. (K6)
- **We can design** UML 2.0 Use Case and Class diagrams to map out the system's actors and object structures. (K6)
- **We can develop** analog workflow diagrams (PAP/Structograms) for core algorithms before digitizing them. (K5)
- **We can evaluate** our architectural models against the requirements from the previously written "Lastenheft". (K6)

## 🧩 Comprehensive Task: The Architecture Blueprint (13 SP)

**The Mission:** Based on the "Lastenheft" you created in Epic 5.1 for your chosen scenario (Neustadt Museum, Mutti's Bakery, or Metropolis Library), you must now design the technical blueprint. Do not write code yet! You must map out the database, the user interactions, the object structures, and the core algorithms using standard modeling languages.

### Tasks

1. **Database Foundation (ERM):** Using a whiteboard, draw an Entity-Relationship Model containing at least 4 core entities for your scenario. Define their primary keys, attributes, and exact cardinalities (1:1, 1:n, m:n).
2. **System Boundaries (Use Case):** Draw an analog UML Use Case Diagram identifying all human and external system actors. Map out at least 5 main use cases, utilizing `«include»` or `«extend»` relationships where appropriate.
3. **Static Structure (Class Diagram):** Based on your ERM and Use Cases, design an analog UML Class Diagram featuring at least 3 associated classes. Include visibility modifiers (+, -, #), attributes, and essential methods. Show at least one inheritance ("is-a") or aggregation ("has-a") relationship.
4. **Dynamic Logic (PAP/Structogram):** Identify the most complex algorithm in your scenario (e.g., scaling a recipe, calculating late fees). Create a Flowchart (PAP) or Nassi-Shneiderman Structogram detailing this specific logical process.
5. **Digitization & Review:** Once all analog models are verified by your team, recreate them cleanly in the digital workspace **AFFiNE**. Compile them into a single Architecture Document.

## **📦 Result Artifact**

An "Architecture Blueprint" (exported as PDF or shared via AFFiNE workspace) containing the digitized ERM, UML Use Case, UML Class Diagram, and PAP/Structogram, accompanied by photographic proof of your analog drafts.

</details>
<details>
<summary>**Chosen Scenario**</summary>

## Scenario B: Mutti's Recipe Collection (The Bakery Scale-Up)

- **Industry:** Food & Beverage / Retail
- **Initial Situation:** "Mutti's Backstube" is a local legend. They are expanding to three new locations. However, the business relies on founder Martha's secret recipes, which are stored in a physical, flour-dusted binder. The recipes use inconsistent units ("2 cups of flour", "500g sugar", "a large pinch of salt") and lack precise scaling factors for industrial production.
- **The Mission:** You must translate this unstructured, analog knowledge into a strict digital format. You will design a system that normalizes ingredients, calculates nutritional values, and allows bakers to scale recipes from 10 to 1,000 portions automatically.
- **Your Main Stakeholder:** **Martha "Mutti" Klein (Founder & Master Baker)**. She is skeptical of "the cloud" and fears her recipes will be stolen. She values tradition over efficiency but understands the business need. The solution must be foolproof for tired kitchen staff working at 3 AM.
- **Special Challenge:** Standardizing highly variable analog data (measurements) and ensuring the digital prototype is usable in a messy kitchen environment (e.g., via a tablet interface).

</details>

# **Architecture Blueprint – Mutti's Recipe Management System**

**Based on:** Lastenheft LF5.1 (Mutti's Secret)

**Epic:** LF5.2 – System Design Modeling

---

### Introduction

This document presents the technical **Architecture Blueprint** for Mutti's Recipe Management System as part of Epic LF5.2. The goal is to design the system architecture and logic visually before writing any code, in order to identify structural flaws early, align with stakeholder expectations, and provide clear blueprints for the implementation phase.

**Reason for choosing the Scenario:** We selected **Scenario B: Mutti's Recipe Collection (The Bakery Scale-Up)** because it presents a rich set of modeling challenges, including complex data normalization, dynamic scaling algorithms, unit conversion logic, strong security and usability requirements in a harsh kitchen environment, and clear role-based access control. This scenario allows full demonstration of all required modeling techniques (ERM, UML Use Case, UML Class Diagram, and dynamic workflow).

## Digital Artifacts (made with draw.io)

![diagram.drawio.svg](files/019dfc48-c5fe-7099-a2a6-a179c460bb8e/diagram.drawio.svg?t=1778677083144)

---

**UML Use Case Diagram**

This Use Case diagram illustrates the functional requirements of the system. It highlights a specialized **Bake Mode** designed for kitchen environments, allowing for hands-free operation via foot pedals and/or voice hints. It also ensures data integrity through mandatory **PIN authentication** and administrative **Audit Trails**.

![diagram.drawio.svg](files/019e20fb-ad2c-7645-8e46-575f9b47754f/diagram.drawio.svg?t=1778670096430)

---

![diagram.drawio.svg](files/019e20fc-532e-70bb-bdbd-ea2da8aee35e/diagram.drawio.svg?t=1778669868142)

---

![diagram.drawio.svg](files/019e20fc-cde5-741b-94de-6dfa0673de3f/diagram.drawio.svg?t=1778669899378)

---

---

# Workshop - Übung

## Szenario / Kontext

**Teilnehmer:innen** eines Ausbildungskurses zu Fachinformatiker:innen sollen ihre **Anwesenheiten im Kurs selbst erfassen**.

Hierfür müssen **mindestens Beginn und Ende der Teilnahme eines Tages** erfasst werden. Eine **zweifelsfreie Zuordnung** von Teilnehmer:in zu Zeitbuchung muss sichergestellt sein. Die tägliche Anwesenheitsdauer soll **7,5h Tätigkeitszeit** betragen. Gesetzliche Vorgaben schreiben mindestens eine **Pause nach spätestens 6h Tätigkeit** vor. Betriebliche Vorgaben sehen einen täglichen Beginn um **09:00h und ein tägliches Ende um 17:00h** vor. An Wochenenden, gesetzlichen Feiertagen, betrieblichen Ruhetagen sollen **keine Buchungen möglich** sein.

Alle täglich erfassten Zeiten müssen als **Einträge in einer Datenbank** vorgehalten werden.

**Mitarbeiter:innen** des Student Success Managements (SSM) müssen die Einträge prüfen können. Sie sollen Fehlzeiten dokumentieren können, dies muss als krankheitsbedingt (Arbeitsunfähigkeits Bescheinigung), autorisiert oder unautorisiert möglich sein. Das SSM muss pro Teilnehmer:innen **Reports über die Anwesenheitszeiten erstellen können**. Reports sollen über beliebige Zeiträume möglich sein.

Teilnehmer:innen sollen zu jeder Zeit **ihre Daten einsehen** können, die Einsicht **anderer als der eigenen Datensätze muss unmöglich** sein. Teilnehmer:innen sollen keine Einträge editieren, **Mitarbeiter:innen SSM müssen Einträge editieren**.

### Aufgaben

1. Erstelle grafisch ein ER-Modell des geschilderten Szenarios.
2. Erstelle exemplarisch je ein Use Case Diagram für die Anwendungsfälle “Zeitbuchung durchführen” und “Zeitbuchungssatz editieren” entsprechend dem Modell aus Aufgabe 1.
3. Erstelle exemplarisch ein schematisches Klassendiagramm für ein Objekt deiner Wahl aus dem Modell aus Aufgabe 1.
4. Erstelle grafisch einen grobschematischen Ablaufplan für den Prozess “Start-Zeitpunkt der Tätigkeit buchen”.
5. Erstelle ein Nassi-Shneiderman-Diagram zur Plausibilitätsprüfung eines Datensatzes vor seiner Anlage gemäß o.g. Szenarios

### ER-Modell

![diagram.drawio.svg](files/019df256-4db8-739c-9923-33f7e02aa6eb/diagram.drawio.svg?t=1778230546501)