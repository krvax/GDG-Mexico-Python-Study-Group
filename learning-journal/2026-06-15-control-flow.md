# Learning Journal — 2026-06-15
## Control Flow and Functions

**Instructor:** Geovanni Zepeda
**Group:** GDG Mexico Python Study Group
**Repo:** https://github.com/krvax/GDG-Mexico-Python-Study-Group

---

## Topics Covered

### 1. Selection Structures (`if / elif / else`)
Execute different blocks depending on a boolean condition.

Examples practiced:
- Grade classification
- Data validation
- Dictionary key verification

### 2. Iteration with `for`
Traverse sequences: lists, strings, dictionaries.

```python
for element in collection:
    # process
```

Applications: list traversal, string processing, dictionary iteration, accumulations.

### 3. Iteration with `while`
Execute while a condition holds.

```python
while condition:
    # code
```

Patterns observed:
- Retry loops
- Interactive menus
- Continuous validation

Exit mechanisms: `break` or flag modification (`active = False`).

### 4. CRUD as Integrative Exercise
Built a contact agenda using lists, dicts, `if`, `for`, `while`.

Operations: Create, Read, Update, Delete.

### 5. Introduction to Functions
Independent, reusable block of code.

```python
def name(param1, param2):
    instructions
    return result
```

Concepts: parameters, body, return, reusability.

### 6. Built-in Functions
`print()`, `input()`, `len()`, `range()`, `list()`, `dict()`, `int()`, `str()`, `sum()`

Core idea: Python already incorporates a large number of reusable abstractions.

---

## Mathematical Connection

Functions understood as:

```
Input → Rule → Output
```

Example discussed:

```
f(x,y) = (2x - y) / ((x-2)² + (y-1)²)
```

Domain: ℝ² - {(2,1)} — undefined when denominator is zero.

---

## Personal Insight

Functions can be understood from three perspectives:

| Perspective | Model |
|-------------|-------|
| Mathematics | Input → Rule → Output |
| Programming | Parameters → Process → Result |
| Software Engineering | Reusable abstraction |

### Connection with Software Archaeology

Built-in functions represent accumulated knowledge. When we use `len()`, `dict()`, `print()` — we are consuming solutions that encapsulate decades of design and implementation.

The same pattern appears everywhere:
- APIs
- Terraform
- `kubectl`
- `make briefing`
- SRE Central

The user consumes a stable interface without knowing all the internal complexity.

---

## Session Reflection

Low attendance today. Still produced several important connections:

- Functions ↔ Mathematics
- Functions ↔ APIs
- Functions ↔ Software Archaeology
- Functions ↔ Personal automation

**Most important observation of the day:**

> Learning fundamentals after years of experience is not going back to the beginning.
> It is better understanding why the upper layers we use every day actually work.
