---
num: "lect07"
lecture_date: 2019-01-30
desc: "Loops"
ready: true
pdfurl: /lectures/pdf/lect07.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
##########################################
# Class Exercise 1 (if-else)
age = int(input("How old are you? "))
if (age % 2 == 0):
	print("Your age is an even number!")
else:
	print("Your age is an odd number!")


# Class Exercise 2 (if-elif-else)
age = int(input("How old are you? "))
if (age % 2 == 0) and (age > 0):
	print("Your age is an even number!")
elif (age % 2 != 0) and (age > 0):
	print("Your age is an odd number!")
else:
	print("You have entered an illegal age!")


# Class Exercise 3 (nested if-else)
age = int(input("How old are you? "))
if (age > 0):
	if (age % 2 == 0):
		print("Your age is an even number!")
	else:
		print("Your age is an odd number!")
else:
	print("You have entered an illegal age!")

##########################################
# for loop example 1
for x in (9, 22, -77, 1):
	y = x + 10
	print (y)


# for loop example 2
for y in ("Hello", "Mother", "Hello", "Father"):
	print (x, "!!")


# for loop example 3
n = 0
for item in ["UCSB Location", (34.4140, -119.8489)]:
	n = n + 1
	print(n, item)


# for loop example using range() 1
for x in range(7):
	print (x)


# for loop example using range() 2
for y in range(2, 9):
	print (x - 2)


# for loop example using range() 3
for item in range(5, -1, -1):
	if item == 0:
		print(item, "Blast off!!")
	else:
		print(item)

##########################################
# while loop example 1
n = 500
counter = 0                   # (1) initialize
while counter < n:            # (2) check condition
    print(counter * counter)
    counter = counter + 1     # (3) change state


# while loop example 2
AllGrades = 0			# (1) initialize
grade = int(input("enter grade or q to quit: "))
while grade != "q":		# (2) check condition
		AllGrades = AllGrades + grades		# process grade
		grade = int(input("enter grade or q to quit: "))	# ask again

# While loop has ended (no indents after here),
# now you can do other stuff…
print("Total grades is:", AllGrades)
print("You're all done now!")
```
