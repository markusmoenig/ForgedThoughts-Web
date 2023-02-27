---
title: "Raymarching"
weight: 4
---

With Forged Thoughts you create distance fields using [signed distance functions](https://en.wikipedia.org/wiki/Signed_distance_function) (or in short SDFs) and use [raymarching](https://en.wikipedia.org/wiki/Ray_marching) to traverse them.

You can adjust the default raymarching settings in the global ```settings``` structure.

```rust
settings.steps = 100000;                // The maximum steps the raymarcher executes, default is 10000
settings.max_distance = 200.0;          // The maximum distance rays traverse, default is 5.0
settings.step_size = 0.5;               // The step size modifier, default is 1.0
```

with these 3 settings you can modify the raymarching inside Forged Thoughts.

Increase the ```steps``` when you see artifacts around shapes.

Increase the ```max_distance``` if your furthest object is further away than 5.0 units from the camera.

Decrease the ```step_size``` if you use shape [modifiers](../../modeling/modifier/) which warp the distance field.

These settings only apply when you render the output into an image. Polygonization has a different set of settings.