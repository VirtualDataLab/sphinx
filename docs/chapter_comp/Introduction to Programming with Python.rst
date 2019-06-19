Introduction to Programming with Python
#######################################

:Authors: Peer Herholz
:Citation: Herholz, P. (2019. Computer stuff. In S.E.P. Boettcher, D. Draschkow, J. Sassenhagen & M. Schultze (Eds.). Scientific Methods for Open Behavioral, Social and Cognitive Sciences. https://doi.org/10.17605/OSF.IO/HCJG9 

This section is meant as a general introduction to Python and is by far not
complete. The goal of this section is to give a short introduction to Python
and help beginners to get familiar with this programming language. We recommend
to follow this section in parallel with a more interactive tutorial by clicking on this button:

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/aylinsgl/Binder_test/master?filepath=01_python_basic.ipynb

What is Python?
-----------------

Python is a simple and powerful programming language.
  - what it can be used for in a scientific way as well as industry applications (which companies use python etc.)

For an introduction to statistics in python take a look at this interactive tutorial:

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/aylinsgl/Binder_test/master?filepath=05_python_statistics.ipynb

For an introduction to visualization in python take a look at this interactive tutorial:

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/aylinsgl/Binder_test/master?filepath=02_python_visualization.ipynb

Basics
--------------

**Indentation**

Whitespace is important in Python. Actually, whitespace at the beginning of the
line is important. This is called indentation. Leading whitespace (spaces and
tabs) at the beginning of the logical line is used to determine the indentation
level of the logical line, which in turn is used to determine the grouping of
statements.

This means that statements which go together must have the same indentation.
Each such set of statements is called a block. We will see examples of how
blocks are important later on. One thing you should remember is that wrong
indentation rises ``IndentationError``.

**Comments**

Comments are anything behind a ``#`` symbol at the beginning of a new line. Python
skips those parts of the program and comments therefor intended to help the
reader of a program to understand what and why a specific statement in the code
is doing. Keep in mind that this person can be yourself in 2 month so it is good
practice to include comments explaining important decisions, details or problems.

Help and Descriptions
-------------------------

Using the function help we can get a description of almost all functions.
Imagine we do not know what the ``math.log()`` function is doing or how to use it...
we can just call the help function and find out.::

  help(math.log)

Variables
-------------------------

**Variable Names**

Variable names in Python can contain alphanumerical characters a-z, A-Z, 0-9 and
some special characters such as an underscore. Normal variable names must start
with a letter. By convention, variable names start with a lower-case letter,
and Class names start with a capital letter. Don't worry if you do not know what
Classes are yet. We will get to that later.

In addition, there are a number of Python keywords that cannot be used as
variable names. These keywords are:

`and, as, assert, break, class, continue, def, del, elif, else, except,
exec, finally, for, from, global, if, import, in, is, lambda, not, or,
pass, print, raise, return, try, while, with, yield.``

Note: Be aware of the keyword ``lambda``, which could easily be a natural variable
name in a scientific program. But being a keyword, it cannot be used as a
variable name.

**Assigning Variables**


The assignment operator in Python is ``=``. Python is a dynamically typed language,
so we do not need to specify the type of a variable when we create one.
Assigning a value to a new variable creates the variable.::

  # assigning x to 1.0 and y to 3
  x = 1.0
  y = 3

Data Types
-----------------

Although not explicitly specified, a variable does have a type associated with
it. The type is derived form the value it was assigned and defines the operations
that can be done with a specific variable.

You can check the data type with: ::

  # check type of x
  type(x)

Python has four standard data types that we will briefly go over now.

**Numbers**

This data type stores numerical data and python supports different numerical
data types including: ::

  # integer
  x = 1

  # float
  x = 1.0

**String**

Strings are the variable type that is used for storing text messages. They are
an array of characters and are indicated through either single or
double quotation marks. ::

  # string
  s = "This is a string"
  s2 = 'This also is a string'

You can specify multi-line strings using triple quotes - (``"""`` or ``'''``). You can
use single quotes and double quotes freely within the triple quotes.
An example is: ::

  '''This is a multi-line string. This is the first line.
  This is the second line.
  "What's your name?," I asked.
  He said "Bond, James Bond."
  '''

Strings can be formatted and handled in multiple ways. For example, we can index
a string using []: ::

  # this gives us the first character in s ("T")
  s[0]

Heads up MATLAB user: Indexing starts at 0!

We can also extract a part of a string using the syntax [start:stop], which
extracts characters between index start and stop. This is called *slicing*: ::

  # output of this will be "This"
  s[0:4]


If we omit either (or both) of start or stop from [start:stop], the default is
the beginning and the end of the string, respectively: ::

  # This hands us "This"
  s[:4]

  # This hands us "is a string"
  s[4:]

We can also define the step size using the syntax [start:end:step]
(the default value for step is 1, as we saw above): ::

  # entire string, step size of 1
  s[::1]

  # entire string, step size of 2. Every second character will be selected
  s[::2]

Python has two string formatting styles. An example of the old style is below,
specifier %.2f transforms the input number into a string, that corresponds to a
floating point number with 2 decimal places and the specifier %d transforms the
input number into a string, corresponding to a decimal number. ::

  # s2 = 'value1 = 3.14. value2 = 1'
  s2 = "value1 = %.2f. value2 = %d" % (3.1415, 1.5)

The same string can be written using the new style string formatting. ::

  s3 = 'value1 = {:.2f}, value2 = {}'.format(3.1415, 1.5)

There are a lot more useful operations that can be done on strings and some of
them can be explored in the interactive part of this introduction.

**Lists**

Lists are very similar to strings, except that each element can be of any type.
A list entails items separated by commas and enclosed in square brackets ``[]``.::

  # list
  l = [1, 2, 3]
  l2 = ["one", "two", "three"]


We can use the same slicing techniques to manipulate lists as we could use on
strings. Elements in a list do not all have to be of the same type and Python
lists can be inhomogeneous and arbitrarily nested:: ::

  # also a list
  l = [1, 'a', 1.0]

  # nested list
  nested_list = [1, [2, [3, [4, [5]]]]]

Lists play a very important role in Python, and are for example used in loops
and other flow control structures (discussed below). There are number of
convenient functions for generating lists of various types, for example the
range function (note that in Python 3 range creates a generator, so you have to
use list function to get a list). ::

  start = 10
  stop = 30
  step = 2

  list(range(start, stop, step))


*Adding, inserting, modifying, and removing elements from lists*

We can modify lists by assigning new values to elements in the list. In technical
jargon, lists are mutable. ::

  # assigning "p" to the second element in l
  l[1] = "p"

  # assigning "s" to the second and "m" to the third element of l
  l[1:3] = ["s","m"]

**Tupels**

Tupels are very similar to lists. The main difference is that tupels are enclosed
in parentheses and cannot be updated after they have been assigned. ::

  # tupel
  t = (1,2,3)

If we try to assign a new value to an element in a tuple we get an error. ::

  point[0] = 20

``TypeError: 'tuple' object does not support item assignment``

**Dictionaries**

Dictionaries are also like lists, except that each element is a key-value pair.
The syntax for dictionaries is ``{key1 : value1, ...}``: ::

  params = {"parameter1" : 1.0,
          "parameter2" : 2.0,
          "parameter3" : 3.0,}

Dictionary entries can only be accessed by their key name. ::

  # accessing entry for key "parameter1"
  params["parameter1"]

  > 1.0

  # changing an entry
  params["parameter1"] = "A"

  # adding a new entry
  params["parameter4"] = "D"

Operators and Comparisons
-----------------------------

Operators can change the value of operands. Python contains different types of
operators and we will touch on two fundamental ones: Arithmetic and comparison
operators.

**Arithmetic Operators**

Arithmetic operators include:

+---------+-----------------+
| ``+``   | Addition        |
+---------+-----------------+
| ``-``   | Subtraction     |
+---------+-----------------+
| ``*``   | Multiplication  |
+---------+-----------------+
| ``/``   | Division        |
+---------+-----------------+
| ``%``   | Modulo          |
+---------+-----------------+
| ``**``  | Power           |
+---------+-----------------+

**Comparison Operators**

These operators are used to compare their operands. They return either ``True`` or
``False`` depending if the condition under which the operands are compared applies
or not.

+-----------+---------------------------------------------------------------------+
| ``==``    | evaluates if operands are equal                                     |
+-----------+---------------------------------------------------------------------+
| ``!=``    | evaluates if operands are not equal                                 |
+-----------+---------------------------------------------------------------------+
| ``>``     | evaluates if left operand is greater than the right operand         |
+-----------+---------------------------------------------------------------------+
| ``<``     | evaluates if right operand is greater than the left operand         |
+-----------+---------------------------------------------------------------------+
| ``>=``    | evaluates if left operand is greater or equal than the right operand|
+-----------+---------------------------------------------------------------------+
| ``<=``    | evaluates if right operand is greater or equal than the left operand|
+-----------+---------------------------------------------------------------------+

Control Flow
---------------
Python usually executes code in an exact top-down order. However, that is not
always what we want. Imagine a situation where different blocks of code should be
executed depending on different situations, conditions or decision. What if a
different sound should be played depending on if participant correctly answered
in a trial?
Python provides different control flow statements to achieve exactly that.

**Conditional statements: if, elif, else**

The Python syntax for conditional execution of code use the keywords ``if, elif (else if), else``:
The ``if`` statement is used to check if a specific condition is met. If this is
the case, the block followed the if-statement (if-block) is executed. If not
this block of code is skipped. ::

  x = 1
  # check if x equals 1 and print the answer
  if x == 1:
    print("Yes, x equals 1")

  > "Yes, x equals 1"

The if-statement can be accompanied by an ``elif`` and/or ``else`` statement: In this
case, python first checks the first if-statement. If this evaluates to "True"
python executes the following indented code block and skips the rest of the
if-elif-else statement as one of them already evaluated to true. Otherwise,
python evaluates every statement in this block until one evaluates to true or it
reaches the else-statement which gets executed if non of the if- or
elif-statements evaluates to true. ::

  x = 5

  if x < 5:
    print("X is smaller than 5")
  elif x >5:
    print("X is bigger than 5")
  else:
    print("X equals 5")

  > "X equals 5"


For the first time, here we encountered the mentioned indentation. This means
that we have to be careful to indent our code correctly, or else we will get
syntax errors.

**for - loop**

The ``for`` loop iterates over the elements of the supplied list (or any other iterable object),
and executes the containing block once for each element. Any kind of list can be used in the for
loop. For example: ::

  for x in [1,2,3]:
    print(x)

  > 1
    2
    3

  for x in range(-1,1):
    print(x)

  > -1
    0
    1

Sometimes it is useful to have access to the indices of the values when
iterating over a list. We can use the enumerate function for this: ::

  for idx, x in enumerate(range(-1,1)):
    print(idx, x)

  > 0 -1
    1 0
    2 1

**while - loop**

The ``while`` loop allows to repeatedly execute a block of code as long as a
specified condition is met. Python checks the condition and if it evaluates to
``True`` executes the while-block. It then checks the condition again, if it is
still ``True`` the block is executed again, else python continues to the next
statement in the block. ::

  # while loop will stop as soon as i = 5
  i = 0

  while i < 5:
    print(i)

    i = i + 1
  print("done")

  > 0
    1
    2
    3
    4
    done

**continue, break, pass**

To control the flow of a certain loop you can also use ``break``, ``continue`` and ``pass``.
``break`` can be used to break out of a loop and force python to stop the execution
of a loop statement. The ``continue`` statement is used to tell Python to skip the
rest of the statements in the current loop block and to continue to the next
iteration of the loop (i.e. start executing the loop-block from the beginning).
``pass`` basically tells python to do nothing and to carry on with executing the
script. ::

  rangelist = list(range(10))

  for number in rangelist:
      # Check if number is one of
      # the numbers in the tuple.
      if number in [4, 5, 7, 9]:
          # "Break" terminates a for without
          # executing the "else" clause.
          break
      else:
          # "Continue" starts the next iteration
          # of the loop. It's rather useless here,
          # as it's the last statement of the loop.
          print(number)
          continue
  else:
      # The "else" clause is optional and is
      # executed only if the loop didn't "break".
      pass # Do nothing

  > [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    0
    1
    2
    3

Functions
----------------

Functions allow to reuse pieces of code by assigning names to them. By calling a
function by their name it is possible to use it anywhere in your program without
having to repeat the code "hidden" behind the name of the function. There are a
lot of build-in functions in oython. However, it is also possible to create your
own functions.
A function in Python is defined using the keyword ``def``, followed by a function
name, a signature within parentheses ``()``, and a colon ``:``. The following code, with
one additional level of indentation, is the function body. ::

  def say_hello():
    # block belonging to the function
    print('hello world')

  say_hello() # call the function

  > 'hello world'

Classes
----------------

Classes are the key features of object-oriented programming. A class is a structure for
representing an object and the operations that can be performed on the object.
In Python a class can contain `attributes` (variables) and `methods` (functions).
A class is defined almost like a function, but using the class keyword, and the class
definition usually contains a number of class method definitions (a function in a class).
Each class method should have an argument ``self`` as it first argument. This object is a self-reference,
meaning it is referring to the current instance of the class.

Some class method names have special meaning, for example:

``__init__`` : The name of the method that is invoked when the object is first created.
``__str__`` : A method that is invoked when a simple string representation of the class is needed,
as for example when printed. There are many more, see http://docs.python.org/3.6/reference/datamodel.html#special-method-names

::

  class Point:
    """
    Simple class for representing a point in a Cartesian coordinate system.
    """

    def __init__(self, x, y):
        """
        Create a new Point at x, y.
        """
        self.x = x
        self.y = y

    def translate(self, dx, dy):
        """
        Translate the point by dx and dy in the x and y direction.
        """
        self.x += dx
        self.y += dy

    def __str__(self):
        return("Point at [%f, %f]" % (self.x, self.y))

    # creating a new instance of a class
    p1 = Point(0, 0)  # this will invoke the __init__ method in the Point class
    print(p1)         # this will invoke the __str__ method

    > Point at [0.000000, 0.000000]

To invoke a class method in the class instance ``point2`` at coordinates ``x=1``, ``y=1``: ::

  point2 = Point(1, 1)
  print(point2)

  > Point at [1.000000, 1.000000]

  point2.translate(2, 2)
  print(point2)

  > Point at [3.000000, 3.000000]

Accessing values of a class object directly: ::

  point3 = Point(1, 4)
  print(point3.y)

  > 4

Modules <--- BIS HIER
-----------
Most of the functionality in Python is provided by modules.
To use a module in a Python program it first has to be imported. A module can be
imported using the import statement. For example, to import the module math,
which contains many standard mathematical functions, we can do::

  import math


This includes the whole module and makes it available for use later in the
program. For example, we can do::

  import math

  x = math.cos(2 * math.pi)

  print(x)

Importing the whole module is often times unnecessary and can lead to longer
loading time or increase the memory consumption. Alternative to the previous
method, we can also chose to import only a few selected functions from a module
by explicitly listing which ones we want to import::

  from math import cos, pi

  x = cos(2 * pi)

  print(x)

It is also possible to give an imported module or symbol your own access name
with the as additional::

  import numpy as np
  from math import pi as number_pi

  x = np.rad2deg(number_pi)

  print(x)


Exceptions
----------------

In Python errors are managed with a special language construct called
"Exceptions". Such exceptions arise when Python cannot cope with a situation in
the code. Imagine you are calling a function but the function does not exist.
Depending on the issue on hand, Python raises different exceptions. If
this exception cannot be handled immediately, the script terminates and quits.

Examples are:

+-------------------+---------------------------------------------------------+
| NameError         | Raised when an identifier is not found                  |
+-------------------+---------------------------------------------------------+
| SyntaxError       | Raised when there is an error in the syntax             |
+-------------------+---------------------------------------------------------+
| IndentationError  | Raised when the indentation is not specified correctly  |
+-------------------+---------------------------------------------------------+

Python also provides the opportunity to protect your code from errors and
exception by placing code snippes into a *try-block*.

+----------------------------------------------------+
|  try:                                              |
|      # normal code goes here                       |
|  except:                                           |
|      # code for error handling goes here           |
|      this code is not executed unless the code     |
|      above generated an error                      |
+----------------------------------------------------+

For example: ::

  try:
    raise Exception("description of the error")
  except(Exception) as err:
    print ("Exception:", err)

How does this work? All the code that might raise exceptions goes after then
try-statement. Everything that goes after the except-statement is only executed
if an error arises and is supposed to handle the error.

**Finally-statement**

Another useful extension of this concept is the finally- statement. It can be
used to specify a block of code that should be executed wether an exception is
raised or not. In other words, code that goes after an finally-statement is
always executed. ::

  try:
    print("test")
    # generate an error: the variable test is not defined
    print(test)
  except Exception as e:
    print("Caught an exception:" + str(e))
  finally:
    print("This block is executed after the try- and except-block.")


File I/O
----------------
This section should give you a basic knowledge about how to read and write CSV
or TXT files.
