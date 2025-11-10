# serde.serialize

Serializes data using the given format.

## Usage

```typescript
declare function serialize(
  format: string,
  plainText: string,
  ...options: unknown[]
): string
```

## Example

### json

```lua
local serde = include("serde")

local luaTable = {
    Index = true
    Array = {
      "Value1",
      "Value2"
    },
    Table = {
      Index1 = "Value1",
      Index2 = "Value2"
    },
}

print(serde.serialize("json", luaTable, true)) --[[
    {
      "Index": true,
      "Array": [
        "Value1",
        "Value2"
      ],
      "Table": {
        "Index1": "Value1",
        "Index2": "Value2"
      }
    }
]]
```

### toml

```lua
local serde = include("serde")

local luaTable = {
  title = "Example",
  owner = {
    name = "Tom",
    dob = "1979-05-27T07:32:00Z"
  }
}

print(serde.serialize("toml", luaTable, true)) --[[
    title = "Example"

    [owner]
    name = "Tom"
    dob = "1979-05-27T07:32:00Z"
]]
```

### yaml

```lua
local serde = include("serde")

local luaTable = {
  Index = true,
  Array = {
    "One",
    "Two",
    "Three"
  },
  Table = {
    Key1 = "Value1",
    Key2 = "Value2"
  }
}

print(serde.serialize("yaml", luaTable)) --[[
    Index: true
    Array:
      - One
      - Two
      - Three
    Table:
      Key1: Value1
      Key2: Value2
]]
```
