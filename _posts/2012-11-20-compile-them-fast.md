---
layout: post
title: "Compile them fast"
date: 2012-08-23 01:09
comments: false
categories: Programming
---

In my previous blogs I mentioned a lot about the build parallelism and source level parallelism. For a typical developer, two core machines was sufficient enough to do their stuffs. I lived most of my time mediocre machines and sometimes with a graphics card depends on the project needs. I primarly work with Microsoft Visual Studio. Multi-processor compilation is really a boon to C++ projects. Unlike languages like, C#, Python, Java etc. A single unit compilation is highly expensive. Especially when you work with large projects, the time it consumes to build your projects can be very expensive.


The developers keep on upgrading their dev-boxes whenver they wanted. I am blessed with a high end workstation with hardware with moderately high configuration. You can't see the source level paralellism and build level parallelism if you're working with a dual core processor. But this is quite visible when you work with multi-core machines.

#Build Parallism
Visual Studio's default configuration make use of all the cores available to build individual projects within the solutions.
