# cs6210

This class is a graduate-level course that addresses a broad range of topics in
operating system design and implementation.

[Here](https://omscs.gatech.edu/cs-6210-advanced-operating-systems) is the
official course webpage.

## Pdfs

In the `./pdfs` folder you'll find all of the papers that were covered in this
course, `./pdfs/papers.zip`, paper summaries that I completed for two of the
papers in this course, `./pdfs/paper_summaries`, and my notebook for the course
, `./pdfs/cs6210.pdf`.

## Projects

I worked on each project for this course in a separate repository. Each project
is added to this repository as a submodule. The submodules in this repository
are private to uphold the Georgia Institute of Technology
[Academic Honor Code](https://osi.gatech.edu/content/honor-code).

### Project 1

This project is an exercise in designing and implementing applications that
interface with a hypervisor to monitor and manage the resources of virtual
machines. The student is tasked with implementing a virtual CPU scheduler that
evenly balances the affinity, mapping, and workload of virtual CPUs to physical
CPUs. The student is also tasked with implementing a memory coordinator that 
evenly balances the memory requirements of multiple virtual macchines.

The entire project is written in C. In this project, I learned how to use
[qemu](https://www.qemu.org/) and [libvirt](https://libvirt.org/) to:

* Acquire statistics for a host machine's physical CPUs
* Acquire statistics for multiple virtual machine CPUs managed by a hypervisor
* Balance virtual CPU affinity and load on physical CPUs
* Acquire statistics for a host machine's memory usage
* Acquire statistics for multiple virtual machine's memory usage
* Balance virtual machine memory allocation based upon usage statistics

### Project 2

This project requires students to implement several barrier synchronization
algorithms presented in the
[paper](https://www.cs.rice.edu/~johnmc/papers/tocs91.pdf), "Algorithms for
Scalable Synchronization on Shared-Memory Multiprocessors", by
Mellor-Crummey and Scott.

The entire project is written in C. In this project, I learned how use the
[OpenMP](https://computing.llnl.gov/tutorials/openMP/) API to implement the
synchronization barriers/algorithms described in the paper above in a shared
memory environment. I then adapted the algorithms so that they would work in a
distributed memory environment using [Open MPI](https://www.open-mpi.org/). I
also learned how to:

* Align shared memory data structures to cache lines to prevent false sharing
* Utilize atomic builtins to implement synchronization primitives
* Test and evaluate algorithms to acquire performance statistics
* Use [gnuplot](http://www.gnuplot.info/) to graph data and make determinations
about algorithm performance

### Project 3

This project requires students to implement a distributed service that
resembles an online store. The store application will query the prices for a
product on behalf of a client from a number of different registered vendors.
The store leverages a threadpool to concurrently handle multiple client
requests and makes asynchronous [gRPC](https://grpc.io/) calls,
collating the prices for the requested product across all registered vendors.
The store service returns this data to the client.

The entire project is written in C++. In this project I learned about:

* Multithreaded programming in C++
* C++ lambda expressions
* C++ futures
* C++ templates
* C++ class constructors and destructors
* Creating and handling asynchronous gRPC calls
* Structuring projects with the CMake build system
* Using the [vcpkg](https://github.com/microsoft/vcpkg) package manager

### Project 4

In this project, students implement the MapReduce framework described in
[this paper](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf).

The entire project is written in C++. In this proejct I learned how to:

* Shard data to spread processing load across a distributed system
* Handle exceptions in C++
* Use advanced file system operations in C++
* Read configuration files with C++
* Conduct input validation in C++
* Leverage C++ inheritance
* Use C++ virtual functions
* Implement robust C++ applications creating and handling asynchronous gRPC
calls that recover from failures and timeouts
* Architect large C++ projects
* Execute map reduction on a large corpus of data
