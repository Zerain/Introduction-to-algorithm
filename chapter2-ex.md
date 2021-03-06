# Exercise
## 2.1-1
Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on the array A = `<31, 41, 59, 26, 41, 58>`.
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
SELECTION-SORT
Input: A = <a1,a2,...,an>
Output: sorted A.
for i = 1 to n-1
  j = FIND-MIN(A,i,n)
  temp = A[i]
  A[i] = A[j]
  A[j] = temp
  
- Assume that FIND-MIN(A,r,s) returns the index of the smallest element in A between indices r and s. Clearly, this can be implemented in O(s-r) time if r>=s.

- As a loop invarient we choose that A(1,...,i-1) are sorted and all other elements are greater than these. We only need to iterate to n-1 since according to the invarient the nth element will then the largest.Then n calls of FIND-MIN gives the following bound on the time complexity:
  
- The best-case and worst-case runnning times are both ![image of formula](http://latex.codecogs.com/gif.latex?%5CTheta%20%28%5Csum_%7Bi%3D1%7D%5E%7Bn%7Di%29%3D%5CTheta%20%28n_%7B%20%7D%5E%7B2%7D%29)

- This hold for both the best-and-worst-case running time.

## 2.2-3
Consider linear search again (see Exercise 2.1-3). How many elements of the in put sequence need to be checked on the average, assuming that the element being searched for is equally likely to be any element in the array? How about in the worst case? What are the average-case and worst-case running times of linear search in Θ-notation? Justify your answers.
> Solution
- Given that each element is equally likely to be the one searched for and the element searched for is present in the array, a linear search will on the average have to search through half the elements. The is because half the search time the wanted element will be in the first half and half the time it will be in the second half. Both the worst-case and average-case of LINEAR-SEARCH is Θ(n).

## 2.2-4
How can we modify almost any algorithm to have a good best-case running time?
> Solution
- Modify the algorithm so it tests whether the input satisfies some special-case condition and, if it does, output a pre-computed answer. The best-case running time is generally not a good measure of an algorithm.

## 2.3-1
Using Figure 2.4 as a model, illustrate the operation of merge sort on the array A = `<3,41,52,26,38,57,9,49>`.
> Solution
```
                  3,9,26,38,41,49,52,57
          3,26,41,52                9,38,49,57
        3,41      26,52           9,49      38,57
      3     41    52    26      38    57    9     49
      
## 2.3-2
Rewrite the MERGE procedure so that it does not use sentinels, instead stopping once either array L or R has had all its elements copied back to A and then copying the remainder of the other array back into A.
> Solution
```
Merge(A[], p, q, r)
    m = q - p + 1
    n = r - q
    L[1..m] = A[p..q]
    R[1..n] = A[q+1..r]
    // Copy into two array.
    i = j = 1
    for k = p to r
        if i == m + 1   // L用完了，拷贝R
            A[k..r] = R[j..n]
            break
        if j == n + 1   // R用完了，拷贝L
            A[k..r] = L[i..m]
            break
        if L[i] <= R[j]
            A[k] = L[i]
            i++
        else
            A[k] = R[j]
            j++

## 2.3-3
Use mathematical induction to show that when n is an exact power of 2,the solution of the recurrence
![image of T(n)](http://latex.codecogs.com/gif.latex?T%28n%29%3D%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%202%20%26%20%26%20%26%20if%20%5C%20n%20%3D%202%5C%5C%202T%28n/2%29&plus;n%20%26%20%26%20%26if%20%5C%20n%3D2_%7B%20%7D%5E%7Bk%7D%2Cfor%20%5C%20k%3E1%20%5Cend%7Bmatrix%7D%5Cright.)

is
![image of T(n)=nlgn](http://latex.codecogs.com/gif.latex?T%28n%29%3Dn%5Clg%20n)
> Solution
- Basic case
 - for n = 2, T(2) = 2lg2 = 2, condition holds.
- Assumed case
 - for n = ![imgae of 2^t](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7Bt%7D), ![image of T(2^T) = 2^t*lg(2t)](http://latex.codecogs.com/gif.latex?T%282_%7B%20%7D%5E%7Bt%7D%29%20%3D%202_%7B%20%7D%5E%7Bt%7D%5Clg2_%7B%20%7D%5E%7Bt%7D) is satisfied.
- Then when ![image of n=2^(t+1)](http://latex.codecogs.com/gif.latex?n%20%3D%202_%7B%20%7D%5E%7Bt&plus;1%7D), 
 - ![image of T(2^(t+1))=2T(2^(t+1)/2+2^(t+1)](http://latex.codecogs.com/gif.latex?T%282_%7B%20%7D%5E%7Bt&plus;1%7D%29%3D2T%282_%7B%20%7D%5E%7Bt&plus;1%7D/2%29&plus;2_%7B%20%7D%5E%7Bt&plus;1%7D)
 - ![image of =2T(2^t)+2^(t+!)](http://latex.codecogs.com/gif.latex?%3D2T%282_%7B%20%7D%5E%7Bt%7D%29&plus;2_%7B%20%7D%5E%7Bt&plus;1%7D)
 - ![image of =2(2^tlg(2t))+2^(t+1)](http://latex.codecogs.com/gif.latex?%3D2%282_%7B%20%7D%5E%7Bt%7D%5Clg2t%29&plus;2_%7B%20%7D%5E%7Bt&plus;1%7D)
 - ![image of =2^(t+1)lg(2^(t+1))](http://latex.codecogs.com/gif.latex?%3D%202_%7B%20%7D%5E%7Bt&plus;1%7D%5Clg2_%7B%20%7D%5E%7Bt&plus;1%7D)
