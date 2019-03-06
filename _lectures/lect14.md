---
num: "lect14"
lecture_date: 2019-03-06
desc: "Character Encoding"
ready: true
pdfurl: /lectures/pdf/lect14.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
def addChars1(char1, char2):
    numAddASCII = ord(char1) +  ord(char2) - 2*ord('0')
    return numAddASCII

print(addChars1('5', '2'))
print(type(addChars1('5', '2')))

###############################
def addChars2(char1, char2):
    numAddASCII = ord(char1) +  ord(char2) - 2*ord('0')
    charNum = chr(numAddASCII + ord('0'))
    return charNum

print(addChars2('5', '2'))
print(type(addChars2('5', '2')))

###############################
def MyCipher(myStr):
    enc_str = ''
    for c in myStr:
        enc_str += chr(ord(c) + 1)
    return enc_str

print(MyCipher('hello'))

def ReverseMyCipher(myStr):
    dec_str = ''
    for c in myStr:
        dec_str += chr(ord(c) - 1)
    return dec_str

print(ReverseMyCipher('ifmmp'))

###############################
def MirrorEncrypt(message): # message is a string type
    result = ''         # start with an empty result
    for c in message:   # go thru every letter in message
                        # let’s apply the “mirror” formula:
        nc = ord(c)
        nr = ord('a') + ord('z') - nc
                        # then accumulate the encoded chars, one at a time
        result = result + chr(nr)
    return result

print(MirrorEncrypt("bye"))
print(MirrorEncrypt("maria"))
print(MirrorEncrypt("abcdefghi"))
print(MirrorEncrypt("zyxwvutsr"))
```
