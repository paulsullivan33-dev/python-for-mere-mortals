# Your First Program

Write a real script, run it, and change it. Use any text editor —
Notepad works, though an editor that numbers lines (VS Code, Notepad++)
makes life easier later.

(Commands below use `python` on Windows, `python3` on Mac/Linux.)

## 1. The one-liner

Open a terminal and run Python with a command directly:

```bash
python -c "print('Hello, world!')"
```

**Check:** it prints `Hello, world!`. The `-c` flag means "run this
code right now." `print()` displays whatever you give it.

## 2. A script file

One-liners get old fast. Create a file called `hello.py` containing:

```python
print("Hello, world!")
```

Run it:

```bash
python hello.py
```

**Check:** same greeting. A script is just commands saved in a file —
Python runs them top to bottom.

## 3. Make it yours

Change the file to:

```python
name = "Ada"
print("Hello,", name)
```

Run it again.

**Check:** it prints `Hello, Ada`. You just used a **variable** — a
named box holding a value. See [Variables and Types](variables-and-types.md).

## 4. Take input

```python
name = input("Your name? ")
print("Hello,", name)
```

**Check:** the program waits, you type your name, it greets you.
`input()` pauses for the keyboard and hands you what was typed — always
as text, even if the user types digits.

## What to try next

- [Variables and Types](variables-and-types.md): strings, numbers,
  lists.
- [Control Flow](control-flow.md): decisions and repetition.
- [Functions](functions.md): reusable chunks.

## Sources

- [Python tutorial: first steps](https://docs.python.org/3/tutorial/introduction.html)
