# LF5.5.1: The Testing Pyramid

<details>
<summary>Briefing</summary>

## User Story

As a QA Engineer, **I** want to understand the different levels of software testing, so that **I** know when to write fast Unit Tests versus comprehensive End-to-End Tests.

## Celebration Criteria

- **I can define** the concept of the Testing Pyramid. (K1)
- **I know how to differentiate** between Unit, Integration, and System testing. (K2)
- **I can explain** why automated tests save time in the long run. (K2)

## Knowledge Briefing

Testing ensures software does what it is supposed to do. The **Testing Pyramid** visualizes how we should distribute our testing efforts:

1. **Unit Tests (Base):** Test individual, isolated functions (e.g., checking if a `calculate_tax()` function returns the right number). They are fast, cheap, and you should have hundreds of them.
2. **Integration Tests (Middle):** Test how different modules work together (e.g., checking if the Python script can successfully query the database). Slower and more complex.
3. **End-to-End / System Tests (Top):** Test the entire application from the user's perspective (e.g., a script clicking through the web interface to buy a product). Slow, expensive to maintain, but highly realistic.

## Common Pitfalls

- Attempting to test _everything_ manually through the graphical user interface. This is known as the "Ice Cream Cone" anti-pattern. UI tests are slow and brittle; focus heavily on the base (Unit Tests).

## Mandatory Tasks

1. Define the three main layers of the standard Software Testing Pyramid. (K1)
2. Explain the primary goal of a "Unit Test" in one sentence. (K2)
3. Describe the difference between a Unit Test and an Integration Test using the metaphor of building a car. (K2)
4. State two reasons why End-to-End (E2E) tests are placed at the very top of the pyramid. (K1)
5. Explain the concept of "Regression Testing" (checking if new code broke old, working features). (K2)

## Optional Tasks

1. Analyze the long-term financial cost of finding a bug during the Unit Testing phase versus finding it in Production after release. (K4)
2. Evaluate the risks of having a testing strategy that relies 100% on manual testing by human QA testers. (K5)
3. Design a test strategy for a simple calculator application, proposing 5 specific Unit Tests and 1 specific Integration Test. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| The Testing Pyramid | YouTube | "Software Testing Pyramid explained" |
| Types of Software Testing | Google | "Unit vs Integration vs System Testing" |

</details>

## Answers

### M1: Define the three main layers of the standard Software Testing Pyramid. (K1)

The Testing Pyramid describes three layers of automated tests, each differing in **scope, speed, and cost**:

**Base - Unit Tests:** Test a single, isolated function or code unit for correctness. They are fast, cheap to write and run, and should make up the largest share of all tests in a project.

**Middle - Integration Tests:** Test how multiple components or modules work together. The focus is on the interfaces between those components - for example, whether a Python module can successfully read data from a database. Slower and more complex than unit tests.

**Top - System Tests:** Test the complete, assembled system against both functional and non-functional requirements. These are the most expensive to run and maintain, and are consequently kept to a minimum.

---

### M2: Explain the primary goal of a "Unit Test" in one sentence. (K2)

A Unit Test verifies that a single, isolated unit of code - such as one function or method - produces the correct output for a given input, completely independent of the rest of the system.

---

### M3: Describe the difference between a Unit Test and an Integration Test using the metaphor of building a car. (K2)

**Analogy:**  
Car factory → individual parts vs. assembly: a Unit Test is like testing a single brake pad in isolation. An Integration Test is what happens when you bolt the brake pad, caliper, disc, and hydraulic line together and check whether they all work as a system. The individual parts may each be fine, yet the combined assembly can still fail - for example, due to a mismatched interface.

**In software terms:** a Unit Test checks whether `calculate_tax(100)` returns `19`. An Integration Test checks whether the tax calculation function, the database query, and the output module all work together correctly.

---

### M4: State two reasons why End-to-End (E2E) tests are placed at the very top of the pyramid. (K1)

E2E tests sit at the top because:

- **They are slow and resource-intensive** - driving a full application through a browser or UI involves many layers (network, database, frontend, backend), making each test run take significantly longer than a unit test.
- **They are brittle and costly to maintain** - any change to the UI or user flow can break dozens of E2E tests at once, even if the underlying logic is perfectly correct. This makes them expensive to keep up to date.

The smaller the quantity at the top, the more manageable those costs remain.

---

### M5: Explain the concept of "Regression Testing" (checking if new code broke old, working features). (K2)

A **Regression Test** is a re-execution of previously passed tests after code changes have been made - whether that means adding a new feature, fixing a bug, or refactoring existing logic. The goal is to confirm that the existing, working functionality has not been accidentally broken ("regressed") by the change.

