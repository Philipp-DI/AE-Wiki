# LF5.1.1: The Specification Duel

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Business Analyst,  
> I want to understand the difference between a "Lastenheft" and a "Pflichtenheft",  
> so that I know which document I am responsible for reading or writing during a project.

## 🎉 Celebration Criteria (Learning Objectives)

- I can **define** the terms "Lastenheft" and "Pflichtenheft". (K1)
  
  |     |     |     |
  | --- | --- | --- |
  | **Begriff (DE)** | **Englisch (Common)** | **Beschreibung / Analogie** |
  | **Lastenheft** | **Customer Requirements Specification (CRS)** | Fokus auf die Bedürfnisse des Kunden. |
  |     | **User Requirements Document (URD)** | Oft in der Softwareentwicklung genutzt: Was will der Endnutzer? |
  | **Pflichtenheft** | **Software Requirements Specification (SRS)** | Das technische Dokument, das genau beschreibt, wie die Software funktionieren wird. |
  |     | **Functional Specification** | Fokus auf die Funktionen und das technische "Wie". |
  
- I **know how to differentiate** between the authors and the main focus of both documents. (K2)
- I can **illustrate** the typical chronological order of these documents in a project. (K2)

## 🧠 Knowledge Briefing

Understanding the separation of concerns in requirement documentation is essential, especially in the DACH region.

### **The Document Dualism**

| Document | Lastenheft (Business Requirements Spec.) | Pflichtenheft (System Requirements Spec.) |
| --- | --- | --- |
| **Author** | Customer / Client | Contractor / IT Team |
| **Focus** | **WHAT** needs to be solved & **WHY** | **HOW** the system will technically solve it |
| **Content** | Problems, goals, use cases, constraints | Architectures, tech stacks, data models |
| **Timing** | Written _before_ the project starts | Written _after_ contract signing, before coding |

## ⚠️ Common Pitfalls

- Mixing up who writes what. Remember: _Lastenheft_ = Customer's burden (Last) to explain the problem. _Pflichtenheft_ = Contractor's duty (Pflicht) to explain the solution.

## 🛠️ Mandatory Tasks

1. Write a short definition (max. 2 sentences) for "Lastenheft" and "Pflichtenheft". (K1)
2. Create a 2x2 comparison table listing the "Author" and "Focus (What vs. How)" for both document types. (K2)
3. Explain in your own words why the "Lastenheft" must be completed _before_ the "Pflichtenheft". (K2)
4. List three typical target audiences for a "Lastenheft" (e.g., Management, External Vendors). (K1)
5. Draw a simple chronological timeline showing the creation of the Lastenheft, the contract signing, and the creation of the Pflichtenheft. (K2)

## 🔥 Optional Tasks

1. Analyze the legal significance of a signed Pflichtenheft in the context of a "Werkvertrag" (Contract for Work and Services) in Germany. (K4)
2. Evaluate a scenario where a contractor starts programming based only on a Lastenheft. What are the potential risks? (K5)
3. Design a one-page template for a minimal Lastenheft suitable for a very small IT project. (K5)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Lastenheft vs. Pflichtenheft | Studyflix / YouTube | "Lastenheft Pflichtenheft Unterschied Studyflix" |
| Requirements Engineering | YouTube | "Requirements Engineering Grundlagen IREB" |

</details>

:::info
:::warning
➕ Very strong analysis of the legal significance of a signed Pflichtenheft within a German "Werkvertrag" (§ 631 BGB), correctly referencing the liability guidelines of § 633 BGB.

➖ Your 2x2 comparison table is incomplete. You correctly listed the authors but failed to map and compare the "WHAT" vs. "HOW" (Focus) dimension for both documents.
:::
:::

### M1: Write a short definition (max. 2 sentences) for "Lastenheft" and "Pflichtenheft". (K1)

**Lastenheft:** Drafted by the customer, sometimes in tandem with the contractor. Entails the **WHAT** & **WHY**.

