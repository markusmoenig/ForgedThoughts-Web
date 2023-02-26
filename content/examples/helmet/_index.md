---
title: "Helmet"
weight: 1
---

TODO: Writeup

```rust
// Main shape

let sphere = Sphere(0.24);
let cone = Cone(0.3, 0.25, 0.0);

let helmet = smin(sphere, cone, 0.5);
helmet.material.rgb = F3("9F6F4A");

// Make it hollow

let cut_out = helmet.copy();
cut_out.position.y -= 0.04;
cut_out.scale = 0.98;

helmet -= cut_out;

// Eye holes

let eyes = Ellipsoid();
eyes.size = F3(0.10, 0.03, 0.1);
eyes.position.x = 0.07;
eyes.position.y -= 0.03;
eyes.position.z = 0.3;
eyes.mirror.x = true;
helmet -= eyes;

// Node and mouth

let cut = Box(F3(0.07, 0.2, 0.1));
cut.position.y -= 0.25;
cut.position.z = 0.2;

let modifier = RayModifier("x", "*", "sin", "y");
modifier.frequency = 10.0;
modifier.amplitude = 0.7;
modifier.addend = 1.0;
cut.modifier = modifier;

helmet -= cut;
```