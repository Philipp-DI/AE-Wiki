# LF5.5.3: The Art of Debugging

<details>
<summary>Briefing</summary>

## User Story

As a Developer, **I** want to use a debugger to step through executing code, so that **I** can inspect variable states in real-time and find hidden logic errors.

## Celebration Criteria

- **I can define** the purpose of a Breakpoint. (K1)
- **I know how to control** program execution using step-over and step-into commands. (K3)
- **I can explain** the advantages of a debugger over print statements. (K2)

## Knowledge Briefing

When code fails, beginners use `print("here")` to find the error. Professionals use a **Debugger**. Modern IDEs (like VSCode) have built-in debuggers for Python.

**Core Debugging Features:**

- **Breakpoint (Haltepunkt):** A red dot you place on a line of code. The program will run at full speed and completely _pause_ right before executing this line.
- **Variable Inspection:** While paused, you can see the exact current value of every variable in memory.
- **Execution Control:**
  - **Step Over (F10):** Execute the current line and pause on the next line. (Does not dive into functions).
  - **Step Into (F11):** If the current line calls a function, dive _inside_ that function to debug it line by line.
  - **Continue / Resume (F5):** Run at full speed again until the next Breakpoint.

## Common Pitfalls

- Putting a breakpoint inside a loop that runs 10,000 times and having to hit "Continue" thousands of times. Use "Conditional Breakpoints" (e.g., pause only if `i == 9999`).

## Mandatory Tasks

1. Define what a "Breakpoint" is in the context of software debugging. (K1)
2. Explain the functional difference between the "Step Over" and "Step Into" commands in a debugger. (K2)
3. Describe how a debugger helps a developer understand the state of variables compared to just reading the code. (K2)
4. State one major disadvantage of using multiple `print()` statements to find a bug instead of using an IDE debugger. (K1)
5. Explain the purpose of the "Continue" (Resume) command when a program is currently paused at a breakpoint. (K2)

## Optional Tasks

1. Analyze a scenario where a logical bug only occurs on the 500th iteration of a `for` loop, and explain how a Conditional Breakpoint solves this. (K4)
2. Evaluate the difficulty of debugging asynchronous or multi-threaded code compared to standard procedural code. (K5)
3. Design a short guide for a junior developer explaining how to attach the VSCode debugger to a Python script running inside a Docker container. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| IDE Debugging Basics | YouTube | "How to use a debugger VSCode Python" |
| Step Into vs Step Over | Google | "Debugger step over vs step into explained" |

</details>

## Answers

## M1: Define what a "Breakpoint" is in the context of software debugging. (K1)

A **Breakpoint** is a marker that a developer sets on a specific line of code inside their IDE. When the program is executed in debug mode, it runs at full speed as normal - but stops execution completely at that marked line. The program is then in a paused state, and the dev can inspect the current values of all variables in memory before deciding how to continue.

‘Westermann’ describes the debugger as a development tool that supports the developer in error-finding by allowing the program to be "executed step by step and the individual program states to be examined" - a Breakpoint is precisely the mechanism that triggers this pause.

---

### M2: Explain the functional difference between the "Step Over" and "Step Into" commands in a debugger. (K2)

Both commands advance execution by one step while the program is paused at a breakpoint, but they differ in what counts as "one step":

**Step Over (F10):** Executes the current line and pauses on the very next line in the same scope. If the current line contains a function call, that entire function runs to completion internally - the debugger does not dive into it. From the developer's perspective, the function call is treated as a single atomic action.

**Step Into (F11):** If the current line contains a function call, Step Into jumps the debugger inside that function, pausing at its very first line. This allows the developer to trace the internal logic of the called function line by line.

**Analogy:**  
Reading a book with footnotes: Step Over reads the sentence and moves to the next one, treating each footnote as already resolved. Step Into stops at the footnote number, flips to the back of the book, and reads the full footnote before returning. Which you choose depends on whether you trust the footnote or suspect it contains the error.

**In practice:** use Step Over to move quickly through code you already trust, and Step Into when you suspect the bug is hiding inside a specific function.

---

### M3: Describe how a debugger helps a developer understand the state of variables compared to just reading the code. (K2)

