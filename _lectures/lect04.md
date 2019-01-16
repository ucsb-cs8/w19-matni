---
num: "lect04"
lecture_date: 2019-01-16
desc: "More about Functions in Python"
ready: true
pdfurl: /lectures/pdf/lect04.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
# My first function! Yay!
def dbl(x):
	"""This function returns double its input x"""
	print(“Doubling the number to:”, x)
	return 2*x	# I need to “return” the result

# This function calculates the distance between (a,b) and (0,0)
def distance(a, b):
	x = a**2	# Note the tab indent!!!
	y = b**2	# Recall ** means “to the power of”
	z = (x + y) ** 0.5
	return z	# I need to “return” the result

# !!! Alternatively !!!
def distance(a, b):
	return ( (a**2) + (b**2) ) ** 0.5
	
def dbl(x):
	return 2*x
y = 2
x = 5
x = dbl(y)
print(x, y, dbl(y))

len("Gaucho Greg")
s = "There once was a man from Nantucket\nWho got fed up and said \"Chuck it!\""
print(s)
len(s)

"uck" in s
"nan" not in s
"e" in s
" e" in s 

name = "Sally"
name.center(12)
cname = name.center(12)
name.count('l')
name.upper()
name.replace('Sa','Bi')
name.replace('l','m I am')

def fortyTwo():
	return 42

fortyTwo
fortyTwo()


def halve( x ):
""" returns half its input, x """
	return div(x, 2)

def div( y, x ):
""" returns y / x """
	return y / x

halve( 85 )

print("Hi", "How are ya?!")
print(1,2,3)

sum(1,2,3)
sum([1,2,3])
l = [1, 5, 7, 9, -12, 0, 22, 3]
max(l)
min(l)

import math
math.sqrt(3)
math.sin(3.14159)
pieye = math.pi
math.tan(pieye/4)
```
