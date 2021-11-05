# Computer Architecture

## Books

- [Computer Organization and Design RISC-V Edition: The Hardware Software Interface](https://www.amazon.co.uk/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757/)
  - I've found this book extremely helpful for understanding a bunch of architecture concepts, including CPU pipelining, various forms of parallelism, cache design and memory hierarchies, and even GPU design! It covers tons of ground, and is written in a highly approachable way. The authors don't shy away from introducing up to date, modern concepts either.

## Architecture Specific Resources

Understanding and comparing various architectures is a great way to develop a more general overview.

### ARM

- [The ARM ARM (Architecture Reference Manual)](https://developer.arm.com/documentation/#sort=relevancy&f:@navigationhierarchiesproducts=[Architectures,CPU%20Architecture,M-Profile,Armv7-M])
  - The comically named ARM ARM is pretty much the bible of understanding this architecture. Well, ARM is actually a lot of different architectures that have one or more common instruction sets. The link here points to the *ARMv7-M Architecture Reference Manual Reference Manual* - which is mainly related to microcontrollers - but on the same website you'll find manuals for all of the others too.

### RISC-V

- [LLJS RISC-V Series](https://www.youtube.com/playlist?list=PLP29wDx6QmW4sXTvFYgbHrLygqH8_oNEH)
  - My own personal quest to build a RISC-V CPU on an FPGA in TypeScript using gateware-ts
- [RISC-V Specifications](https://riscv.org/technical/specifications/)
  - RISC-V is interesting for a number of reasons. For one, it's not actually an architecture per se, but rather an ISA specification. A RISC-V processor can be implemented however a designer likes, and so long as it adheres to what is stated in the specification, it can be called a RISC-V processor. Secondly, it's open source. This means that anyone can build a RISC-V processor without having to pay license fees (unlike ARM). It's also very cleverly designed, and beautifully minimalistic.
- [RV32I Instruction Overview](https://raw.githubusercontent.com/RobertBaruch/lmarv/master/lmarv-1/riscv-instructions-book/instr.pdf) by Robert Baruch
  - A nice, semi-graphical overview of the instructions. I like this because it presents what the instructions do in various forms:
    - A worded description
    - The classic `rd <- SomeOperation` functional form
    - A graphical view of the datapath
    - An example
- [Overview of the Base ISA by Andrew Waterman](https://www.youtube.com/watch?v=XWuZSQ6lJlo)
  - This is a talk given by one of the founders of RISC-V, and explains most of the instructions as well as the rationale behind the design. Really worth watching if you find yourself confused by the encoding at any point while reading the specs!
- [Awesome RISC-V Resources (github page)](https://github.com/suryakantamangaraj/AwesomeRISC-VResources)
  - One of the "awesome" collections, which links to docs, open-source cores, emulators etc

## "Ultimate" Talks

There's a great series of talks that discuss the details of various classic gaming/computing systems, often covering the CPU in depth. You can really learn a lot by seeing and comparing how the different systems were designed - what tradeoffs were made, and how they built on top of each other.

- [The ultimate gameboy talk](https://www.youtube.com/watch?v=HyzD8pNlpwI)
- [The ultimate atari 2600 talk](https://www.youtube.com/watch?v=qvpwf50a48E)
- [The ultimate commadore 64 talk](https://www.youtube.com/watch?v=ZsRRCnque2E)

## Reverse Engineering / Jailbreaking Systems

- [Reverse Engineering the MOS 6502 CPU](https://www.youtube.com/watch?v=fWqBmmPQP40)
  - A deep dive into the processor architecture on a very deep level. It's an old CPU of course, and a modern `x86_64` but there's a lot to be learned
- [Wii Fail: "Jailbreaking" the Wii](https://www.youtube.com/watch?v=0rjaiNIc4W8)
  - This video is a short recounting of how the wii console was owned, and provides a pretty decent look into the architecture of a more modern special purpose system
- [Hacking Wii U](https://www.youtube.com/watch?v=oss_dwj-IkE)
  - Another talk from a few years later, about how the same team broke the security of the Wii U
- [Hacking the Switch](https://www.youtube.com/watch?v=Ec4NgWRE8ik)
  - A different team, but same kind of idea.
- [Hacking the PS4](https://www.youtube.com/watch?v=QMiubC6LdTA)
  - Marcan (from the team twiizers) presenting how the security of the PS4 was comprimised
- [Making Pioneer DDJ-RB USB audio work on Linux](https://www.youtube.com/watch?v=cUVuTBH51GY)
  - This is a stream where marcan reverse engineers a proprietary MIDI device in order to write a driver for linux. An amazing insight to how to proceed when faced with a black box.

## Game Specific

- [Mechanics Explained](https://www.youtube.com/channel/UCwRqWnW5ZkVaP_lZF7caZ-g)
  - A channel where game consoles, and specific games are discussed in detail - often at the assembly level. Really insightful, well made videos - and the knowledge is transferable!
- [Fig](https://www.youtube.com/channel/UCHcxE9An6Lusrphb_Slmm1A)
  - Fig is one of the people working on the Zelda OOT/Majoras Mask decompilation project, which aims to recreate a fully documented and buildable C project for both games. Lately he's been making some videos where he dives deep into glitches by analysing the C code. There's a lot of focus on speedrunning - so glitches, exploits, and arbitrary code execution are discussed with some importance!

## Operating Systems and Kernel Internals

I'm not very knowledgable about Operating System development, but I find it really interesting. 

- [Andreas Kling](https://www.youtube.com/channel/UC3ts8coMP645hZw9JSD3pqQ)
  - Andreas has been publicly building a POSIX-ish OS on youtube, and it's incredible. I really enjoy watching him work through problems; he's great at explaining his thought process as he's working.
- [Book: Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652) 
  - A very readable guided tour through the architecture, subsystems, and data structures of the linux kernel. Might not be completely up to date, but should suffice on a conceptual level.

[Back to the main page](./README.md)
