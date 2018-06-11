## Uploading to pypi.org

PyPI (the Python Package Index) is the key repository for Python distributions. You can find Python software created and shared by other developers and install it. 

When you install Python modules using `pip` e.g.

```bash 
pip install guizero
```

`pip` downloads the package from pypi.org and then runs the `setup.py` program for you.

When you have a Python module you wish to share and have created a **setup** you can use it to create a **distribution** and upload it to pypi.org allowing others to find and install your **package**.


To upload a package to pypi.org you will need an account. 

--- task ---

Open a browser, go to [pypi.org/account/register](https://pypi.org/account/register/) and create an account.

![pypi register](images/pypi_register.PNG)

--- /task ---

Next you will use your setup program to create a **distribution**, this is a compressed file which contains your Python module, its source code and your **setup**.

--- task ---

Open a **Command Prompt** and run your `setup.py` program passing the parameter `sdist`.

--- collapse ---

---
title: Windows
---

```bash
python setup.py sdist
```

![setup dist windows](images/setup_sdist_windows.PNG)

--- /collapse --- 

--- collapse ---

---b
title: Raspberry Pi, Linux, MacOS
---

Open a **Terminal** and run your `setup.py` program passing the parameter `sdist`.


```bash
python3 setup.py sdist
```

--- /collapse ---

--- /task ---
