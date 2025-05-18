# cede.compress

Compresses data using a compression algorithm.

## How to use

```typescript
function cede.compress(
  algorithm: string,
  plainData: string
): string
```

## Example

### lz4

```lua
local cede = include("cede")
local codec = include("codec")

local compressed = cede.compress("lz4", "Hello, World!")

print(codec.encode(
    "base64",
    compressed
)) -- BCJNGEBw3w0AAIBIZWxsbywgV29ybGQhAAAAAA
```

### zstd

```lua
local cede = include("cede")
local codec = include("codec")

local compressed = cede.compress("zstd", "Hello, World!")

print(codec.encode(
  "base64",
  compressed
)) -- 80jNycnXUQjPL8pJUQQA==
```

### deflate

```lua
local cede = include("cede")
local codec = include("codec")

local compressed = cede.compress("deflate", "Hello, World!")

print(codec.encode(
  "base64",
  compressed
)) -- 80jN...
```
