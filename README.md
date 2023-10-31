# Reproducer for a Metal bug affecting comparison

See `shader.metal` for the MSL code, along with comments about alternatives that
both do and do not exhibit the problem.

## Reproduced on:

```
 macOS: Sonoma 14.1
 Model Name: MacBook Pro
 Chip: Apple M1 Pro
```

Does not reproduce on Intel or AMD GPUs running macOS 14.1.

## Building and Running

```bash
make
./metal-comparison-bug
```

This should produce:
```
output = 0
```

But on Apple M1 running macOS 14.1 instead produces:
```
output = -992
```
