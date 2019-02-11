---
num: "lect09"
lecture_date: 2019-02-11
desc: "Advanced Exercises with Loops"
ready: true
pdfurl: /lectures/pdf/lect09.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
def drawSpiral(myTurtle, maxSide):
    for sideLength in range(1, maxSide+1, 5):
        myTurtle.forward(sideLength)
        myTurtle.right(90)

import turtle
t = turtle.Turtle()
drawSpiral(t, 500)

######################################

listX = [ [1, 2, 3], [4, 5, 6], [7, 8, 9] ]
for i in listX:
	for j in i:
		print(j)

######################################

def drawRectangle(width, height):
    for i in range(height):
        for j in range(width):
            print("*", end="")
        print("")

drawRectangle(5, 3)

######################################

def countElements(myL):
    # Assume the user puts in a list
    count = 0
    for item in myL:
        count = count + 1
    return count

print( countElements([1, 3, 4, 7, 8]) )

######################################

def countOddNumbers(myL):
    count = 0
    for item in myL:
        if item % 2 != 0: # if item is odd
            count += 1   # count = count + 1
    return count

print( countOddNumbers([1, 2, 3, 4, 5]) )

######################################

def countWords(sentence):
    # THIS IS WHAT WE FINISHED WITH, BUT IT'S NOT COMPLETE!!!
    # THE ALGORITHM IS NOT FULLY CORRECT: CAN YOU FIGURE IT OUT?!
    # IF NOT, DON'T WORRY: WE WILL SOLVE THIS FOR GOOD IN LECTURE 10! :)
    
    count  = 0
    if len(sentence) == 0:
        return count
    
    else:
        for c in sentence:
            if c == " ":
                count += 1
    
    return count


print( countWords("Hello, I must be going") )
print( countWords(""))

```
