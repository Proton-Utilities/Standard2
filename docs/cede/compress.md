# cede.compress

Compresses data using a compression algorithm.

## How to use

[Algorithm Enum reference](<algos.md>)

```typescript
function compress(
  algorithm: number,
  input: string,
  ...options: unknown[]
): string
```

## Example

### lz4

```lua
local cede = import("cede")
local codec = import("codec")

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

### deflate

```lua
local cede = import("cede")
local codec = import("codec")

local deflateCompressed = cede.compress(
    "deflate", 
    "Hello, World!", 
    "Zlib", 
    "Dynamic"
)

local encoded = codec.encode(
    "base64",
    deflateCompressed
)

print(encoded) -- eJwFg...
```
