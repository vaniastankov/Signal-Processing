# Signal-Processing

An example of many cool things in one project:

1. How Digital Signal Processing (or simply DSP) works;
2. How WebAssembly can work;
3. How fast DSP + Wasm can really be;

I did not expect both Forward and Inverse Fast Fourier Transforms (FFT) to work this well in web browser. 

In this example I try to work on ECG data that has some noise in it.

Every time you press a button Wasm does it's thing. The signal that's being used is 10000 samples long. I am applying various methods in following order: Detrend -> Normalize -> Filter the Signal. I am also plotting Spectral Density of the signal. 

All algorithms are written in C and then translated in Wasm using Emscripten so that this code could be used in Web world.

You have to host simple http Server in order to watch this demo work. Otherwise you wont be able to load WebAssembly Module. (go to the folder where you have this demo located and run, for instance, Python http Server: *python3 -m http.server*

I've also used CanvasJS for demonstration purposes, it's a great tool, as far as I can see.

This code is of no Commercial Use and is only here to show the possibilities of Wasm + DSP. 