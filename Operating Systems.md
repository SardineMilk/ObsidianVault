Privileged *kernel* level
Unprivileged *user* software

### Kernel
Has direct access to hardware

Userspace software makes *system calls* to request services from kernel

Creates and manages processes
Protects processes from each other
Distributes computer resources

Maps user view of storage (file paths) to physical hardware locations

### Types of OS
Mainframe - transaction/batch processing
Server - security, network, I/O
Personal Computer
Mobile
Real-time - Guaranteed to respond in fixed time for hardware
Embedded

Linux kernel can be flexible by adjusting userspace

### Processes
Running instance of program

**State**
- virtual address space
- CPU registers
- open files
- other resources

**Process Table**
Array of structures in kernel
Stores state of processes
`top` command lists processes in linux

#### Scheduler
Shares CPUs between processes
By context switching
Choices on how to switch
- Round robin - do all in sequence for fixed time
- Deadline - pick the process that needs to be done soonest (useful in real-time)

#### States
A process may be:

Running
Ready
- Waiting to be scheduled
Blocked
- I/O bound

If two or more processes are blocked by resources held by each other
This is a *deadlock*
The OS ensures this doesn't happen when allocating resources


### Memory Fragmentation
Repeated allocations and freeing of memory can fragment free sections
This can mean that even if enough memory is free, there is no sufficient contiguous block


### Disk I/O Scheduling
OS can reorder requests to make it more efficient

First Come FIrst Served
Shortest Seek Time First
Scan