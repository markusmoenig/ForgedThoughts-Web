---
title: "Polygonization"
weight: 3
---

If you do not want to render the scene to an image but would rather triangulate it. Use the ```polygonize``` command for *ftc*.

You have a number of settings available to customize the triangulation:

* ```grid_size```. This defines the area of the scene which gets triangulated. A value of 1.0 (the default) will triangulate from -1.0 to 1.0 in the x, y and z axis. So the actual area which gets sampled is actually double the grid_size.
* ```grid_step_size```. The step size in the grid, the smaller the more triangles will get created. The default value is *0.01*. You will probably need smaller values for complex objects.
*  ```iso_value```. This value defines the triangulation threshhold in the volume field, the default value is 0.006.

You can define these values in the settings structure like this.

```rust
settings.grid_size = 0.5;           // Sample from -0.5..0.5.
settings.height = 0.005;            // A sample every 0.005 units.
settings.iso_value = 0.001;         // Set the sampling threshhold to 0.001
```
