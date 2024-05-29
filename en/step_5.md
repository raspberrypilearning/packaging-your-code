## Install your package

Running the build command generated a new folder called `dist` which contains a version of your package that you can give to other people. 

To be able to use your package from anywhere, you need to install it.

--- task ---

From a command prompt, change directory so that you are inside the `dist` directory.

--- /task ---

--- task ---
Install the package by typing the following command:

--- code ---
---
language: bash
line_numbers: false
---
pip3 install motivate.whl

--- /code ---

--- /task ---


--- task ---

Test the `motivate` module has been installed by moving the test program to a directory **outside** your `my_project` directory, and running it. The code should work as expected and print the motivational message. 

If you are presented with the error `ImportError: No module named motivate`, the module installation has not been completed successfully.

--- /task ---
