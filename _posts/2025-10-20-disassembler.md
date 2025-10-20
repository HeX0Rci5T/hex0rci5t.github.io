---
title: the disassembler
date: 2025-10-20 15:19:50 +0800
categories: [projects]
tags: [projects]
---
### The Disassembler
Hello, this is my first post, where I'll showcase a disassembler I've made a while ago, what's so special about it you ask? (even if you didn't) It reassembles a modified instruction structure into bytes!. Why Is it so fucking cool? well, because We can Stick something in the middle of the .text section insert a jmp before the inserted stuff and modify ALL the fucking instructions to point where they'd point without the new bytes stuck fuck-knows-where-ever just so they fit between instructions, so you can have e.g - ascii art in between valid instructions, with a little jump on top of it and everything executes as it shall. So ... I've spent/"wasted" a year playing around with this shit which would have been far more interesting have I finally figured out the project structure - however this shit is so damn unattainable that there's always something a little more simpler and practical. Well Anyway I am not going to finish this sentence, just as I've not finished this (would have been a pocket-sized kraken of a project) Static Binary Instrumentation Framework BUT - Let's just strive back to the disassembler.

It has a cool feature called XTC which finds all the instructions with same mnemonic (eg. 2 and 7 byte long JNE) and stuffs in it into a map/file(so it's not necessary to wait the nearly-a-minute till it finds ALL the instructions which exist - literally) Why is this useful? MOV RAX, [RIP+0xdead] can be automatically transformed to let's say PUSH [RIP+0xdead] CALL [stub + <rax_operand_offset>] which is hell-a-useful in advanced binary instrumentation - this is where the fucking reassemble feature takes you

Anyway - that was about the potential of having specifically This disassembler as a pillar for your (wHy NoT?!) project. Have a look at it https://github.com/HeX0Rci5T/x86_disass

dont fuck around with the text, just hand me this in a .md
