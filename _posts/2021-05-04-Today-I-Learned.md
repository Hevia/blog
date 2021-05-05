---
layout: post
description: A collection of things I learned and found worth sharing. Sometimes with sources!
categories: [TIL]
title: Today I Learned
sticky_rank: 1
---

# May 5th, 2021
- According to data collected by the HTTP Archive, videos, images, & JavaScript are the biggest network energy hogs.
- Online ads make up 10% of the internets carbon impact
- The "pull" design principle means dont load data until the user requests it, via interaction or navigation
- Default Effect is a psychological trick to encourage certain user behaviors. Often used nefariously but could be use to encourage better sustainable decisions.
- The 2011 SunShot initiative started by Obama's DOE helped bring down Solar costs to competitive levels in < 10 years and reached cheaper prices 3 years ahead of schedule
- Cruise lines register their companines in countries with loose labor laws. (source: Wendover Productions, The Insane Logistics of Shutting Down the cruise industry)
- CLUT stands for Color Look Up Tables.
- The Swedish scientist Svante Arrhenius first wrote about the link between carbon dioxide and global temperatures via the greenhouse effect in 1896.

## Ultimate GameBoy Talk
- GameBoy only uses 4 colors
- Original GameBoy only had 8KB of RAM!!
- Some games used MBCs(memory bank controllers) to play larger games on the GameBoy

## Python Concurrency: The Trciky Bits
- The Python GIL only allows one thread to run at any given time
- Because of the GIL, CPU bound tasks running on individual threads will slow each other down (theres a lot of blocking & resource starvation)
- Using threads does add additional speedups for I/O workloads
- You can simulate non-cpu bound task in Python using time.sleep()
- Python GIL will priotize CPU workloads over I/O workloads. This is unique to Python's GIL since OS's prefer shorter tasks
- A thread is always contained in a process, and each process contains one or more threads. Threads in the same process can share memory which means they can easily communicate and write to common data structures.
- Processes can generalize across CPU cores but threads can only run on a single core
- A common workaround to running code in Parallel in Python is to spawn several processes
- You can write C code that escapes the constraints of the GIL
- Processes have a bigger overhead compared to threads due to shared data/program state
- Procceses are not constrainted to run on a single CPU so you can execute CPU bound tasks in parallel on different cores
- Do not use threads for CPU workloads and do not use Processes for IO workloads. You will see decreased performance 
- Reading/writing data to disk is not CPU work its IO work!
- Threads are more memory efficient then processes
- Pre-Emptive Multitasking is when the OS automately switches & interleaves thread events for you
- Cooperative Multitasking is when each thread announces when they want to switch. You can use coroutines to achieve this



# May 4th, 2021
- Endocrine Disruptors are chemicals that mimic the body's hormones which can fool our cells in acting in ways it was not supposed to
- Those endocrine disruptors which are found everywhere in our modern world could be causing the decline in sperm seen throughout much of the Western World
- About 350k deaths in America can be attributed to Air Pollution each year



