# pydataberlin2017

Slides and code for PyData Berlin 2017, Introduction to Julia, tutorial.

Please go through the installation instructions below prior to attending the
workshop. They have been tested on Mac OS X and Debian Stretch.

## 1. Install Julia

For this workshop, we will use Julia v0.6 which was released on june 19th 2017.
A pre-built binary version can be [downloaded](https://julialang.org/downloads/)
for your operating system.

## 2. Install required packages

The workshop material depends on several packages from the Julia community.
Please execute the following commands in the REPL to download and install them:

```julia
Pkg.add("DataFrames")
Pkg.add("Plots")
Pkg.add("PyPlot")
Pkg.add("StatPlots")
Pkg.add("JuMP")
Pkg.add("Cbc")
```

## 3. Test and precompile packages

Please also run the following lines in the REPL. This will check whether the
installation was succesful and also precompile some Julia code or even some
third-party C library.

```julia
using DataFrames
using Plots
using PyPlot
using StatPlots
using JuMP
using Cbc
```
