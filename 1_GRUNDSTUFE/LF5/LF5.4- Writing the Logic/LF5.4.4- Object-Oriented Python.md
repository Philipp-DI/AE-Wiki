# LF5.4.4: Object-Oriented Python

<details>
<summary>Briefing</summary>

## User Story

As a Software Engineer, **I** want to implement UML Class Diagrams in Python, so that **I** can model complex, encapsulated data structures using Object-Oriented Programming (OOP).

## Celebration Criteria

- **I can define** a Python Class with properties and methods. (K1)
- **I know how to instantiate** an object from a class using the `__init__` constructor. (K3)
- **I can apply** the concept of `self` to access object attributes. (K3)

## Knowledge Briefing

Translating the UML Class Diagrams from Epic 5.2 into Python requires understanding OOP syntax.

- **Class vs. Object:** The Class is the blueprint (e.g., `Car`). The Object is the actual instance built from it (e.g., `My Red Toyota`).
- `__init__` **Method:** The constructor. It runs automatically when a new object is created.
- `self`**:** The first parameter in every method inside a class. It represents the specific object itself. You use `self.attribute` to store data _inside_ that specific object.
- **Encapsulation:** Python doesn't have strict `private` keywords. By convention, prefixing an attribute with an underscore (e.g., `self._password`) signals to other developers: "Do not touch this directly from the outside."

## Common Pitfalls

- Forgetting to pass `self` as the first argument when defining a method inside a class. This will result in a `TypeError` when you try to call it.

## Mandatory Tasks

1. Define the difference between a "Class" and an "Object" using an everyday metaphor. (K1)
2. Write the Python code to define an empty class named `User`. (K3)
3. Explain the purpose of the `__init__` method in a Python class. (K2)
4. Write a complete Python class named `Book` with an `__init__` method that accepts and stores a `title` and an `author` using `self`. (K3)
5. Describe how Python developers simulate "private" visibility for an attribute, since Python lacks a strict `private` keyword. (K2)

## Optional Tasks

