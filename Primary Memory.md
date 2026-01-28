# RAM
volatile
# ROM
non-volatile
# Cache
- Frequently used instructions
- Registers -> L1 -> L2 -> L3 -> RAM
- Organised by Speed, size and proximity to CPU
- Hierarchy to minimise latency and maximise performance by prioritising faster memory for critical tasks
### L1 Cache
- Located directly on the CPU, making it the fastest type of cache. 
- Smallest, often only a few kilobytes 32KB to 128 KB
- Each cpu has their own L1 cache, which is typically split into 2 sections - L1i for instructions L1d for data
- amd 9700x 640 kb total so 80 kb per core
### L2 Cache
- Either on the cpu or situated very close (depending on archetecture)
- Larger than L1 (256KB - 2MB per core)
- Still very fast anbd significantly spoeeds up porcessing by reducting the need to fetch data from the slower RAM
- 9700x has 8 MB total so 1MB per core
### L3 Cache
- Located the furthest from CPU chip
- L3 cache might be shared on multiple core CPUS, while L1 and L2 are core-exclusive
- Largest of the 3: 4 - 64MB
- slowest of the 3 types
- 9700x has 32 MB

## Organisation Techniques:
#### Prefetching
Prefetching is a performance optimization technique that proactively fetches data or resources (like web pages, images, or CPU instructions) into faster memory (cache) before they are explicitly requested, anticipating future needs to reduce latency and speed up access
not strictly guessing
#### Cache coherence
In [computer architecture](https://en.wikipedia.org/wiki/Computer_architecture "Computer architecture"), **cache coherence** is the uniformity of shared resource data that is stored in multiple [local caches](https://en.wikipedia.org/wiki/Cache_\(computing\) "Cache (computing)"). In a cache coherent system, if multiple clients have a cached copy of the same region of a shared memory resource, all copies are the same. 
Makes sure that all processes are accesing the same data, and that if one of them is changed the process wont apply to the wrong value
#### Memory management
a form of [resource management](https://en.wikipedia.org/wiki/Resource_management_\(computing\) "Resource management (computing)")applied to [computer memory](https://en.wikipedia.org/wiki/Computer_memory "Computer memory"). The essential requirement of memory management is to provide ways to dynamically allocate portions of memory to programs at their request, and free it for reuse when no longer needed.
## Cache Hit & Cache Miss
basically when a computer is requesting data and seeing if its in cache. Hit means its in there, meaning the computer can just take the data out. Cache MIss means its not meaning the computer needs to look other places like RAM.

#### Types of Cache Miss:
Compulsory - first access, capacity - cache full, conflict - data evicted due to mapping
# Pipelining
- Divides instructions processing into stages (fetch decode and execute)
- Allowing multiple instructions to be processed simultaneously at different stages​
- Each stage operates concurrently, increasing instruction throughput in a single core
- We can identify 5 distinct stages in the process -​
	1. Fetch ​
	2. Decode ​
	3. Execute​
	4. Memory Access​
	5. [[Primary Memory#Write Back Stage|Write Back]]​
- Divide and conquer:![[Screenshot 2026-01-20 at 15.22.38.png]]
**4 instructions in 8 FDE cycles when it usually takes 20**
so n+4 instead of 5n

### Write Back Stage
- Final stage where the results of the execute stage are written to registers or memory​
- Ensures data (e.g., ALU results or loaded memory values) is stored for use in subsequent instructions
- Write-back allows the CPU to complete an instruction and free resources for the next instruction in the pipeline​
- Reduces pipeline stalls by ensuring results are available without delaying subsequent stages​
- In multi-core systems, write-back ensures data consistency across cores, often using cache coherence protocols