# Caching


## What is Caching?

Caching is the process of storing frequently used data in a faster, easily accessible place so it can be retrieved quickly the next time it’s needed.

### Simple Example:

Imagine you always check your timetable every morning. Instead of going to the college office every day to ask for it, you save a photo of it on your phone. That saved photo is your cache — fast, easy, and saves time.

### In Computers:

When an app, website, or system needs the same data often, it keeps a copy in cache memory.

This helps the system work faster, reduces load, and serves users quickly.

Caching is like keeping important things close to you so you don’t have to go far to get them every time.

For example, if you always use a pen at work, you keep it on your desk instead of going to the cupboard every time you need it. Computers do something similar to work faster. They often keep data they use in a special, fast place called a cache.


## 1. Caching Inside the Computer (Hardware-Level)

    The CPU (Central Processing Unit) is the brain of the computer. It uses several types of cache to quickly access data:
### L1 Cache: 
        This is the smallest but fastest. It’s right inside the CPU and stores the most-used information.
### L2 Cache: 
        Bigger than L1 and a bit slower. Still close to the CPU.
### L3 Cache: 
        Even bigger and slower. Usually shared by many CPU parts (called cores).


## 2. Caching by the Operating System

    The Operating System (OS) is the software that manages your computer’s hardware.

It uses cache too:

### Page Cache: 
        When you open files from the hard drive, the OS keeps a copy in memory. Next time, it can get it faster.

### Inode Cache: 
        This keeps information about files (like their size or last change time), so it doesn’t have to look it up every time.


## 3. Caching in Apps and the Internet

    Caching helps apps and websites load faster:

### Web Browsers: 
        When you visit a website, your browser saves parts of it (like images or code). If you visit again, it loads faster.

### Search Engines (like Elasticsearch): 
        They store data in a way that makes searching lightning-fast.


## Why Caching Is Important

Caching helps systems:

Run faster

Handle more users at once

Use fewer resources

Give users a smoother experience

By storing data closer to where it's needed, systems don't waste time getting it from slower places.


## References:

* [Understand Caching by ByteByteGo video explanation](https://www.youtube.com/watch?v=dGAgxozNWFE)

* [Understanding Caching by GeeksForGeeks](https://request.geeksforgeeks.org/?p=468000)