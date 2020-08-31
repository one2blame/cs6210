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
