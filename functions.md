# Functions

A **function** is a named, reusable chunk of work. You define it once,
then call it by name whenever needed. If you copy-paste the same block
three times, it wants to be a function.

## Defining and calling

```python
def greet(name):
    return "Hello, " + name

message = greet("Ada")
print(message)   # Hello, Ada
```

- `def` starts the definition; the indented block is the function body.
- `name` is a **parameter** — a placeholder the caller fills in.
- `return` hands a value back. Without `return`, the function gives
  back `None`.

## Why bother

1. **No repetition.** Fix a bug once, not in five copied blocks.
2. **Names explain.** `calculate_total(items)` says more than ten
   lines of arithmetic.
3. **Testing.** A function with inputs and an output can be checked in
   isolation.

## Parameters with defaults

```python
def greet(name, greeting="Hello"):
    return greeting + ", " + name

greet("Ada")            # Hello, Ada
greet("Ada", "Hi")      # Hi, Ada
```

Defaults make the common case short while keeping flexibility.

## Scope: where variables live

```python
total = 0

def add(amount):
    result = total + amount   # reads the outer variable fine
    return result

def broken(amount):
    total = total + amount   # ERROR — see below
```

Variables created *inside* a function stay inside it. Reading an outer
variable is fine, but *assigning* to a name makes it local — so
`broken()` fails because its local `total` doesn't exist yet on the
right-hand side. When in doubt, pass values in as parameters and return
results out. (The `global` keyword exists; beginners should treat it
as a warning sign, not a tool.)

## Keep them small

A function should do one thing. If you can't describe it in a sentence
without "and," split it. Ten small functions beat one giant one.

Next: [Files and Data](files-and-data.md).

## Sources

- [Python tutorial: functions](https://docs.python.org/3/tutorial/controlflow.html#defining-functions)
