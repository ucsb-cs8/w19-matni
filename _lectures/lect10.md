---
num: "lect10"
lecture_date: 2019-02-11
desc: "String Formats"
ready: true
pdfurl: /lectures/pdf/lect10.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
################################################
# Note that there's more than one way to solve this problem!
#
def countWords(sentence):
	""" returns the number of words in the string sentence """
	sum = 0    
	for count in range(len(sentence)):        
		if (sentence[count] == " ") or (count == len(sentence) – 1):
            sum += 1    
	return sum

################################################
def createListOfOdd(lst):
	""" returns a new list that contains all """ 
	""" the odd numbers in lst """
	newList = []
	for item in lst:        
		if item % 2 != 0:            
			newList.append(item)        
	return newList

################################################
s = "How I wish you were here.nWe're just two lost souls swimming in a fishbowl,\nYear after year"

s = """How I wish you were here.
We’re just two lost souls swimming in a fishbowl,
Year after year"""

################################################
s = "What about Bob?"
l = s.split()
print(l)

l = s.split('a')
print(l)

################################################
def countWords(sentence):
	""" returns the number of words in the string sentence """
	sum = 0    
	MyNiceList = sentence.split()
	for item in MyNiceList:
		sum += 1
	return sum
# SOOOO much easier!!!

def countWords(sentence):
	""" returns the number of words in the string sentence """
	MyNiceList = sentence.split()
	return len(MyNiceList)
# EVEN EASIER!!!!!!

################################################
print(42)		# prints 42 and then a newline (wow)
print(42, "!")		# prints '42 !' and then a newline (note the space)
print(42, end="")	# prints 42 WITHOUT a newline character
print(42, end="!")	# prints 42! WITHOUT a newline character (note NO space!)

################################################
hour = 12
minute = 55
second = 31

print('{0}:{1}:{2}'.format(hour, minute, second)

################################################
a = 19 
b = 42
print('{0:3}***{1:5}'.format(a, b))

################################################
a = "Be"
b = "Mine!"
print('{:7}{:7}'.format(a, b))

################################################
print('{:7.2}'.format(100/3))

print('{:10.1e}'.format(100/3))
```
