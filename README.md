# bench2
- a basic dotnet benchmark

## running
BenchMarkDotNet requires a release config so use 
```
dotnet run -c release
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