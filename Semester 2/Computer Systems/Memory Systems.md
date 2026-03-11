### Memory Hierarchy
As you go down the hierarchy, speed decreases and capacity increases
Different levels are implemented using different hardware and software

Registers
- 32 x 32 bits
- Inside CPU
Cache
- Organised into Lines
- 256 x 1024 bytes
- Static RAM
	- Very fast
	- Very expensive and low capacity
Main Memory
- Stores large amounts of data, organised into Words
- 32G x 32 bits
- Dynamic RAM
	- Slightly slower
	- Cheaper
Virtual Memory
- Stores huge amounts of data as if in main memory, may be stored on disk etc
- Organised into pages (normally 4Kib each)
- 1G x 4096 bytes
- On Disk
	- Managed by operating system software

### Memory Performance
Often have multiple memory channels/banks
Allows requests to be parallelised

Latency
- Time taken to complete a single operation in seconds

Throughput
- Operations / second

Bandwidth
- Overall rate of data movement in bits/s


### Memory Structure
Arranged in grids of cells
Decoder uses upper half of address bits to get **word line**, making all cells in line to output
Multiplexer uses lower half of bits to select
correct value from line

Dynamic RAM 
- main memory
- needs refreshed
 - Values stored in a small capacitor that decays with time (~64 ms)
 - Very space efficient and cheap
 - ~10 ns access
 
Static RAM
- cache memory
- can maintain values as long as it has power
- Uses two inverters feeding into each other
- ~1 ns access

Modern CPUs have 1-10 GHz clock speed
0.1 - 1 ns per instruction
Memory operations is the main bottleneck in modern software

### Cache
Keeps track of memory addresses currently in cache
When the CPU requests an address, it checks if its in the cache first
If it is, that's a **cache hit**
If its not, that's a **cache miss**
It is then fetched from main memory and stored in the cache 

Cache hit rate = $[hits / (hits + misses)] * 100$
Debugging tools can show you this rate for every line of code

#### Cache locality of reference principle
If memory address $N$ is cached
Then locations $N-1$ and $N+1$ are often cached as well

This size can be increased for higher hit rate, at the cost of more data transfer


Tag array contains one entry for each line in the cache
Valid bit
- Does the line contain data
Dirty bit
- 0 when loaded, 1 when first written to
Reference bit
- 0 when first loaded, 1 when used
### Virtual Memory

