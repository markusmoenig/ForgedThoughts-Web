---
title: "Backgrounds"
weight: 4
---


You can set the background color in the global settings structure:

```rust
settings.background = F3(0.1, 0.2, 0.3);
```

or you can define a ```background``` function in your script to create a procedural background:

```rust
fn background(ray) {
    let t = 0.5 * (ray.direction.y + 1.0);
    to_linear( ( (1.0 - t) * F3(1.0) + t * F3(0.5, 0.7, 1.0)) * 0.6)
}
```

The ```ray``` struct contains the ```origin``` and ```direction``` of the ray at the current pixel.

### Opacity

The ```opacity``` field in the settings structure has a default value of 1.0. If you want to render with a transparent background you can set the value to 0.0:

```rust
settings.opacity = 0.0;
```