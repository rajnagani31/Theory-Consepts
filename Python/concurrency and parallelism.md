# Concurrency 

## Defination
Many tasks are making progress “at the same time” (overlapping), often by switching.
<br>
OR
<br>
Doing many tasks at once by quickly switching between them, so each task gets some attention, but not necessarily at the exact same time.


- Tasks progress together by sharing time—like taking turns.

### uses
- threading (thread)
- asyncio



# parallelism 

Doing many tasks at the exact same time, using multiple processors or CPU cores.

- they work with all task bu one by one

- Many tasks, truly at once, on multiple CPUs (good for CPU: math/processing).

- two freind are make two diffrent Tea.

### uses

- multiprocessing
