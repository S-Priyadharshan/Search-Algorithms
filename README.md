# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
"""
Description: Program to search an item in a list one by one fron start to end 
Developed By: Priyadharshan S
Reference No.: 212223240127
"""


def search(array,key,n):
    for i in range(0,n):
        if(key == array[i]):
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
"""
Description: Program to find an element in a list with the use of Binary search algorithm
Developed By: Priyadharshan S
Reference No.: 212223240127
"""
def BinarySearch(array,key,n):
    left=0
    right=n-1
    while left<=right:
        mid=(left+right)//2
        if(key==array[mid]):
            return mid
        elif array[mid] < key:
            left=mid+1
        else:
            right=mid-1
    return -1
array=eval(input())
key=int(input())
n=len(array)
array.sort()
result=BinarySearch(array,key,n)
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
"""
Description: Program to find element in a list recursively using Binary Search algorithm (recursive Method)
Developed By: Priyadharshan S
Reference No.: 212223240127
"""
def BinarySearch(array,left,right,key,n):
    if left>right:
        return -1;
    mid=(right+left)//2
    if array[mid]==key:
        return mid
    elif array[mid]>key:
        return BinarySearch(array,left,mid-1,key,n)
    else:
        return BinarySearch(array,mid+1,right,key,n)
array=eval(input())
key=int(input())
n=len(array)
array.sort()
result=BinarySearch(array,0,n-1,key,n)
print(array)
if(result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)

```
## Sample Input and Output

![image](https://github.com/S-Priyadharshan/Search-Algorithms/assets/145854138/cdd79aab-27ce-4f07-b36b-c1a62d7b418b)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
