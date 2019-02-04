---
num: "lect08"
lecture_date: 2019-01-30
desc: "More on Loops"
ready: true
pdfurl: /lectures/pdf/lect08.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
s = "Take me home, country roads"
#s = "TAKE ME HOME, COUNTRY ROADS"
t = 0
for c in s:
	if c in ('a', 'e', 'i', 'o', 'u'):
		print("Vowel found: ", c)
		t = t + 1
print("There were", t, "vowels found")

###################################

def prime(n):
    p = True
    for i in range(2,n):
        if n % i == 0:
            p = False
    return p

for i in range(2, 3000):
    if prime(i):
        print(i, end=" , ")

###################################

def drawSquare2(myTurtle, sideLength):
    for i in range(4):
        myTurtle.forward(sideLength)
        myTurtle.right(90)

def drawTriangle(myTurtle, sideLength):
    for i in range(3): 		# draw 3 sides, not 4
        myTurtle.forward(sideLength)
        myTurtle.right(120) 	# 120°× 3

def drawPolygon(myTurtle, sideLength, numSides):
    turnAngle = 360 / numSides
    for i in range(numSides):
        myTurtle.forward(sideLength)
        myTurtle.right(turnAngle)

import turtle
t = turtle.Turtle()
drawSquare2(t, 200)
drawTriangle(t, 50)
drawPolygon(t, 50, 12)

###################################
# We didn't get into these too deeply, but will re-visit after the midterm

listX = [ [1, 2, 3], [4, 5, 6], [7, 8, 9] ]
for i in listX:
	for j in i:
		print(j)

###################################

AllGrades = 0			# (1) initialize
grade = input("enter grade or q to quit: ")
while grade != "q":		# (2) check condition
		AllGrades = AllGrades + int(grade)			# process grade
		grade = input("enter grade or q to quit: ")	# ask again

# While loop has ended (no indents after here),
# now you can do other stuff…
print("Total grades is:", AllGrades)
print("You're all done now!")
```
