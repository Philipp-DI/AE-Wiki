# LF5.1.4: The IEEE Formulator

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Requirements Engineer,  
> I want to formulate requirements using standardized IEEE 29148 syntax,  
> so that I ensure every requirement is atomic, testable, and completely unambiguous for developers.

## 🎉 Celebration Criteria (Learning Objectives)

- I can **apply** the standard IEEE syntax to write requirements. (K3)
- I **know how to transform** vague statements into measurable, atomic requirements. (K3)
- I can **split** compound requirements into single, testable items. (K2)

## 🧠 Knowledge Briefing

Writing requirements is a strict discipline. The **IEEE 29148 standard** provides the grammatical foundation.

**The Golden Syntax:** _"The system shall \[function\] under \[condition\]."_

### The Rules of Good Requirements

- **Atomic:** One requirement = one sentence = one feature. Never use "and" / "or".
- **Unambiguous:** No room for interpretation. Avoid words like "fast", "user-friendly", "robust".
- **Testable:** You must be able to write a clear Yes/No test for it.
- **Binding:** Use "shall" (must have) or "should" (nice to have), but stick to "shall" for core features.

## ⚠️ Common Pitfalls

- Using compound sentences: "The system shall log in the user AND load their profile." If the login works but the profile fails, is the requirement met? Split it into two!

## 🛠️ Mandatory Tasks (K1 - K3)

1. State the standard IEEE 29148 requirement syntax formula. (K1)
2. Explain what makes a software requirement "atomic". (K2)
3. Rewrite the vague sentence "The app needs to load pictures really fast" into a testable, measurable requirement. (K3)
4. Split the following compound requirement into two atomic requirements: "The system shall export the data as PDF and email it to the admin." (K3)
5. Describe the problem with using words like "should", "could", or "maybe" in technical specifications. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze the consequences of writing ambiguous requirements on the software testing phase. (K4)
2. Evaluate a set of 5 poorly written, non-atomic requirements from a generic website and completely restructure them. (K5)
3. Design a validation checklist to ensure peer-reviewed requirements meet IEEE 29148 standards. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| IEEE 29148 Standard | Google | "IEEE 29148 Requirements specification structure" |
| Atomic Requirements | Google | "How to write atomic software requirements" |

</details>

### M1: State the standard IEEE 29148 requirement syntax formula. (K1)

> **"The system shall \[function\] under \[condition\]."**

**Example:** "The system shall authenticate the user within 3 seconds under normally functioning network conditions."

---

### M2: Explain what makes a software requirement "atomic". (K2)

An “atomic” requirement means that it contains exactly one specific task/function. Example: _NOT Atomic (compound):_ “The system shall boot within 2 seconds and automatically logs in the previous user.” → _Atomic:_ “The system shall boot within 2 second.” + “After booting, the system shall automatically log in the previous user.”

---

### M3: Rewrite the vague sentence "The app needs to load pictures really fast" into a testable, measurable requirement. (K3)

**Measurable:** "The system shall display images with a size of under 10MB within 2 seconds, using a standard LTE connection with a minimum download speed of 10 Mbit/s."

---

### M4: Split the following compound requirement into two atomic requirements: "The system shall export the data as PDF and email it to the admin." (K3)

**1:** "The system shall export the selected data as a PDF document."

**2:** "The system shall send the exported PDF document to the configured administrator email address upon successful export completion."

---

### M5: Describe the problem with using words like "should", "could", or "maybe" in technical specifications. (K2)

These words are open to interpretation. For example, a “should”-feature could be left out entirely because the wording makes it non-mandatory.

According to IEEE 29148: **"shall" = binding (for core functions); "should" = recommended, but optional; "may" = permitted.**

---

### O1: Analyze the consequences of writing ambiguous requirements on the software testing phase. (K4)

As with any ambiguity, each person might interpret them differently. That’s why - especially for the testing phase - it is mandatory to have specific, atomic requirements. Otherwise, there can be risks and problems such as:

- Testing is written and executed under differing assumptions which might lead to errors.
- The final result might match the expectations of the developer, but not those of the client.
- Additional work and fixing within the testing phase can be quite costly. Both in terms of money and time.

---

### O2: Evaluate a set of 5 poorly written, non-atomic requirements from a generic website and completely restructure them. (K5)

| DON’T | Issues | BETTER |
| --- | --- | --- |
| "The system should be fast." | “should” leaves room; not measurable | "The system shall respond to user input within 200ms under standard load conditions." |
| "The app must be user-friendly." | not measurable | "The system shall enable a new user to complete the registration process within 3 minutes without external assistance." |
| "Data must be secure." | too vague | "The system shall encrypt all user passwords using “XYZ-encryption-system”." |
| "The system should handle lots of users." | not measurable | "The system shall support 500 concurrent users without response time exceeding 1 sec." |
| "The export function must work with big files." | not measurable | "The system shall successfully import files of up to 2 GB in size without crashing or data loss." |

---

### O3: Design a validation checklist to ensure peer-reviewed requirements meet IEEE 29148 standards. (K6)

## Anforderungs-Checkliste (IEEE 29148)

### 1\. Syntax

- [ ] Using: "The system shall [function] under [condition]."?
- [ ] Contains a single measurable function?

### 2\. Atomicity

- [ ] No “and” or “or”?
- [ ] Can it be broken down further?

### 3\. Measurability

- [ ] Does it contain a quantifiable entity such as numbers, percents?
- [ ] Does it avoid vague wording?

### 4\. Testability

- [ ] Is a proper “yes-or-no” acceptance criteria check possible?
- [ ] Does it contain the necessary [condition], if there is any?

### 5\. Commitment

- [ ] Is “shall” being used for all core functionality/requirements?
- [ ] Are more ambiguous modal verbs such as “should” used properly?

### 6\. Unambiguity

- [ ] Is the interpretation consistent?
- [ ] Are technical terms explained properly (glossary)?