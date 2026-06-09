# LF5.5.5: User Acceptance Testing (UAT)

<details>
<summary>Briefing</summary>

## User Story

As a Product Owner, **I** want to prepare and conduct User Acceptance Testing (UAT), so that **I** can prove to the stakeholder that the software meets their business requirements before final sign-off.

## Celebration Criteria

- **I can define** the purpose of User Acceptance Testing (UAT). (K1)
- **I know how to differentiate** between UAT and system testing. (K2)
- **I can explain** the importance of a formal acceptance protocol. (K2)

## Knowledge Briefing

The code compiles, the unit tests are green, and the CI pipeline passes. Are we done? No. The final step is **User Acceptance Testing (UAT)**.

- **What it is:** The software is handed over to the actual end-users or stakeholders (the client). They test the software in a real-world scenario to ensure it solves their business problem.
- **Who does it:** NOT the developers. Developers test if the software works _technically_. Users test if the software works _practically_.
- **The Result:** If UAT passes, the client signs a formal **Acceptance Protocol (Abnahmeprotokoll)**. This is a legal milestone. It means the project is officially delivered and can be billed.

## Common Pitfalls

- Letting developers guide the client during UAT ("Just click here, don't click there"). The client must use the software naturally to uncover real usability issues or misunderstood requirements.

## Mandatory Tasks

1. Define the term "User Acceptance Testing" (UAT) in your own words. (K1)
2. Explain why the developers who wrote the code should _not_ be the ones conducting the UAT. (K2)
3. Describe the difference between System Testing (done by QA) and UAT (done by the client). (K2)
4. State the legal or project-management significance of a signed Acceptance Protocol. (K1)
5. Explain what happens in a project lifecycle immediately after a successful UAT sign-off. (K2)

## Optional Tasks

1. Analyze a scenario where the software passes all technical Unit Tests, but completely fails the UAT phase with the customer. How did this happen? (K4)
2. Evaluate the importance of basing UAT test scenarios directly on the original "Lastenheft" (Requirements Specification). (K5)
3. Design a formal 1-page "User Acceptance Sign-Off Document" suitable for a stakeholder to sign. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| User Acceptance Testing | YouTube | "What is UAT User Acceptance Testing" |
| Software Acceptance Sign-off | Google | "Software project acceptance protocol template" |

</details>

## Answers

### M1: Define the term "User Acceptance Testing" (UAT) in your own words. (K1)

**UAT** is the final test phase where the actual client or end-users take the software for a spin in a real-world scenario - _not to check whether the code is technically correct, but whether it actually solves their business problem_. According to Westermann (see → LF 1-5), the ‘Abnahmetest’ is “carried out by the customer or with their involvement" and forms the basis for the decision to formally accept the project.

---

### M2: Explain why the developers who wrote the code should not be the ones conducting the UAT. (K2)

Developers test whether the software works technically. Users test whether it works practically - and those are very different questions.

The dev knows every shortcut, every edge case they avoided, every assumption baked into the UI. They will unconsciously navigate around problems the real user would walk straight into. Beyond that, they are emotionally invested in the result. A client who has never seen the system before will reveal misunderstood requirements, missing workflows, and usability problems within minutes - precisely because they bring no prior knowledge of how it "should" be used.

_UAT and research connected to it are also an_ **_essential part of UX Design_**_, which I would like to practice in the future. The research and premeditated data part is key here, since UX work involves intensive, client-centric up-front research._

The Common Pitfall in the briefing above makes this concrete: a developer "guiding" the client during UAT defeats the entire purpose.

---

### M3: Describe the difference between System Testing (done by QA) and UAT (done by the client). (K2)

**System Testing** is the final internal test of the complete system, carried out by QA, verifying both functional and non-functional requirements against the technical specification. The question is: "Does this software do what the spec says it should?"

**UAT (Abnahmetest)** happens after that, in the client's environment, with the client's people. The question shifts to: "Does this software actually solve our business problem?" It checks business logic, real workflows, and practical usability - not just technical correctness.

One can pass completely while the other fails. That's the whole point of keeping them separate.

---

### M4: State the legal or project-management significance of a signed Acceptance Protocol. (K1)

Formal acceptance is legally required under § 640 BGB. The signed “Abnahmeprotokoll” triggers several immediate legal consequences:

- **Payment** becomes due (§ 641 BGB)
- **Risk** of accidental damage **transfers** to the client (§ 644 BGB)
- **Known defects not explicitly noted** in the protocol can **no longer be claimed later** (§§ 640, 341 BGB)
- **Warranty periods begin** to run (§ 634a BGB)

In project management terms: it's the official milestone that defines "delivered”. Without it, a project is not closed.

---

### M5: Explain what happens in a project lifecycle immediately after a successful UAT sign-off. (K2)

