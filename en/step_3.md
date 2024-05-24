## Package your code

Now that you have written some code, you will package it so that other people can install and use it. 

--- task ---

Create a file called `pyproject.toml`, and save it in the `my_project` directory.

--- /task ---

This file will contain all of the information about your package that Python needs to be able to build it. 


--- task ---

Copy and paste the template into your `pyproject.toml` file:

--- code ---
---
language: markdown
filename: pyproject.toml
line_numbers: true
line_number_start: 1
---

[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"

[project]
name = "motivate"
version = "0.0.1"
authors = [
  { name="Example Name", email="example@example.com" },
]

--- /code ---

--- /task ---

--- task ---

In the `[project]` section, change the author's name and email address to your name and email address.

The `name` of the project must be the same as the folder name which contains the module. In this example, we called it `motivate`, but if you called the folder something different, change the name here too. 
--- /task ---


