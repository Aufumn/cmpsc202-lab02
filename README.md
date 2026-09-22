# Lab 02: Asymptotic Analysis and Algorithm Running Times

Work with your Project 1 team to complete the exercises found in `exercises.pdf`. Put your solutions and explanations below. When you are finished, commit and push your repo.

# Part 1:

## Problem 1.1

T(n)=3n2+15n+100

Dropping multiplicative constants:
3n^2 = O(n^2)
Polynomial degree grows faster:
15n = O(n^2)
A constant grows slower than (n^2):
100 = O(n^2)
Summation Rule: When adding terms, we use the largest-growing term.

T(n)=O(n2)

## Problem 1.2

T(n)=4⋅2n+8n^5

First, drop the constants: 4x2^n=O(2^n) and 8n^5=O(n^5)

The lab tells us that exponential functions grow faster than polynomial functions.

Therefore: n^5=O(2^n)

So both terms are (O(2^n)).

Using the Summation Rule:

4⋅2^n+8n^5=O(2^n)

T(n)=O(2n)

# Part 2:

## Algorithm A
function algoA(n):
    count = 0
    for i = 1 to n:
        print(i)
        for j = 1 to n:
            for k = 1 to n:
                count = count + 1
    return count

## Explanation
There are three loops nested inside each other, and each loop runs \(n\) times.

So:
n×n×n=n^3

## Algorithm B
function algoB(n):
    val = n
    steps = 0
    while val >= 1:
        val = val / 2
        steps = steps + 1
        print("Processing steps: ", steps)

## Explanation

The important idea is that the algorithm cuts the problem in half every time.

That's why it takes logarithmic time rather than linear time. The lab specifically identifies base-2 logarithm as the function describing how many times we can divide (n) by 2 before reaching 1.
        
# Part 3:

## Reflection

1. Which of the Big-O rules feels the least intuitive to your group?

The rule that feels the least intuitive is that exponential functions grow faster than polynomial functions. It is difficult to understand at first because both functions get larger, but (2^n) eventually becomes much larger than something like (n^5).

2. Did you find any part of the exercises particularly challenging? If so, which part and why?

The most challenging part was figuring out the exact number of steps in Algorithm B. It was easier to understand after looking at examples such as 8, 16, and 32 and noticing that the number of steps increases by one each time the starting value doubles.

3. Do you have any feedback about the class?

The examples and step-by-step explanations were helpful. More examples of how to count exact operations in loops would be useful because it makes it easier to understand how the Big-O answer is obtained.
