# Developer Study Notes

A reference library for learning Python, debugging, APIs, automation, AI agents, MCP, and the habits of reliable software engineers.

**Learning status:** beginner. These are study notes, not proof of professional production engineering.

## Index

1. [Excel formulas versus Python assignments](#excel-formulas-versus-python-assignments)
2. [Variable names and case sensitivity](#variable-names-and-case-sensitivity)
3. [A reliable debugging habit](#a-reliable-debugging-habit)
4. [Learning roadmap](#learning-roadmap)

## Excel formulas versus Python assignments

**Excel:** With automatic calculation enabled, a cell containing `=A1+B1` typically recalculates when A1 or B1 changes.

**Python:** A normal assignment such as `total = rent + deposit` calculates and stores a value *at that point in execution*. Updating `rent` later does not automatically recalculate `total`.

```python
rent = 1000
deposit = 500
total = rent + deposit  # 1500
rent = 1200
print(total)             # 1500, not 1700
total = rent + deposit
print(total)             # 1700
```

Python can be programmed to recompute values automatically through additional mechanisms, but ordinary variable assignments are not reactive spreadsheet formulas.

**Mental model:** Excel formulas are often live dependencies; basic Python assignments are steps executed in order.

## Variable names and case sensitivity

- `rent` and `Rent` are different names.
- `print()` is the standard built-in display function; `Print()` is not.
- Spaces are not allowed inside a variable name: use `new_price`, not `new price`.
- Choose descriptive names: `updated_price` is clearer than `update` when the value represents a price.

```python
initial_price = 100
price_increase = 25
updated_price = initial_price + price_increase
visits = 4
total = updated_price * visits
print(total)  # 500
```

## A reliable debugging habit

1. Read the code top to bottom.
2. Track the current value of each variable.
3. Identify the exact line that assigns or changes a value.
4. Predict the output before running the code.
5. If the result differs, isolate the smallest example and test your assumption.

**Feedback log:** Early practice showed correct arithmetic reasoning, with occasional capitalization errors, a missing assignment operator, and a variable name containing a space. These are syntax issues to check deliberately.

## Learning roadmap

- **Foundations:** printing, variables, arithmetic, strings, conditions, loops, functions.
- **Practical development:** files, modules, exceptions, testing, Git and GitHub.
- **Business automation:** invoices, service schedules, and synthetic account records.
- **APIs:** HTTP, GET/POST, JSON, authentication, error handling.
- **AI applications:** model APIs, evaluation, structured outputs, agents, and tool calling.
- **MCP:** client/server concepts, tools, resources, prompts, permissions, and security.
- **Engineering habits:** readable code, version control, tests, documentation, security, and honest evidence of what was built.

## Evidence policy

Keep exercises, AI-assisted samples, and independently built projects clearly labeled. Never publish secrets, customer data, or employer-confidential materials.
