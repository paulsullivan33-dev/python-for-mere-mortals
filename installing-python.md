# Installing Python

Get Python running on your computer, with checks that it worked.
Pick your system below.

## Windows

Download the installer from [python.org/downloads](https://www.python.org/downloads/).
**Important:** on the first installer screen, check the box that says
**"Add python.exe to PATH"** before clicking Install. Without it, the
`python` command won't work in PowerShell.

Open a **new** PowerShell window and run:

```powershell
python --version
```

**Check:** you should see something like `Python 3.13.2`. If Windows
says the command isn't recognized, you skipped the PATH checkbox —
re-run the installer, choose Modify, and add it.

## Mac

Macs don't ship a usable Python 3 by default. The cleanest path is the
installer from [python.org/downloads](https://www.python.org/downloads/)
(macOS 64-bit universal2). Then in Terminal:

```bash
python3 --version
```

**Check:** a version number prints. (Note: it's `python3` on Mac, not
`python`.)

## Linux

Most Linux distributions include Python 3. Check first:

```bash
python3 --version
```

If it's missing, install it with your package manager — for example on
Debian/Ubuntu:

```bash
sudo apt update && sudo apt install python3
```

**Check:** `python3 --version` prints a version number.

## Confirm it can run code

On any system, run:

```bash
python --version   # Windows
python3 --version  # Mac/Linux
```

then:

```bash
python -c "print('it works')"    # Windows
python3 -c "print('it works')"   # Mac/Linux
```

**Check:** it prints `it works`. You're ready.

## A note on versions

Any Python 3.10 or newer is fine for these guides. Don't chase the
absolute latest release on day one — libraries you might use later
sometimes lag behind brand-new versions by a few weeks.

Next: [Your First Program](first-program.md).
