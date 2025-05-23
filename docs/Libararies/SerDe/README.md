# SerDe

**SerDe** stands for **Serialization and Deserialization**. It refers to the process of:

- **Serialization**: Converting data into transmittable and formatted data.
- **Deserialization**: Converting formatted data into a usable data structure.

!!! warning
    SerDe is **not** responsible for:

    - **Compression** *(e.g., lz4, zlib)*
        - Use the [cede](<../CeDe/README.md>) library
    - **Encoding** *(e.g., base64, hex)*
        - Use the [codec](<../Codec/README.md>) library
    - **Cryptography** *(e.g., hashing, encryption)*
        - Use the [crypto](<../Crypto/README.md>) library

## Purpose

SerDe helps in the process of data persistence, mainly between the network boundary.

## Use Cases

- Saving configurable files
- Sending formatted data through the network boundary, mostly using API's.
- Saving parsable data to the disk
