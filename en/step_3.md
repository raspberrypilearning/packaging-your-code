## Package your module

At the moment, your module can only be accessed if the program that is calling it is saved in the `my_project` directory. For your module to be accessible to all Python programs, it needs to be installed.

So that you can install the Python module, you have to package it. Later you will also use this program to create a **distribution** you can share with the world.

--- task ---

Create a file called `pyproject.toml`, and save it in the `my_project` directory.

--- /task ---

This file will contain all of the information about your package that Python needs to be able to build it. 


--- task ---

Copy and paste the following template into your `pyproject.toml` file:

```markdown
[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"

[project]
name = "motivate"
version = "0.0.1"
authors = [
  { name="Example Name", email="example@example.com" },
]

```

--- /task ---

--- task ---

In the `[project]` section, change the author's name and email address to your name and email address.

The `name` of the project must be the same as the folder name which contains the module. In this example, we called it `motivate`, but if you called the folder something different, change the name here too. 
--- /task ---


In the next step, you will run the build process to build the `motivate` module.
