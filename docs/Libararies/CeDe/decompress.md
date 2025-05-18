# cede.decompress

Decompresses compressed data using a decompression algorithim.

## How to use

```typescript
function cede.decompress(
  algorithm: number,
  compressedData: string,
  ...options: unknown[]
): string
```

## Example

### lz4

```lua
local cede = include("cede")
local codec = include("codec")

local decoded = codec.decode(
    "base64"
    "BCJNGEBw3w0AAIBIZWxsbywgV29ybGQhAAAAAA=="
)

local lz4Decompressed = cede.decompress(
    "lz4", 
    decoded
)

print(encoded) -- Hello, World!
```
