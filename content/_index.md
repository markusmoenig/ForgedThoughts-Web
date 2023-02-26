+++
archetype = "home"
title = "Forged Thoughts"
+++

Forged Thoughts is a modeling and rendering *programming* language. It is open source under the MIT license and currently in early development. The language utilizes 3D and 2D SDFs and is written in Rust and can be easily [installed](basics/installation) as a Rust subcommand.

![pic](main.png)

# Goals

Forged Thoughts strives to create high-quality distance field models for rendering and poligonization. It utilizes multi-threaded CPU based rendering prevent the limitations of SDFs on the GPU. The focus is on quality, rather than speed.

The overall project goals are:

* Create signed distance fields for rendering and poligonization.
* Focus is on quality rather than speed (although all example render in just a few hundred ms on my machine).
* CPU based rather than GPU based.
* Provide an easy but powerful syntax to model and render SDFs without any limitations.

# License

Forged Thoughts is licensed under the MIT.