---
num: "lect15"
lecture_date: 2019-03-11
desc: "Recursive Functions"
ready: true
pdfurl: /lectures/pdf/lect15.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
############################################
# Functions Calling Functions
#
def demo(x):
    return x + f(x)

def f(x):
    return 11*g(x) + g(x/2)

def g(x):
    return -1 * x

print(demo(-4))

############################################
# Factorial - Regular (looped) Version
#
def factorial(n):
    f = 1
    for m in range(1, n+1):
        f = f * m
    return f

print(factorial(5))

############################################
# Factorial - Recursive Version
#
def fac(N):
    if N <= 1:
        return 1
    else:
        return N * fac(N-1)

for i in range(10):
    print(str(i)+"! =", fac(i))

############################################
# Exercise
#
# What does this return for MyRecFun(3)?
def MyRecFun(n):
    if n == 0:
        return 2
    else:
        return 2*MyRecFun(n-1)

print(MyRecFun(3))

############################################
# Fibonacci Series
#
def fibo(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else: # is this else necessary?
        return fibo(n-1) + fibo(n-2)

for i in range(10):
    print("Fibonacci("+str(i)+") =", fibo(i))
```
