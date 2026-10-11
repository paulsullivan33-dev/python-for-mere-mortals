# Variables and Types

A **variable** is a named box holding a value. A **type** is what kind
of value it holds — text, a number, a list. Python figures out the type
from what you put in; you don't declare it.

## The types you'll use daily

```python
name = "Ada"          # str — text (string). Quotes required.
age = 36              # int — whole number.
height = 1.65         # float — number with a decimal point.
is_member = True      # bool — True or False. Capital T/F matters.
nothing = None        # None — deliberately empty. Not zero, not "".
```

**Check** your understanding: `age = "36"` with quotes is *text*, not a
number — `"36" + 1` is an error, while `36 + 1` is 37. Quotes decide.

## Lists: ordered collections

```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])      # apple — counting starts at 0, not 1
fruits.append("date") # add to the end
print(len(fruits))    # 4 — how many items
```

Lists can mix types, but keeping one kind per list saves confusion.

## Dictionaries: labeled boxes

```python
person = {"name": "Ada", "age": 36}
print(person["name"])       # Ada
person["city"] = "London"   # add a label
```

Use a dict when each value has a name. Use a list when order matters
and items are alike.

## Converting between types

```python
text = "42"
number = int(text)      # "42" -> 42
price = float("19.99")  # "19.99" -> 19.99
label = str(42)         # 42 -> "42"
```

Conversions fail loudly on bad input: `int("hello")` is an error, which
is good — better than silently guessing. Remember `input()` always
gives you text; convert it before doing math.

## Two habits that prevent bugs

- **Name things clearly.** `total_price` beats `x`. Future you is the
  main reader.
- **Don't reuse a variable for two jobs.** A variable holding a name
  shouldn't later hold a count. New job, new name.

Next: [Control Flow](control-flow.md).

## Sources

- [Python tutorial: data structures](https://docs.python.org/3/tutorial/datastructures.html)
