## Test your code

Test your code works before you package it.

--- task ---

Create a file called `test.py` and save it in the `my_project` directory.

--- /task ---

--- task ---

In `test.py`, add the following code to import the `motivate_me` function from the `motivate` module.

--- code ---
---
language: python
filename: test.py
line_numbers: true
---
from motivate import motivate_me

--- /code ---

--- /task ---

--- task ---

Add code to call the `motivate_me` function.


--- code ---
---
language: python
filename: test.py
line_numbers: true
line_number_start: 1
line_highlights: 2
---

   from motivate import motivate_me
   motivate_me()

--- /code ---

--- /task ---

--- task ---

Run the `test.py` program.

--- /task ---

You should see your motivating message appear!

![motivate me](images/motivate_me.gif)

