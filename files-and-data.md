# Files and Data

Most useful scripts read something, change it, and write something.
Files are the everyday version of that.

## Reading a text file

```python
with open("notes.txt") as f:
    text = f.read()
print(text)
```

The `with` block opens the file and closes it for you when done —
always use it. `f.read()` gives you the whole file as one string.

For line-by-line work:

```python
with open("notes.txt") as f:
    for line in f:
        print(line.strip())   # strip() removes the trailing newline
```

## Writing a file

```python
with open("output.txt", "w") as f:
    f.write("Hello, file!\n")
```

`"w"` means write — it **replaces** the file if it exists. `"a"`
appends instead. Double-check which one you mean before running; `"w"`
on the wrong filename deletes data.

## Working with structured text

**CSV** (comma-separated values — spreadsheets as text):

```python
import csv

with open("people.csv", newline="") as f:
    for row in csv.DictReader(f):
        print(row["name"], row["age"])
```

**JSON** (the format web APIs and configs use):

```python
import json

with open("config.json") as f:
    settings = json.load(f)
print(settings["theme"])

settings["theme"] = "dark"
with open("config.json", "w") as f:
    json.dump(settings, f, indent=2)
```

`import` loads one of Python's built-in toolboxes. `csv` and `json`
ship with Python — no installation needed.

## Paths: where files live

Scripts look for files relative to where you *run* them, not where the
script lives. Running `python scripts/tool.py` from the project root
means `"data.txt"` refers to the root's `data.txt`. When a file isn't
found, check your working directory first — it's the usual culprit.

## A practical pattern

```python
import json

with open("scores.json") as f:
    scores = json.load(f)

average = sum(scores) / len(scores)
print("Average:", round(average, 1))
```

Read data, compute, report. An enormous number of real scripts are some
version of this.

Next: [Troubleshooting](troubleshooting.md).

## Sources

- [Python tutorial: input and output](https://docs.python.org/3/tutorial/inputoutput.html)
- [csv module](https://docs.python.org/3/library/csv.html),
  [json module](https://docs.python.org/3/library/json.html)
