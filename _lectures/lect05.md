---
num: "lect05"
lecture_date: 2019-01-23
desc: "Data Mutation and Related Topics"
ready: true
pdfurl: /lectures/pdf/lect05.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
Python 3.7.2 (default, Dec 27 2018, 07:35:06) 
[Clang 10.0.0 (clang-1000.11.45.5)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
WARNING: The version of Tcl/Tk (8.5.9) in use may be unstable. Visit
http://www.python.org/download/mac/tcltk/ for current information.
>>> 
>>> 
>>> def return_dbl( x ):
	return x*2

>>> def print_dbl( x ):
	print(x*2)

>>> a = 13
>>> 
>>> return_dbl(a)
26
>>> print_dbl(a)
26
>>> 

# At this point, we created a program with the same instructions as above:

=================== RESTART: /Users/ziadmatni/Untitled.py ===================
Here's the result of return_dbl()
Here's the result of print_dbl()
26
>>> 

# Then we added some instructions in the program to clarify what var. a value was and what the function value was
#
# def return_dbl(x):
#	return x*2
#
# def print_dbl(x):
#	print (x*2)
#
# a =13
# print("Here's the result of return_dbl()")
# print("a = ", a)
# print("the function return value: ", return_dbl(a))
# print("-------------------------------")
# print("Here's the result of print_dbl()")
# print("a = ", a)
# print("the function return value: ", return_dbl(a))
#
=================== RESTART: /Users/ziadmatni/Untitled.py ===================
Here's the result of return_dbl()
a =  13
the function returned value:  26
-------------------------------
Here's the result of print_dbl()
26
a =  13
26
the function returned value:  None
>>> 

>>> a = range(5)
>>> print(a)
range(0, 5)
>>> 
>>> a = list(range(5))
>>> print(a)
[0, 1, 2, 3, 4]

>>> a = list(range(55))
>>> print(a)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54]
>>> 

>>> a = list(range(5, 11))
>>> print(a)
[5, 6, 7, 8, 9, 10]

>>> a = list(range(5, 21))
>>> print(a)
[5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]

>>> a = list(range(5, 21, 2))
>>> print(a)
[5, 7, 9, 11, 13, 15, 17, 19]

>>> a = list(range(5, 21, 3))
>>> print(a)
[5, 8, 11, 14, 17, 20]

>>> a = list(range(4, 21, 2))
>>> print(a)
[4, 6, 8, 10, 12, 14, 16, 18, 20]

>>> a = list(range(4, 21, 5))
>>> print(a)
[4, 9, 14, 19]

>>> a = list(range(-4, 21, 5))
>>> print(a)
[-4, 1, 6, 11, 16]

>>> a = list(range(-4, -21, 5))
>>> print(a)
[]

>>> a = list(range(-41, -21, 5))
>>> print(a)
[-41, -36, -31, -26]

>>> a = list(range(42, 21, -5))
>>> print(a)
[42, 37, 32, 27, 22]
>>> 
```
