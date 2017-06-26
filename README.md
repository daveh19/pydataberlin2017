# pydataberlin2017
Slides and code for PyData Berlin 2017, Introduction to Julia, tutorial.

Please go through the installation instructions below prior to attending the
workshop. They have been tested on Mac OS X and Debian Stretch.

The actual material will be published just before the event.

## 1. Install Julia

For this workshop, we will use Julia v0.6 which was released on June 19th 2017.
A pre-built binary version can be [downloaded](https://julialang.org/downloads/)
for your operating system.

## 2. Install required packages

The workshop material depends on several packages from the Julia community.
Please execute the following commands in the REPL to download and install them:

```julia
Pkg.add("IJulia")
Pkg.add("DataFrames")
Pkg.add("Plots")
Pkg.add("PyPlot")
Pkg.add("StatPlots")
Pkg.add("JuMP")
Pkg.add("Cbc")
Pkg.add("BenchmarkTools")
Pkg.add("ProfileView")
```

Please also attempt to install Gallium, but it may not be updated properly to version 0.6 yet:

```julia
Pkg.add("Gallium")
```

**OpenCL** will work out of the box for Mac users. For Windows and Linux users it typically requires some external packages be installed. This is not a workshop on OpenCL, so we'll provide a notebook with the calculated outputs which you can follow, but please note when installing OpenCL that you need a **driver** or a **library** which provides OpenCL support directly for your system and not just the header files. (apt-get install opencl typically only grabs the headers).

If you want to install OpenCL there are a number of options:
1. If you have an NVIDIA GPU then you automatically have OpenCL installed if you install CUDA development system. Note that the NVIDIA implementation can only compile OpenCL for the GPU device.
2. You can install ATIs APP SDK, which is natively OpenCL, for ATI GPU devices. _This system can also compile for CPU giving you the best of both worlds!_
3. Intel provide OpenCL compilers for CPUs.
4. Apple pre-install OpenCL support on their computers, for both CPU and GPU.

Following installation of the OpenCL drivers, run the following to download the Julia OpenCL package:
```julia
Pkg.add("OpenCL")
```


## 3. Test and precompile packages

Please also run the following lines in the REPL. This will check whether the
installation was successful and also precompile some Julia code or even some
third-party C libraries.

```julia
using IJulia
using DataFrames
using Plots
using PyPlot
using StatPlots
using JuMP
using Cbc
using BenchmarkTools
using ProfileView
```

```julia
using Gallium
```

```julia
using OpenCL
```

Once that is finished, you can also try to start the Jupyter notebook server, by
calling `notebook()` in the REPL, which should open a browser menu.


## Join us at the Julia Users Group - Berlin

After the workshop you may wish to join us at our bi-monthly meet-up in Berlin. Check our [website](http://julia-users-berlin.github.io) or [meet-up.com](https://www.meetup.com/Julia-Users-Group/) for details.
