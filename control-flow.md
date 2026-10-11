# Control Flow

Programs get interesting when they make decisions and repeat things.
Three tools do almost all of it: `if`, `for`, and `while`.

## if: making decisions

```python
age = 20

if age >= 18:
    print("adult")
else:
    print("minor")
```

**Indentation is the syntax.** The indented lines belong to the `if`.
Python doesn't use braces — four spaces (not tabs) mark the block.
Inconsistent indentation is the most common beginner error; see
[Troubleshooting](troubleshooting.md).

Chain decisions with `elif` (else-if):

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "F"
```

## for: repeating over things

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print("I like", fruit)
```

The loop runs once per item, with `fruit` holding each in turn.
`range()` counts when you need numbers:

```python
for i in range(5):
    print(i)   # 0, 1, 2, 3, 4 — starts at 0, stops before 5
```

## while: repeating until something changes

```python
count = 3
while count > 0:
    print(count)
    count = count - 1
print("go!")
```

`while` keeps going as long as its condition is true. **Warning:** if
the condition never becomes false, the loop never ends — press
Ctrl+C in the terminal to stop a runaway loop.

## A practical pattern

```python
for filename in ["a.txt", "b.txt", "missing.txt"]:
    try:
        text = open(filename).read()
        print(filename, "has", len(text), "characters")
    except FileNotFoundError:
        print(filename, "not found, skipping")
```

`try/except` says "attempt this; if this specific thing goes wrong,
do that instead of crashing." Use it for expected problems (missing
files, bad network) — not to hide bugs you should fix.

Next: [Functions](functions.md).

## Sources

- [Python tutorial: control flow](https://docs.python.org/3/tutorial/controlflow.html)
