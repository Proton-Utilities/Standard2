# include

`include` is the base function to fetch all libraries.

## How to use

```typescript
function include(
  library: string,
): Record<string, any>
```

## Example

```lua
local CeDe = include("cede")
CeDe.compress("lz4", "Hello, World!")
```
