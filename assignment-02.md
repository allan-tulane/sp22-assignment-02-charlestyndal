# CMPS 2200 Assignment 2

**Name:** Charles Tyndal

In this assignment we'll work on applying the methods we've learned to analyze recurrences, and also see their behavior
in practice. As with previous
assignments, some of of your answers will go in `main.py`.. You
should feel free to edit this file with your answers; for handwritten
work please scan your work and submit a PDF titled `assignment-02.pdf`
and push to your github repository.


1. Derive asymptotic upper bounds of work for each recurrence below.
  * $W(n)=2W(n/3)+1$
    * log_b a = log_3 2 == .6209
    * k == 0
    * since log_b a > k ->
    * O(n) = O(n^log_3 2)
.  
.  
.  
  * $W(n)=5W(n/4)+n$
    * log_b a = log_4 5 = 1.16
    * k = 1
    * since log_b a < k ->
    * O(n) = O(n^1.16)
.  
.  
.  
.  
  * $W(n)=7W(n/7)+n$
    * log_b a = log_7 7 = 1
    * k = 1
    * p = 0
    * O(n) = O(n*logn)
.  
.  
.  
.  
  * $W(n)=9W(n/3)+n^2$
    * log_b a = 2
    * k = 2
    * p = 0
    * since log_b a = k ->
    * O(n) = O(n*logn)
.  
.  
.  
.  
  * $W(n)=8W(n/2)+n^3$
    * log_b a = 3
    * k = 3
    * since log_b a = k ->
    * O(n) = O(n^2 * logn)
.  
.  
.  
.  
.  
  * $W(n)=49W(n/25)+n^{3/2}\log n$
    * log_25 49 = 1.209...
    * k = 3/2 = 1.5
    * since log_b a < k -->
    * O(n) = O(n^3/2 * logn)
.  
.  
.  
.  
.  
  * $W(n)=W(n-1)+2$
    * work + constant --> O(n)
.  
.  
.  
.  
  * $W(n)= W(n-1)+n^c$, with $c\geq 1$
    * W(n-1) = W(n-2) + (n-1)^c
    * W(n) = 1^c + 2^c + 3^c = n^(c+1)
    * O(n^c)
.  
.  
.  
.  
  * $W(n)=W(\sqrt{n})+1$
    * W(n) = W(sqrt{n} + 1) = W(n^1/2)
    * O(log_2(n))

2. Suppose that for a given task you are choosing between the following three algorithms:

  * Algorithm $\mathcal{A}$ solves problems by dividing them into
      five subproblems of half the size, recursively solving each
      subproblem, and then combining the solutions in linear time.
    
  * Algorithm $\mathcal{B}$ solves problems of size $n$ by
      recursively solving two subproblems of size $n-1$ and then
      combining the solutions in constant time.
    
  * Algorithm $\mathcal{C}$ solves problems of size $n$ by dividing
      them into nine subproblems of size $n/3$, recursively solving
      each subproblem, and then combining the solutions in $O(n^2)$
      time.

    What are the asymptotic running times of each of these algorithms?
    Which algorithm would you choose?
      I would choose algorithm 3 as its big O would be O(n^2) which is the lowest value given the information since the first would be O(n^2.3...) and the second algorithm would be O(c^n)


3. Now that you have some practice solving recurrences, let's work on
  implementing some algorithms. In lecture we discussed a divide and
  conquer algorithm for integer multiplication. This algorithm takes
  as input two $n$-bit strings $x = \langle x_L, x_R\rangle$ and
  $y=\langle y_L, y_R\rangle$ and computes the product $xy$ by using
  the fact that $xy = 2^{n/2}x_Ly_L + 2^{n/2}(x_Ly_R+x_Ry_L) +
  x_Ry_R.$ Use the
  stub functions in `main.py` to implement Karatsaba-Ofman algorithm algorithm for integer
  multiplication: a divide and conquer algorithm that runs in
  subquadratic time. Then test the empirical running times across a
  variety of inputs to test whether your code scales in the manner
  described by the asymptotic runtime. Please refer to Recitation 3 for some basic implementations, and Eqs (7) and (8) in the slides https://github.com/allan-tulane/cmps2200-slides/blob/main/module-02-recurrences/recurrences-integer-multiplication.ipynb
 
 


