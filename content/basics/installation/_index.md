---
title: "Installation"
weight: 2
---

Forged Thoughts can be easily installed as a [Rust](https://www.rust-lang.org) subcommand.

First, if you do not have already, install *Rust* and *cargo* on your system by following the easy steps [here](https://www.rust-lang.org/tools/install).

After that you can install Forged Thoughts by typing the following command in your terminal:

```shell
cargo install ftc
```

This installs [ftc](https://crates.io/crates/ftc), the compiler and renderer front-end for Forged Thoughts. You can now invoke *ftc* in your terminal.

If you want to update *ftc* to the latest version just enter the above terminal command again.

## Usage

Invoking *ftc* without any arguments will load, compile and render the *main.ft* file in the current directory.

You can change the input file with the ```input``` command or polygonize the input (instead of rendering it) via the ```polygonize``` command (see [Polygonization](../../rendering/polygonization/)).

Use ```--help``` to display all available commands.
