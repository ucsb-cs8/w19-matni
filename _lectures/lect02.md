---
num: "lect02"
lecture_date: 2019-01-09
desc: "Basic Data Types and Operators"
ready: true
pdfurl: /lectures/pdf/lect02.pdf
annotatedpdfurl:
annotatedready: false
---

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```
Python 3.7.2 (default, Dec 27 2018, 07:35:06) 
[Clang 10.0.0 (clang-1000.11.45.5)] on darwin
Type "help", "copyright", "credits" or "license()" for more information.
WARNING: The version of Tcl/Tk (8.5.9) in use may be unstable. Visit
http://www.python.org/download/mac/tcltk/ for current information.
>>> grade = 3.8
>>> type(grade)
<class 'float'>
>>> grade=3
>>> type(grade)
<class 'int'>
>>> type("Green Eggs and Ham")
<class 'str'>
>>> type(True)
<class 'bool'>
>>> type(true)
Traceback (most recent call last):
  File "<pyshell#6>", line 1, in <module>
    type(true)
NameError: name 'true' is not defined
>>> 


>>> pi = 3.14
>>> type(pi)
<class 'float'>
>>> p = int(pi)
>>> type(p)
<class 'int'>
>>> print(p)
3
>>> 
>>> int(4.2)
4
>>> int(True)
1
>>> int(False)
0
>>> float(False)
0.0
>>> float(True)
1.0
>>> str(42)
'42'
>>> int("42")
42
>>> a = "42"
>>> b = 2
>>> a - b
Traceback (most recent call last):
  File "<pyshell#23>", line 1, in <module>
    a - b
TypeError: unsupported operand type(s) for -: 'str' and 'int'
>>> int(a) - b
40
>>> 


>>> pi = 3.14159
>>> radian_angle = 0.7853975
>>> degree_angle = radian_angle * 180 / pi
>>> print(degree_angle)
45.0
>>> 
```

