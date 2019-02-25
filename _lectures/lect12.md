---
num: "lect12"
lecture_date: 2019-02-20
desc: "More File I/O, Random Number Generators"
ready: true
pdfurl: /lectures/pdf/lect12.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

The text file, rainfall.txt, that was used as a read (input) file in this lesson can be copied from <a href="http://cs.ucsb.edu/~zmatni/cs8w19/rainfall.txt">THIS SITE.</a>

```python
###############################
infile = open("ThatInput.txt", "r")

lines = infile.readlines()

for line in lines:
    if "Once" in line:
        line = line.replace("Once", "At one point in time")
    print(line)
    
infile.close()

###############################
# Rainfall Example
# (c) 2017 by Ziad Matni for CS8

inputFile = open("rainfall.txt","r")
outputFile = open("report.txt", "w")

outputFile.write("Here's the rainfall report from around the nation!\n")
outputFile.write("--------------------------------------------------\n")

allLines = inputFile.readlines()

for line in allLines:    
	values = line.split()    
	outputFile.write(values[0]+" had "+values[1]+" inches of rain.\n")

inputFile.close()
outputFile.close()

###############################
# Rainfall Example
# WITH accumulated sum and average calculations
# (c) 2017 by Ziad Matni for CS8

inputFile = open("rainfall.txt","r")
outputFile = open("report.txt", "w")

outputFile.write("Here's the rainfall report from around the nation!\n")
outputFile.write("--------------------------------------------------\n")

allLines = inputFile.readlines()
count = 0
sum = 0

for line in allLines:    
	values = line.split()    
	outputFile.write(values[0]+" had "+values[1]+" inches of rain.\n")
	count += 1
	sum += float(values[1])

average = sum/count
print("The average rainfall is: ", average)
outputFile.write("The average rainfall is: " + str(average))

inputFile.close()
outputFile.close()

###############################
import random

for i in range(25):
    print(random.random())      # Generates a random no. between 0 and 1 (float)
    print(random.randrange(10)  # Generates a random no. between 0 and 10 (int)
    print(random.randint(1,6))  # Generates a random no. between 1 and 6 (int)
```