**Pflichtenheft:** Contractor uses the “Lastenheft” as the basis to create a technical requirements document that’s about the **HOW**.

---

### M2: Create a 2x2 comparison table listing the "Author" and "Focus (What vs. How)" for both document types. (K2)

|     | Lastenheft | Pflichtenheft |
| --- | --- | --- |
| **Author** | Customer / Client | IT-Team / Contractor |
| **Focus** | WHAT & WHY (problem & goal) | HOW (technical) |

---

### M3: Explain in your own words why the "Lastenheft" must be completed _before_ the "Pflichtenheft". (K2)

The BRS defines the problem and the customer's goal – the SRS defines the solution and its implementation by the contractor. Logically, it would therefore be nonsensical to start with the functional specifications. If that were the case, the customer's wishes and intentions would be completely disregarded, and the end result would be a technical implementation that very likely has little to nothing in common with the customer's intentions.

---

### M4: List three typical target audiences for a "Lastenheft" (e.g., Management, External Vendors). (K1)

1. **Management** (Budgeting, strategic alignment)
2. **External Contractors** (offers & their creation)
3. **IT-Team / Devs / Contractor** (first overview → projectscope)

---

### M5: Draw a simple chronological timeline showing the creation of the Lastenheft, the contract signing, and the creation of the Pflichtenheft. (K2)

![diagram.drawio.svg](files/019dce1e-598b-7119-965f-529dde3f73d7/diagram.drawio.svg?t=1777281499769)

---

### O1: Analyze the legal significance of a signed Pflichtenheft in the context of a "Werkvertrag" (Contract for Work and Services) in Germany. (K4)

:::warning
Ein unterzeichnetes Pflichtenheft hat im Rahmen eines **Werkvertrags (§ 631 BGB)** erhebliche rechtliche Bedeutung: Es definiert verbindlich den geschuldeten "Werkerfolg". Weicht das gelieferte System von den darin beschriebenen Spezifikationen ab, liegt ein Mangel im Sinne des § 633 BGB vor - der Auftraggeber hat dann **Anspruch auf Nachbesserung**, Minderung oder im Extremfall Schadensersatz. Das Pflichtenheft wird damit faktisch zum **zentralen Beweisdokument** bei Streitigkeiten.
:::

This means the SRS is and its contents are binding and it can be used as a central piece of evidence in case of a dispute. It’s important to have for both parties. As a customer → when there’s a problem with product (e.g. missing feature), I have a a legal claim to have the contractor fix the issue or pay for damages in certain cases. As a contractor → I also have a legal basis with which I can deflect claims from the customer that are out of the scope of the project.

---

### O2: Evaluate a scenario where a contractor starts programming based only on a Lastenheft. What are the potential risks? (K5)

Without a (signed) SRS there are multiple risks:

- **“Scope Creep”:** Client keeps re-iterating their requests and the scope gets out of bounds.
- **Legal uncertainties:** Once the product is finished, both sides could make claims that would be out of scope.
- **Technicalities:** Without architectural premise, the team could use the “wrong” approach, which could end up costly.
- **Missing basis for testing:** QA needs to test against the contents of the SRS → “pass” or “not passed”.

---

### O3: Design a one-page template for a minimal Lastenheft suitable for a very small IT project. (K5)

# “Lastenheft” (Customer/Business Requirements Specifications) - \[projectname\]

**Client:**  
**Date:**  
**Version:**

---

## 1\. Description of the project

\[What is planned (brief summary)?\]

## 2\. Problem

\[What is the underlying problem? How do you imagine this could be solved?\]

## 3\. Ziele

\[What are the decisive goals?\]

## 4\. Requirements

\[What are the requirements for the project?\]

## 5\. Framework

\[How does the framework look like? (e.g. budget, platform)\]

## 6\. Boundaries

\[What is explicitly excluded and NOT in the scope/project?\]

## 7\. Stakeholder

| Name | Role / Position | Contact |
| --- | --- | --- |
| Philipp Phillips | Philipper | philipp.phillips@philippering.phil |