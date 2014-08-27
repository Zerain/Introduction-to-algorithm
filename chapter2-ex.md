# Exercise
## 2.1-1
Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on the array A = {31, 41, 59, 26, 41, 58}.
> Solution
  31,41,59,26,41,58
  31,41,59,26,41,58
  31,41,59,26,41,58
  26,31,41,59,41,58
  26,31,41,41,59,58
  26,31,41,41,58.59
  
## 2.1-2
Rewrite the INSERTION-SORT procedure to sort into nonincreasing instead of nondecreasing order.
> Solution
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
 Solution
```  
  for i = 1 to n
    if A[i] == v
      return i
    end if
  end for
  return NIL

## 2.1-4
Consider the problem of adding two n-bit binary integers, stored in two n-element
arrays A and B. The sum of the two integers should be stored in binary form in
an (n+1)-element array C. State the problem formally and write pseudocode for
adding the two integers.
