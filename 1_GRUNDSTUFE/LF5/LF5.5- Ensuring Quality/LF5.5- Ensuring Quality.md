# LF5.5: Ensuring Quality

## Epic User Story

As IT Consultants, **we** want to systematically test and debug our prototype, so that **we** can ensure high software quality, prevent regressions using automation, and confidently hand the product over for formal customer acceptance.

## Celebration Criteria (Definition of Done)

- **We can evaluate** the overall system stability using structured testing methodologies. (K6)
- **We know how to formulate** and execute precise test cases based on initial requirements. (K5)
- **We can implement** automated quality checks using basic CI/CD pipelines. (K4)
- **We can conduct** a formal User Acceptance Test (UAT) to secure stakeholder approval. (K5)

## Comprehensive Task: The Quality Gate (13 SP)

**The Mission:** Your prototype from Epic 5.4 is running. But does it actually work according to the "Lastenheft" from Epic 5.1? You must subject your code (for the Neustadt Museum, Mutti's Bakery, or Metropolis Library) to rigorous testing. You will document bugs, fix them using a debugger, automate code checks, and prepare the final acceptance document for your stakeholder.

**Tasks:**

1. **Analog Test Plan:** On a whiteboard, map out 5 critical test cases based on the Functional Requirements defined in Epic 5.1. Define the Precondition, the exact Input, and the strictly Expected Output for each case.
2. **The Bug Hunt (Debugging):** Deliberately plant a logical error in your Python `main.py` (e.g., a wrong calculation or incorrect if-condition). Use the VSCode Debugger to set a Breakpoint just before the error. Step through the code, inspect the variable values, and take a screenshot proving you found the error via the debugger.
3. **Automated Pipeline (CI/CD):** In your GitHub repository, create a simple GitHub Actions Workflow (e.g., `.github/workflows/lint.yml`). Configure it so that every time someone pushes code, it automatically runs a Python linter (like `flake8`) to check for syntax and style errors.
4. **UAT Protocol drafting:** Draft a formal "User Acceptance Test Protocol" document in Docmost. It must include sections for the Stakeholder Name, Date, Tested Features, Pass/Fail checkboxes, and a final Signature line.
5. **Final Review:** Execute the 5 analog test cases against your running Docker container. Document the "Actual Results" in Docmost alongside your test plan. Ensure all automated GitHub Actions pass with a green checkmark.

**Result Artifact:** A verified GitHub repository featuring a green CI/CD badge, accompanied by a comprehensive "Quality Assurance & Acceptance Report" in Docmost containing the test cases, debugging screenshots, and the blank UAT Protocol.