The signed acceptance protocol ends the delivery phase. From that point:

- The **invoice** can be issued and **payment** demanded
- **Responsibility** for the system formally **transfers** to the client/operator
- The project moves into the **maintenance and operations phase**
- Any remaining **open points** noted in the protocol get **tracked** against agreed deadlines and responsibilities
- The **development team's primary obligation** under the contract is **fulfilled**

In agile contexts, a successful UAT sign-off on a release also feeds back into the Product Backlog - new requirements, adjustments, and follow-up features surface naturally during the client's real-world use.

---

### O1: Analyze a scenario where the software passes all technical Unit Tests, but completely fails the UAT phase with the customer. How did this happen? (K4)

**Scenario**—a development team builds an invoicing module. Every unit test is green—tax calculations correct, database writes confirmed, PDF generation working. CI pipeline: all checks passed. Then the client's accounting team sits down for UAT and the whole thing falls apart.

**How and why?** Several failure modes, often in combination:

- **Requirements were misunderstood:** The Lastenheft said "support multiple currencies." The dev team implemented currency display. The client expected automatic exchange rate conversion on export. Both are "correct" readings, but only one solves the business problem. Unit tests can't catch this because the code does exactly what the developer thought was required.
- **The real workflow was never modelled:** The system was tested in isolation with clean test data. In practice, the client's accountants work with 400-line import files, partial invoices, and approval chains that span three departments. None of this was part of the test scenarios.
- **Non-functional requirements weren't taken seriously:** The system is technically correct but takes 30 seconds to load a client's invoice history. Technically a "pass." Practically unusable.
- **The UI was designed by engineers, not users:** The logic is sound but the interface is disorienting to anyone who isn't a developer. UAT surfaces this immediately.

The root cause in most cases: insufficient involvement of actual end-users during requirements gathering. The Lastenheft (written by the client) and Pflichtenheft (written by the contractor) are only as good as the conversations that produced them.

---

### O2: Evaluate the importance of basing UAT test scenarios directly on the original "Lastenheft" (Requirements Specification). (K5)

The Lastenheft is the contractual definition of what the software was supposed to do—written by the client before a single line of code was written. UAT test scenarios derived from it are therefore the most objective measure available: does the delivered software fulfil the original agreed requirements?

**Without this anchor**, UAT drifts into subjectivity. Users test what they happen to think of in the moment, developers defend design decisions based on what they built rather than what was ordered, and "pass/fail" becomes a **matter of opinion rather than a verifiable fact**.

The Pflichtenheft—which is the contractor's technical response to the Lastenheft—should already contain acceptance criteria. UAT scenarios built from these criteria create a direct **traceability chain:** requirement in the Lastenheft → acceptance criterion in the Pflichtenheft → test scenario in UAT. If the scenario passes, the requirement is demonstrably fulfilled. If it fails, there is no ambiguity about what is owed.

There is also a legal dimension. In the event of a dispute, a signed acceptance protocol based on Lastenheft-derived criteria is far stronger evidence of fulfilment or non-fulfilment than a vague "the client seemed happy."

The practical risk of skipping this: UAT becomes exploratory testing dressed up as formal acceptance. New requirements disguised as "bugs" appear. Scope creep enters through the back door. The project never actually closes.

---

### O3: Design a formal 1-page "User Acceptance Sign-Off Document" suitable for a stakeholder to sign. (K6)

## User Acceptance Sign-Off Document

**Project:**

**Contract No.:**

**Software / Version:**

**Date of UAT:**

**Location:**

---

**Participants**

| Name | Company | Role |
| --- | --- | --- |
|     |     |     |
|     |     |     |

---

**System Environment Tested**

- Operating system:
- Browser/Runtime:
- Test environment:

---

**Acceptance Criteria Results**

| #   | Requirement (referencing Lastenheft) | Test Scenario | Result |     | Notes |
| --- | --- | --- | --- |     | --- | --- |
| Pass | Fail |
| 1   |     |     |     |     |     |
| 2   |     |     |     |     |     |
| 3   |     |     |     |     |     |
| 4   |     |     |     |     |     |

---

**Open Points** _(items to be resolved post-sign-off)_

| #   | Description | Responsible | Due Date |
| --- | --- | --- | --- |
|     |     |     |     |
|     |     |     |     |

---

**Overall Assessment**

- [ ] Software is accepted as contractually delivered - no open defects
- [ ] Software is accepted with reservations - open points listed above must be resolved by agreed dates
- [ ] Software is not accepted - reasons stated in notes above

---

**Signatures**

Client:

Date:

Contractor:

Date:

---

_A signed copy of this document confirms contractual delivery per § 640 BGB and triggers payment terms per § 641 BGB (as mentioned in M4)._