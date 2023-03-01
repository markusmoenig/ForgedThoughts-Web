---
title: "Lighting"
weight: 2
---

## Point Lights

Point lights are supported by all renderers in Forged Thoughts.

You can create and customaize a light like this:

```rust
let light = PointLight();

light.position = F3(2.0, 3.0, 5.0);     // The position of the light
light.rgb = F3(1.0, 0.1, 0.1);          // Make it a red light. F3(1.0) by default.
light.intensity = 1.5;                  // The intensity of the light. By default is 1.0.
light.radius = 2.0;                     // The radius of the light. Only supported by the BSDF pathtracer. 1.0 by default.
```
