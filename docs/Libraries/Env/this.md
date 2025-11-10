# env.this

Returns the current, **custom** environment. This is a shared environment of all threads made by the custom lua state.

## Usage

```typescript
let this: Record<string, unknown>
```

## Example

```lua
local env = include("env")

print(env.this.env) -- env

env.helloworld = "Hello, World!"
print(env.this.helloworld) -- Hello, World!
```
