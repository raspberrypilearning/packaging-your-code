## Add extra information

Currently, your `setup.py` program only contains the minimum amount of information needed to get the installation to run. 

You should add additional information about your project into `setup.py`, so that potential users can answer important questions about your project such as who created it, where to get help with it, and what sort of project it is. It's also a good idea to add keywords so that your project is easier to find.

You can do this by passing additional parameters to the `setup` function when you call it.

First, you will add information about who created this module (you!) and how to get in touch with them.

--- task ---

Create a new variable for the `author` parameter. This is information about who wrote the module, so it should contain your own name.

```python
__author__ = "Mickey Mouse"

```

--- /task ---

--- task ---

Pass the `author` variable to the `setup` function.

```python
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
    author = __author__,
)
```

--- /task ---

--- task ---

Add `author_email` information to the `setup.py` program.

--- hints ---

--- hint ---

The function parameter you need to add is called `author_email`.

--- /hint ---

--- hint ---

Create a variable called `__author_email__`, set it to your email address, and pass this to the `setup` function as the `author_email` parameter.

--- /hint ---

--- hint ---

Add this code to create the `__author_email__` variable and set it to your email address:

```python
__author_email__ = "mickey@disney.com"
```

Modify the `setup` function call to also pass it the `author_email` parameter.

```python
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
    author = __author__,
    author_email = __author_email__,
)
```

--- /hint ---

--- /hints ---

--- /task ---

If your project has a website or a GitHub repository, you can provide a `url`. If you're interested in learning to create a project website and documentation for your code, have a look at our [Documenting your code](https://projects.raspberrypi.org/en/projects/documenting-your-code) project.

Next, you should add some **classifiers** to your setup file. These will allow your project to be categorised with other similar projects, and they also provide useful information about your project's compatibility, such as what versions of Python it works with.

--- task ---

Create a list of classifiers and to show your project is for use with Python 3, its status is 'Alpha', and its intended audience 'Education'.

```python
__classifiers__ = [
    "Development Status :: 3 - Alpha",
    "Intended Audience :: Education",
    "Programming Language :: Python :: 3",
]
```

--- /task ---

--- task ---

Pass the classifiers to the **setup** function.

```python
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
    author = __author__,
    author_email = __author_email__,
    classifiers = __classifiers__,
)
```

--- /task ---

--- task ---

Review the [list of classifiers](https://pypi.org/pypi?%3Aaction=list_classifiers), and add any others you think are appropriate to your project.

--- /task ---

The `keywords` parameter allows you to provide words which someone may use to search for a project like yours.

--- task ---

Create a list of keywords that are appropriate to this project, such as "motivation" or "learning", and add it to the `setup` function.

--- hints ---

--- hint ---

The syntax to create a list of words is `my_list = ["hi", "bye]`.

--- /hint ---

--- hint ---

You should create a list called `__keywords__` and pass it to the `keyword` parameter of the `setup` function. 

--- /hint ---

--- hint ---

You create a `__keywords__` list like this:

```python
__keywords__ = ["motivation", "learning"]
```

Then pass it to the `keyword` parameter of `setup`:

```python
setup(
    name = __project__,
    version = __version__,
    description = __description__,
    packages = __packages__,
    author = __author__,
    author_email = __author_email__,
    classifiers = __classifiers__,
    keywords = __keywords__,
)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Test your setup program by running `setup.py` from the command line.

--- /task ---

If your project requires other Python packages to be installed to work, you can specify these by passing a list to the `requires` parameter of `setup`, for example:

```python
__requires__ = ["guizero"]

setup(
    ...
    requires = __requires__,
)
```

To learn more about distributing your Python projects, have a look at the [Python packaging user guide](https://packaging.python.org/tutorials/packaging-projects/).
