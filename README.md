# Objective-C ARC Strong Reference Cycle Memory Leak

This repository demonstrates a common issue in Objective-C development: memory leaks caused by strong reference cycles when using Automatic Reference Counting (ARC).

The `bug.m` file shows the flawed code that creates a retain cycle between two objects.  The `bugSolution.m` file provides a corrected version using `weak` references to break the cycle.

## How to Reproduce
1. Clone this repository.
2. Open the project in Xcode.
3. Run the code. Observe that the deallocation messages are not printed (in the buggy version).
4. Run the fixed code and observe that deallocation messages are printed correctly.