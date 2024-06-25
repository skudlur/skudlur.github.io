---
title: "A primer on CPU design"
date: 2024-06-25T11:00:00+05:30
draft: false
---
## CPU - The heart of a computer

The design of a central processing unit (CPU) involves building and testing various complex micro-architectural modules. We will discuss on what it takes for an enthusiastic beginner to get into the art of designing modern-day CPUs.

## Von-Neumann vs. Harvard Architectures

Every computer comprises of the same primitive structures i.e. compute and memory. Compute refers to the modules that perform logical, arithmetic and other similar operations on data. Memory refers to the space where we store the said data that requires to be processed by the compute.

John Von-Neumann et al described their way of organizing the compute and memory in which the both instructions and data that requires processing share the same memory space and hence there cannot be a concurrent instruction fetch and data operation (i.e. read, write). This architecture is commonly known as the **Von-Neumann Architecture**.

![vn-arch](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/Von_Neumann_Architecture.svg/2880px-Von_Neumann_Architecture.svg.png "Von-Neumann Architecture")

Harvard Mark had set up a relay-based computer which stored instructions on punched tapes and data in electro-mechanical counters. With contrast to the Von-Neumann Architecture, the instructions and the data memory spaces are split up and hence facilitating fetching instructions and performing reads and writes on data without concerns of hazards(wrong flow of memory operations leading to incorrect output). This architecture is commonly known as the **Harvard Architecture**.

![hv-arch](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Harvard_architecture.svg/2880px-Harvard_architecture.svg.png "Harvard Architecture")

Now, these are two basic schools of thought to orgranize your compute and memory. Each have their own advantages and disadvantages and please do not disregard one because the other is "better". Both these architectures can prove to be potent depending on your usecase for the CPU you design.

You can read more about here - [Von-Neumann Architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture) and [Harvard Architecture](https://en.wikipedia.org/wiki/Harvard_architecture).

## Defining the Processing in Central Processing Unit

The word _"processing"_ refers to _"the act or process of treating or preparing something by a special method."_ In this case of a CPU, we will do exactly that. The something in this case consist of instructions. These instructions, like the name suggests, are processes to be performed.

For example, let us say I am training my dog and he sits down every time I say "Sit!". The instruction is "Sit!" and the action is that he sits down. Similarly, we need to instruct our computer to perform certain tasks (i.e. computation).

![doggo](https://qph.cf2.quoracdn.net/main-qimg-bfc7482b8026e5f687b615a0a617fa66-lq "Dog obeying an instruction")

But, do you think a(n expensive) piece of silicon and metals understands English? Does a light pole understand English? Neither of these are true. (Calm down NLP lads) Our semiconductor chips only "understand" electrons. We don't understand electrons (none of us are Neil deGrasse Tyson). Here is where we need *abstraction*!

The binary system consists of conveying data with the combination of just 0s and 1s. This representation can translate well to electricity in digital systems since we direct current. 1 would mean that the signal is high (3.3v/5v etc.) and 0 would mean that the signal is low (0v).

![meme](https://i.pinimg.com/originals/8a/8b/13/8a8b133c722b8ac807e57de6cb410d85.png "meme")

Now that we have established a common lingo that we can somewhat understand, let us try to understand what an instruction means in this context for a CPU.

An instruction is a set of binary numbers of size in the powers of 2. Why powers of 2? We will get to that later. This instruction needs to be understood, there needs to be a format or a syntax to this "sentence" that I just said to the computer. The instruction's format comprises of fields like memory addresses, immediate values, opcodes, function values and offset values. I will explain what these mean going ahead.

The premise that a computer understands instructions that are in binary is now set, but what does it "process". The computer needs to decode this instruction to understand what logical or arithmetic operation to perform on what bit of data. The fields mentioned in the last line all help with deducing what operations are done on which data. Hence, leading to computation i.e. processing!

