Release Notes
=============

## [3.18.0](https://github.com/dariogriffo/alglib.net.gpl/releases/tag/3.18.0)

The project now generates 2 nuget packages

- [alglib.net](https://www.nuget.org/packages/alglib.net/)
- [alglib.net.simd](https://www.nuget.org/packages/alglib.net.simd/)

Added net6.0 target framework.

The most important improvement in ALGLIB 3.18.0 is that ALGLIB became the first open source numerical library to support .NET 5 SIMD intrinsics!

Hardware intrinsics are well known to C/C++ programmers, but C# lacked them for tens of year. As a result, it was impossible to utilize modern SIMD instructions in C# and performance of the numerical C# code was way below that of the well-optimized C/C++ one. Many numerical libraries (including ALGLIB) solved the problem by providing C# interface to high-performance native code. However, having native code in your application has its own drawbacks.

Thankfully, .NET Core 3.0 finally introduced SIMD support into C# and it matured in .NET 5, and we are glad to announce that ALGLIB for C# now includes optional SIMD kernels for many performance-critical functions. Here 'optional' means that one may compile ALGLIB under .NET 5 with SIMD intrinsics enabled and enjoy unprecedented performance - or compile it without SIMD and enjoy unprecedented portability to any .NET version released since .NET Framework 2. This feature is present in both commercial and open source editions of ALGLIB.

In addition to that major improvement, ALGLIB 3.18.0 also includes following features:

- Sparse GMRES solver for linear equations
- Sparse Cholesky decomposition now comes with AVX2/FMA-capable C++/C# kernels
- Faster AMD ordering (optimized handling of matrices with dense rows)
- Interior point LP and QP solvers became much faster due to new Cholesky and extensive optimization of the solver code itself
- Finally, the open source edition of ALGLIB for C++ also become faster due to introduction of AVX2/FMA-capable linear algebra kernels
- We also fixed several minor bugs (see issues tracker for a complete list). Thanks to all for staying with ALGLIB!

[Original notes here](https://www.alglib.net/arcnews.php#date_27_10_2021)
