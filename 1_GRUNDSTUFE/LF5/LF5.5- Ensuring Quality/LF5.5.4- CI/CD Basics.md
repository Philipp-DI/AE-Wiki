# LF5.5.4: CI/CD Basics

<details>
<summary>Briefing</summary>

## User Story

As a DevOps Engineer, **I** want to automate testing using CI/CD pipelines, so that **I** can prevent broken code from being merged and ensure a consistent standard of quality across the team.

## Celebration Criteria

- **I can define** the acronyms CI and CD. (K1)
- **I know how to identify** the benefits of automated code checks on every Git push. (K2)
- **I can explain** the purpose of a Linter in a CI pipeline. (K2)

## Knowledge Briefing

Testing manually is error-prone. **CI/CD (Continuous Integration / Continuous Deployment)** automates this process. Platforms like **GitHub Actions** or GitLab CI run scripts automatically whenever someone pushes code.

- **Continuous Integration (CI):** Every time a developer pushes a branch, an automated server builds the code and runs all Unit Tests. If a test fails, the Pull Request is blocked. This prevents broken code from entering the `main` branch.
- **Continuous Deployment (CD):** If the CI phase is green (all tests pass), the CD phase automatically deploys the new code to the live production server.
- **Linters (e.g., flake8 for Python):** Often the very first step in CI. A tool that analyzes source code to flag programming errors, bugs, and stylistic errors without even running the code.

## Common Pitfalls

- Creating a CI pipeline that takes 45 minutes to run. Developers will stop waiting for it and start bypassing it. CI must be fast to provide quick feedback.

## Mandatory Tasks

1. Define the terms "Continuous Integration" and "Continuous Deployment". (K1)
2. Explain how a CI pipeline prevents a developer from accidentally destroying the `main` branch with faulty code. (K2)
3. Describe the purpose of a "Linter" in the context of software development. (K2)
4. State the typical trigger event that starts a CI pipeline (e.g., in GitHub Actions). (K1)
5. Explain why it is important for automated CI tests to run quickly. (K2)

## Optional Tasks

1. Analyze the cultural shift required in a development team to move from monthly manual deployments to fully automated daily CD pipelines. (K4)
2. Evaluate the potential risks of implementing Continuous Deployment (CD) without having a robust suite of automated Unit and Integration tests. (K5)
3. Design a conceptual CI pipeline flowchart (from `git push` to `deploy`) outlining 4 distinct automated checks that should run sequentially. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| CI/CD Basics | YouTube | "What is CI/CD Pipeline simply explained" |
| GitHub Actions | Studyflix / YouTube | "GitHub Actions tutorial for beginners" |

</details>

## Answers

### M1: Define the terms "Continuous Integration" and "Continuous Deployment". (K1)

**CI - Continuous Integration:** Every developer's code changes get automatically built and tested the moment they're pushed. If something breaks, the team knows immediately - not three weeks later.

**CD - Continuous Deployment:** Once CI is green, the code is automatically shipped to production. No manual release day, no stress - just a smooth, automated handoff.

CI combines config management, development, and testing tools to get rapid feedback on code problems; CD automates delivery of tested changes into staging or production environments.

---

### M2: Explain how a CI pipeline prevents a developer from accidentally destroying the `main` branch with faulty code. (K2)

Simple: the PR can't be merged until CI passes. When a dev pushes their branch, the pipeline spins up automatically, runs the full test suite, and either gives the green light or blocks the merge. The `main` branch never sees code that failed the test pipeline.

**Analogy:**  
Passport control at the airport - you don't get through to the gate just because you want to. The pipeline is the checkpoint, and broken code doesn't have a valid passport.

---

### M3: Describe the purpose of a "Linter" in the context of software development. (K2)

A linter (e.g. Ruff → also a formatter) statically analyses source code - without executing it - and flags syntax errors, style violations, unused variables, and other common problems. It's typically the very first step in a CI pipeline precisely because it's fast and catches a surprising number of issues before any tests even run.

**Analogy:**  
A spellcheck for code: it won't tell you whether your logic is correct, but it will tell you that your formatting is a mess and you forgot to import something.

---

### M4: State the typical trigger event that starts a CI pipeline (e.g., in GitHub Actions). (K1)

