# LF5.4.3: Python Fundamentals (Procedural)

<details>
<summary>Briefing</summary>

## User Story

As a Developer, **I** want to master Python's procedural syntax, so that **I** can write functions, implement logic using loops and conditions, and understand Python's unique structure.

## Celebration Criteria

- **I can execute** Python scripts containing variables and basic data types. (K3)
- **I know how to implement** control structures (if/else) and loops (for/while). (K3)
- **I can explain** the critical role of indentation in Python. (K2)

## Knowledge Briefing

Python is renowned for its readability. It forces clean code by using whitespace instead of brackets.

**Key Concepts:**

- **Indentation (Einrückung):** Python uses 4 spaces to define blocks of code (instead of `{}` used in C or Java). If your indentation is wrong, the code crashes (IndentationError).
- **Dynamic Typing:** You don't declare the data type. `x = 10` (Integer), `x = "Hello"` (String).
- **Control Structures:**
  - `if condition:` followed by an indented block.
  - `for item in list:` (Iterates over collections).
  - `while condition:` (Loops as long as true).
- **Functions:** Defined using `def my_function(param):`. They encapsulate logic to make it reusable.

## Common Pitfalls

- Mixing spaces and tabs. Pick one (preferably 4 spaces, which modern IDEs like VSCode handle automatically). Mixing them will cause fatal errors.

## Mandatory Tasks

1. Explain the unique way Python defines code blocks (like the inside of an `if` statement) compared to languages like Java or C. (K2)
2. Write a Python snippet that defines a function named `greet` which takes a `name` parameter and prints "Hello \[name\]". (K3)
3. Write a Python `if/else` statement that checks if a variable `age` is greater than or equal to 18. (K3)
4. Write a Python `for` loop that iterates over a list of numbers `[1, 2, 3]` and prints each number. (K3)
5. Identify the error in this code block and explain why it fails: `if True:` `print("It is true")` (K2)

## Optional Tasks

1. Analyze how Python's dynamic typing affects memory usage and execution speed compared to a statically typed language. (K4)
2. Evaluate the use of "List Comprehensions" in Python to write highly efficient and concise loops. (K5)
3. Design a procedural Python script that reads a text file, counts the frequency of each word, and prints the top 3 most common words. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Python Basics | YouTube | "Python in 100 Seconds" |
| Python Indentation | Google | "Why does Python use indentation" |

</details>

## Answers

### M1: Explain the unique way Python defines code blocks (like the inside of an `if` statement) compared to languages like Java or C. (K2)

In Java or C, code blocks are delimited by **curly braces** `{ }` - the compiler doesn't care about whitespace at all. You could write an entire `if` block on a single line and it would compile fine.

Python takes a fundamentally different approach: **indentation is the syntax** (Westermann, LF1-5, S. 527-528: "Leerzeichen haben eine Bedeutung und das Einrücken von Programmzeilen ist zur Bildung von Programmblöcken unbedingt notwendig"). A block begins after a colon `:` and ends when the indentation level returns to where it was before. Convention - and PEP 8, Python's official style guide - prescribes **4 spaces per level**.

```python
# Python - indentation IS the block
if temperature > 30:
    print("It's hot")   # inside the if-block: 4 spaces
    print("Stay hydrated")
print("Done")           # back at 0: outside the block
```

```java
// Java - braces define the block, indentation is optional
if (temperature > 30) {
    System.out.println("It's hot");
System.out.println("Still in the block, even though badly indented");
}
```

A wrong indentation level in Python isn't a style problem - it's a hard crash (`IndentationError`). This forces clean, readable structure from the very first line.

---

### M2: Write a Python snippet that defines a function named `greet` which takes a `name` parameter and prints "Hello \[name\]". (K3)

```python
def greet(name):
    print("Hello " + name)

greet("Alice")
```

Output: `Hello Alice`

The `def` keyword introduces the function signature (Westermann, LF1-5, S. 549). The parameter `name` is listed in the parentheses. Everything indented below belongs to the function body. The function is then called by its name with a concrete argument.

---

### M3: Write a Python `if/else` statement that checks if a variable `age` is greater than or equal to 18. (K3)

```python
age = 20

if age >= 18:
    print("Access granted.")
else:
    print("Access denied - you must be 18 or older.")
```

The comparison operator `>=` ("greater than or equal to") returns `True` or `False` (Westermann, LF1-5, S. 544). The `else` branch catches every case where the condition was not met - no separate condition needed there.

---

### M4: Write a Python `for` loop that iterates over a list of numbers `[1, 2, 3]` and prints each number. (K3)

```python
for number in [1, 2, 3]:
    print(number)
```

Output:

```
1
2
3
```

