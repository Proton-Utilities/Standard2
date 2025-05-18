# Standard2

Standard2 is a naming initiative to make custom environments feel more intuitive. It's intention is to unify the ex

## How to use

> `import` is the base function to get all libraries.

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
