# Learning Resources

This repository serves as a list of resources that I have personally found useful for learning about certain concepts - especially those discussed in the low level javascript videos. Where applicable, the resource will be annotated with a media type and description. This list will forever be a work-in-progress, and I'll do my best to keep it updated as I think of/find interesting resources!

## Contributing

If you'd like to add your own informative (and relevant) resources, feel free to open a PR! I'll merge it if I think it fits with the spirit of the repo.

## General Learning

Learning about low level topics can be quite overwhelming, because the subjects are actually very broad. The key thing that helps me learn when I feel out of my depth reviewing a resource is to accept that I might not (and probably won't) understand everything from it at once. That's fine. Exposing myself to the terminology and concepts creates a cummulative understanding over time. I look up terms on wikipedia - despite what some people say, wikipedia is one of the worlds greatest achievements. If I don't understand the terms O find on the wikipedia page, then I open up all the links in new tabs, and fall down the rabbit hole until things start making sense!

### Keeping A Journal / Lab Notebook

Keeping notes as you learn - be it in a real notebook, a wiki, or just a text file - is frustratingly effective. When you're working on something hard, you can write about what you want to do, what you found, the problems you ran into, etc. It makes it so easy to look back at what you've done. It's also one of the worlds most effective debuggers. When you hit a problem you don't understand - you can apply the scientific method:

1. Write down your observations of the system
2. Form a hypothosis about what the problem might be
3. Design an experiment to test the hypothosis (this can be as simple as `console.log('here?')`
4. Run the experiment
5. Return to step 1

Using the above methodology, you will undoubtedly end up understanding the system better. If you're so inclined, you can transform knowledge gained in this way to tests for your system - allowing you to see when something you thought was true later breaks down under different conditions.

As a final point, lab notes can be make for some of the most interesting blogs! They allow you to showcase your problem solving skills, and I personally have a lot of respect for people who show their entire process.

### Don't try to learn in a black box

As a quick note, some people will, when working on a project - perhaps from misplaced principles - actively avoid reading other peoples code when trying to solve a problem; I've been guilty of this myself as well. But it really is a *life hack* to get past that pride - because not only will it speed you up dramatically, it will likely reveal to you other, perhaps better ideas. This isn't stealing (at least as long as you're not ripping code out directly or actively trying to avoid attribution!) - this is learning! Discovery feels great, but sometimes you're doing youself a disservice by avoiding the hard work that others have already done.

## CPUs and Computer Architecture

### Books

- [Computer Organization and Design RISC-V Edition: The Hardware Software Interface](https://www.amazon.co.uk/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757/)
  - I've found this book extremely helpful for understanding a bunch of architecture concepts, including CPU pipelining, various forms of parallelism, cache design and memory hierarchies, and even GPU design! It covers tons of ground, and is written in a highly approachable way. The authors don't shy away from introducing up to date, modern concepts either.

### Architecture Specific Resources

Understanding and comparing various architectures is a great way to develop a more general overview.

#### ARM

- [The ARM ARM (Architecture Reference Manual)](https://developer.arm.com/documentation/#sort=relevancy&f:@navigationhierarchiesproducts=[Architectures,CPU%20Architecture,M-Profile,Armv7-M])
  - The comically named ARM ARM is pretty much the bible of understanding this architecture. Well, ARM is actually a lot of different architectures that have one or more common instruction sets. The link here points to the *ARMv7-M Architecture Reference Manual Reference Manual* - which is mainly related to microcontrollers - but on the same website you'll find manuals for all of the others too.

#### RISC-V

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

### "Ultimate" Talks

There's a great series of talks that discuss the details of various classic gaming/computing systems, often covering the CPU in depth. You can really learn a lot by seeing and comparing how the different systems were designed - what tradeoffs were made, and how they built on top of each other.

- [The ultimate gameboy talk](https://www.youtube.com/watch?v=HyzD8pNlpwI)
- [The ultimate atari 2600 talk](https://www.youtube.com/watch?v=qvpwf50a48E)
- [The ultimate commadore 64 talk](https://www.youtube.com/watch?v=ZsRRCnque2E)

### Reverse Engineering / Jailbreaking Systems

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

### Game Specific

- [Mechanics Explained](https://www.youtube.com/channel/UCwRqWnW5ZkVaP_lZF7caZ-g)
  - A channel where game consoles, and specific games are discussed in detail - often at the assembly level. Really insightful, well made videos - and the knowledge is transferable!
- [Fig](https://www.youtube.com/channel/UCHcxE9An6Lusrphb_Slmm1A)
  - Fig is one of the people working on the Zelda OOT/Majoras Mask decompilation project, which aims to recreate a fully documented and buildable C project for both games. Lately he's been making some videos where he dives deep into glitches by analysing the C code. There's a lot of focus on speedrunning - so glitches, exploits, and arbitrary code execution are discussed with some importance!

### Operating Systems and Kernel Internals

I'm not very knowledgable about Operating System development, but I find it really interesting. 

- [Andreas Kling](https://www.youtube.com/channel/UC3ts8coMP645hZw9JSD3pqQ)
  - Andreas has been publicly building a POSIX-ish OS on youtube, and it's incredible. I really enjoy watching him work through problems; he's great at explaining his thought process as he's working.
- [Book: Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652) 
  - A very readable guided tour through the architecture, subsystems, and data structures of the linux kernel. Might not be completely up to date, but should suffice on a conceptual level.

## Security

- [LiveOverflow](https://www.youtube.com/channel/UClcE-kVhqyiHCcjYwcpfj9w)
  - This is such a great channel. The style is unique and the presentation of complex concepts is really well done IMO. You can learn all about different exploitation techniques like buffer overflow, reverse engineering insights, and explorations of bugs and vunerabilities in great detail.

## FPGA and HDL

- [nandland](https://www.youtube.com/channel/UCsdA-aNqtMA1_2T15aXePWw)
  - A YouTube channel that specifically teaches FPGA and HDL from the very basics up to some more advanced projects. There's also a blog which has code and more detail about the concepts discussed in the videos
- [Robert Baruch](https://www.youtube.com/channel/UCBcljXmuXPok9kT_VGA3adg)
  - Robert makes a lot of interesting videos, some of which are specifically about building CPUs on FPGAs. His HDL of choice is nMigen, which is a python based embedded hardware description language. Check out the `6800 CPU with nMigen`and the `LMARV` series.
- [Ferris](https://www.youtube.com/channel/UC4mpLlHn0FOekNg05yCnkzQ)
  - Ferris is a demoscener and rust enthusiast, who also happens to be creating his own embedded HDL in rust, and using it to create a game console on an FPGA. He streams all of his work and uploads it to youtube. His other videos are also well worth checking out!
- [gateware-ts](https://github.com/gateware-ts/gateware-ts)
  - I can't help but plug my own TypeScript based HDL here! `gateware-ts` is an ongoing effort to make it possible to create FPGA hardware in TypeScript - and is designed specifically to work with the open source toolchain. It's still quite rough around the edges - it doesn't have much in the way of documentation (though some can be generated from the code), and the toolchain must be installed separately - but it's coming along quite nicely. Check out the examples folder to get an idea of how it looks.

## Driving LED Panels

I've recently gotten interested in driving LED panels from an FPGA. These panels are typically combined in larger quanities to create large video wall displays. You can buy the individual panels cheaply from sites like Aliexpress (a 64x64 display is something like €20!).

Here are a few resouces that I've been referencing:

- [Scanlime - FPGA driver for 64x64 LED Panel in icestudio series](https://www.youtube.com/watch?v=aRAyVoljc_w)
- [Mike's Electric Stuff - Driving a 32x64 Display](https://www.youtube.com/watch?v=Sq8SxVDO5wE)
- [The Signal Path - The design of a 32x32 LED Panel driver](https://www.youtube.com/watch?v=h6NH_3KpWe8) 
- [Panel datasheets and schematics](https://github.com/esden/led-panel-docs)
- [Everything You Didn't Want to Know About RGB Matrix Panels](https://www.sparkfun.com/news/2650)

- [Building FPGA Hardware Using TypeScript: Driving An RGB LED Panel](https://www.youtube.com/watch?v=Otx96lJnLeo)
  - This video shows some of the first principles of driving panels, with the demonstration being built using gateware-ts.
