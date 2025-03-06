---
title: Why is C Faster Than Python? OS-Level Perspective
summary: A comparison between C and Python language in the context of Operating System level.
date: 2025-03-05
type: docs
math: false
tags:
  - Python
  - C
  - Operating System
  - Programming Language
image:
  caption: 'Why is C Faster Than Python?'
---

So, we know that Python is one of the most widely used programming languages today. It powers data science, automation, web development, and machine learning. However, when it comes to raw performance, Python is often criticized for being slow compared to lower-level languages like C.

But why exactly is Python slower? Is it just because it’s an interpreted language, or perhaps there are deeper system-level reasons? In this article, I’ll try to elaborate my best to explore how execution models, memory management, system calls, and CPU efficiency impact the performance of Python and C.

## Video

Watch a fully explanation here.

{{< youtube bIzWk98DHGE >}}

## Detailed Explanation on My Medium!

Read full detailed explanation here! [Click Here!](https://medium.com/@raihansltn/why-is-c-faster-than-python-os-level-perspective-04d6e485e3ae)

## Benchmarking C vs Python - How Slow is Python?

So, I made a roughly same program for both languages. A simple benchmark test. We’ll count prime numbers up to 250.000 in both C and Python.

Specifically, they:
1. Check wether a number is prime using a function
2. Count the number of prime numbers up to 250.000 using a loop
3. Print the total count of prime numbers found within that range

C program — prime.c

    ```C
    #include <stdio.h>

    int isPrime(int n) {
        if (n < 2) return 0; 
        if (n == 2) return 1; 
        if (n % 2 == 0) return 0; 

        for (int i = 3; i * i <= n; i += 2) {
            if (n % i == 0) {
                return 0;
            }
        }
        return 1;
    }

    int main() {
        int numPrimes = 0;
        
        for (int i = 2; i <= 250000; i++) {
            numPrimes += isPrime(i);
        }

        printf("Number of primes up to 250000: %d\n", numPrimes);
        return 0;
    }
    ```

Python program — prime.py

```python
    def is_prime(n):
        if n < 2:
            return 0
        if n == 2:
            return 1
        if n % 2 == 0:
            return 0
        
        for i in range(3, int(n**0.5) + 1, 2):
            if n % i == 0:
                return 0
        return 1

    def main():
        num_primes = sum(is_prime(i) for i in range(2, 250001))
        print("Number of primes up to 250000:", num_primes)

    if __name__ == "__main__":
        main()
```

## Execution Time Comparison

C Result:

```bash
$ time ./prime #it is C
real    0m0.012s
Python Result:

$ time python3 prime.py #it is Python
real    0m0.261s
```

As we can see on the results, the C program finished in just 0.012 seconds, while Python took 0.261 seconds, that is more than 20 times slower! But why does this happen tho?

Read full detailed explanation here! [Click Here!](https://medium.com/@raihansltn/why-is-c-faster-than-python-os-level-perspective-04d6e485e3ae)
Or watch my presentation about it here! [Click Here to Watch!](https://www.youtube.com/watch?v=bIzWk98DHGE&t=629s&ab_channel=RaihanSultan)