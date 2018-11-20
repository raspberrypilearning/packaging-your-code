## Introduction

In this project, you will learn everything you need to know to package your own Python code so that others can install and use it by creating a simple Python module and then packaging it.

### What you will make

When programming in Python, you very quickly get used to using `import` statements to use external **modules** within your programs. For example:

```python
from guizero import App
```

or:

```python
from numpy import array
```

These modules have been created by other programmers, who have shared them as **distributions** that you can install using the command line tool `pip`. For example:

```bash
pip3 install guizero
```

Bundling code into distributions that you can share is called **packaging**, and packaging makes it much easier for people to download, install, and use your programs.

You will write a basic Python module called `motivate` that prints motivating messages, and learn how to package it.

--- no-print ---

![motivate me](images/motivate_me.gif)

--- /no-print ---

--- print-only ---

![motivate me](images/motivate_me.PNG)

--- /print-only ---

--- collapse ---

---
title: What you will learn
---

You will learn:

+ How to structure Python projects
+ How to package Python modules

This project covers elements from the following strands of the [Raspberry Pi Digital Making Curriculum](http://rpf.io/curriculum){:target="_blank"}:

+ [Apply higher-order programming techniques to solve real-world problems](https://curriculum.raspberrypi.org/programming/maker/){:target="_blank"}
+ [Engage and share with the digital making community](https://curriculum.raspberrypi.org/community-and-sharing/creator/){:target="_blank"}

--- /collapse ---

--- collapse ---

---
title: What you will need
---

### Hardware

+ A computer capable of running Python 3

### Software

+ Python 3
+ The following Python modules, which can be installed using `pip3`:
  + setuptools
  + twine

--- /collapse ---

--- no-print ---

If you need to print this project, please use the [printer-friendly version](https://projects.raspberrypi.org/en/projects/packaging-your-code/print){:target="_blank"}.

Use the link in the footer to access the GitHub repository for this project, which contains all resources (including an example finished project) in the 'en/resources' folder.

--- /no-print ---

