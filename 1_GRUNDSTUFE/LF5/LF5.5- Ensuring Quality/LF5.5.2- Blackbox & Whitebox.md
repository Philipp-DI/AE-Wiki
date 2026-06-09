# LF5.5.2: Blackbox & Whitebox

<details>
<summary>Briefing</summary>

## User Story

As a QA Engineer, **I** want to design structured test cases using different testing methodologies, so that **I** can systematically verify software behavior without bias and document failures accurately.

## Celebration Criteria

- **I can contrast** Blackbox and Whitebox testing techniques. (K2)
- **I know how to structure** a formal test case. (K3)
- **I can formulate** expected results based on requirements. (K3)

## Knowledge Briefing

You cannot just click around and call it testing. Professional QA relies on structured methodologies.

**1\. Testing Methodologies:**

- **Blackbox Testing:** The tester does _not_ look at the source code. They only know the requirements. They provide inputs and check if the outputs are correct. (Focus on user perspective).
- **Whitebox Testing:** The tester _looks_ at the source code. They design tests to ensure every specific `if` statement and `for` loop is executed at least once (Code Coverage).

**2\. Test Case Structure:** A formal test case must be reproducible by anyone. It contains:

- **Test ID & Title:** (e.g., `TC-01: Valid User Login`).
- **Preconditions:** (e.g., "User account exists and database is running").
- **Test Steps:** (1. Enter username 'admin', 2. Enter password '1234', 3. Click Login).
- **Expected Result:** (User is redirected to the dashboard).
- **Actual Result:** (Filled out during execution. E.g., "Pass" or "Failed: Error 500 occurred").

## Common Pitfalls

- Writing vague expected results like "It should work." If another tester runs your case, they must know exactly what "working" looks like (e.g., "A green checkmark appears").

## Mandatory Tasks

1. Define the fundamental difference between Blackbox and Whitebox testing regarding access to the source code. (K1)
2. List the 5 standard components of a formal Test Case document (ID, Preconditions, Steps, Expected Result, Actual Result). (K1)
3. Write a strictly formatted, 3-step test case for withdrawing money from an ATM (assume a valid PIN is a precondition). (K3)
4. Explain why it is crucial to document the "Preconditions" before listing the test steps. (K2)
5. Formulate an exact "Expected Result" for a test case where a user tries to create an account with a password that is too short. (K3)

## Optional Tasks

1. Analyze how "Equivalence Partitioning" (testing one representative value from a valid range instead of every single number) saves time in Blackbox testing. (K4)
2. Evaluate the psychological reasons why developers are often poor Blackbox testers for their own code. (K5)
3. Design a Whitebox test plan that aims to achieve 100% "Branch Coverage" for a simple `if-else-if` code block. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Blackbox vs Whitebox | YouTube | "Black Box vs White Box Testing" |
| Writing Test Cases | Google | "How to write a software test case standard format" |

</details>

## Answers

### M1: Define the fundamental difference between ==Blackbox== and Whitebox testing regarding access to the source code. (K1)

**==Blackbox Testing:==**  
A _specification-oriented_ _method_. The tester has no knowledge of the internal source code or program structure. Test cases are derived exclusively from the requirements specification - the tester provides inputs and checks whether the outputs match expectations. The focus is the external behaviour, i.e., the user's perspective.

**Whitebox Testing:**  
A _structure-oriented method_. The tester works with full knowledge of the source code. Tests are designed to exercise specific internal paths - for example, ensuring that every `if`\-branch, loop, or statement is executed at least once (code coverage). Whitebox tests are primarily used at the unit and component test level.

**Analogy:**  
Car inspection: ==a Blackbox tester sits in the driver's seat, turns the steering wheel, and checks whether the car responds correctly - without ever looking under the hood==. A Whitebox tester opens the hood, traces every cable and hose, and deliberately tests each one in isolation.

---

### M2: List the 5 standard components of a formal Test Case document (ID, Preconditions, Steps, Expected Result, Actual Result). (K1)

A formal, reproducible test case consists of these five components:

