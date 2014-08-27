# Exercise

## 1.1-1
Give a real-world example that requires sorting or a real-world example that requires computing a convex hull.
> Solution
- Sorting the marks of exams; 
- The application of computing convex hull in game.

## 1.1-2
Other than speed, what other measures of efficiency might one use in a real-world setting?
> Solution
- Data structure
- Space complexity
- Convenience
- Safety
- Maintenance...

## 1.1-3
Select a data structure that you have seen previously, and discuss its strengths and limitations.
> Solution
- List
- [单向链表中prev指针的妙用](https://chrome.google.com/webstore/detail/%E9%A9%AC%E5%85%8B%E9%A3%9E%E8%B1%A1/kidnkfckhbdkfgbicccmdggmpgogehop/)

## 1.1-4
How are the shortest-path and traveling-salesman problems given above similar? How are they different?
> Solution
- Similarity: To find a lowest overall way.
- Difference: The outset and destination are determined, but the way through delivery are uncertain.

## 1.1-5
Come up with a real-world problem in which only the best solution will do. Then come up with one in which a solution that is “approximately” the best is good enough.
> Solution
- Speech Recognition
- GPS


## 1.2-1
Give an example of an application that requires algorithmic content at the application level, and discuss the function of algorithms involved.
> Solution
- Finding the lowest overall distant, and the application of GPS(global positioning system).

## 1.2-2
Suppose we are comparing implementations of insertion sort and merge sort on the same machine. For      inputs of size n,insertion sort runs in ![image of 8n^2](http://latex.codecogs.com/gif.latex?8n%5E%7B2%7D) steps, while merge sort runs in ![image of 64nlgn](http://latex.codecogs.com/gif.latex?%5C64%20nlg%20n) steps. For which values of n does insertion sort beat merge sort?
> Solution
- ![image of 8n^2<64nlgn](http://latex.codecogs.com/gif.latex?8n_%7B%20%7D%5E%7B2%7D%20%3C%20%5C64%20n%5Clg%20n)
- ![image of n<8lgn](http://latex.codecogs.com/gif.latex?n%20%3C8%20%5Clg%20n)
- ![image of n<43](http://latex.codecogs.com/gif.latex?%5C%20n%3C%2043)

## 1.2-3
What is the smallest value of n such that an algorithm whose running time is 100n^2 runs faster than an algorithm whose running time is2^n on the same machine?
> Solution
- ![image](http://latex.codecogs.com/gif.latex?100n%5E2%20%3C%202%5En)
- ![image](http://latex.codecogs.com/gif.latex?n_%7Bmin%7D%3D15)

# Problem

## 1.1 Comparism of running times
For each function ![image of f(n)](http://latex.codecogs.com/gif.latex?f%28n%29) and time ![image of t](http://latex.codecogs.com/gif.latex?t) in the following table, determine the largest size ![image of n](http://latex.codecogs.com/gif.latex?n) of a problem that can be solved in time ![image of t](http://latex.codecogs.com/gif.latex?t), assuming that the algorithm to solve the problem takes ![image of f(n)](http://latex.codecogs.com/gif.latex?f%28n%29) microseconds.

      | 1 second| 1 minute   | 1 hour | 1 day | 1 month| 1 year| 1 century 
 ----|------------ | -------------|----------|--------|-----------|---------|-------------
![image of lgn](http://latex.codecogs.com/gif.latex?%5Clg%20n) | ![image of 2^10^6](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B10_%7B%20%7D%5E%7B6%7D%7D) | ![image of 2^(6*10^7)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B6%5Ctimes10_%7B%20%7D%5E%7B7%7D%7D) | ![image of 2^(3.6*10^9)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B3.6%5Ctimes10_%7B%20%7D%5E%7B9%7D%7D) | ![image of 2^(9.24*10^10)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B9.24%5Ctimes10_%7B%20%7D%5E%7B10%7D%7D) | ![image of 2^(2.59*10^12)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B2.59%5Ctimes10_%7B%20%7D%5E%7B12%7D%7D) | ![image of 2^(3.37*10^13)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B3.37%5Ctimes10_%7B%20%7D%5E%7B13%7D%7D) | ![image of 2^(3.11*10^15)](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7B3.11%5Ctimes10_%7B%20%7D%5E%7B15%7D%7D)
![image of sqrt](http://latex.codecogs.com/gif.latex?%5Csqrt%5B%5D%7Bn%7D) | ![image of 10^12](http://latex.codecogs.com/gif.latex?10_%7B%20%7D%5E%7B12%7D) | ![image of 3.6*10^15](http://latex.codecogs.com/gif.latex?3.6%5Ctimes10_%7B%20%7D%5E%7B15%7D) | ![image of 1.30*10^19](http://latex.codecogs.com/gif.latex?1.30%5Ctimes10_%7B%20%7D%5E%7B19%7D) | ![image of 8.54*10^21](http://latex.codecogs.com/gif.latex?8.54%5Ctimes10_%7B%20%7D%5E%7B21%7D) | ![image of 6.72*10^24](http://latex.codecogs.com/gif.latex?6.72%5Ctimes10_%7B%20%7D%5E%7B24%7D) | ![image of 1.14*10^27](http://latex.codecogs.com/gif.latex?1.14%5Ctimes10_%7B%20%7D%5E%7B27%7D) | ![image of 9.67*10^30](http://latex.codecogs.com/gif.latex?9.67%5Ctimes10_%7B%20%7D%5E%7B30%7D)
![image of n](http://latex.codecogs.com/gif.latex?n) | ![image of 10^6](http://latex.codecogs.com/gif.latex?10_%7B%20%7D%5E%7B6%7D) | ![image of 6*10^7](http://latex.codecogs.com/gif.latex?6%5Ctimes10_%7B%20%7D%5E%7B7%7D) | ![image of 3.6*10^9](http://latex.codecogs.com/gif.latex?3.6%5Ctimes10_%7B%20%7D%5E%7B9%7D) | ![image of 9.24*10^10](http://latex.codecogs.com/gif.latex?9.24%5Ctimes10_%7B%20%7D%5E%7B10%7D) | ![image of 2.59*10^12](http://latex.codecogs.com/gif.latex?2.59%5Ctimes10_%7B%20%7D%5E%7B12%7D) | ![image of 3.37*10^13](http://latex.codecogs.com/gif.latex?3.37%5Ctimes10_%7B%20%7D%5E%7B13%7D) | ![image of 3.11*1015](http://latex.codecogs.com/gif.latex?3.11%5Ctimes10_%7B%20%7D%5E%7B15%7D)
![image of nlgn](http://latex.codecogs.com/gif.latex?n%5Clg%20n) | 62746 | 2801400 | ![image of 1.33*10^8](http://latex.codecogs.com/gif.latex?1.33%5Ctimes10_%7B%20%7D%5E%7B8%7D) | ![image of 2.94*10^9](http://latex.codecogs.com/gif.latex?2.94%5Ctimes10_%7B%20%7D%5E%7B9%7D) | ![image of 7.19*10^10](http://latex.codecogs.com/gif.latex?7.19%5Ctimes10_%7B%20%7D%5E%7B10%7D) | ![image of 8.51*10^11](http://latex.codecogs.com/gif.latex?8.51%5Ctimes10_%7B%20%7D%5E%7B11%7D) | ![image of 6.77*10^13](http://latex.codecogs.com/gif.latex?6.77%5Ctimes10_%7B%20%7D%5E%7B13%7D)
![image of n^2](http://latex.codecogs.com/gif.latex?n_%7B%20%7D%5E%7B2%7D) | ![image of 10^3](http://latex.codecogs.com/gif.latex?10_%7B%20%7D%5E%7B3%7D) | ![image of 7.75*10^3](http://latex.codecogs.com/gif.latex?7.75%5Ctimes10_%7B%20%7D%5E%7B3%7D) | ![image of 6*10^4](http://latex.codecogs.com/gif.latex?6%5Ctimes10_%7B%20%7D%5E%7B4%7D) | ![image of 3.04*10^5](http://latex.codecogs.com/gif.latex?3.04%5Ctimes10_%7B%20%7D%5E%7B5%7D) | ![image of 1.61*10^6](http://latex.codecogs.com/gif.latex?1.61%5Ctimes10_%7B%20%7D%5E%7B6%7D) | ![image of 5.81*10^6](http://latex.codecogs.com/gif.latex?5.81%5Ctimes10_%7B%20%7D%5E%7B6%7D) | ![image of 5.58*10^7](http://latex.codecogs.com/gif.latex?5.58%5Ctimes10_%7B%20%7D%5E%7B7%7D)
![image of n^3](http://latex.codecogs.com/gif.latex?n_%7B%20%7D%5E%7B3%7D) | ![image of 10^2](http://latex.codecogs.com/gif.latex?10_%7B%20%7D%5E%7B2%7D) | 391.4868 | ![image of 1.53*10^3](http://latex.codecogs.com/gif.latex?1.53%5Ctimes10_%7B%20%7D%5E%7B3%7D) | ![image of 4.52*10^3](http://latex.codecogs.com/gif.latex?4.52%5Ctimes10_%7B%20%7D%5E%7B3%7D) | ![image of 1.37*10^4](http://latex.codecogs.com/gif.latex?1.37%5Ctimes10_%7B%20%7D%5E%7B4%7D) | ![image of 3.23*10^4](http://latex.codecogs.com/gif.latex?3.23%5Ctimes10_%7B%20%7D%5E%7B4%7D) | ![image of 1.46*10^5](http://latex.codecogs.com/gif.latex?1.46%5Ctimes10_%7B%20%7D%5E%7B5%7D)
![image of 2^n](http://latex.codecogs.com/gif.latex?2_%7B%20%7D%5E%7Bn%7D) | 19 | 26 | 31 | 36 | 41 | 44 | 51
![image of n!](http://latex.codecogs.com/gif.latex?n%21) | 9 | 10 | 12 | 14 | 15 | 16 | 17


Above all, ![image of lgn](http://latex.codecogs.com/gif.latex?%5Clg%20n) stands for ![image of log_{2}n](http://latex.codecogs.com/gif.latex?%5Clog%20_%7B2%7Dn).
