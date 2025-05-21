# Python Identifiers and Naming Conventions (With Examples)

_A quick reference from “Python 3: Deep Dive – Part 1”_

---

## ✅ Identifier Rules

### 1. Case Sensitivity

Python treats identifiers with different casing as **distinct**.

```python
myvar = 10
MyVar = 20
print(myvar)   # 10
print(MyVar)   # 20
```

---

### 2. Valid Identifier Names

- Must start with a **letter (A–Z or a–z)** or **underscore `_`**
- Can include letters, digits, and underscores
- **Cannot start with a digit**
- **Cannot use reserved keywords**

✅ Valid:
```python
name = "Alice"
_name = "internal"
name2 = "user2"
_index_1 = 5
```

❌ Invalid:
```python
2name = "Bob"       # SyntaxError
def = 10            # SyntaxError (keyword)
```

---

## 🔐 Special Identifier Conventions

### `_single_leading_underscore`
Indicates internal or “private” use by convention.

```python
_internal_data = "do not import"
```

Excluded when using:
```python
from module import *  # _internal_data won't be imported
```

---

### `__double_leading_underscore`
Used in class properties for name mangling (avoid name conflicts in inheritance).

```python
class MyClass:
    def __init__(self):
        self.__token = "secret"

obj = MyClass()
print(obj._MyClass__token)  # Accesses mangled name
```

---

### `__double_leading_and_trailing__`
**Reserved by Python** for special functions (dunder methods).

```python
def __init__(self):   # Object constructor
def __lt__(self, other):   # Less-than operator override
```

❗ Don’t create your own names in this pattern.

---

## 🧠 PEP 8 Naming Conventions

| Element     | Style                   | Example                    |
|-------------|--------------------------|-----------------------------|
| Package     | lowercase                | `utilities`, `parser`       |
| Module      | lowercase with `_`       | `db_utils.py`, `email_api`  |
| Class       | UpperCamelCase           | `BankAccount`, `UserRepo`   |
| Function    | snake_case               | `open_account()`, `send_email()` |
| Variable    | snake_case               | `account_id`, `total_cost`  |
| Constant    | UPPER_CASE_WITH_UNDERSCORE | `MAX_RETRIES`, `TIMEOUT`  |

---

## 🔗 Additional Tip

> Consistency matters. Following naming conventions improves readability and helps other developers understand your code at a glance.

---

## 🔍 Reference

- [PEP 8 – Python Style Guide](https://peps.python.org/pep-0008/)
