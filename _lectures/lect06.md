---
num: "lect06"
lecture_date: 2019-01-28
desc: "Modules and Conditionals"
ready: true
pdfurl: /lectures/pdf/lect06.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
# This is what's inside your created module 
# (we called it PinkFloyd.py in class
#

# Doubling function
def dbl(x):
	return 2*x

# Halving function 
def half(x):
	return x/2

if __name__ == "__main__":
	print("I'm inside PinkFloyd.py")
	print(dbl(82.12))

####################################
# This is what's inside your own file that IMPORTS PinkFloyd.py
#
# We want to use those functions in PinkFloyd.py
import PinkFloyd
# from PinkFloyd import *      # another way to do this

print("Inside PinkFloyd.py")

print(PinkFloyd.dbl(5))
print(PinkFloyd.dbl("UCSB"))
print(PinkFloyd.dbl([1, 2, 3]))

print(PinkFloyd.half(42))


####################################
# Boolean Operators
####################################

x = True
y = False
z = True
print( x and y )
print( x and not y )
print( (x and y) or z )



a = 3
b = 4
c = 5
print( a == 3 and b == 4)
print( not (b < 2) and not (a != 5) )
print( (a > 0 or b == 0) and (c <= 5) )


def CheckNegInt(x):
	c = False
	if (type(x) == int) and (x < 0):
		c = True
	return c

####################################
# Conditional Statements 
####################################

# Classic Example:

x = int(input("Enter any integer: "))
if x >= 0:
	print ("You entered a positive number!")
	print ("Or it could be zero!")
else:
	print ("You entered a negative number!")


####################################
# This is an example of using if-elif-else

a = int(input("Enter a number: "))

if (a < 5):
	print("It’s less than five!")

elif (a > 5):
	print("It’s more than five!!!")

else:
	print("It’s equal to five!!!!!")


####################################
# This is an example of NESTED if-else statements

a = int(input("What is the cost of item X? "))
b = int(input("Enter (0) for not available, (1) for available "))

if (b == 0):
	print("It doesn’t matter what it costs: it’s not available!")
else:
	if (a >= 100):
		print("That’s expensive!")
	else:
		print("That’s not too expensive!")

```