A `git push` to any branch - or more specifically, opening or updating a **Pull Request**. In GitHub Actions this is configured as a `push` or `pull_request` event trigger in the **workflow YAML file**. From that moment, the pipeline runs automatically without any manual intervention.

---

### M5: Explain why it is important for automated CI tests to run quickly. (K2)

Because a pipeline everybody waits for is a pipeline nobody uses. If a CI run takes 45 minutes, devs stop waiting for the result, push anyway, and the whole point is lost. Fast feedback (ideally under 10 minutes) keeps the pipeline integrated into the actual workflow instead of becoming a bureaucratic obstacle people work around.

**The Common Pitfall** in the briefing nails it: slow CI gets bypassed. Speed isn't a nice-to-have - it's what makes the system work in practice.

---

### O1: Analyze the cultural shift required in a development team to move from monthly manual deployments to fully automated daily CD pipelines. (K4)

Monthly manual deployments carry a specific culture with them: big batches of changes, lengthy release checklists, a "release day" that everyone dreads, and a clear separation between "dev throws it over the wall" and "ops deploys it." Accountability is diffuse because so many changes land at once.

Daily CD flips every single one of those assumptions:

**From batch to flow:** Small, frequent changes replace large releases. This is psychologically uncomfortable at first - it feels riskier to deploy constantly, even though the opposite is true. Smaller changes are easier to reason about, easier to roll back, and less likely to contain catastrophic surprises.

**From fear to trust:** Manual releases are often nerve-wracking because they're rare and consequential. When deployment is automated and daily, it becomes routine. The fear diminishes. But getting there requires the team to genuinely trust their test suite - which means investing in it, not treating it as optional.

**Shared ownership:** Westermann's DevOps material (see → LF 6-9) highlights that DevOps exists precisely to eliminate the friction between development (wanting to ship constantly) and operations (wanting stability). CD only works if both sides see themselves as responsible for production quality - not just at the moment of deployment, but throughout development.

**The hardest part** is usually not the tooling - it's convincing people that "deploy every day" is safer than "deploy once a month and pray."

---

### O2: Evaluate the potential risks of implementing Continuous Deployment (CD) without having a robust suite of automated Unit and Integration tests. (K5)

CD without solid tests is essentially an automated way to ship bugs faster. The risks compound across multiple dimensions:

**No safety net:** CD's entire value proposition rests on the assumption that "if CI is green, it's safe to ship." Remove meaningful CI checks and that assumption collapses. Green just means "it compiled" - not "it works."

**Rapid blast radius:** In a manual monthly release, a bad bug sits in staging for weeks before hitting production. In daily CD, it's live within hours or minutes of being merged. The speed that makes CD powerful also makes defects propagate faster.

**Rollback pressure vs. fix-forward pressure:** Without tests, teams lose confidence in both deploying and rolling back. Rolling back a bad deploy in CD should be a non-event - but only if you trust your pipeline enough to know the previous version was actually clean. Without test coverage, you don't know that.

**False confidence:** A pipeline that passes but doesn't actually test meaningful behaviour is arguably worse than no pipeline at all - it creates the illusion of safety. Teams may invest less in manual review or QA because "the pipeline will catch it," when in fact it won't.

_The bottom line: CD is an accelerator, not a safety system on its own. Deploying faster without tests just means failing faster._

---

### O3: Design a conceptual CI pipeline flowchart (from `git push` to `deploy`) outlining 4 distinct automated checks that should run sequentially. (K6)

![diagram.drawio.svg](files/019e9193-3c04-735b-ae9b-149c1a79fe07/diagram.drawio.svg?t=1780558806956)

1. **Linter & Formatter** - fastest and cheapest check, runs first. Catches syntax issues, style violations, and obvious mistakes without executing a single line. No point running tests against code that doesn't even conform to the project's standards.
2. **Unit tests** - the bulk of the automated suite. Fast, isolated, and the first real proof that the logic does what it should.
3. **Integration tests** - slower, but verify that the modules actually work together. DB connections, API calls, service boundaries - everything a unit test deliberately ignores.
4. **Deploy** - only reached if all three prior stages pass. Fully automated push to production. The gate is real: a failed check at any stage kills the pipeline and blocks the PR.

The fail path is intentional - it returns to the dev, not to a human reviewer. That's the whole point of CI: the feedback loop stays fast and automated.