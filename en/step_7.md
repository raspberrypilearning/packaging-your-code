## Upload to PyPI

[PyPI, the Python Package Index](https://pypi.org) is the key repository for Python distributions where you can find Python software created and shared by other developers to install and use in your own programs.

Whenever you install Python modules using `pip`, e.g.:

```bash 
pip install guizero
```

what happens is that `pip` downloads the package from [pypi.org](https://pypi.org) and then runs the `setup.py` program for you.

When you want to share a Python module of your own, and you and have created a `setup.py` for it, you can use this to create a **distribution** and upload it to PyPI to allow others to find and install your **package**.

--- task ---

To upload a package to [pypi.org](https://pypi.org), you will need an account. 

Open a browser, go to [pypi.org/account/register](https://pypi.org/account/register/), and sign up for an account.

![pypi register](images/pypi_register.PNG)

--- /task ---

--- task ---

Check for an email from PyPi and confirm your registration.

**Note:** you will not be able to upload a distribution to PyPi until you have done so.

--- /task ---

--- task ---

Next, use your setup program to create a **distribution**. This is a compressed file that contains your Python module, its source code, and your `setup.py` file.

On the command line, run your `setup.py` program with the parameter `sdist`.

--- collapse ---

---
title: Windows
---

Open a **Command Prompt** window and run your `setup.py` program, passing the parameter `sdist` to it.
```bash
python setup.py sdist
```

![setup sdist windows](images/setup_sdist_windows.PNG)

--- /collapse --- 

--- collapse ---

---
title: Raspberry Pi/Linux/macOS
---

Open a **Terminal** window and run your `setup.py` program, passing the parameter `sdist` to it.

```bash
python3 setup.py sdist
```

![setup sdist pi](images/setup_sdist_pi.PNG)

--- /collapse ---

**Note:** the `sdist` parameter tells `setup.py` to create a **source distribution**, which can be used to install your module on any computer which can run Python. There are other distribution types, e.g. `bdist_wheel`, which is a binary distribution. This type is quicker to install but may not work on every computer, so it is good idea to always create a source distribution.

--- /task ---

`setup.py` will have created a directory called `dist` in your `my_project` directory that contains the distribution files for your project. 

Once you have created your distribution, you can upload it to PyPI using `twine`.

--- task ---

Change directory `cd` to the `dist` directory.

```bash
cd dist
```

--- /task ---

--- task ---

Upload all the distribution files `*` using `twine`.

```bash
twine upload *
```

You will be prompted to enter your PyPI username and password, and your project will then be uploaded.

--- /task ---

![twine upload](images/twine_upload.PNG)

Once your project has been uploaded, other people can download and install it using `pip`.

```bash
pip3 install my_project
```

Whenever you want to upload a new version of your project to PyPI, do the following:
1. Update the version number in `setup.py`
1. Run `setup.py` to create a new source distribution
1. Upload the new version using `twine`