| Component | Content |
| --- | --- |
| **Test ID & Title** | Unique identifier and short description (e.g., `TC-01: Valid User Login`) |
| **Preconditions** | Everything that must be true before the test can run (e.g., "User account exists in the database") |
| **Test Steps** | Numbered, exact sequence of actions to execute |
| **Expected Result** | The precise, measurable outcome that indicates a pass |
| **Actual Result** | Filled in during execution - either "Pass" or a concrete description of what went wrong |

The most common mistake in practice: writing vague expected results. Every component must be specific enough that a different tester gets the same result.

---

### M3: Write a strictly formatted, 3-step test case for withdrawing money from an ATM (assume a valid PIN is a precondition). (K3)

<div class="joplin-table-wrapper"><table style="min-width: 163px"><tbody><tr><th colspan="1" rowspan="1" colwidth="138"><p data-id="tkvbutomzucq">Component</p></th><th colspan="1" rowspan="1"><p data-id="xaftfjiituvp">Content</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="138"><p data-id="pjwohnabgspu"><strong>Test ID &amp; Title</strong></p></td><td colspan="1" rowspan="1"><p data-id="esfbmndmlrsr">TC-ATM-01: Successful cash withdrawal with sufficient balance</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="138"><p data-id="rruususuxwkv"><strong>Preconditions</strong></p></td><td colspan="1" rowspan="1"><p data-id="jgzkasiduaqn">User has entered a valid PIN. Account balance is 200 EUR. Requested amount: 50 EUR.</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="138" style="background-color: #c1b7f2" data-background-color="#c1b7f2" data-background-color-name="purple"><p data-id="hlxlyofamaoz"><strong>Test Steps</strong></p></td><td colspan="1" rowspan="1" style="background-color: #c1b7f2" data-background-color="#c1b7f2" data-background-color-name="purple"><ol><li><p data-id="rtcdyivwnkyw">Select "Cash Withdrawal" from the main menu.</p></li><li><p data-id="sroatcolhxdp">Enter the amount 50 and confirm.</p></li><li><p data-id="cyreiyrqsnsy">Collect the dispensed cash and the card.</p></li></ol></td></tr><tr><td colspan="1" rowspan="1" colwidth="138"><p data-id="kxkrkvuqmojp"><strong>Expected Result</strong></p></td><td colspan="1" rowspan="1"><p data-id="iepsrmkdpatu">The ATM dispenses 50 EUR in cash. The account balance is updated to 150 EUR. A receipt is offered. The card is returned.</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="138"><p data-id="kpmeeywaxplk"><strong>Actual Result</strong></p></td><td colspan="1" rowspan="1"><p data-id="nkpesrkjfnzk"><em>(to be filled in during test execution)</em></p></td></tr></tbody></table></div>

---

### M4: Explain why it is crucial to document the "Preconditions" before listing the test steps. (K2)

Preconditions define the exact starting state that must exist before the test is run. Without them, the same test steps can produce different results depending on the environment - making failures non-reproducible and conclusions unreliable.

Consider the ATM example: if the precondition "account balance is 200 EUR" is not documented, one tester might run the test with an empty account. The withdrawal fails - but not because of a bug. Without the precondition, the tester would falsely report a defect.

**Analogy:**  
A recipe without mise en place: the cooking steps say "add the beaten eggs" - but if you did not know you needed to beat them first, the dish fails for a reason completely unrelated to the recipe itself. Preconditions are the mise en place of testing.

In short: preconditions separate environmental setup from the test logic itself, which is a prerequisite for any meaningful, repeatable result.

---

### M5: Formulate an exact "Expected Result" for a test case where a user tries to create an account with a password that is too short. (K3)

**Bad version (too vague):** "The system should reject the password."

**Correct version:** The registration form does not submit. An inline error message appears directly below the password field reading: "Password must be at least 8 characters long." The user remains on the registration page. No account is created in the database.

**The key principle:** an expected result must be so precise that any tester - regardless of prior knowledge - can determine unambiguously whether the test passed or failed. Color, position, exact wording, and system state all belong in the expected result when they are verifiable.

---

### O1: Analyze how "Equivalence Partitioning" (testing one representative value from a valid range instead of every single number) saves time in Blackbox testing. (K4)

