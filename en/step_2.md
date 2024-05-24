## Build a demo package

First, you will create a demo Python package called `motivate`, so that you can use it to practice packaging. 

--- task ---

Create a directory called `my_project` for your project.

--- /task ---

--- task ---

Create a directory **inside** the `my_project` directory called `motivate` - this is the name of the package.

--- /task ---

--- task ---

Using a Python IDE, create a new Python file, and save it as `me.py` in the `motivate` directory.

--- /task ---

--- task ---

In `me.py`, write code for a function called `motivate_me` which prints a motivational message.


--- code ---
---
language: python
filename: me.py
line_numbers: true
---
def motivate_me():
  print("You are awesome")

--- /code ---

--- /task ---

To turn your Python code into a package, you need to create a special file called `__init__.py`, which will **initialise** your package and tell Python about the package contents.

--- task ---

In the `motivate` directory, create a new file and save it as `__init__.py`.

There are **two** underscores `_` `_` before and after `init`. It's important to get this right, otherwise your program won't work.

--- /task ---

--- task ---

Open the file `__init__.py` in your Python IDE. Import the `motivate_me` function from the `me.py` module like this.

--- code ---
---
language: python
filename: __init__.py
line_numbers: true
---
from .me import motivate_me

--- /code ---

--- /task ---

Your project should now have the following directory structure:

+ **project** - `my_project`
  + **package** - `motivate`
    + **module** - `me.py`
    + **initialisation file** - `__init__.py`

It's really important that you get the structure correct, otherwise the next steps won't work.
