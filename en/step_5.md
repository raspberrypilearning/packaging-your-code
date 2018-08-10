## Adding additional information

Currently your setup program is only using the minimum amount of information to get the install to run. 

You should add additional information about your project into `setup.py` so that potential users can answer important questions such as "who created it", "where to get help", "what sort of project it is" and add keywords so that it is easier to find.

This is done by passing additional parameters to the `setup` function when it is called.

First you will add information about who created this module (you) and how to get in touch with them.

--- task ---

Create new variable for the `author` parameter, this is information about who created this module and should contain your own name.

```python
__author__ = "Mickey Mouse"

```

--- /task ---

--- task ---

Pass the **author** variable to the `setup` function.

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

Add **author_email** information to the **setup**.

--- hints ---

--- hint ---

The parameter you need to add to the `setup` function is called `author_email`.

--- /hint ---

--- hint ---

Create a variable called `__author_email__`, set it to your email address and pass this to the `setup` function as the `author_email` parameter.

--- /hint ---

--- hint ---

Add this code to create the `__author_email__` variable and set it to your email address

```python
__author_email__ = "mickey@disney.com"
```

Modify the `setup` function call to pass it as the `author_email` parameter.

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

If your project has a website or perhaps github repository you can provide a `url`. If you are interested in knowing more about creating a project website or how to provide documentation for your code, have a look at the [Documenting your code](https://projects.raspberrypi.org/en/projects/documenting-your-code) project

Next, you should add some **classifiers** to your **setup** this allows your project to be categorised with other similar projects and also provide useful information about your projects compatibility, such as what versions of Python it works with.

--- task ---

Create a list of classifiers and set it to show your project is for use with _Python 3_, its status is _Alpha_ and that intended audience is _Education_.

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

Review the [list of classifiers](https://pypi.org/pypi?%3Aaction=list_classifiers) and add any others which you think are appropriate to your project.

--- /task ---

The **keywords** parameter allows you to provide words which someone may search for when looking for a project.

--- task ---

Create a list of **keywords** which are appropriate to this project such as "motivation" or "learning" and add it to the **setup**.

--- hints ---

--- hint ---

The syntax to create a list of words is `my_list = ["hi", "bye]`.

--- /hint ---

--- hint ---

You should create a list called `__keywords__` and pass it to the `keyword` parameter of the `setup` function. 

--- /hint ---

--- hint ---

You would create a __keywords__ list using:

```python
__keywords__ = ["motivation", "learning"]
```

Before passing it to the `keyword` parameter of `setup`:

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

Test your **setup** by running `setup.py` program from the Command Prompt or Terminal.

--- /task ---

If your project required other python packages to be installed to work you can specify them by passing a list to the `requires` parameter of `setup` e.g.

```python
__requires__ = ["guizero"]
setup(
    ...
    requires = __requires__,
)
```

To learn more about distributing your Python projects have a look at the [Python Packaging User Guide](https://packaging.python.org/tutorials/packaging-projects/).