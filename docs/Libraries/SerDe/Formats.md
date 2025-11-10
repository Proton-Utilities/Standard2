# Formats

The **SerDe** library supports multiple serialization formats.

| Algorithm |
| - |
| **[`json`](https://www.json.org)**|
| **[`toml`](https://toml.io)**|
| **[`yaml`](https://yaml.org)**|

## Additional options

Some formats include additional options. </br> The options should be listed in your function call in the indice order they appear in the table below. *(After the base arguments)*

### `json`

| name | description | type | default |
| - | - | - | - |
| `pretty` | Whether to format the data for human readability or not. | `boolean` | `false` |