**Analogy:**  
Renovating a house: you add a new room. A regression test is the walkthrough you do afterwards to make sure the heating, electricity, and water still work in all the _old_ rooms - the new addition should not have broken anything that was already fine.

In practice, automated regression tests are the main reason why having a large suite of unit tests pays off: after any code change, the entire suite runs automatically and immediately flags anything that broke.

---

### O1: Analyze the long-term financial cost of finding a bug during the Unit Testing phase versus finding it in Production after release. (K4)

The cost of a bug escalates dramatically the later it is found in the development lifecycle - this principle is well established in software quality management.

**During Unit Testing:** The developer who wrote the code finds the bug immediately, often within minutes. The fix is localized - only the affected function needs to change. No other systems are involved, no customers are affected, no incident report is required. Cost: low, measured in developer-minutes.

**During Production:** A bug in production means real users are encountering the failure. The costs multiply across several dimensions:

- **Detection cost** → the bug must first be reported, reproduced, and triaged, often by support staff and a senior developer.
- **Incident cost** → if the bug causes downtime or data corruption, then SLA penalties, customer compensation, or reputation damage may follow.
- **Fix cost** → a production fix typically requires an emergency patch process, re-testing across multiple environments, and a deployment outside the normal release cycle.
- **Opportunity cost** → the development team is pulled away from planned work to fight the fire.

Studies in software engineering have repeatedly shown that the cost ratio between finding a bug in unit testing versus finding it in production can reach 10:1 to 100:1 depending on the severity and domain. _For safety-critical or financial systems, the ratio is probably much higher - as the risk increases_.

**Conclusion:** investing time in writing good unit tests is not a quality luxury - it is a financial decision.

_Source(s):_ [_istqb.org_](http://istqb.org)

---

### O2: Evaluate the risks of having a testing strategy that relies 100% on manual testing by human QA testers. (K5)

A purely manual testing strategy introduces several compounding risks that become harder to manage as a project grows:

**Scalability failure:** Manual testing does not scale with software complexity. As the codebase grows, the number of test cases that need to be re-run after every change grows with it. A team of testers cannot realistically re-execute hundreds of test cases after every small commit.

**Human error and inconsistency:** Testers are subject to fatigue, distraction, and varying interpretations of what "correct behavior" looks like. Two testers running the same test case may reach different conclusions.

**Regression blindness:** Without automated regression tests, developers have no immediate feedback when a change breaks something old. Bugs that would be caught within seconds by an automated suite may survive undetected for days or entire sprints.

**Speed mismatch with modern delivery:** Practices like _Continuous Integration (CI) and Continuous Delivery (CD)_ rely on the ability to run thousands of tests in minutes after every code push. Manual testing creates a bottleneck that makes these practices impossible.

**Cost over time:** Manual testing appears cheaper upfront but becomes increasingly expensive as the project matures, because every new feature adds more test cases that must be re-executed manually in every release cycle.

The balanced assessment is that manual testing has a permanent and valuable role - especially for exploratory testing, usability evaluation, and UAT - but as the _sole_ strategy it is unsustainable and progressively risky.

---

### O3: Design a test strategy for a simple calculator application, proposing 5 specific Unit Tests and 1 specific Integration Test. (K6)

**Unit Tests:**

| ID  | Function under test | Input | Expected Result |
| --- | --- | --- | --- |
| UT-01 | `add(a, b)` | `add(3, 4)` | `7` |
| UT-02 | `subtract(a, b)` | `subtract(10, 3)` | `7` |
| UT-03 | `multiply(a, b)` | `multiply(6, 7)` | `42` |
| UT-04 | `divide(a, b)` | `divide(10, 2)` | `5.0` |
| UT-05 | `divide(a, b)` - edge case | `divide(10, 0)` | Raises `ZeroDivisionError` (or returns defined error value) |

**UT-05** is particularly _important_: edge cases and boundary values (like division by zero) are a classic source of undetected bugs and should always be covered explicitly.

---

**Integration Test:**

| ID  | Scenario | Steps | Expected Result |
| --- | --- | --- | --- |
| IT-01 | Full calculation pipeline | 1\. Call `divide(10, 2)`, store result. 2. Pass stored result to `display_result()`. | Display component shows `"5.0"` without error - confirming that the calculation module and the display module correctly exchange data. |

This integration test does not re-test the math logic (that is UT-04's job). It tests the _connection_ between the two modules - the interface. That is the defining characteristic of an integration test.