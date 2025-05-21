# Python Conditionals Summary (Python 3: Deep Dive - Part 1)

This is a quick summary of the **Conditionals** lecture from the *Python 3: Deep Dive (Part 1 - Functional)* Udemy course by Dr. Fred Baptiste.

---

## 🧠 Basic `if` Statement

```python
a = 2
if a < 5:
    print("a is less than 5")
```

- Executes block **only if** the condition is true.
- If `a = 6`, nothing happens.

---

## 🔁 `if-else` Statement

```python
a = 6
if a < 5:
    print("a is less than 5")
else:
    print("a is greater than or equal to 5")
```

---

## 🔀 Nested `if` Statements

```python
a = 10

if a < 5:
    print("a is less than 5")
else:
    if a < 10:
        print("a is between 5 and 10")
    else:
        print("a is greater than or equal to 10")
```

You can nest inside `if` or `else`. But nesting too deeply can reduce readability.

---

## 🔀 Replacing Nested `if` with `elif`

```python
a = 12

if a < 5:
    print("a is less than 5")
elif a < 10:
    print("a is between 5 and 10")
elif a < 15:
    print("a is between 10 and 15")
elif a < 20:
    print("a is between 15 and 20")
else:
    print("a is greater than or equal to 20")
```

- `elif` = “else if”
- Cleaner than nested `if` blocks

---

## ❓ Ternary (Conditional) Expression

```python
b = "a is less than 5" if a < 5 else "a is greater than or equal to 5"
print(b)
```

- Useful for **one-line conditional value assignment**
- Cannot contain code blocks, only **expressions**

Also works interactively:

```python
a = 4
"a is less than 5" if a < 5 else "a is greater than or equal to 5"
```

---

## 🔍 When to Use

| Use Case                  | Statement Type   |
|---------------------------|------------------|
| Multiple branches         | `if`, `elif`, `else` |
| Simple yes/no             | `if`, `else`     |
| One-line assignment       | Ternary operator |
| Complex conditions        | Nested or chained `if` |

---

## 📘 Key Takeaways

- Use `if/elif/else` for branching logic.
- Prefer `elif` over deeply nested `if`s.
- Use ternary expressions for quick, inline decisions.
- Python has no `switch`/`case`, so use `elif` chains instead.

---
