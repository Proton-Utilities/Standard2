# env.rbx

Returns the entire datamodel environment. This is **not** isolated from `env.this`, any changes made here are reflected to the custom lua state environment.

## Usage

```typescript
let rbx: Record<string, unknown>
```

## Example

```lua
local env = include("env")

------

print(env.rbx.print) -- print

------

env.print = function()
    return 1
end

print(env.rbx.print) -- 1

------

env.helloworld = "Hello, World!"
print(env.rbx.helloworld) -- Hello, World!
print(env.this.helloworld) -- Hello, World!
```