Reading code statically means relying on mental simulation - the developer has to trace variable values in their head, which becomes increasingly error-prone as program complexity grows. A loop with conditional updates, a function modifying a variable passed by reference, a counter that is incremented in three different places - these are genuinely difficult to follow mentally.

A debugger solves this by showing the actual, live state of every variable in memory at the exact moment execution is paused. There is no simulation involved. The developer sees the real value `counter = 47` on the screen, not the value they assumed it would be.

**This is the critical distinction:** the code tells you what is _supposed_ to happen. The debugger's variable inspection window tells you what is _actually_ happening. In the case of a logic error, those two things differ - and the debugger makes the difference visible immediately.

**Analogy:**  
Weather forecast vs. thermometer: you can read the forecast (the code) and believe it will be 20°C. But only the thermometer (the debugger) tells you it is actually 13°C outside right now. Logical bugs live in the gap between forecast and reality.

---

### M4: State one major disadvantage of using multiple `print()` statements to find a bug instead of using an IDE debugger. (K1)

The most significant disadvantage is that `print()` debugging permanently modifies the source code. Every debug statement must be manually inserted before the test run, and then manually removed or commented out before the code goes anywhere near production. _Sadly, this is how I tested the majority of code that I wrote until just now._

Beyond that: `print()` only captures what you specifically thought to print at the moment you wrote the statement. A debugger gives you access to the entire program state - every variable, every object attribute - without having anticipated in advance which one would matter.

---

### M5: Explain the purpose of the "Continue" (Resume) command when a program is currently paused at a breakpoint. (K2)

When a program is paused at a breakpoint, the developer has the option to inspect variables, evaluate expressions, or step through code line by line. The **Continue command** (F5 in VSCode) ends this paused state and resumes full-speed execution - until the next breakpoint is encountered, at which point the program pauses again.

This is particularly useful when a bug only appears under a specific condition and multiple breakpoints have been placed throughout the code. Instead of stepping through every line of every function manually, the dev lets the program run freely between the relevant pausing points.

**Analogy:**  
A security guard doing rounds: they walk the entire building at normal speed, but stop and inspect closely at each checkpoint they marked as important. Continue is the command to "walk normally until the next checkpoint."

---

### O1: Analyze a scenario where a logical bug only occurs on the 500th iteration of a `for` loop, and explain how a Conditional Breakpoint solves this. (K4)

**Scenario:**

A Python script processes a list of 10,000 sensor readings. Somewhere around index 500, a calculation produces an unexpected negative value that corrupts all following results. The bug does not occur on the first iteration, or the second, or any of the first 499 - only from 500 onward.

**Why a regular breakpoint would be insufficient:**

Placing a normal breakpoint inside the loop body is the obvious first instinct. The problem: the program will pause on iteration 1, then iteration 2, then 3 - and the developer must press Continue 499 times before the interesting state is even reached. In a loop running 10,000 times, this is completely unusable.

**The Conditional Breakpoint:**

Modern IDEs (including VSCode) allow a breakpoint to _carry an attached condition_ - a boolean expression that is evaluated at runtime each time that line is reached. The breakpoint only triggers and pauses execution if the condition evaluates to `True`.

**For this scenario:** right-clicking the breakpoint and entering the condition `i == 499` (or `sensor_value < 0`) means the program **runs freely through all previous iterations** and only **pauses when exactly the interesting state exists**. The developer arrives precisely at the moment the bug occurs, with all variables set to their actual problematic values, ready for inspection.

This mirrors the Common Pitfall described in the story's briefing above - and is the professional solution to it. The key insight is that the condition can reference any variable in scope, including the loop counter, the current element's value, or any computed intermediate result.

---

### O2: Evaluate the difficulty of debugging asynchronous or multi-threaded code compared to standard procedural code. (K5)

Debugging procedural code rests on one fundamental assumption: **execution is deterministic and sequential**. Line 10 runs before line 11, always. A developer can set a breakpoint and know exactly what state the program is in when it pauses. The mental model of "the program is here" maps cleanly to a single point in a single sequence of instructions.

Both assumptions are null in asynchronous and multi-threaded code.

