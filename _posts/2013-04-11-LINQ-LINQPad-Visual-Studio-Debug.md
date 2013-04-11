---
layout: post
title: "Howto: Debug LINQ Query on LINQPad with Visual Studio"
date: 11 April 2013
categories: Tips
comments: true
---
Suppose if you want to debug a LINQ Query wrote in [LINQPad](http://www.linqpad.net/) with Visual Studio?

It's simple
 - Open Visual Studio (Tested only 2010 or above)
 - Open `Debug->Attach to Proces` `(Ctrl+Alt+P)`
 - Attach to LINQPad.exe

Now start debugging. The easiest way around to break into debugger is by putting `Debugger.Break()` in your LINQ Query (on LINQPad)

```C#
void Main()
{
     int[] arr = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
     var evens = from numb in arr where (odds % 2) == 0 select odds;
     Debugger.Break(); // Notice the Debugger.Break() here.
     foreach (var n in evens)
     Console.WriteLine(n);
}
```
