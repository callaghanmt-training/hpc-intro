---
title: "Why Use a HPC Cluster?"
teaching: 15
exercises: 5
questions:
- "Why would I be interested in High Performance Computing (HPC)?"
- "What can I expect to learn from this course?"
objectives:
- "Be able to describe what an HPC system is"
- "Identify how an HPC system could benefit you."  
keypoints:
- "High Performance Computing (HPC) typically involves connecting to very large computing systems
  elsewhere in the world."
- "These other systems can be used to do work that would either be impossible or much slower or
  smaller systems."
- "The standard method of interacting with such systems is via a command line interface called
  Bash."
---

## Why Use These Computers?

> ## What do you need?
>
> Talk to your neighbour about your research. How does computing help you do your research? How could
> more computing power help you do more or better research?
{: .challenge}

Frequently, research problems that use computing can outgrow the desktop or laptop computer where
they started:

* A statistics student wants to cross-validate their model. This involves running the model 1000
  times -- but each run takes an hour. Running on their laptop will take over a month!

* A genomics researcher has been using small datasets of sequence data, but soon will be receiving a
  new type of sequencing data that is 10 times as large. It's already challenging to open the
  datasets on their computer -- analyzing these larger datasets will probably crash it.

* An engineer is using a fluid dynamics package that has an option to run in parallel. So far, they
  haven't used this option on their desktop, but in going from 2D to 3D simulations, simulation time
  has more than tripled and it might be useful to take advantage of that feature.

* A geographer is running a matlab model that needs lots of computer memory. With a limited amount of memory
  on their laptop there is a maximum simulation size they can run.

In all these cases, what is needed is access to more computers with more resource (computer cores and memory) 
that can be used at the same time.

Luckily, large scale computing systems -- shared computing resources with lots of computers -- are
available at many universities, labs, or through national networks. Leeds has particularly good University-level 
resources (we call these **Tier 3** resources; regional resources are **Tier 2**, national resources **Tier 1** and 
supra-national resources **Tier 0**)

These resources usually have more central processing units (CPUs), CPUs that operate at higher speeds, more memory, more storage, and faster connections with other computer systems. They are frequently called "clusters",
"supercomputers" or resources for "high performance computing" or HPC. In this lesson, we will
usually use the terminology of HPC and HPC cluster.

Using a cluster often has the following advantages for researchers:

* **Speed.** With many more CPU cores, often with higher performance specs than a typical laptop or
  desktop, HPC systems can offer significant speed up.
* **Volume.** Many HPC systems have both the processing memory (RAM) and disk storage to handle very
  large amounts of data. Terabytes of RAM and petabytes of storage are available for research
  projects.
* **Efficiency.** Many HPC systems operate a pool of resources that are drawn on by many users. In
  most cases when the pool is large and diverse enough the resources on the system are used almost
  constantly.
* **Cost.** Bulk purchasing and government funding mean that the cost to the research community for
  using these systems is significantly less than it would be otherwise. In some Universities HPC is free 
  at the point of use for researchers.
* **Convenience.** Maybe your calculations just take a long time to run or are otherwise
  inconvenient to run on your personal computer. There's no need to tie up your own computer for
  hours when you can use someone else's instead.

This is how a large-scale compute system like a cluster can help solve problems like those listed at
the start of the lesson.

> ## Thinking ahead
>
> How do you think using a large-scale computing system will be different from using your laptop?
> Talk to your neighbor about some differences you may already know about, and some
> differences/difficulties you imagine you may run into.
{: .challenge}

## Using the Command Line

Using HPC systems often involves the use of a Linux shell through a command line interface (CLI) and
either specialised software or programming techniques. 

Many researchers only have experience of using Windows and although learning to use the shell may take a 
short while, it will be time well spent.

The shell is a program with the special role of having the job of running other programs rather than 
doing calculations or similar tasks itself.

What the user types goes into the shell, which then figures out what commands to run and orders the
computer to execute them. (Note that the shell is called "the shell" because it encloses the
operating system in order to hide some of its complexity and make it simpler to interact with.) 

Think of it this way:
* The user communicates with the shell
* The shell works out what commands to run and communicates with the computer's operating system
* The operating systems communicates with, controls and manages the computer's hardware.

[Diagram]

The most popular Unix and Linux shell is Bash, the Bourne Again SHell (so-called because it's derived from a shell
written by Stephen Bourne). Bash is the default shell on most modern implementations of Unix and in
most packages that provide Unix-like tools for Windows.

Interacting with the shell is done via a command line interface (CLI) on most HPC systems. In the
earliest days of computers, the only way to interact with early computers was to rewire them. From
the 1950s to the 1980s most people used line printers. These devices only allowed input and output
of the letters, numbers, and punctuation found on a standard keyboard, so programming languages and
software interfaces had to be designed around that constraint and text-based interfaces were the way
to do this. 

Typing-based interfaces are often called a **command-line interface**, or CLI, to
distinguish it from a **graphical user interface**, or GUI, which most people now use. The heart of
a CLI is a **read-evaluate-print loop**, or REPL: when the user types a command and then presses the
Enter (or Return) key, the computer reads it, executes it, and prints its output. The user then
types another command, and so on until the user logs off.

[Diagram]

Learning to use Bash or any other shell sometimes feels more like programming than like using a
mouse. Commands are terse (often only a couple of characters long), their names are frequently
cryptic, and their output is lines of text rather than something visual like a graph. However, using
a command line interface can be extremely powerful, and learning how to use one will allow you to
reap the benefits described above.

## The rest of this lesson

The only way to use these types of resources is by learning to use the command line. This
introduction to HPC systems has two parts:

* We will learn to use the UNIX command line (also known as Bash).
* We will use our new Bash skills to connect to and operate a high-performance computing
  supercomputer.

The skills we learn here have other uses beyond just HPC - Bash and UNIX skills are used everywhere,
be it for web development, running software, or operating servers. It's become so essential that
Microsoft now ships as [part of Windows][_ms-ubuntu])! Knowing how to use Bash and HPC systems will
allow you to operate virtually any modern device. With all of this in mind, let's connect to a
cluster and get started!

[_ms-ubuntu]: https://www.microsoft.com/en-us/store/p/ubuntu/9nblggh4msv6

{% include links.md %}
