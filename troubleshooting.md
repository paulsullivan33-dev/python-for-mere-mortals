# Troubleshooting

Python errors look scary but they're helpful — the last line tells you
what went wrong, and the lines above tell you where. Read error
messages **bottom-up**: the final line first, then the file and line
number above it.

## The errors you'll meet first

**IndentationError / unexpected indent.** Blocks must line up exactly —
four spaces per level, no tabs mixed in. Most editors can show invisible
characters; turn that on while learning.

```python
if True:
print("oops")   # IndentationError — needs indent
```

**NameError: name 'x' is not defined.** You used a variable that
doesn't exist — usually a typo (`nmae` vs `name`) or using it before
assignment. Check the spelling at the line number given.

**TypeError: can only concatenate str.** Mixing types: `"age: " + 36`
fails. Convert first: `"age: " + str(36)`.

**IndexError: list index out of range.** `fruits[5]` on a 3-item list.
Remember counting starts at 0, and check `len()` before indexing by a
computed position.

**FileNotFoundError.** The file isn't where Python looked. Check your
working directory (see [Files and Data](files-and-data.md)) and the
exact filename — including extension and capitalization.

**SyntaxError: invalid syntax.** Python can't parse the line — often a
missing parenthesis, quote, or colon on the line *above* the one
reported. Check upward.

## Debugging habits

- **Print the value.** `print("x is:", x)` right before the failing
  line. Half of all bugs surrender to this.
- **Read the traceback bottom-up.** Last line: what. Lines above:
  where, innermost call last.
- **Change one thing, re-run.** Same as 3D printing: shotgun edits
  teach nothing.
- **Rubber-duck it.** Explain the code line by line, out loud, to
  anything that listens. The bug usually announces itself mid-sentence.

## When to ask for help

Copy three things: the full error message (all of it), the smallest
code that reproduces it, and what you expected instead. "NameError on
line 12, here's 10 lines, I expected the total to print" gets answers;
"it doesn't work" doesn't.

Related: [Your First Program](first-program.md),
[Glossary](glossary.md).
