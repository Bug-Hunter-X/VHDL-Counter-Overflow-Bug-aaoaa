# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that can overflow. The `buggy_counter.vhdl` file contains the buggy code.  The `fixed_counter.vhdl` provides the corrected version.

**Bug:**
The `buggy_counter` entity uses an integer type with a limited range (0 to 15). However, the code does not handle the case where the counter exceeds 15.  This leads to an overflow, causing undefined behavior.

**Solution:**
The `fixed_counter` entity addresses this by adding a modulo operation to keep the counter within the defined range.  This prevents overflow and ensures the counter wraps around correctly.

This example highlights the importance of carefully considering the range of integer types and handling potential overflow conditions in VHDL designs.