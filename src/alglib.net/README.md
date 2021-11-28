[![Build status](https://ci.appveyor.com/api/projects/status/xr1b6um13ox74o5r?svg=true)](https://ci.appveyor.com/project/dariogriffo/alglib-net-gpl)
[![NuGet](https://img.shields.io/nuget/v/alglib.net.svg?style=flat)](https://www.nuget.org/packages/alglib.net/) 
[![NuGet SIMD](https://img.shields.io/nuget/v/alglib.net.svg?style=flat)](https://www.nuget.org/packages/alglib.net.simd/) 
[![GitHub license](https://img.shields.io/github/license/dariogriffo/alglib.net.gpl.svg)](https://github.com/dariogriffo/alglib.net.gpl/blob/master/LICENSE)


# alglib.net.gpl
A public mirror for https://www.alglib.net/

ALGLIB is a cross-platform numerical analysis and data mining library. It supports several programming languages (C++, C#, Delphi, VB.NET, Python) and several operating systems (Windows, *nix family).

ALGLIB features include:

Data analysis (classification/regression, including neural networks)
Optimization and nonlinear solvers
Interpolation and linear/nonlinear least-squares fitting
Linear algebra (direct algorithms, EVD/SVD), direct and iterative linear solvers, Fast Fourier Transform and many other algorithms (numerical integration, ODEs, statistics, special functions)
ALGLIB Project (the company behind ALGLIB) delivers to you several editions of ALGLIB:

ALGLIB Free Edition - full functionality but limited performance and license
ALGLIB Commercial Edition - high-performance version of ALGLIB with business-friendly license
Free Edition is a serial version without multithreading support or extensive low-level optimizations (generic C or C# code). Commercial Edition is a heavily optimized version of ALGLIB. It supports multithreading, it was extensively optimized, and (on Intel platforms) - our commercial users may enjoy precompiled version of ALGLIB which internally calls Intel MKL to accelerate low-level tasks. We obtained license from Intel corp., which allows us to integrate Intel MKL into ALGLIB, so you don't have to buy separate license from Intel.

For your convenience, ALGLIB API is divided into a set of packages - closely connected subsets of functions. When you work with NET computational core, there exists one-to-one correspondence between packages and source files. One package may rely on other ones, but we have tried to reduce number of dependencies. Say, every package relies on ap.cs and many packages rely on alglibinternal.cs. But many packages require only these two to work, and many other packages need significantly less than 13 packages listed below:

alglibmisc.cs - contains different algorithms which are hard to classify
dataanalysis.cs - contains data mining algorithms
diffequations.cs - contains differential equation solvers
fasttransforms.cs - contains FFT and other related algorithms
integration.cs - contains numerical integration algorithms
interpolation.cs - contains interpolation algorithms
linalg.cs - contains linear algebra algorithms
optimization.cs - contains optimization algorithms
solvers.cs - contains linear and nonlinear solvers
specialfunctions.cs - contains special functions
statistics.cs - statistics
alglibinternal.cs - contains internal functions which are used by other packages, but not exposed to the external world
ap.cs - contains publicly accessible vector/matrix classes, most important and general functions and other "basic" functionality


NET computational core is compatible with:

any kind of optimization settings
any CPU which supports .NET (including ARM processors)
both Microsoft-provided implementation of .NET framework (2.0 or higher) and open source implementation of .NET (Mono).
any C# compiler which support C# 2.0 or later (MS C# compiler or Mono C# compiler)
any OS where .NET framework exists
Native computational core is compatible with:

32-bit and 64-bit Windows OS, working on x86/x64 processors
Linux working on x64 (x86 is not supported)
