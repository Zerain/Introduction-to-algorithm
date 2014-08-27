# Exercise
## 2.1-1
Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on the array A = {31, 41, 59, 26, 41, 58}.
> Solution
```
  31,41,59,26,41,58
  31,41,59,26,41,58
  31,41,59,26,41,58
  26,31,41,59,41,58
  26,31,41,41,59,58
  26,31,41,41,58.59
  
## 2.1-2
Rewrite the INSERTION-SORT procedure to sort into nonincreasing instead of nondecreasing order.
> Solution
```
  INSERTION-SORT(A)
  for j = 2 to A.length
      key = A[j]
      //Insert A[j] into the sorted sequence A[1..j-1]
      i = j - 1
      while i > 0 and A[i] < key
        A[i+1] = A [i]
        i = i - 1
      A[i+1] = key

## 2.1-3
Consider the searching problem:
Input: A sequence of numbers A<a1;a2;...;an>and a value.
Output:An index i such that v = A[i] or the special value NIL if v does not appear in A.
Write pseudocode for linear search, which scans through the sequence, looking
for. Using a loop invariant, prove that your algorithm is correct. Make sure that
your loop invariant fulfills the three necessary properties.
> Solution
```  
  for i = 1 to n
    if A[i] == v
      return i
  return NIL

## 2.1-4
Consider the problem of adding two n-bit binary integers, stored in two n-element
arrays A and B. The sum of the two integers should be stored in binary form in
an (n+1)-element array C. State the problem formally and write pseudocode for
adding the two integers.
> Solition
```
  BINARY-ADD(A,B,C)
  flag = 0
  for j = 1 to n
  key = A[j] + A[j] + flag
  C[j] = key mod 2
  if key > 1
    flag = 1
  if flag = 1
    C[n+1] = 1

## 2.2-1
Express the function ![image of n^3/1000 - 100n^2 - 100n + 3](http://latex.codecogs.com/gif.latex?n_%7B%20%7D%5E%7B3%7D/1000-100n_%7B%20%7D%5E%7B2%7D-100n&plus;3) in terms of Θ-notation.
> Solution
- ![image of theta^3](http://latex.codecogs.com/gif.latex?n_%7B%20%7D%5E%7B3%7D/1000-100n_%7B%20%7D%5E%7B2%7D-100n&plus;3%3D%5CTheta%20%28n_%7B%20%7D%5E%7B3%7D%29)
  
## 2.2-2
Consider sorting n numbers stored in array A by first finding the smallest element of A and exchanging it with the element inA(1). Then find the second smallest element of A, and exchange it withA(2). Continue in this manner for the first n-1 elements of A. Write pseudocode for this algorithm, which is known as selection sort. What loop invariant does this algorithm maintain? Why does it need to run for only the first n-1 elements, rather than for allnelements? Give the best-case and worst-case running times of selection sort in Θ-notation.
> Solution
```
Assume that FIND-MIN(A,r,s) returns the index of the smallest element in A between indices r and s. 
Clearly, this can be implemented in O(s-r) time if r>=s.
SELECTION-SORT
Input: A = <a1,a2,...,an>
Output: sorted A.
for i = 1 to n-1
  j = FIND-MIN(A,i,n)
  temp = A[i]
  A[i] = A[j]
  A[j] = temp
As a loop invarient we choose that A(1,...,i-1) are sorted and all other elements are greater than these. 
We only need to iterate to n-1 since according to the invarient the nth element will then the largest.
Then n calls of FIND-MIN gives the following bound on the time complexity(This hold for both the best-and-worst-case running time).
  
![image of formula](http://latex.codecogs.com/gif.latex?%5CTheta%20%28%5Csum_%7Bi%3D1%7D%5E%7Bn%7Di%29%3D%5CTheta%20%28n_%7B%20%7D%5E%7B2%7D%29)

