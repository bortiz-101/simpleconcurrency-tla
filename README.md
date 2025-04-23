# TLA+ Simple Concurrency Example

[![Syntax-check models](https://github.com/lucformalmethodscourse/simpleconcurrency-tla/actions/workflows/main.yml/badge.svg)](https://github.com/lucformalmethodscourse/simpleconcurrency-tla/actions/workflows/main.yml)

This example models a very basic system where N threads concurrently attempt to increment a shared variable.

## References

- Section 3 in the instructor's [book chapter on concurrency](https://arxiv.org/abs/1705.02899)
- Sections 6.1-6.3 in the [programming languages lecture notes](https://lucproglangcourse.github.io/concurrency.html)
- [Excercises 23 and 24](homes.cs.aau.dk/~kgl/esv04/exercises/#Exercise_23) from the Aarhus systems validation course

### **Initial Formula**

Shared = K

### **Findings**

| **K/N->** | **1**|   **2**  | **3** |  **4**  |
|-----------|------|----------|-------|---------|
| **1**     |   1  |     2    |   3   |    4    |
| **2**     |   1  |     2    |   2   |    2    |
| **3**     |   1  |     2    |   2   |    2    |
| **4**     |   1  |     2    |   2   |    2    |

### **Revised Formula**

$$
f(shared) = \begin{cases} N & \text{if } K = 1\\
                          shared <= 2 & \text{ if } K > 1
\end{cases}\
$$
### **Discussion**

- Our initial assumptions prior to experimentation was that the minimal value of shared could not be lower than the value of N
- Quickly during experimentation we found that the value of shared could go lower N and often did for most values of K
- During the experimentation process of this assignment we found that in order to complete the computation in timely manner for large K and N values it was necessary to run the TLC with the following flags "-coverage 1 -deadlock -workers auto" due to the size of the state space
