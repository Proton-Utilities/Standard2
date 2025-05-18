# cede.decompress

Decompresses compressed data using a decompression algorithm.

## How to use

```typescript
function cede.decompress(
  algorithm: number,
  compressedData: string,
): string
```

## Example

### lz4

```lua
local cede = include("cede")
local codec = include("codec")

local decoded = codec.decode("base64", "BCJNGEBw3w0AAIBIZWxsbywgV29ybGQhAAAAAA==")

print(cede.decompress("lz4", decoded)) -- Hello, World!
```

### zstd

```lua
local cede = include("cede")
local codec = include("codec")

local decoded = codec.decode("base64", "KLUv/SANaQAASGVsbG8sIFdvcmxkIQ==")

print(cede.decompress("zstd", decoded)) -- Hello, World!
```

### deflate

```lua
local cede = include("cede")
local codec = include("codec")

local decoded = codec.decode("base64", "80jNycnXUQjPL8pJUQQA==")

print(cede.decompress("deflate", decoded)) -- Hello, World!
```
