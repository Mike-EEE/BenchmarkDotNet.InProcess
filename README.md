﻿# BenchmarkDotNet.InProcess

### First Run (no `BenchmarkDotNet.Artifacts` folder)

```
// * Summary *

BenchmarkDotNet=v0.10.14, OS=Windows 10.0.14393.2214 (1607/AnniversaryUpdate/Redstone1)
Intel Core i7-4820K CPU 3.70GHz (Haswell), 1 CPU, 8 logical and 4 physical cores
Frequency=3613273 Hz, Resolution=276.7574 ns, Timer=TSC
  [Host] : .NET Core 2.1.0-rc1 (CoreCLR 4.6.26426.02, CoreFX 4.6.26426.04), 64bit RyuJIT

Toolchain=InProcessToolchain  LaunchCount=1  TargetCount=5
WarmupCount=5

  Method |     Mean |     Error |    StdDev |  Gen 0 |  Gen 1 | Allocated |
-------- |---------:|----------:|----------:|-------:|-------:|----------:|
 ToArray | 21.31 us | 0.6226 us | 0.1617 us | 7.6294 | 0.8240 |  39.13 KB |
```

### Second Run (with `BenchmarkDotNet.Artifacts` folder)

```
  Method |     Mean |     Error |    StdDev |  Gen 0 |  Gen 1 | Allocated |
-------- |---------:|----------:|----------:|-------:|-------:|----------:|
 ToArray | 21.11 us | 0.4698 us | 0.1220 us | 7.6294 | 0.8240 |  39.13 KB |
```