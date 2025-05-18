# cede.algo

A table of enumeral compression algorithims.

## How to use

| Index | Name | Description |
| - | - | - |
| 1 | lz4 | Fastest compression and decompression, lower compression ratio |
| 2 | deflate | Fast compression, slower decompression, higher compression ratio |

### Additional arguments

Some algorithms support optional configuration. These arguments should be passed after the base arguments in the function call.

#### deflate

| Position | Type   | Name | Description | Accepted Values | Default |
| - | - | - | - | - | - |
| 1 | string | headerType | Selects to deflate raw, or use zlib headers. | `"Raw"`, `"ZLib"` | `"ZLib"` |
| 2 | string | compressionMethod | Selects the internal block type used by Deflate. | `"Dynamic"`, `"Fixed"`, `"None"` | `"Dynamic"` |

## Example

### lz4

```lua
local cede = import("cede")
local codec = import("codec")

local lz4Compressed = cede.compress(
    cede.algos.lz4, 
    "Hello, World!"
)

local encoded = codec.encode(
    codec.algos.base64,
    deflateCompressed
)

print(encoded) -- BCJNG...
```

### deflate

```lua
local cede = import("cede")
local codec = import("codec")

local deflateCompressed = cede.compress(
    cede.algos.deflate, 
    "Hello, World!", 
    "Zlib", 
    "Dynamic"
)

local encoded = codec.encode(
    codec.algos.base64,
    deflateCompressed
)

print(encoded) -- eJwFg...
```
