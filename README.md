# Bench2
- a basic .NET benchmark

## Running
- install .NET core: https://dotnet.microsoft.com/download/dotnet 

BenchMarkDotNet requires a release config so use 
```
dotnet run -c release
```

for non-windows OS you may see

> Failed to set up high priority. Make sure you have the right permissions. Message: Permission denied

in this case use 
```
sudo dotnet run -c release
```

## Sample results

### 1
BenchmarkDotNet=v0.13.1, OS=macOS Monterey 12.0.1 (21A559) [Darwin 21.1.0]
Apple M1 Pro, 1 CPU, 8 logical and 8 physical cores
.NET SDK=6.0.100
  [Host]     : .NET 6.0.0 (6.0.21.52210), Arm64 RyuJIT
  DefaultJob : .NET 6.0.0 (6.0.21.52210), Arm64 RyuJIT

| Method |      Mean |     Error |    StdDev |
|------- |----------:|----------:|----------:|
| Sha256 |  4.197 us | 0.0171 us | 0.0142 us |
|    Md5 | 18.609 us | 0.0197 us | 0.0174 us |

### 2
BenchmarkDotNet=v0.13.1, OS=Windows 10.0.22504
Unknown processor
.NET SDK=6.0.100
  [Host]     : .NET 6.0.0 (6.0.21.52210), X64 RyuJIT
  DefaultJob : .NET 6.0.0 (6.0.21.52210), X64 RyuJIT

| Method |      Mean |     Error |    StdDev |    Median |
|------- |----------:|----------:|----------:|----------:|
| Sha256 |  5.820 us | 0.1713 us | 0.4998 us |  5.624 us |
|    Md5 | 24.549 us | 0.3828 us | 0.3580 us | 24.587 us |

### 3
BenchmarkDotNet=v0.13.1, OS=Windows 10.0.22000
Intel Core i7-8650U CPU 1.90GHz (Kaby Lake R), 1 CPU, 8 logical and 4 physical cores
.NET SDK=6.0.100
  [Host]     : .NET 6.0.0 (6.0.21.52210), X64 RyuJIT
  DefaultJob : .NET 6.0.0 (6.0.21.52210), X64 RyuJIT

| Method |     Mean |    Error |   StdDev |
|------- |---------:|---------:|---------:|
| Sha256 | 66.80 us | 1.200 us | 1.064 us |
|    Md5 | 29.07 us | 0.332 us | 0.311 us |

### 4
BenchmarkDotNet=v0.13.1, OS=macOS Monterey 12.4 (21F79) [Darwin 21.5.0]
Apple M1 Max 2.40GHz, 1 CPU, 10 logical and 10 physical cores
.NET SDK=6.0.300
  [Host]     : .NET 6.0.5 (6.0.522.21309), X64 RyuJIT
  DefaultJob : .NET 6.0.5 (6.0.522.21309), X64 RyuJIT


| Method |     Mean |    Error |   StdDev |
|------- |---------:|---------:|---------:|
| Sha256 | 33.52 us | 0.284 us | 0.265 us |
|    Md5 | 24.67 us | 0.101 us | 0.094 us |

// * Legends *
  Mean   : Arithmetic mean of all measurements
  Error  : Half of 99.9% confidence interval
  StdDev : Standard deviation of all measurements
  1 us   : 1 Microsecond (0.000001 sec)

### 5
BenchmarkDotNet=v0.13.1, OS=macOS Monterey 12.4 (21F79) [Darwin 21.5.0]
Apple M1 Max, 1 CPU, 10 logical and 10 physical cores
.NET SDK=6.0.300
  [Host]     : .NET 6.0.5 (6.0.522.21309), Arm64 RyuJIT
  DefaultJob : .NET 6.0.5 (6.0.522.21309), Arm64 RyuJIT


| Method |      Mean |     Error |    StdDev |
|------- |----------:|----------:|----------:|
| Sha256 |  4.245 us | 0.0026 us | 0.0020 us |
|    Md5 | 18.735 us | 0.0226 us | 0.0200 us |