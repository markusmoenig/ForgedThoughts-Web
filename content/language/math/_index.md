---
title: "Math"
weight: 1
---

On overview of all math functions.

# Basics

The basic math functions. F indicates a floating point value and F2 and F3 are the vector classes of Forged Thoughts.

```rust
F = ceil(F);                // Returns the ceil.
F3 = cross(F3, F3);         // Returns the cross product between a and b.
F = dot(F3, F3);            // Returns the dot product.
F = floor(F);               // Returns the floor.
F = length(F2|F3);          // Returns the length of the vector.
F|F3 = mix(F|F3, F|F3, F);  // Mixes the two values.
F2|F3 = normalize(F2|F3);   // Normalizes the vector.
F = smoothstep(F, F, F);    // Creates a smooth interpolation.
F3 = to_linear(F3);         // Converts the F3 to linear space.
```

# Procedural

Functions for procedural content creation.

```rust
F = checker(F2, F);         // Returns a checkerboard value (0.0 or 1.0) for the given 2D position and the pattern size.
F = checker(F2, F, F);      // Same as above but accepts separate x and y sizes
```