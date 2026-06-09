# LF5.1: Artifact / Epic

<details>
<summary>Briefing</summary>

## 👥 Epic User Story

> As IT Consultants,  
> **we** want to systematically analyze unstructured customer data and formulate clear, binding requirements,  
> so that **we** can design a software solution that precisely solves the customer's problem without wasting development resources.

## 🥳 Celebration Criteria (Core Competencies)

- We can **analyze** unstructured data sets and categorize core problems. (K4)
- We **know how to formulate** functional and non-functional requirements using standard syntax (IEEE 29148) and quality characteristics (ISO/IEC 25010). (K5)
- We can **design** a formal "Lastenheft" (Requirements Specification) structure based on industry standards. (K5)
- We can **create** and digitize an analog cluster of requirements to build a final specification document. (K6)

## 🧩 Comprehensive Task: The "Lastenheft" (13 SP)

**The Mission:** Your stakeholder has provided you with a pile of chaotic, unstructured information regarding their current crisis. Before you can design a system or write code, you must create a formal Requirements Specification (Lastenheft) to ensure you understand exactly _what_ they need.

**Tasks:**

1. **Kick-off & Analysis:** Review the provided scenario description (Neustadt Museum, Mutti's Bakery, or Metropolis Library) and identify the primary stakeholder and their main concerns.
2. **Analog Clustering:** Use a whiteboard or Metaplan wall. Brainstorm all mentioned features, fears, and rules. Cluster them into logical groups (e.g., User Management, Core Functions, Security).
3. **Digitization:** Transfer the clustered points into your Docmost instance, establishing a clear hierarchy for your document.
4. **Requirement Drafting:** Translate the clustered points into at least 10 specific functional requirements, 3 non-functional requirements, and 2 constraints. Apply the IEEE 29148 syntax ("The system shall...") and the ISO/IEC 25010 characteristics.
5. **Finalization:** Structure the document with an Introduction, Initial Situation, Target Concept, and System Context. Ensure photographic proof of your analog cluster is embedded.

## **📦 Result Artifact**

A complete, structured "Lastenheft" (Markdown format) within your Docmost instance, containing embedded photos of your analog clustering phase.

</details>

# Lastenheft (Customer Requirements Specification)

## Mutti's Backstube – Digital Recipe Management System

---

| Document Information |     |
| --- | --- |
| **Document Title** | Customer Requirements Specification (Lastenheft) |
| **Project Name** | Mutti's Backstube – Digital Recipe & Scaling System |
| **Document Version** | 1.0 |
| **Date** | 2026-04-29 |
| **Author** | Project Team |
| **Primary Stakeholder** | Martha "Mutti" Klein, Founder & Baker |
| **Document Standard** | IEEE 29148 / ISO/IEC 25010 |
| **Document Status** | Draft – Pending Stakeholder Review |

---

## Table of Contents

1. Introduction
2. Initial Situation
3. Stakeholder Analysis
4. Analog Clustering – Brainstorming Phase
5. Target Concept
6. System Context
7. Functional Requirements
8. Non-Functional Requirements
9. Constraints
10. Glossary
11. Sign-Off & Approval

---

## 1\. Introduction

### 1.1 Purpose of This Document

This document is the formal Customer Requirements Specification (Lastenheft) for the digital recipe management system to be developed for **Mutti's Backstube**. It captures _what_ the customer needs — not _how_ it will be built. It serves as the binding agreement between the stakeholder (Martha Klein) and the development team before any technical design begins.

This document was created following a structured requirements elicitation process, including a kick-off interview with the primary stakeholder, an analog brainstorming and clustering session (documented in Section 4), and subsequent digitization of the clustered findings.

### 1.2 Scope

The system in scope is a **tablet-based digital recipe and scaling platform** for Mutti's Backstube. It covers:

- Digital storage and retrieval of all bakery recipes
- Normalization of inconsistent measurements into standardized units
- Automatic scaling of ingredient quantities from 10 to 1,000 portions
- Basic nutritional value calculation per recipe and per portion
- A simple, kitchen-safe user interface designed for use by baking staff at any hour

The system does **not** cover: payroll, inventory ordering, customer-facing sales, or cloud-based external sharing of recipes.

### 1.3 Intended Audience

| Audience | Purpose |
| --- | --- |
| Martha "Mutti" Klein | Approval and sign-off as primary stakeholder |
| Bakery Staff | Validate usability requirements |
| Development Team | Technical implementation reference |
| Project Manager | Scope and milestone control |

---

## 2\. Initial Situation

### 2.1 Business Background

Mutti's Backstube is an established, well-loved local bakery with a loyal customer base and a strong reputation for authentic, traditional baked goods. The business was founded and is led by Martha Klein, whose personal recipes are the foundation of the bakery's identity and competitive advantage.

The business has grown to the point where expansion to **three new locations** is planned. This represents a significant operational milestone — and an equally significant operational challenge.

### 2.2 The Core Problem

All recipes currently exist in a single **physical binder**, handwritten by Martha over many years of practice. This binder:

- Is the **only copy** of all recipes
- Uses **inconsistent and informal measurement units** (e.g., "2 cups of flour," "500g sugar," "a large pinch of salt," "bake until golden")
- Contains **no scaling information** — recipes are written for small home-kitchen batches
- Relies on **tacit knowledge** — Martha and her most experienced staff understand nuances that are not written down
- **Cannot be copied or sent** to new locations without exposing Martha to the risk of recipe theft

### 2.3 Pain Points Identified

The following pain points were identified during the stakeholder interview:

- **Risk of total loss:** If the binder is destroyed (fire, water, theft), all recipes are gone permanently.
- **No scaling guidance:** New staff at expansion locations cannot independently scale a recipe from 12 rolls to 800 rolls without risking quality inconsistency.
- **Unit confusion:** A baker trained in metric units and one trained with volume measures may produce different results from the same recipe.
- **Knowledge dependency:** The business is entirely dependent on Martha's personal presence for quality assurance.
- **Staff errors at night:** Baking often begins at 3:00 AM. Tired staff working from an unclear handwritten page are prone to errors.
- **Security concerns:** Martha is deeply uncomfortable with any system that could allow her recipes to be accessed by unauthorized parties or "stolen by the cloud."

### 2.4 Why Change Is Needed Now

The planned expansion to three new locations makes the status quo impossible to maintain. Each new location will require:

- Access to the full recipe collection
- The ability to scale recipes to varying batch sizes
- Consistent quality output without Martha's physical presence
- Trained staff who may not have years of experience with Mutti's methods

Without a digital system, expansion cannot proceed safely or consistently.

---

## 3\. Stakeholder Analysis

### 3.1 Primary Stakeholder

**Martha "Mutti" Klein – Founder & Baker**

Martha is the ultimate decision-maker and the source of all intellectual property in scope. Her buy-in is essential for project success. She is characterized by:

- **Deep expertise** in baking; the recipes encode decades of craft knowledge
- **Skepticism of technology**, particularly cloud-based systems
- **Strong emotional attachment** to her recipes — they are her life's work
- **Pragmatism** — she understands the business need for expansion even if she fears the risks
- **Primary concern:** Recipe theft or unauthorized access

> _"My recipes are my life. I don't want them sitting on some server in America where anyone can steal them."_ — Martha Klein, stakeholder interview

**Key motivations:** Protect her recipes. Keep quality consistent. Enable the business to grow. Not be replaced by a machine.

### 3.2 Secondary Stakeholders

| Stakeholder | Role | Main Concern |
| --- | --- | --- |
| Bakery Staff (all locations) | End users of the system | Ease of use, especially at night |
| Location Managers | Oversee daily operations | Recipe access, no downtime |
| Business Investor / Partner | Financial interest in expansion | Scalability, reliability |
| New Location Staff | Trained users | Simple onboarding |

---

## 4\. Analog Clustering – Brainstorming Phase

> **Note on Process:** Before this document was produced digitally, the project team conducted a physical brainstorming session using a Metaplan wall and sticky notes. All stakeholder concerns, feature ideas, risks, and rules were written on cards and organized into clusters. The photograph below represents the analog clustering artifact from that session.

---

### 4.1 Analog Cluster Map (Simulated Documentation)

```
╔══════════════════════════════════════════════════════════════════════════╗
║         METAPLAN CLUSTER SESSION – MUTTI'S BACKSTUBE                    ║
║         Participants: Project Team + Martha Klein                        ║
╠══════════════════════╦═══════════════════════╦══════════════════════════╣
║  🧂 DATA & RECIPES   ║  🔒 SECURITY & ACCESS  ║  📱 USABILITY (KITCHEN) ║
║──────────────────────║───────────────────────║──────────────────────────║
║ Inconsistent units   ║ No cloud storage       ║ Big fonts / buttons      ║
║ Missing quantities   ║ Martha controls access ║ Works on tablet          ║
║ "Large pinch" etc.   ║ No recipe export       ║ Works with wet hands     ║
║ Home-scale only      ║ Local-only data        ║ Night shift friendly      ║
║ No nutritional info  ║ Password protection    ║ No complex menus         ║
║ No allergen labels   ║ Audit who accessed     ║ Can't crash mid-bake     ║
╠══════════════════════╬═══════════════════════╬══════════════════════════╣
║  ⚖️ SCALING          ║  👩‍🍳 USER ROLES        ║  ⚠️ FEARS & RISKS       ║
║──────────────────────║───────────────────────║──────────────────────────║
║ 10 to 1,000 portions ║ Martha = admin         ║ Recipes stolen           ║
║ Auto-calculate grams ║ Bakers = read-only     ║ System crashes           ║
║ Round sensibly       ║ Manager = limited edit ║ Staff won't use it       ║
║ Show steps clearly   ║ No sharing externally  ║ Quality drops            ║
║ Unit normalization   ║ Audit log              ║ Martha loses control      ║
║ Yield recalculation  ║                        ║ "The cloud"              ║
╚══════════════════════╩═══════════════════════╩══════════════════════════╝
```

_\[In a live project, a photograph of the physical Metaplan wall would be embedded here as a PNG/JPG image.\]_

---

### 4.2 Cluster Summary

From the brainstorming session, six primary clusters were identified:

| Cluster | Theme | Key Cards |
| --- | --- | --- |
| **A** | Data & Recipes | Unit normalization, missing values, nutritional data |
| **B** | Security & Access | No cloud, local data, access control |
| **C** | Usability | Tablet UI, big text, night-shift simplicity |
| **D** | Scaling | 10–1,000 portions, auto-calculation, rounding |
| **E** | User Roles | Martha as admin, read-only bakers, managers |
| **F** | Fears & Risks | Theft, crashes, loss of control, quality drop |

---

## 5\. Target Concept

### 5.1 Vision Statement

The system shall provide Mutti's Backstube with a **secure, locally-operated digital recipe library** that stores all recipes in a standardized format, enables kitchen staff to scale any recipe from 10 to 1,000 portions automatically, and displays the result in a format that is easy to read and act upon — even at 3:00 AM, even in a messy kitchen.

Martha retains full control over who can view or edit her recipes at all times.

### 5.2 Key Goals

1. **Preserve and protect** the recipe collection as a reliable digital archive
2. **Standardize** all measurement units into a single, consistent format (grams, milliliters, and whole count)
3. **Automate scaling** so any baker can confidently produce any batch size
4. **Calculate** estimated nutritional values per portion automatically
5. **Enforce access control** so Martha's intellectual property is never exposed without her authorization
6. **Deliver a UI** that requires no training beyond a brief onboarding and can be used reliably under kitchen conditions

### 5.3 What Success Looks Like

> A baker at the new Schillerstraße location, at 3:15 AM, needs to produce 450 Quarkbällchen. She opens the tablet, taps the recipe, enters "450" as the portion count, and receives a clear, step-by-step ingredient list in grams. She bakes. The result is identical to what Martha would have made.

---

## 6\. System Context

### 6.1 System Boundary

```
┌─────────────────────────────────────────────────────────┐
│                MUTTI'S RECIPE SYSTEM                    │
│                                                         │
│  ┌──────────────┐    ┌───────────────┐                  │
│  │ Recipe DB    │    │ Scaling Engine│                  │
│  │ (local)      │◄──►│               │                  │
│  └──────────────┘    └───────────────┘                  │
│         │                    │                          │
│  ┌──────▼──────────────────▼──────┐                    │
│  │     Tablet User Interface      │                    │
│  └────────────────────────────────┘                    │
│                   │                                     │
└───────────────────┼─────────────────────────────────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
   Martha        Baker      Manager
   (Admin)    (Read-only)  (Limited edit)
```

### 6.2 What Is IN Scope

- Recipe digitization and storage
- Unit normalization engine
- Automatic scaling (10–1,000 portions)
- Nutritional value display
- Role-based access control
- Tablet-optimized interface
- Local data storage (no external cloud)

### 6.3 What Is OUT of Scope

- Online ordering or customer-facing features
- Stock or inventory management
- Payroll or HR
- Automatic recipe sharing between locations (must be manual and authorized)
- Integration with external platforms (social media, delivery apps, etc.)

---

## 7\. Functional Requirements

Requirements are written in IEEE 29148 syntax: **"The system shall…"** ISO/IEC 25010 quality characteristics are noted per requirement.

---

### 7.1 Recipe Management

**FR-01 – Recipe Storage** The system shall store all recipes in a structured digital format that includes: recipe name, category, base portion count, ingredient list, preparation steps, and creation/modification date. _ISO/IEC 25010: Functional Suitability – Functional Completeness_

**FR-02 – Ingredient Input with Flexible Units** The system shall accept ingredient quantities entered in any of the following units: grams (g), kilograms (kg), milliliters (ml), liters (l), cups, tablespoons, teaspoons, and whole-count items (e.g., "3 eggs"). _ISO/IEC 25010: Functional Suitability – Functional Appropriateness_

**FR-03 – Unit Normalization** The system shall automatically convert all ingredient quantities to a single standardized base unit (grams for solids, milliliters for liquids) upon saving a recipe, and store both the original entry and the normalized value. _ISO/IEC 25010: Functional Suitability – Functional Correctness_

**FR-04 – Ambiguous Quantity Flagging** The system shall flag any ingredient entry that uses a non-quantifiable descriptor (e.g., "a large pinch," "to taste," "until golden") and prompt the authorized user (Martha or a Manager) to provide a specific numeric value before the recipe is marked as complete. _ISO/IEC 25010: Reliability – Fault Tolerance_

---

### 7.2 Scaling Engine

**FR-05 – Automatic Portion Scaling** The system shall allow any baker to enter a target portion count between 10 and 1,000 portions, and shall automatically calculate and display all ingredient quantities scaled proportionally from the recipe's base portion count. _ISO/IEC 25010: Functional Suitability – Functional Completeness_

**FR-06 – Intelligent Rounding** The system shall apply sensible rounding rules when scaling quantities: values above 10g shall be rounded to the nearest 5g; values above 500g shall be rounded to the nearest 10g; values below 10g shall be rounded to one decimal place. All rounded values shall be visually flagged to alert the baker. _ISO/IEC 25010: Usability – Appropriateness Recognizability_

**FR-07 – Yield Display** The system shall display the expected output yield alongside the scaled ingredient list (e.g., "Expected yield: 450 rolls at approx. 65g each"). _ISO/IEC 25010: Usability – User Error Protection_

---

### 7.3 Nutritional Information

**FR-08 – Nutritional Calculation** The system shall calculate and display estimated nutritional values per portion (calories, carbohydrates, protein, fat) based on standardized nutritional reference data for each ingredient. _ISO/IEC 25010: Functional Suitability – Functional Completeness_

**FR-09 – Allergen Labeling** The system shall automatically identify and display common allergens (gluten, dairy, eggs, nuts, soy) present in each recipe based on its ingredients, in accordance with EU Food Information Regulation No. 1169/2011. _ISO/IEC 25010: Functional Suitability – Functional Appropriateness_

---

### 7.4 Access Control & Security

**FR-10 – Role-Based Access Control** The system shall enforce three distinct user roles: (1) **Administrator** (Martha only) — full read/write/delete and user management access; (2) **Manager** — read access plus ability to flag ingredient queries; (3) **Baker** — read-only access to recipes and scaling tool. _ISO/IEC 25010: Security – Access Control_

**FR-11 – Local Data Storage** The system shall store all recipe data exclusively on a local device or local network server. The system shall not transmit any recipe data to external servers, cloud services, or third-party platforms at any time, under any circumstances. _ISO/IEC 25010: Security – Confidentiality_

**FR-12 – Access Audit Log** The system shall record a time-stamped log of every login event, recipe view, recipe edit, and scaling action, identifying the user account responsible. This log shall be viewable only by the Administrator. _ISO/IEC 25010: Security – Accountability_

---

### 7.5 Usability

**FR-13 – Tablet-Optimized Interface** The system shall provide a touch-screen interface optimized for tablet use, with a minimum button and text size of 18pt, sufficient contrast for a brightly-lit kitchen environment, and interactive elements spaced to allow accurate tapping with food-covered hands. _ISO/IEC 25010: Usability – Operability_

---

## 8\. Non-Functional Requirements

**NFR-01 – Availability** The system shall be available for use 24 hours a day, 7 days a week, including during early morning production hours. The system shall target an uptime of 99.5% or greater, measured monthly. Planned maintenance windows shall be scheduled between 14:00 and 16:00 only. _ISO/IEC 25010: Reliability – Availability_

**NFR-02 – Response Time** The system shall display a scaled recipe result within 2 seconds of a user submitting a portion count. Recipe search results shall appear within 1 second of a search query being entered. _ISO/IEC 25010: Performance Efficiency – Time Behaviour_

**NFR-03 – Learnability** A new bakery staff member with no prior experience of the system shall be able to independently locate a recipe, enter a target portion count, and read the scaled ingredient list within 10 minutes of a single onboarding walkthrough, without referring to a manual. _ISO/IEC 25010: Usability – Learnability_

---

## 9\. Constraints

**CON-01 – No External Cloud Dependency** The system must operate entirely on local hardware. Any network dependency (e.g., for updates) must be optional and must not affect the system's core recipe and scaling functionality if the network is unavailable. This constraint is non-negotiable and reflects the primary stakeholder's explicit requirement.

**CON-02 – Martha's Exclusive Administrative Authority** Recipe creation, recipe deletion, and user account management shall be restricted exclusively to the Administrator account held by Martha Klein. No other user — including Location Managers or the development team — shall be able to add, modify, or remove recipes without Martha's direct action. Technical implementations that would allow developer-level access to recipe data are prohibited.

---

## 10\. Glossary

| Term | Definition |
| --- | --- |
| **Lastenheft** | German term for Customer Requirements Specification — describes _what_ the customer needs, not _how_ it will be built |
| **Pflichtenheft** | Contractor's response document describing _how_ the requirements will be fulfilled |
| **Portion** | One serving unit of a recipe as defined by the base recipe |
| **Scaling** | The process of proportionally adjusting ingredient quantities for a different number of portions |
| **Unit Normalization** | The conversion of all ingredient quantities into a consistent base unit (grams / milliliters) |
| **DXA** | Device-independent unit used in document formatting; not relevant to kitchen staff |
| **IEEE 29148** | International standard for requirements engineering |
| **ISO/IEC 25010** | International standard defining software quality characteristics |
| **NFR** | Non-Functional Requirement — defines _how well_ a system performs, not what it does |
| **FR** | Functional Requirement — defines _what_ the system must do |
| **Allergen (EU 1169/2011)** | A substance listed under EU regulation that must be declared in food products |
| **Admin** | Administrator role — Martha Klein only |

---

## 11\. Sign-Off & Approval

This document represents the agreed-upon requirements baseline for the Mutti's Backstube Digital Recipe System. Changes after sign-off require written consent from the primary stakeholder and must be documented as a formal change request.

| Role | Name | Signature | Date |
| --- | --- | --- | --- |
| Primary Stakeholder / Founder | Martha Klein | \___\___\___\___\___\____ | \___\___\____ |
| Project Lead | \___\___\___\___\___\____ | \___\___\___\___\___\____ | \___\___\____ |
| Lead Developer | \___\___\___\___\___\____ | \___\___\___\___\___\____ | \___\___\____ |
| Quality Assurance | \___\___\___\___\___\____ | \___\___\___\___\___\____ | \___\___\____ |

---

_Document prepared in accordance with IEEE 29148 – Systems and Software Engineering: Requirements Engineering. Quality attributes referenced per ISO/IEC 25010 – Systems and Software Quality Requirements and Evaluation (SQuaRE)._

_Version 1.0 | 2026-04-29 | Mutti's Backstube Project_