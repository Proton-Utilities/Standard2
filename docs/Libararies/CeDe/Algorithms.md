# Algorithms

The **CeDe** library supports multiple compression algorithms, each with their own use cases and trade-offs.

| Algorithm | Compression Ratio | Compression Speed | Decompression Speed |
| - | - | - | - |
| **[lz4](https://github.com/lz4/lz4)** | Low | Fastest | Fastest |
| **[zstd](https://github.com/facebook/zstd)** | Highest | Fast | Fast |
| **[deflate](https://www.pkware.com)** | High | Fast | Medium |

## Use cases

- lz4 – Very fast, use if you prefer speed over size
- zstd – Best compression, less supported
- deflate – Most compatible
