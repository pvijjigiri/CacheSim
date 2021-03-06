CacheSim
========
CacheSim is a simple cache simulator, written in Python, that implements an
N-way set-associative LRU cache, used for exploring the cache hit and miss
rates when feeding in address traces from two programs, generated by the
`pinatrace` [Pin][pin] tool. These accesses are interleaved to simulate context
switching between different threads.

This program is compatible with Python 2.6.

To generate an input file, run:

    pin -t /path/to/pinatrace.so -- <executable>

Good sample programs to try are those involving interesting data reference
patterns, such as image processing programs or those working with matrices.
Trace files around a gigabyte in size are relatively quick to work with.

CacheSim also allows for working with and implementing different cache
partitioning mechanisms. Built-in ones include no partitioning, static
partitioning, and dynamic partitioning. Run `cachesim.py --help` to see other
configurable options.

[pin]: https://software.intel.com/en-us/articles/pin-a-dynamic-binary-instrumentation-tool
