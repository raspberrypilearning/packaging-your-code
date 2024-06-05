## Package your code

Now you will package your code so that other people can install and use it. 

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

In the `[project]` section, you can set the author's name and email address. **This information will be public** - ask an adult before sharing personal information. If you don't intend to publish your package, you can leave the example values as they are.

The `name` of the project must be the same as the folder name which contains the code. In this example, we called it `motivate`, but if you called the folder something different, change the name here too. 
--- /task ---

--- task --- 
In a command prompt, make sure you are in the same directory as the `pyproject.toml` file, then type these commands to install the build tool and build the package:

--- code ---
---
language: bash
line_numbers: false
---
python3 -m pip install build
python3 -m build

--- /code ---
--- /task ---


