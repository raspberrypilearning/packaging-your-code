## Build your python package

In this first step you will be creating a python package called `motivate` and structuring the code into a set of directories.

--- task ---

Open a **Command Prompt** (Windows) or **Terminal** (Raspberry Pi, Linux, MacOS).

--- /task ---

--- task ---

Create a directory for your **project**, this will hold all the directories and files which make up your project.

```bash
mkdir my_project
```

--- /task ---

--- task ---

Change directory to your new project directory you just created.

```bash
cd my_project
```

--- /task ---

--- task ---

Create a directory for your python **package**, this directory will hold the code for your Python module.

The name of this directory will also be the name of your python package, in our example this is `motivate`.

```bash
mkdir motivate
```

--- /task ---

--- task ---

Open a Python 3 editor (such as IDLE), create a new file and save it was `me.py` in the Python module directory, `motivate`, you just created.

This python program will hold the python code which will print motivating messages.

--- /task ---

--- task ---

Create a function called `motivate_me` and have it print a message.

```python

def motivate_me():
    print("you are doing great, keep it up")

```

--- /task ---

In order to turn your Python code into a package and provide users access to your new function `motivate_me` you need to create a special file called `__init.py__` which will **initialise** your package and tell Python about its contents.

--- task ---

Create a new file and save it as `__init__.py`.

**Note**: there are 2 underscores `_` `_` before and having the `init`, its important to get this right otherwise your program wont work.

--- /task ---

--- task ---

Add the following code to `__init__.py` to import the `motivate_me` function from the `me.py` module.

```python
from .me import motivate_me
```

--- /task ---

Your project should now have the following structure:

+ **project** - `my_project`
  + **package** - `motivate`
    + **module** - `me.py`
    + **initialisation file** - `__init__.py`

Its really important you get the structure correct or you may find that other steps don't work.

You can test that your project is setup correctly using the `tree` command to print the directory and file structure.

--- collapse ---

---
title: Windows
---

Run the command:

```bash
tree /F
```

![tree windows](images/tree_windows.PNG)

--- /collapse ---

--- collapse ---

---
title: Raspberry Pi, Linux, MacOS
---

Run the command :

```bash
tree
```

![tree pi](images/tree_pi.PNG)

--- /collapse ---

### Test your code

You should test your module before packaging and installing it.

--- task ---

Create a new Python 3 file and save it into the **project** directory as `test.py`

--- /task ---

--- task ---

Add the following code to import the `motivate_me` function from the `motivate` module.

```python
from motivate import motivate_me
```

--- /task ---

--- task ---

Add the code to call the `motivate_me` function.

```python
motivate_me()
```

--- /task ---

--- task ---

Run the `test.py` program.

--- /task ---

You should see your motivating message appear.

![motivate me](images/motivate_me.gif)
