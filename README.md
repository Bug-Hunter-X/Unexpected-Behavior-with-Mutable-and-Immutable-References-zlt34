# Unexpected Behavior with Mutable and Immutable References in Rust
This example demonstrates a potential issue when using mutable and immutable references in Rust. Modifying a value through a mutable reference can affect other references, even immutable ones, if they point to the same data. 

**Bug:** The code demonstrates that modifying x through y affects the value accessed via z, even though z is an immutable reference.

**Solution:** The solution addresses the issue by ensuring that only one mutable reference exists at any given time. This avoids the race conditions and data inconsistencies mentioned in the description.