1. Analyze the concept of OOP "Inheritance" by creating a parent class `Employee` and a child class `Manager` in Python. (K4)
2. Evaluate how "Polymorphism" allows different Python classes to share the same method name but behave differently. (K5)
3. Design a set of classes that strictly demonstrate "Composition" (e.g., a `Computer` class that instantiates a `Processor` class inside its own `__init__`). (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Python OOP | YouTube | "Object Oriented Programming in Python" |
| Python Dunder Methods | Google | "Python init self explained" |

</details>

## Answers

### M1: Define the difference between a "Class" and an "Object" using an everyday metaphor. (K1)

A **class** is a blueprint or template - it describes _what something looks like and what it can do_, but it doesn't exist as a real, tangible thing yet. An **object** is a concrete instance built from that blueprint.

**Analogy/metaphor?:** A class is the architect's floor plan for a house. The plan itself doesn't have a front door you can open or a kitchen you can cook in. The moment a contractor builds from that plan, an actual house exists → **the object**. You can build ten different houses from the same plan; each one has its own address, its own paint colour, its own residents, but they all share the same structure.

---

### M2: Write the Python code to define an empty class named `User`. (K3)

```python
class User:
    pass
```

The `pass` keyword is required because Python doesn't allow an empty indented block. It's a placeholder that means "nothing here yet" - the class is valid but has no attributes or methods defined. You'd replace `pass` as soon as you add content. You could also use `…`.

---

### M3: Explain the purpose of the `__init__` method in a Python class. (K2)

`__init__` is Python's **constructor** - the method that runs automatically the moment a new object is created from the class. Its job is to **initialize** **the new object's attributes** by assigning starting values to them via `self`.

**Example:**

```python
class Car:
    def __init__(self, brand, colour):
        self.brand = brand
        self.colour = colour

new_car = Car("Toyota", "white")
```

When `Car("Toyota", "white")` is called, Python creates a blank object, then immediately calls `__init__` on it, passing `"Toyota"` and `"red"` as arguments. By the time the line finishes, `new_car` is a fully initialized object with its own `brand` and `colour`.

Without `__init__`, every object would start empty and you'd have to set attributes manually afterwards - which could lead to errors or inconsistency.

---

### M4: Write a complete Python class named `Book` with an `__init__` method that accepts and stores a `title` and an `author` using `self`. (K3)

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

# Creating an object from the class
new_book = Book("title", "author")
```

`self.title` and `self.author` are **instance attributes** - they belong to each individual object. The class itself holds no data; only the objects do.

---

### M5: Describe how Python developers simulate "private" visibility for an attribute, since Python lacks a strict `private` keyword. (K2)

Python has no enforced `private` keyword the way Java or C# do. Instead, visibility is communicated through **naming conventions**:

| Prefix | Convention | Meaning |
| --- | --- | --- |
| `name` | No prefix | `public` - accessible from anywhere |
| `_name` | Single underscore | `protected` - signals "internal use only"; technically still accessible, but devs treat it as off-limits from outside |
| `__name` | Double underscore | `private` - Python applies **name mangling**, renaming it to `_ClassName__name` internally, making accidental outside access much harder |

**Example:**

```python
class UserAccount:
    def __init__(self, username, password):
        self.username = username        # public
        self._session_token = None      # protected - internal implementation detail
        self.__password = password      # private - don't touch this from outside

account = UserAccount("alice", "s3cr3t")
print(account.username)         # works fine
print(account._session_token)   # works, but the underscore is a clear warning sign
print(account.__password)       # AttributeError - name mangling prevents direct access
print(account._UserAccount__password)  # works by deliberately bypassing the convention
```

The double-underscore approach isn't impenetrable - Python is a language that trusts its developers. It's a “social contract” enforced by convention rather than by the compiler.

---

### O1: Analyze the concept of OOP "Inheritance" by creating a parent class `Employee` and a child class `Manager` in Python. (K4)

Inheritance lets a new class take on all properties and methods of an existing one and extend them:

```python
class Employee:
    def __init__(self, name: str, employee_id: str, salary: int):
        self.name = name
        self.employee_id = employee_id
        self._salary = salary  # protected: subclasses may need it

    def get_info(self):
        return f"[{self.employee_id}] {self.name} | Salary: {self._salary} EUR"

    def work(self):
        return f"{self.name} is completing assigned tasks."


class Manager(Employee):
    def __init__(self, name: str, employee_id: str, salary: int, department: str):
        super().__init__(name, employee_id, salary)  # call parent constructor
        self.department = department
        self._reports: list[Employee] = []

    def add_report(self, employee: Employee):
        self._reports.append(employee)

    def get_info(self):  # method overriding
        base = super().get_info()
        return f"{base} | Dept: {self.department} | Reports: {len(self._reports)}"

    def work(self):  # overridden behaviour
        return f"{self.name} is conducting the team meeting."


dev = Employee("Toma Te", "E-101", 52000)
mgr = Manager("Franz Branntwein", "M-007", 178000, "Engineering")
mgr.add_report(dev)

print(dev.get_info())
print(mgr.get_info())
print(dev.work())
print(mgr.work())
```

**Notes on this:**

- `super().__init__(...)` calls the parent's constructor so you don't have to duplicate `name`, `employee_id`, and `salary` setup in every child class.
- `Manager` **inherits** `get_info()` **and** `work()` **from** `Employee`, but overrides both with its own versions. The original `Employee.get_info()` isn't lost - `super().get_info()` lets the `Manager` version reuse it before appending extra info.
- `Manager` **extends** `Employee` by adding `department` and `_reports` - attributes that make no sense on a plain `Employee` but are essential for the management role.

**Analogy:** `Employee` is the general job contract every staff member signs. `Manager` starts with that same contract (inherited), then adds a rider covering department responsibilities and team authority. They don't rewrite the whole contract - they extend it.

---

### O2: Evaluate how "Polymorphism" allows different Python classes to share the same method name but behave differently. (K5)

Here’s an auto-generated **example** to help understanding:

```python
class Shape:
    def area(self):
        raise NotImplementedError("Subclass must implement area()")

    def describe(self):
        return f"I am a {type(self).__name__} with area = {self.area():.2f}"


class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * self.radius ** 2


class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height


class Triangle(Shape):
    def __init__(self, base, height):
        self.base = base
        self.height = height

    def area(self):
        return 0.5 * self.base * self.height


# Polymorphism in action - one loop, three different behaviours
shapes = [Circle(5), Rectangle(4, 6), Triangle(3, 8)]

for shape in shapes:
    print(shape.describe())
```

Output:

```
I am a Circle with area = 78.54
I am a Rectangle with area = 24.00
I am a Triangle with area = 12.00
```

The `for` loop calls `.describe()` on each object. `describe()` internally calls `self.area()`. Python's **dynamic binding** figures out at runtime which `area()` to use - the one for `Circle`, `Rectangle`, or `Triangle`. The calling code doesn't need to know or care what type it's dealing with.

**Why this matters in practice:** you can write generic functions (`print_report(shapes)`, `sort_by_area(shapes)`) that work on any `Shape` subclass - including ones that don't exist yet. New shapes can be added later without changing a single line of the calling code. This is the extensibility that makes large codebases maintainable.

---

### O3: Design a set of classes that strictly demonstrate "Composition" (e.g., a `Computer` class that instantiates a `Processor` class inside its own `__init__`). (K6)

Composition is the alternative to inheritance for building complex objects. Instead of saying "a `Computer` _is a_ `Processor`" (which would be inheritance and is obviously wrong), you say "a `Computer` _has a_ `Processor`" - and the Computer _owns_ that Processor as an internal part.

```python
class Processor:
    def __init__(self, model: str, cores: int, clock_ghz: float):
        self.model = model
        self.cores = cores
        self.clock_ghz = clock_ghz

    def get_info(self):
        return f"{self.model} ({self.cores} cores @ {self.clock_ghz} GHz)"


class RAM:
    def __init__(self, capacity_gb: int, speed_mhz: int):
        self.capacity_gb = capacity_gb
        self.speed_mhz = speed_mhz

    def get_info(self):
        return f"{self.capacity_gb} GB DDR5 @ {self.speed_mhz} MHz"


class Storage:
    def __init__(self, capacity_tb: int, storage_type: str):
        self.capacity_tb = capacity_tb
        self.storage_type = storage_type

    def get_info(self):
        return f"{self.capacity_tb} TB {self.storage_type}"


class GPU:
    def __init__(self, model: str, capacity_gb: int):
        self.model = model
        self.capacity_gb = capacity_gb

    def get_info(self):
        return f"{self.model} ({self.capacity_gb} GB)"


class Computer:
    def __init__(self, name: str):
        self.name = name
        # Composition: Computer creates and owns its components
        self.processor = Processor("Intel Core i9-14900K", 24, 3.2)
        self.ram = RAM(32, 6000)
        self.storage = Storage(2, "NVMe SSD")
        self.gpu = GPU("RTX 5080", 20)

    def specs(self):
        print(f"--- {self.name} ---")
        print(f"  CPU:      {self.processor.get_info()}")
        print(f"  RAM:      {self.ram.get_info()}")
        print(f"  Storage:  {self.storage.get_info()}")
        print(f"  GPU:      {self.gpu.get_info()}")


workstation = Computer("Dev Workstation")
workstation.specs()

Print Output:
--- Dev Workstation ---
  CPU:      Intel Core i9-14900K (24 cores @ 3.2 GHz)
  RAM:      32 GB DDR5 @ 6000 MHz
  Storage:  2 TB NVMe SSD
  GPU:      RTX 5080 (20 GB)
```

**The key design decision:** `Processor`, `RAM`, `Storage`, and `GPU` are _instantiated_ _inside_ `Computer.__init__`. They don't exist independently - when the `Computer` object is destroyed, its components go with it. This is strict composition (as opposed to **aggregation**, where components could exist on their own and be passed in from outside).

**Composition vs. Inheritance - when to use which:**

| Scenario | Use |
| --- | --- |
| "`Manager` is a special kind of `Employee`" - true specialization | Inheritance |
| "`Computer` has a `Processor`" - one thing contains another | Composition |
| You want to reuse behaviour without implying a type relationship | Composition |
| The "is-a" test fails even slightly | Composition |

A common mistake in early OOP code is reaching for inheritance because it seems to enable reuse. Composition is usually safer - it creates fewer hidden dependencies between classes and makes the code easier to modify later.