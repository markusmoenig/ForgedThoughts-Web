---
title: "Materials"
weight: 3
---

## Materials

Materials in Forged Thoughts are full BSDF materials.

```rust
let mat = Material();

mat.rgb = F3(0.5, 0.5, 0.5);
mat.emission = F3(0.0, 0.0, 0.0);
mat.anisotropic = 0.0;
mat.metallic = 0.0;
mat.roughness = 0.5;
mat.subsurface = 0.0;
mat.specular_tint = 0.0;

mat.sheen = 0.0;
mat.sheen_tint = 0.0;

mat.clearcoat = 0.0;
mat.clearcoat_gloss = 0.0;
mat.spec_trans = 0.0;
mat.ior = 1.5;
```

The above values are the default values.

### Procedural Materials

You can create procedural materials by assigning a function to the materials procedural member. For example this function creates a checkerboard pattern for a plane:

```rust
plane.material.procedural = |hit| {
    let c = checker(hit.hit_point.xz, 0.5);
    if c < 1.0 {
        c = 0.1;
    } else {
        c = 0.25;
    }
    hit.material.rgb = F3(c);
    hit.material.roughness = 1.0;
    hit.material
};
```

The procedural function gets passed a hit variable and has to return a material. You can access the following members:

```rust
hit.hit_point               // The hit point (F3)
hit.ray.origin              // The ray origin (F3)
hit.ray.direction           // The ray direction (F3)
hit.normal                  // The normal at the hit point (F3)
hit.material                // The material of the hit shape, you can modify it but have to return the material
```
