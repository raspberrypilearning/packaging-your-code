## Install your package

Running the build command generated a new folder called `dist` which contains a version of your package that you can give to other people. 

To be able to use your package from anywhere, you need to install it.

--- task ---

From a command prompt, change directory so that you are inside the `dist` directory.

--- /task ---

--- task ---
Install the package by typing the foll

--- /task ---


--- task ---

Test the `motivate` module has been installed by recreating the test program, saving it **outside** your `my_project` directory, and running it.

```python
from motivate import motivate_me
motivate_me()
```

**Note:** if you are presented with the error `ImportError: No module named motivate`, the module installation has not been completed successfully.

--- /task ---