In ==Blackbox== testing, the tester derives test cases from the requirements specification alone. For any function that accepts a numeric input, the theoretical number of possible inputs is enormous - often in the millions. Testing every single value is economically impossible.

Equivalence Partitioning (Äquivalenzklassenbildung) solves this by grouping all possible input values into classes where the system is expected to behave identically. Within one class, any single representative value is assumed to expose the same bugs as any other. You therefore only need one test case per class rather than one per value.

A concrete example from Westermann's LF 8 material: a function `isTemperatureOk(temp)` returns `True` for temperatures <= 30°C and `False` above. Two equivalence classes result:

| Class | Range | Representative test value | Expected result |
| --- | --- | --- | --- |
| 1 - valid | temp <= 30 | 20.0 | True |
| 2 - invalid | temp > 30 | 40.0 | False |

Instead of testing all integers from, say, -273 to 1000, two test cases cover the entire input space.

The time savings compound quickly: a function with three input parameters, each with two equivalence classes, requires 6 test cases instead of potentially millions. For larger systems with dozens of input fields, this reduction is what makes systematic testing economically viable at all.

The Grenzwertanalyse (boundary value analysis) extends this further: since errors in code tend to cluster at the edges of ranges (e.g., `<` written where `<=` was intended), you additionally test the values exactly at the class boundaries (30.00 and 30.01), which dramatically increases the defect detection rate with minimal extra effort.

---

### O2: Evaluate the psychological reasons why developers are often poor Blackbox testers for their own code. (K5)

This is a well-recognized problem in software quality management, and the reasons are both cognitive and motivational.

**Confirmation bias:** A developer unconsciously designs tests that confirm the code works the way they intended it to, rather than aggressively probing for failure. Their mental model of the function's behaviour was formed while writing it - so they test against that model, not against the specification.

**Blind spots from implementation knowledge:** The Blackbox method explicitly excludes knowledge of the source code. A developer cannot un-know how they implemented something. They will naturally avoid inputs that "shouldn't happen" according to their internal logic, even if the requirements say nothing about excluding them.

**Emotional investment:** Code that a developer spent hours writing carries an unconscious ownership effect. Finding a bug in someone else's work feels neutral; finding one in your own can feel like a personal failure. This subtly reduces the aggression and creativity needed for effective destructive testing.

**Spec vs. implementation drift:** Developers often build a slightly different mental model of "what this should do" than what is written in the requirements - especially after days of working on a problem. A Blackbox tester who has only ever read the spec has no such drift.

The practical consequence is that professional QA teams and developers are kept separate, and Blackbox testing is assigned to someone who was not involved in writing the code in question. The tester's ignorance of the implementation is not a limitation - it is the entire point.

---

### O3: Design a Whitebox test plan that aims to achieve 100% "Branch Coverage" for a simple `if-else-if` code block. (K6)

**Code block:**

```python
def classify_score(score):
    if score >= 90:
        return "A"
    elif score >= 70:
        return "B"
    else:
        return "C"
```

**Goal: 100% Branch Coverage**

Branch coverage requires that every possible branch of every decision point is executed at least once. For an `if-elif-else` structure with three branches, this means three test cases - one per branch.

_Note: simple statement coverage would only require that every line runs once. Branch coverage is stricter - it also demands that the_ `False`_\-path of every condition is tested, including implicit empty branches._

| Test ID | Input | Branch taken | Expected Result |
| --- | --- | --- | --- |
| TC-WB-01 | `score = 95` | `if score >= 90` → True | `"A"` |
| TC-WB-02 | `score = 75` | `if score >= 90` → False, `elif score >= 70` → True | `"B"` |
| TC-WB-03 | `score = 50` | both conditions → False, `else` | `"C"` |

- TC-WB-01 forces the first branch to be taken.
- TC-WB-02 forces the first condition to evaluate to `False` (its False-branch) and the second to `True`.
- TC-WB-03 forces both conditions to evaluate to `False`, hitting the `else`\-branch.

With these three test cases, every possible execution path through the function has been traversed at least once - 100% branch coverage is achieved. A Whitebox tester can verify this because they can see the structure of the code; a Blackbox tester, working only from the spec "returns A, B, or C based on score", would likely arrive at the same tests - but cannot confirm coverage without seeing the code.