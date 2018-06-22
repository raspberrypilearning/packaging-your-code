## Creating a setup

At the moment your module can only be accessed if the program which is calling it is saved to the **project** directory, to make your module accessible to all Python programs it needs to be installed.

To install a Python module you have to create a **setup** program which packages the module into a **distribution** you can install.

The **setup** program is just a python program which calls a function called `setup` passing all the information it needs to install your module.

--- task ---

Create a new Python 3 program and save it as `setup.py` in your **project** directory.

--- /task ---

First you will just create a really simple setup program which does the minimum to install your project and you will expand on it later to include additional information.

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
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
)
```

--- /task ---

In the next step you will run your `setup.py` program to install and test the `motivate` module.