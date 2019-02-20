---
num: "lect11"
lecture_date: 2019-02-20
desc: "String Formats and File I/O"
ready: true
pdfurl: /lectures/pdf/lect11.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

The text file, itsybitsy.txt, that was used in this lesson can be copied from <a href="http://cs.ucsb.edu/~zmatni/cs8w19/itsybitsy.txt">THIS SITE.</a>

```python
###############################
print(42, end="")
print(43)
print(44)

hour = 12
minute = 55
second = 31

print('{1} hrs {0} min {2} sec'.format(hour, minute,second))
print('{} hrs {} min {} sec'.format(hour, minute,second))

###############################
a = "Hemoglobin"
print('{:7}'.format(a))

###############################
n = 33.33333333
print('{:9.3f}'.format(n))

###############################
outfile = open('Z_Output.txt', 'w')

outfile.write("Hello! This is a new file I just made!\n")

outfile.close()

###############################
infile = open('itsybitsy.txt', 'r')

listOfLines = infile.readlines()

infile.close()

for line in listOfLines:
    print(line, "***")
    
```
