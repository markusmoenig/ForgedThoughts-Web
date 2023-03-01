---
title: "Basics"
weight: 1
---

Forged Thoughts comes with a number of different renderers. A Phong and PBR renderer as well as a full-featured BSDF pathtracer.

By default the PBR renderer is used.

You can create a custom renderer and use it by assigning it to the global settings structure:

```rust
let bsdf = BSDF();
bsdf.iterations = 300;              // Pathtrace 300 iterations
bsdf.depth = 2;                     // With a recursion depth of 2

settings.renderer = bsdf;           // Use it
```

For the Phong and PBR renderer you can use the antialiasing field of the settings structure for anti-aliasing.

```rust
settings.antialias = 3;             // Use a 3x3 matrix for anti-aliasing, default is 1 (no anti-aliasing).
```

Other important settings for rendering are

```rust
settings.width = 300;               // Width of the output image
settings.height = 300;              // Height of the output image
settings.opacity = 1.0;             // Opacity of the background, 0.0 would render a transparent background. Default is 1.0.
settings.background = F3("444");    // Background color. Default is black.
```

The Phong renderer has two more specific configuration options:

```rust
let phong = Phong();
phong.ambient = F3(0.2, 0.2, 0.3);  // Set a custom ambient color. Default is (0.1, 0.1, 0.1).
phong.specular = F3(0.8, 0.8, 0.8); // Set a custom specular color.
```

See also the Lighting chapter.