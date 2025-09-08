ftmalloc is a research project aiming to build the most resilient, fault-tolerant, and secure dynamic memory allocator available for POSIX systems.
We use a combination of a tightly controlled tokenized access model, POSIX memory protections, checksums per memory block and per allocation, and Reed-Solomon coding, to accomplish this.

Here you'll find the full ftmalloc source code released under an MIT license, once released, as well as other supporting projects and papers.

Roadmap to public beta release:
- [x] Secure initialization and sanity checks
- [x] Token-to-address mappings
- [x] Implement base allocation functions
- [ ] XOR parity within each parity region (RAID 5 style)
- [ ] Custom signal handler to catch SIGSEGV and SIGBUS and rebuild from parity

Post public release roadmap:
- [ ] Implement extra allocation functions (ftvalloc, ftaligned_alloc, etc.)
- [ ] Fork curl and patch to use ftmalloc
- [ ] Reed-Solomon coding within each parity region (RAID 6 style)

Other tasks:
- [X] Replace OpenSSL dependency with a similarly secure and performant, smaller keyed hashing algorithm
- [x] Replace zlib dependency with a standalone crc32

