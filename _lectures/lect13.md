---
num: "lect13"
lecture_date: 2019-03-04
desc: "Dictionaries"
ready: true
pdfurl: /lectures/pdf/lect13.pdf
annotatedpdfurl:
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

```python
#######################################
# Operations on Python lists
#
nums = [2, 5, -5, 4, 0]
names = ['hannah', 'joe', 'sam', 'bert']

# What happens with each of these?
print(min(nums))
print(max(nums))
print(sum(nums))
print(min(names))
print(max(names))
print(sum(names))

nums.sort()
print(nums)

names.sort()
print(names)

nums.reverse()
names.reverse()
prints(names, nums)

nums.remove(-5)
names.remove('sam')
print(names, nums)

nums.count(2)
names.insert(2, 'tabitha')
nums.pop()

#######################################
# Find the median in a list of numbers
#
def median(alist):
    # Make a copy so we won't change "alist" itself (why worry about that?)
    CopyList = alist
    CopyList.sort() 		# guess what this does??

    if len(CopyList)%2 == 0:	# if there is an even no. of things in the list,
        			# then, we should identify the middle 2 numbers
        rightMiddle = len(CopyList)//2	# That’s the *position* of the right-middle no.
	leftMiddle = rightMiddle – 1	# That’s the *position* of the left-middle no.
	median = (CopyList[leftMiddle] + CopyList[rightMiddle])/2

    else:			# if there is an odd no. of things in the list,
				# then, it’s easier: just find the middle number
	index_of_middle = len(CopyList)//2
	median = CopyList[index_of_middle]

    return median

#######################################
# Dictionaries in Python
#
ages = { 'sam':19, 'alice':20 }

print(ages['alice'])

ages['pete'] = 24
print(ages)

del(ages['pete'])
print(ages)

print(ages.keys())
print(ages.values())

ages = { 'sam':19, 'alice':20, 'ben': 22, 'bert': 44 }

for item in ages:
	print(item)

for item in ages.keys():
	print(item)

for item in ages.values():
	print(item)

for item in ages.items():
	print(item)

for item in ages.items():
	print(item[0])


#######################################
# Find the mode in a list of numbers
#
def mode(alist):
    countdict = {} 		    # Start with a blank dictionary
    for item in alist:
        if item in countdict:	    # Is it already in the dictionary?
            countdict[item] += 1    # if so, increment its “value”
  	else:   		    # If it ISN’T in the dictionary…
            countdict[item] = 1	    # Put it in there! Give it “value” = 1

    countlist = countdict.values()  # Make a values list
    maxcount = max(countlist) 	    # Get the biggest value

    modelist = [ ]  		    # make a list of the modes (why a list?)
    for item in countdict:	    # Go thru the dictionary you’ve created
        if countdict[item] == maxcount:	  # If you find the “biggest value”
            modelist.append(item)  # Add the “biggest value” key

    return modelist

```
