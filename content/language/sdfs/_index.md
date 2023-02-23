---
title: "SDFs"
weight: 3
---

On overview of all currently available SDF (signed distance function) classes and their properties and available transformations.

The SDFs will always be created at the center of the scene with a standard size of 1.0 by default.

## Transformations

```rust
// Change the position
v.position = F3(-1.0, 2.0, 3.0)
v.position.x += -2;

// Rotation
```

## Available SDFs

```rust
// Sphere
let v = Sphere();           // Create a sphere with a radius of 1.0.
let v = Sphere(1.5);        // Create a sphere with a custom radius
v.radius = 1.2;

// Cube
```