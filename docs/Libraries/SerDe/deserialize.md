# serde.deserialize

Deserializes data in a given format into a parsable lua table.

## Usage

```typescript
declare function deserialize(
  format: string,
  serializedText: string
): unknown;
```

## Example

### json

```lua
local serde = include("serde")

local jsonText = [[
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

local result = serde.deserialize("json", jsonText)

print(result.Index)         --> true
print(result.Array[1])      --> Value1
print(result.Table.Index2)  --> Value2
```

### toml

```lua
local serde = include("serde")

local tomlText = [[
title = "Example"

[owner]
name = "Tom"
dob = "1979-05-27T07:32:00Z"
]]

local result = serde.deserialize("toml", tomlText)

print(result.title)       --> Example
print(result.owner.name)  --> Tom
print(result.owner.dob)   --> 1979-05-27T07:32:00Z
```

### yaml

```lua
local serde = include("serde")

local yamlText = [[
Index: true
Array:
  - One
  - Two
  - Three
Table:
  Key1: Value1
  Key2: Value2
]]

local result = serde.deserialize("yaml", yamlText)

print(result.Index)       --> true
print(result.Array[2])    --> Two
print(result.Table.Key2)  --> Value2
```
