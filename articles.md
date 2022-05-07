# Articles

This collection is articles is currently an unorganised mixed bag. PRs that add structure welcome.

- [Library order in static linking ](https://eli.thegreenplace.net/2013/07/09/library-order-in-static-linking)
  - A thorough walkthrough of the library linking process for gcc. Pretty interesting if you're trying to understand the process of assembling a final application from all of the separately compiled units a deeper level.
- [Dumping Firmware With a 555](https://jrainimo.com/build/2022/01/dumping-firmware-with-a-555/)
  - I'm interested in *glitching*; the process of injecting faults into electronic devices to cause intended side effects. Usually this is done with an FPGA or device like the ChipWhisperer, but the author shows how you can use the humble 555 (or at least a variant) to achieve the same thing, with a little more work.
- [Regular Expression Matching Can Be Simple And Fast (but is slow in Java, Perl, PHP, Python, Ruby, ...) ](https://swtch.com/~rsc/regexp/regexp1.html)
  - Russ Cox's deep dive into regular expression implementation details. I'm currently working through this and other resources to build a Regex VM.
- [C Structure Padding Initialization](https://interrupt.memfault.com/blog/c-struct-padding-initialization)
  - Structures in languages like C, C++, and Rust often have padding between the fields added automatically by the compiler for various reasons. How that padding is intitialsed turns out to go pretty deep, and has some interesting security implications.

[Back to the main page](./README.md)
