- acts as an intermediary between hardware and user applications
- abstracts hardware complexities by hiding low-level hardware details
- provides a user-friendly interface, like GUI or CLI to interact with hardware like CPU, memory, storage
- Allocates and optimises hardware resources, eg CPU, memory, storage, I/O devices among processes
- ensures efficient multitasling by scheduling processes and managing resoujrce conflicts

### Maintaining system integrity
Ensures reliable operation by monitoring hardware and software for error or crashes


# Functions
memory management, file system, device management, scheduling, security, accounting, gui, virtualisation, networking

### Memory Management
- Allocates and deallocates memory for processes
- Ensures efficient use of RAM
- Uses techniques like virtual memory to extend available memory via storage (eg. paging/swapping)
### File system Management
organises, stores, ad retreieves data on storage devices. 
Uses file systems like ext4, NTFS, APFS
manages file access, permissions and dictionary structures

### Device management
Controls hardware devices (eg. printers, keyboards) via device drivers
facilitates communication with applications
Handles I/O operations and resource alllocation for drivers.
- techniques like buffering, caching and spooling are used

### Virtualization​
- Enables running multiple OS instances or virtual machines on a single physical system​
- Example: VMware or Hyper-V allows Linux and Windows to run simultaneously​
# Process scheduling
- Determines which processes run on the CPU and for how long
- algorithms like round-robin, priority scheduling
- resource distribution
- aims to optimise throughput, minimmise response time and ensure fair resource equal distribution
- 
### Algorithms
- First Come First Server - in a queue, executed in the order they arrive in; non-preemptive - process runs to completion
- Round Robin - each processeosis give a bit of time to every process and then is et5xecuted for that bit of time until it is done
- Multilevel Queue - Different queues based on type or priority
- Priority Scheduling - Assigns CPU time based on process priority, 
# Multitasking
Operating systems can handle many tsasks at once
- abstraction opf scheduling
- it switches processes periodically so that it seems like its multitasking
### Deadlocks
- A process must not create a deadlock, in which processes block each other by holding resources while waiting for others.
- Occurs when processes form a circular ? - Process A holds Resource 1 and waits for resource 2, while Process B holds Resource 2 and waits for Resource 1
- Deadlock Prevention techniques, eg. resource ordering, monitoring resource allocation, or recovery - terminating or rolling back processes.
# Interrupts
A signal that tells the OS that somnething needs attention
Useful when events don't occur regularly unlike polling

What happens with interruopts:
1. Interrupt recieved
2. Process state saved (FDE cycle is finished and saved)
3. interrupt processed/serviced
4. Process re-loaded, execution continues
5. for less frequent / triggered stuff, like mouse movement, mouse click etc.

# Polling
- allows one unit to check the status of another unit at regular intervals
- checks regularly for new stuff
- constantly requires processing power 
- can be more efficient in some cases, like when things are constantly changing
- for stuff which is happening very regularly. unlike interrupts
- good for high-frequency events where constantly checking is justified, like time, resource monitoring, etc.
- more power & more CPU overhead
- 
