# Python-Programming-Week-10
1.

Merge Sort

Write a Python program to sort a list of elements using the merge sort algorithm.



CODE:

b=int(input())



a=input().split(" ")

a .sort()

for i in range(b):

 print(int(a[i]),end=" ")

2.Bubble Sort

Given an listof integers, sort the array in ascending order using the Bubble Sort algorithm above. Once sorted, print the following three lines:

1.      List is sorted in numSwaps swaps., where numSwaps is the number of swaps that took place.

2.      First Element: firstElement, the  first element in the sorted list.

3.      Last Element: lastElement, the last element in the sorted list.

For example, given a worst-case but small array to sort: a=[6,4,1]. It took  3 swaps to sort the array. Output would be

Array is sorted in 3 swaps.  

First Element: 1  

Last Element: 6   



CODE:



def bubble_sort(arr):

    n = len(arr)

    num_swaps = 0

    for i in range(n):

        for j in range(0, n - i - 1):

            if arr[j] > arr[j + 1]:

                arr[j], arr[j + 1] = arr[j + 1], arr[j]

                num_swaps += 1

    

    print("List is sorted in {} swaps.".format(num_swaps))

    print("First Element:", arr[0])

    print("Last Element:", arr[-1])



def main():

    n = int(input())

    arr = list(map(int, input().split()))

    bubble_sort(arr)



main()

#3.

Peak Element

Given an list, find peak element in it. A peak element is an element that is greater than its neighbors.

An element a[i] is a peak element if

A[i-1] <= A[i] >=a[i+1] for middle elements. [0<i<n-1]

A[i-1] <= A[i] for last element [i=n-1]

A[i]>=A[i+1] for first element [i=0]



CODE:

def find_peak(arr):

    peak_elements = []

    n = len(arr)

    

    if n == 1:

        return arr[0]



    if arr[0] >= arr[1]:

        peak_elements.append(arr[0])



    for i in range(1, n - 1):

        if arr[i - 1] <= arr[i] and arr[i] >= arr[i + 1]:

            peak_elements.append(arr[i])



    if arr[n - 1] >= arr[n - 2]:

        peak_elements.append(arr[n - 1])



    return peak_elements



n = int(input())

arr = list(map(int, input().split()))

peaks = find_peak(arr)

print(*peaks)

#4.Frequency of Elements

To find the frequency of numbers in a list and display in sorted order.

Constraints: 

1<=n, arr[i]<=100 

CODE:

a=input().split()

a.sort()

l=[]

b=[]

for i in range(len(a)):

 b .append(int(a[i]))

b.sort()

#print(b)

for i in range(len(b)):

 count=0

 for j in range(len(b)):

  if int(b[i]) not in l:

   if int(b[i])==int(b[j]):

    count+=1

 l.append(int(b[i]))

 if count!=0:

  print(int(b[i]),count)

 #5.Binary Search

Write a Python program for binary search.




def binary_search(arr, target):

    left, right = 0, len(arr) - 1

    while left <= right:

        mid = (left + right) // 2

        if arr[mid] == target:

            return True

        elif arr[mid] < target:

            left = mid + 1

        else:

            right = mid - 1

    return False



arr = list(map(int, input().split()))

target = int(input())



result = binary_search(arr, target)

print(result)







