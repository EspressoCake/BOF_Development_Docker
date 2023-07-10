# BOF_Development_Docker

## Summary

This repository serves as a fully functional, **lightweight** template for developing and compiling `BOF` or otherwise `Windows`-centric applications via `Visual Studio Code`.

## Why

`Visual Studio Code` has supported idempotent, purpose-built containers for development for a few years. 

This is meant to illustrate on how powerful this is, namely:
- Remote installation of extension configurations
- Reliable `Intellisense` for development using path inspection
- Quick, reliable, readily deployable images for rapid development
- Lack of configuration drift between traditional virtual machine IDEs

## How

Opening this folder within `Visual Studio`, you will be prompted to reopen within a container.

Acknowledging this (and assuming you have the [Docker VSCode extension](https://code.visualstudio.com/docs/containers/overview), and `Docker` already installed) will reload the current window to be *inside* of the container it has built for you. That's it. Happy hacking.

## Elections and Benefits

I'm currently using `musl` as the set of header files/libraries/compiler options. This plays a *lot* nicer with the numerous hacks of function pointers leveraged within many popular projects, to include reflective loaders of choice.

We're running on a slim `Alpine` image due to its size and first-class support of `musl` natively. This is just one less headache, and we can leave the "kitchen sink" bloat of other images.

The configuration of the extensions is already done for you, so `Intellisense` among other things (such as peeking definitions) is a single right-click away.