Python's `for` loop iterates directly **over the elements** of a collection - no index counter, no manual increment needed (Westermann, LF1-5, S. 556: "Zahlschleife"). The variable `number` takes on each value in the list in turn, one iteration per element.

**Analogy:** A Java `for` loop says "start at index 0, go while `i < list.size()`, then `i++`." Python's `for` says "just give me each item" - the mechanics are handled for you.

---

### M5: Identify the error in this code block and explain why it fails: `if True:` `print("It is true")` (K2)

**_DISCLAIMER_**_: The above code on its own runs regardless of the indentation error!_

The `print` statement is **not indented**. Written out as it would appear in a file:

```python
if True:
print("It is true")    # IndentationError: expected an indented block
```

Python expects at least one indented statement after the colon that opens the `if` block. Finding a line at the same indentation level as `if` itself, the interpreter has no block to execute and raises:

```
IndentationError: expected an indented block after 'if' statement on line 1
```

The fix is straightforward:

```python
if True:
    print("It is true")    # 4 spaces: now belongs to the if-block
```

This is a direct consequence of what M1 described: in Python, indentation is not decorative - it is functional.

---

### O1: Analyze how Python's dynamic typing affects memory usage and execution speed compared to a statically typed language. (K4)

In a statically typed language like Java or C, the compiler knows the exact type of every variable at compile time. It can therefore allocate a fixed, minimal amount of memory - an `int` is always exactly 4 bytes, a `double` always 8 bytes - and generate highly optimized machine instructions tailored to that specific type.

Python works differently. Every value, even a simple integer, is stored as a **full Python object** at runtime (Westermann, LF1-5, S. 537: "Variablen haben in Python keinen bestimmten Datentyp"). That object carries extra overhead: a reference count for garbage collection, a pointer to its type, and the actual value. A Python `int` with the value `1` occupies around **28 bytes** in CPython, compared to 4 bytes in Java.

The speed impact follows from the same cause. Because Python only knows a variable's type at the moment a line executes, the interpreter must look up the type on every operation. Adding two numbers in Python involves: resolve the variable names → look up the type of each object → find the appropriate addition method → call it → wrap the result in a new object. In C, the compiler emits a single machine instruction.

**The practical consequences:**

|     | Python (dynamic) | Java / C (static) |
| --- | --- | --- |
| **Memory per integer** | ~28 bytes | 4 bytes |
| **Type resolution** | At runtime, every operation | At compile time, once |
| **Raw execution speed** | 10-100x slower than C for CPU-bound work | Near-native |
| **Flexibility** | Reassign any variable to any type freely | Type locked at declaration |

**Why Python is still widely used despite this:** the performance gap largely disappears when the heavy lifting is delegated to libraries written in C - `numpy`, `pandas`, and `tensorflow` all execute their core loops in compiled C or Fortran. Python becomes the orchestrator rather than the worker. For I/O-bound tasks (web requests, database queries, file operations), the bottleneck is the network or disk, not the interpreter.

Where raw CPU performance genuinely matters - video codecs, game physics, OS kernels - Python is the wrong tool, and the ecosystem doesn't pretend otherwise.

---

### O2: Evaluate the use of "List Comprehensions" in Python to write highly efficient and concise loops. (K5)

Thanks to ‘List Comprehensions’ in Python you save the work of having an additional `for` -Loop. The logic can be written in a single line of code.  
The **basic Syntax** looks like this:

`newlist = [{expression} for {item} in {iterable} if {condition} == True]`  
The return value is a new list, leaving the old list unchanged.

**Practical example/comparison:**

**Without LC**

```python
list = ["car", "bike", "bus", "train"]
newlist = []

for x in list:
  if "b" in x:
    newlist.append(x)

print(newlist)

"""
Output:
["bike", "bus"]
"""
```

**With LC**

```python
list = ["car", "bike", "bus", "train"]
newlist = [x for x in list if "b" in x]

print(newlist)

"""
Output:
["bike", "bus"]
"""
```

_Source(s): https://www.w3schools.com/python/python_lists_comprehension.asp_

---

### O3: Design a procedural Python script that reads a text file, counts the frequency of each word, and prints the top 3 most common words. (K6)

```python
import string

with open("demo.txt", "r", encoding="utf-8") as f:
    text = f.read()

words_counted: dict[str, int] = {}

# clean-up
clean = text.strip().lower()
clean = clean.translate(clean.maketrans("", "", string.punctuation))

words = clean.split()

for word in words:
    if word in words_counted:
        words_counted[word] += 1
    else:
        words_counted[word] = 1

sort_high_to_low_word_count = sorted(
    words_counted.items(), key=lambda item: item[1], reverse=True
)

print("Top 3 Occurrences:\n")

for rank, (k, v) in enumerate(sort_high_to_low_word_count[:3], start=1):
    print(f"{rank}. {k}: {v}")
```