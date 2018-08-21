## Create a setup program

At the moment, your module can only be accessed if the program that is calling it is saved in the `my_project` directory. For your module to be accessible to all Python programs, it needs to be installed.

So that you can install the Python module, you have to create a **setup** program. This is just a Python program that calls the `setup` function, passing it all the information necessary to install your module. Later you will also use it to create a **distribution** you can share with the world.

--- task ---

Create a new Python 3 program, and save it as `setup.py` in the `my_project` directory.

--- /task ---

For now, you'll write a very simple setup program that does the minimum to install your module. You will expand on it later to include additional information.

--- task ---

Import the `setup` function from the `setuptools` module:

```python
from setuptools import setup
```

--- /task ---

--- task ---

Create four variables to hold the essential information about your distribution:
+ `__project__`: the name of your project
+ `__version__`: the version number, typically in the format `0.0.0`
+ `__description__`: a description
+ `__packages__`: a list of packages this distribution should install

```python
__project__ = "motivate"
__version__ = "0.0.1"
__description__ = "a Python module to motivate you"
__packages__ = ["motivate"]
```

--- /task ---

**Note:** these variables are called **module level dunders** and start and end with double underscores ('dunder' being short for 'double underscore').

--- task ---

Call the `setup` function, passing the variables you just created to it.

```python
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
)
```

--- /task ---

In the next step, you will run your `setup.py` program to install and test the `motivate` module.
