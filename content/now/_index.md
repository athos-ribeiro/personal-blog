+++
date = "2024-11-30T06:11:11-03:00"
+++

### Ubuntu

I am currently working on the next Ubuntu release, plucky puffin. There, I am
preparing the next versions of packages in the container stack (docker,
containerd, runc), the high availability packages (pacemaker, corosync, etc),
PHP (the interpreter, extensions, and other related packages), and PostgreSQL.

### Debian

I have been mostly forwarding the work I do in Ubuntu to Debian and preparing a
new version of isc-kea (2.6).

### Reading

**Capitães da areia**.  This is a novel from 1937 by the Brazilian writer
**Jorge Amado** about the life of a group of children living on the streets
of Salvador, Bahia.

**Learning eBPF**.  This is a nice and practical introductory book on eBPF I
used to get started with writting the [Ubuntu Server introduction to
eBPF](https://documentation.ubuntu.com/server/explanation/intro-to/ebpf/#introduction-to-ebpf).

**Linkers and Loaders**.  This is a classic, but it is not an easy read at
all if you really want to dive in the topic.

### Studying

I have been going through [Crafting
Interpreters](https://craftinginterpreters.com/) and implementing the first
part of the book in Rust instead of using the book's code, which is in Java.
This way, I can study the 2 topics (compilers and Rust) at the same time.  The
second part of the book is written in C to show students the issues one may
face while having to deal with memory management. I am considering doing that
part in RiscV assembly when the time comes. I may need to get myself some RiscV
board for that matter though.