**The core problem - non-determinism:** In a multi-threaded program, two or more threads _execute concurrently_ and may access shared memory. The order in which they do so depends on the _OS scheduler, CPU timing, and system load_ at that exact moment. A bug caused by a _race condition_ (two threads reading and writing a shared variable in an interleaved order that produces an invalid state) may appear on one run and disappear on the next - with identical input data.

**The observer effect:** Pausing execution with a debugger in a multi-threaded context changes the timing relationships between threads. A race condition that reliably triggers in production may never trigger under the debugger, because _the act of pausing thread A changes the window of opportunity for thread B to cause the problem_. The bug genuinely disappears when you try to observe it - a software equivalent of **Heisenberg's uncertainty principle**.

**Async complexity:** In async/await code (e.g., Python's `asyncio`), execution can jump between coroutines at `await` points in ways that are difficult to follow with standard step-through debugging. The call stack shown in the debugger may not represent the logical flow the developer might expect.

**Practical consequence:** Multi-threaded and async debugging requires **specialized tools** (thread-aware debuggers, logging frameworks that capture timestamps and thread IDs, dedicated race condition detectors) and a fundamentally different approach - one that relies less on step-through inspection and more on structured logging, reproducible minimal test cases, and static analysis tools.

---

### O3: Design a short guide for a junior developer explaining how to attach the VSCode debugger to a Python script running inside a Docker container. (K6)

**Goal:** Step through Python code running inside a Docker container using VSCode's built-in debugger, without stopping and restarting the container on every change.

---

**Prerequisites:**

- VSCode with the "Python" extension installed
- Docker Desktop running, container already built
- The Python package `debugpy` available inside the container (via `pip install debugpy`)

---

**Step 1: Start the Python script with debugpy inside the container**

Instead of running your script directly, start it via `debugpy` and tell it to wait for a debugger to attach before continuing:

```bash
python -m debugpy --listen 0.0.0.0:5678 --wait-for-client your_script.py
```

The `--wait-for-client` flag causes the script to pause immediately at start-up until VSCode connects. `5678` is the port debugpy listens on.

---

**Step 2: Expose the debug port when starting the container**

When running the container, map port 5678 from the container to your local machine:

```bash
docker run -p 8080:5678 your-image-name
```

---

**Step 3: Create a VSCode launch configuration**

In your project, open (or create) `.vscode/launch.json` and add this configuration:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Attach to Docker",
      "type": "python",
      "request": "attach",
      "connect": {
        "host": "localhost",
        "port": 8080
      },
      "pathMappings": [
        {
          "localRoot": "${workspaceFolder}",
          "remoteRoot": "/app"
        }
      ]
    }
  ]
}
```

The `pathMappings` entry is critical: it tells VSCode how your local file paths map to paths inside the container (here, `/app` is the working directory inside the container - adjust to match yours).

---

**Step 4: Attach from VSCode**

With the container running and waiting, go to the Run & Debug panel in VSCode (Ctrl+Shift+D), select "Attach to Docker" from the dropdown, and press the green play button. VSCode connects to `debugpy` on port 5678, and the script resumes - but now pauses at any breakpoints you have set in your local code files.

---

**What you can now do:**

- Set breakpoints in your `.py` files as normal - they work inside the container
- Inspect variables, step through code, use the debug console
- The container keeps running; you do not need to rebuild or restart for every debug session

---

**Common issue:** If the path mapping is wrong, breakpoints will not trigger. Double-check that `remoteRoot` matches the actual working directory defined in your `Dockerfile` (`WORKDIR /app` or similar).

:::success
**Question I still have:** _How is this useful/relevant since containers are stateless? If I modify a script inside a container, the changes won’t be saved. I’d need to re-build it._

_→ As discussed in Teams, you can use bind mounts in this case to inject a local file into the container without having to rebuild it. For further information, see:_ [_https://dev.to/meghasharmaaaa/bind-mount-46d0_](https://dev.to/meghasharmaaaa/bind-mount-46d0)  
_Danke, wollt ich mir auch gerade einfügen ☺️_
:::

_Source(s): code.visualstudio.com/docs/containers/debug-python; debugpy GitHub documentation_