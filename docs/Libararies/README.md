# import

`import` is the base function to get all libraries.

## How to use

```typescript
function import(
  library: string,
): Record<string, any>
```

## Example

```lua
local CeDe = import("cede")
CeDe.compress("lz4", "Hello, World!")
```
