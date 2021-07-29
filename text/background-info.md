# Background info
My original intention for this section was to provide a small history of operating systems to
present some context for the task ahead; while attempting to do so however, one thing became
quickly apparent: I'm a 21 y/o with zero experience in OS development and only a beginner's
understanding of how they work: wth could I say on the
history of operating systems? I wasn't around when programs were literally circuits that were
physically connected to computers and I've never touched a punch card; the first computer
I used ran Windows 7. That being said, I may return to write something of a history here 
after progressing further into this project if I feel like I have something insightful to say,
but, as it stands right now, I'd feel much more comfortable leaving the subject of operating
system history to more capable sources (the 
[wikipedia page](https://en.wikipedia.org/wiki/History_of_operating_systems) is a good jumping
off point).

There is, however, plenty of background information we should still cover first before we can
even attempt to write something bootable, the most pressing of which being: what is an
operating system?

Now, if you've ever owned a computer, you're likely to have an idea of what an operating
system is; you've probably heard of Windows, MacOS or Linux. But if you had to define what an
operating system does, what its purpose and responsibilities are, what would that defintion
look like? Turns out, there isn't one supreme, all-encompassing definition that fits every
OS; there are a lot of different operating systems out there, and each one was designed to
solve a different set of problems. Nevertheless, there are problems that every operating
system needs to solve and this is exactly how we'll construct our initial definition:

*An operating system is a piece of software whose main responsibility is managing the computer's
hardware (i.e. operating the system) and providing an environment and an interface for userland
programs.*

Let's take a quick stroll through this definition. *An operating system operates the system*: the
most underlying responsibility of an OS is to manage the computer's hardware efficiently and
effectively. Similar to an orchestra, a computer is made up of many differentiated components
that need to work together in order to make the system function productively as a whole.
Extending this metaphor, a conductor is needed to direct and delegate such a performance: this
is where our operating system fits into that orchestra.

That brings us to the second part of the definition: an operating system should provide an
environment and interface for userland programs. One important principle of computer science is
that of modularity: breaking a problem or task into small, modular and independent pieces that
fit together to form an overall solution. Modularity simplifies problem-solving and makes software
easier to manage, repair and scale. Imagine if every program you wrote also needed to worry about
the internal mechanics and comlexity of writing to a external device such as an SSD or a display;
a better way to solve this problem is to have one program solve the problem of writing to such a
device and then to simply pass what you want written to that program (of course, this is not how
it exactly works, but you get the idea). This is what we mean by providing an interface. By 
environment, we mean the ability to isolate running programs from one another for the purposes 
of security, manageability and simplicity for the user application programmer's sake.

For right now, we're keeping all of this simple: there's no reason to really cross any of these
bridges yet. But trust me, there will be many bridges to cross. We *are* trying to write an OS
after all.

So, at this point we have a better idea of what an operating system is and what we're getting
ourselves into. Let's talk game plan then for what comes next. In the next section, we should
aim to write something that can boot; that's it. It should do literally nothing but boot. We'll
talk all about how we'll achieve that in the next section, but first a word on what you'll need
before moving forward.

1. **A good handle on the C programming language and x86 Assembly**

	We will be writing our OS principally in C and x86 Assembly, so being competent with those
	technologies is an obvious prerequisite.

2. **Qemu, NASM, and GCC**

	We will be using Qemu to emulate an x86 environment, and GCC and NASM to compile and assemble
	our code. Look up how to install and set up these tools on your computer beforehand.

With that out of the way, let's jump in.
