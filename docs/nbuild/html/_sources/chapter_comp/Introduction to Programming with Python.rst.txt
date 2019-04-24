Introduction to Programming with Python
#######################################

This section is meant as a general introduction to Python and is by far not
complete.The goal of this section is to give a short introduction to Python
and help beginners to get familiar with this programming language.


What is Python?
-----------------
Python is a simple and powerful programming language.
  - what it can be used for in a scientific way:

For an introduction to statistics in python take a look at this interactive tutorial:

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/aylinsgl/Binder_test/master?filepath=05_python_statistics.ipynb

For an introduction to visualization take a look at this interactive tutorial:

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/aylinsgl/Binder_test/master?filepath=02_python_visualization.ipynb

Basics
--------------

Modules
-----------
Most of the functionality in Python is provided by modules.
To use a module in a Python program it first has to be imported. A module can be imported using the import statement. For example, to import the module math,
which contains many standard mathematical functions, we can do::

  import math


This includes the whole module and makes it available for use later in the program. For example, we can do::

  import math

  x = math.cos(2 * math.pi)

  print(x)

Importing the whole module is often times unnecessary and can lead to longer loading time or increase the memory consumption. Alternative to the previous method, we can also chose to import only a few selected functions from a module by explicitly listing which ones we want to import::

  from math import cos, pi

  x = cos(2 * pi)

  print(x)

It is also possible to give an imported module or symbol your own access name with the as additional::

  import numpy as np
  from math import pi as number_pi

  x = np.rad2deg(number_pi)

  print(x)

Help and Descriptions
-------------------------
Using the function help we can get a description of almost all functions.
Imagine we do not know what the math.log()-function is doing or how to use it...
we can just call the help function and find out.::
  help(math.log)

Variables and Types
-------------------------

**Variable Names**

Variable names in Python can contain alphanumerical characters a-z, A-Z, 0-9 and
some special characters such as an underscore. Normal variable names must start
with a letter. By convention, variable names start with a lower-case letter,
and Class names start with a capital letter. Don't worry if you do not know what Classes are yet. We will get to that later.

In addition, there are a number of Python keywords that cannot be used as
variable names. These keywords are:

and, as, assert, break, class, continue, def, del, elif, else, except, exec,
finally, for, from, global, if, import, in, is, lambda, not, or, pass, print,
raise, return, try, while, with, yield

Note: Be aware of the keyword lambda, which could easily be a natural variable
name in a scientific program. But being a keyword, it cannot be used as a
variable name.


**Indentation**
Whitespace is important in Python. Actually, whitespace at the beginning of the
line is important. This is called indentation. Leading whitespace (spaces and
tabs) at the beginning of the logical line is used to determine the indentation level of the logical line, which in turn is used to determine the grouping of statements.

This means that statements which go together must have the same indentation.
Each such set of statements is called a block. We will see examples of how blocks are important later on. One thing you should remember is that wrong indentation rises IndentationError.

**Comments**

**Assigning Variables**

The assignment operator in Python is =. Python is a dynamically typed language,
so we do not need to specify the type of a variable when we create one.
Assigning a value to a new variable creates the variable.::

  # assigning x to 1.0 and y to 3
  x = 1.0
  y = 3

**Data Types**
Although not explicitly specified, a variable does have a type associated with it. The type is derived form the value it was assigned and defines the operations
that can be done with a specific variable. Python has five standard data types.

You can check the data type with: ::
  # check type of x
  type(x)

*Numbers*

This data type stores numerical data and python supports different numerical
data types including: ::

  # integer
  x = 1

  # float
  x = 1.0

*String*

Strings are the variable type that is used for storing text messages. They are
an array of characters and are indicated through either single or
double quotation marks. ::

  # string
  s = "This is a string"
  s2 = 'This also is a string'

Strings can be formatted and handled in multiple ways. For example, we can index
a string using []: ::
  # this gives us the first character in s ("T")
  s[0]

Heads up MATLAB user: Indexing starts at 0!

We can extract a part of a string using the syntax [start:stop], which extracts characters between index start and stop. This is called *slicing*: ::



*Lists*

A list entails items separated by commas and enclosed in square brackets [].::

  # list
  l = [1, 2, 3]
  l2 = ["one", "two", "three"]

*Tupels*

Tupels are very similar to lists. The main difference is that tupels are enclosed
in parentheses and cannot be updated after they have been assigned. ::

  # tupel
  t = (1,2,3)

*Dictionaries*

Operators and Comparisons
-----------------------------
Operators can change the value of operands. Python contains different types of
operators and we will touch on two fundamental ones: Arithmetic and comparison
operators.

**Arithmetic Operators**

Arithmetic operators include:

+---------+-----------------+
| +       | Addition        |
+---------+-----------------+
| -       | Subtraction     |
+---------+-----------------+
| *       | Multiplication  |
+---------+-----------------+
| /       | Division        |
+---------+-----------------+
| %       | Modulo          |
+---------+-----------------+
| **      | Power           |
+---------+-----------------+

**Comparison Operators**

These operators are used to compare their operands. They return either "true" or
"false" depending if the condition under which the operands are compared applies
or not.

+---------+---------------------------------------------------------------------+
| ==      | evaluates if operands are equal                                     |
+---------+---------------------------------------------------------------------+
| !=      | evaluates if operands are not equal                                 |
+---------+---------------------------------------------------------------------+
| >       | evaluates if left operand is greater than the right operand         |
+---------+---------------------------------------------------------------------+
| <       | evaluates if right operand is greater than the left operand         |
+---------+---------------------------------------------------------------------+
| >=      | evaluates if left operand is greater or equal than the right operand|
+---------+---------------------------------------------------------------------+
| <=      | evaluates if right operand is greater or equal than the left operand|
+---------+---------------------------------------------------------------------+

Control Flow
---------------

Loops
----------

Functions
----------------

Classes
----------------

Exceptions
----------------

File I/O
----------------
