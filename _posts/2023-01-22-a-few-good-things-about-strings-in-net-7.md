---
title: "A few good things about strings in .net 7"
date: "2023-01-22"
tags: 
  - "news"
  - "performance"
  - "strings"
---

Back in 2003, when the web was young (and so was I), Joel Spolsky, co-creator of StackOverflow [declared this](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/):

> “So I have an announcement to make: if you are a programmer working in 2003 and you don’t know the basics of characters, character sets, encodings, and Unicode, and I catch you, I’m going to punish you by making you peel onions for 6 months in a submarine.”

Underpinning his sentiments was a critical need he felt for developers to understand how strings work, how they are stored, what is optimal usage and to be mindful of how effective use of them can have significant impact on their work.

As a young developer at the time, I valued his advice and took it to heart. 

So, when I saw the continuing improvements to how strings are handled in .NET 7, I felt something approaching delight. I suspect Joel would be pleased. 

When using strings, s**ome of the main challenges when optimizing string operations include:**

- Understanding the complex algorithms associated with string manipulation

- Recognizing that part of the optimization challenge is that strings are often used in conjunction with other data types, such as arrays and lists, which can make the process more challenging.

- Operations often need to take into account the encoding and decoding of characters, which adds an additional layer of complexity.

- The immutability of string objects which make it hard to perform in-place operations and it could lead to a lot of memory allocation and GC pressure.

Added to this strings are used in a wide range of applications, so any optimization must not only improve performance but also maintain backwards-compatibility.

String operations are often used in performance-critical areas such as network communication, data parsing, web scraping and so on. These areas require a balance between performance and memory usage.

This is precisely why the **improvements to string operations in .NET 7 are critical as strings are one of the most commonly used data types in software development.**

There have been performance improvements in the IndexOf and SequenceEquals family of method, for example, leading to significant performance gains in applications that make heavy use of these operations. 

These improvements were achieved through the use of hardware intrinsics, Vector128<T> and Vector256<T>, and JIT optimizations.

Encoding.UTF8 was also improved, with the implementations of GetMaxByteCount and GetMaxCharCount being streamlined and commonly inlined when used directly off of Encoding.UTF8.

C# 11 introduced support for UTF8 literals, enabling the compiler to perform the UTF8 encoding into bytes at compile-time and hardcoding the resulting bytes. This saves the cost of performing the encoding at run-time and also benefits from the JIT being able to see information about the encoded data, like its length, enabling knock-on optimizations.

These changes can lead to significant performance improvements in applications that handle large amounts of text data as well as lead to faster and more efficient applications generally, which can have a big impact on user experience and business operations.

There's a lot more to the performance improvement story on .net 7, which you can see [here](https://devblogs.microsoft.com/dotnet/performance_improvements_in_net_7/).
