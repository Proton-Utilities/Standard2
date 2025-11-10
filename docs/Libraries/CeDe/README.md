# CeDe

**CeDe** stands for **Compression and Decompression**. It refers to the process of:

- **Compression**: Compressing data into it's smallest form
- **Decompression**: Reverting compressed data into a form that retains the same output

!!! warning
    CeDe is **not** responsible for:

    - **Serialization** *(e.g., json, toml)*
        - Use the [serde](<../SerDe/README.md>) library
    - **Encoding** *(e.g., base64, hex)*
        - Use the [codec](<../Codec/README.md>) library
    - **Cryptography** *(e.g., hashing, encryption)*
        - Use the [crypto](<../Crypt/README.md>) library

## Purpose

CeDe helps in the process of data minification, it helps when sending or writing large amounts of data.

## Use Cases

- Transferring large amounts of data between the network boundary
- Saving large amounts of data to the disk
- Improving query preformance
