## Creating a setup

At the moment you module can only be accessed if the program which is calling it is saved to the **project** directory, to make your module accessible to all Python programs it need to be installed.

To install a Python module you have to create a **setup** program which packages the module into a **distribution** you can install.

The **setup** program is just a python program which calls a function called `setup` passing all the information it needs to install your module.

--- task ---

Create a new Python 3 program and save it as `setup.py` in your **project** directory.

--- /task ---

First you will just create a really simple setup program which does the minimum to create a install, you will expand on it later to include additional information.

--- task ---

Import the `setup` function from the `setuptools` module:

```python
from setuptools import setup
```

--- /task ---

--- task ---

Create 4 variables to hold the essential information about your distribution:
+ `__project__` - the name of your project
+ `__version__` - the version number, typically in the format `0.0.0`
+ `__description__` - a description
+ `__packages__` - a list of packages this distribution should install

```python
__project__ = "motivate"
__version__ = "0.0.1"
__description__ = "a python module to motivate you"
__packages__ = ["motivate"]
```

--- /task ---

**Note:** these variables are called "module level dunders" and start and end with double underscores (dunder being short for double underscore) and are a way to provide information about your distribution.

--- task ---

Call the `setup` function passing the variables you just created.

```python
setup()
```

--- /task ---

### Test your setup program

To test and install your module, you need to run your `setup.py` program. 

You will need to run it from the **Command Prompt** or **Terminal** as you need to pass the additional `install` parameter and in Linux run it with super user privileges.

--- task ---

Run your `setup.py` program.

--- collapse ---

---
title: Windows
---

Open a **Command Prompt**, change directory (`cd`) to your **project** directory and run:

```bash
python setup.py install
```

--- /collapse ---

--- collapse ---

---
title: Raspberry Pi, Linux
---

Open a **Terminal**, change directory (`cd`) to your **project** directory and run:

```bash
sudo python3 setup.py install
```

--- /collapse ---

--- collapse ---

---
title: MacOS
---

Open a **Terminal**, change directory (`cd`) to your **project** directory and run:

```bash
python3 setup.py install
```

--- /collapse ---

--- /task ---


