# Standard2

Standard2 is a naming initiative to make custom environment's feel more intuitive. It's intention is to unify the ex

## How to use

To import libaries, use the `import` global.

> Note that the `import` global does not *insert* the library into the current environment. It returns a library/table, which you can assign a variable to or insert into your environment.

### Example

```lua
local Filesystem = import("fs")
fs.writeFile("Hello.txt", "Hello, World!")
```

## Cached access

If you want per-thread imports, such as to not interfere with existing definitions, you can store imported libraries as a variable reference.

### Example

```lua
local Filesystem = import("fs")
local Serde = import("serde")
local Drawing = import("drawing")
```

## Global access

### Example

#### Defining

```lua
getgenv().fs = import("fs")
getgenv().serde = import("serde")
getgenv().drawing = import("drawing")
```

#### Using

```lua
print(fs.writeFile) -- function 0x.....
print(serde.encode) -- function 0x.....
print(drawing.new) -- function 0x.....
```
