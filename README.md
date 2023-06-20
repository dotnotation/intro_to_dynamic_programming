# intro_to_dynamic_programming
Coursework for Colt Steele's JS Algorithms and Data Structures Masterclass

Dynamic Programming
    - A method for solving a complex problem by breaking it down into a collection of simpler subproblems, solving each of those subproblems just once, and storing their solution
    - by Richard Bellman
    - dynamic meaning to capture the time-varying aspect of the problems
    - both a mathematical optimization method and a computer programming method
    - can only use when there is an optimal substructure and overlapping subproblems
        - ex. Fibonacci sequence

Overlapping subproblems
    - when a problem can be broken down into subproblems which are reused several times
    - think of in the Fibonacci sequence where you are having to add together the two previous numbers but also having to reference the same numbers again which isn't very efficient 
        - to get 3 you have to add 1 and 2 together
        - to get 5 you have to add 3 and 4 together which makes you add 3 + 2 for 4 and 2 + 1 for 3 which required 1 + 2 so you are constantly going backwards to get the current number
    - MergeSort is NOT an overlapping subproblem!
        - it is sorting different data each time, not referencing the same data over and over again as you are dividing it into smaller sections
        - however if the MergeSort is referencing the same numbers over and over again, then it is the edge case that is an overlapping subproblem 
            - it has to be repetitive data that is evenly spaced
            - ex. mergeSort([10, 24, 10, 24])