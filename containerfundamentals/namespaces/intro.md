## This scenario will help you to understand a Kernel feature called **namespaces**. We will run a process isolated in the namespace that will will create.

### Namespaces are a feature of the Linux kernel that partitions kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources.

The key feature of namespaces is that they isolate processes from each other. On a server where you are running many different services, isolating each service and its associated processes from other services means that there is a smaller blast radius for changes, as well as a smaller footprint for security‑related concerns. 

The 7 types of namespaces are listed below:

1. Mount - isolate filesystem mount points
2. UTS - isolate hostname and domainname
3. IPC - isolate interprocess communication (IPC) resources
4. PID - isolate the PID number space
5. Network - isolate network interfaces
6. User - isolate UID/GID number spaces
7. Cgroup - isolate cgroup root directory
