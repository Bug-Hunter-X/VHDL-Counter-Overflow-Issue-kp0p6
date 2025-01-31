# VHDL Counter Overflow Bug

This repository demonstrates a common but subtle bug in VHDL counters: the handling of overflow conditions.  The `buggy_counter.vhdl` file contains a counter that, while functionally correct in its basic operation, lacks robustness. The potential for issues becomes apparent when the counter reaches its maximum value and is then incremented, leading to unexpected behavior or even simulation failures.

The `fixed_counter.vhdl` file presents a more robust solution that explicitly addresses the overflow condition, improving the code's reliability and maintainability.

## Bug Description
The `buggy_counter` VHDL code implements a simple counter. However, if the `internal_count` reaches its maximum value (15), the next clock cycle should reset the counter to 0. While this functionality is present, a more robust approach is required to eliminate potential issues.

## Solution
The `fixed_counter` example uses a `when` statement to directly reset to 0 at 15 instead of the `if-else` statement. This makes the intention more explicit, further enhancing readability and maintainability.  This ensures cleaner and more predictable behavior.

## How to use this repository
1. Clone this repository
2. Simulate each VHDL file with a VHDL simulator (e.g., ModelSim, GHDL, VUnit). Observe the behavior of both the buggy and fixed versions.