---
title: "Vectors"
weight: 2
---

On overview of all vector classes.

# F3

A three component vector.

```rust
let v = F3();               // Create an F3 filled with zeroes.
let v = F3(1.0, 0.5, .01);  // Create an F3
let v = F3(1.0);            // Create an F3 with all values being 1.0
let v = F3("B87333");       // Create an F3 from a hex color
let v = F3("#B87333");      // Same as above.

v.length();                 // Returns a float value representing the length of the F3.
v.normalize();              // Returns a normalized version of the F3.
```