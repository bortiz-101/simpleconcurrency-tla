# TLA+ Simple Concurrency Example

[![Syntax-check models](https://github.com/lucformalmethodscourse/simpleconcurrency-tla/actions/workflows/main.yml/badge.svg)](https://github.com/lucformalmethodscourse/simpleconcurrency-tla/actions/workflows/main.yml)

This example models a very basic system where N threads concurrently attempt to increment a shared variable.

## References

- Section 3 in the instructor's [book chapter on concurrency](https://arxiv.org/abs/1705.02899)
- Sections 6.1-6.3 in the [programming languages lecture notes](https://lucproglangcourse.github.io/concurrency.html)
- [Excercises 23 and 24](homes.cs.aau.dk/~kgl/esv04/exercises/#Exercise_23) from the Aarhus systems validation course

### **Findings**

| **Experiment #** | **K Value**|   **N Value**  | **Result**        |
|------------------|------------|----------------|-------------------|
| **1**            |  1         |    1           |   XXXXX           |
| **2**            |  1         |    2           |   XXXXX           |
| **3**            |  1         |    3           |   XXXXX           |
| **4**            |  1         |    4           |   XXXXX           |
| **5**            |  2         |    1           |   XXXXX           |
| **6**            |  2         |    2           |   XXXXX           |
| **7**            |  2         |    3           |   XXXXX           |
| **8**            |  2         |    4           |   XXXXX           |
| **9**            |  3         |    1           |   XXXXX           |
| **10**           |  3         |    2           |   XXXXX           |
| **11**           |  3         |    3           |   XXXXX           |
| **12**           |  3         |    4           |   XXXXX           |
| **13**           |  4         |    1           |   XXXXX           |
| **14**           |  4         |    2           |   XXXXX           |
| **15**           |  4         |    3           |   XXXXX           |
| **16**           |  4         |    4           |   XXXXX           |
