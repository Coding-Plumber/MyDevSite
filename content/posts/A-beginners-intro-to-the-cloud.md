---
author: "Kyle McAndrew"
title: "Beginners journey to the cloud"
date: "2024-04-02"
tags:
  - cloud
  - aws
---

I have wrote this as a beginner in using cloud services, my intention is to improve my writing skills, hold myself accountable and to be able to look back on my growth in the future. Therefore it is far from perfect it's harder to write than i imagined, if anybody has some resources on helping to write be it technical documentation or articles and books on brainstorming and formatting then please do share.

## Bytes & bits

### What's a Bit?

Imagine a lightbulb: it's either on (1) or off (0). This binary choice represents the most basic unit of data in computing, known as a bit.

### And a Byte?

A byte combines 8 of these bits (e.g., 01001000). With each bit having 2 possible states, a byte offers 2^8 (256) possible combinations, forming the basis of digital language.

I’m now going to try and explain a VPC at a high level using an analogy, let's see how this goes.

### Internet Gateway (IGW)

Think of the internet as a vast network of roads. Entering a private cloud network (VPC) from this expansive network requires passing through a security checkpoint—the Internet Gateway (IGW). This IGW acts much like a guard, scrutinizing the source and destination of data packets to ensure they comply with the security standards of the VPC. It's this meticulous check that keeps our digital gated community safe and connected.

This could be seen like the following.

You pull off the main road (internet) and go down a private road, pulling up to a security booth where you're greeted by a guard. This guard does a few checks before giving you any access. In the world of cloud computing, this guard is the Internet Gateway (IGW), a critical checkpoint that controls the flow of parcels (data packets) between the gated community (VPC) and the world outside (the internet).

The guard checks the labels (source and destination IP addresses) on your parcel to ensure it's destined for an address within the community and that it has the right permissions to enter. If everything checks out, the gate swings open, and you're allowed to proceed along the private roads (network paths) inside the gated community to deliver your parcel.

However, if you're a resident trying to send a parcel out into the world, the guard (IGW) plays an equally crucial role. They ensure your parcel is safely handed off to the postal service on the main road, making sure it reaches its destination anywhere in the world. This process is seamless, providing a secure and controlled way for information to move in and out of the gated community, ensuring the safety and privacy of its residents.

### VPC (Virtual Private Cloud)

A VPC is a private cloud environment that we use to host and protect our services. This is a nice gated community so it costs, you pay for the security and features provided. We have the correct identification to allow us into the complex so they let us in and send us to the correct building for our parcel delivery which is addressed to a certain building within the complex.

### CIDR Block (Classless Inter-Domain Routing Block)

Let's say the address for the VPC location is ‘AWS Complex 10.0.1.0/16’ – this is called the CIDR block, and I'll try to explain it below. Upon entering the AWS cloud complex, ready to deliver your parcel, you encounter its unique addressing system. Unlike traditional street addresses, this complex uses a special layout for naming its buildings—think "Ivy Cottage" or "The Stables". This unique layout is defined by what's known as a CIDR block. It's like the architectural blueprint of the complex, detailing how addresses are allocated and the total number of buildings it can accommodate. A CIDR block sets the boundaries for all possible addresses within the complex, ensuring each building has its own distinct location for precise delivery.

### Understanding IP Addresses

An IPv4 address is made up of 4 bytes and would look something like this: 192.168.1.0 Using an IPv4 address of 192.168.1.0, we can picture this as an address we would use for our house: Full address: 192.168.1.0 192.168 could be the area, like Manchester, Didsbury 1.0 represents the specific building and apartment number We have our address for AWS Complex 10.0.0.0/16 ....wait, you said it's 4 bytes and you've thrown a /16 at me! What is this?!?! Don't panic! This is just a way of organising the unique IP addresses (or house locations), and it's actually simple how we work it out. If we have 10.0.0

My intention is this gives an insight into the very basic understanding, and maybe i can use it as a refresher if i ever forget for a high level overview.

Thank You
