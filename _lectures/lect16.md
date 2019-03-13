---
num: "lect16"
lecture_date: 2019-03-11
desc: "Recursive Functions and Final Exam Review"
ready: true
pdfurl: /lectures/pdf/lect16.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
############################################
# Linear Series using Recursion
#
def series(n):
    if n <= 0:
        return 0
    return (3*series(n-1) + 1)

print(series(5))

"""
############################################
# Reversing a String using Recursion
#
def revStr(s):
    if len(s) == 0:
        return s
    return revStr(s[1:]) + s[0]

print(revStr("I love UCSB!"))
```
