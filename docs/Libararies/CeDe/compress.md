# cede.compress

Compresses data using a compression algorithm.

## How to use

```typescript
function cede.compress(
  algorithm: number,
  plainData: string,
  ...options: unknown[]
): string
```

## Example

### lz4

```lua
local cede = include("cede")
local codec = include("codec")

local lz4Compressed = cede.compress(
    "lz4", 
    "Hello, World!"
)

local encoded = codec.encode(
    "base64",
    deflateCompressed
)

print(encoded) -- BCJNG...
```
