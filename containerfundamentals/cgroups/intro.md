## This scenario will help you to understand a Kernel feature called "Cgroups". We will create a cgroup and try to attach a process to this cgroup manually.

#### A control group (cgroup) is a Linux kernel feature that limits, accounts for, and isolates the resource usage (CPU, memory, disk I/O, network, and so on) of a collection of processes. Cgroups provide the following features:
1. **Resource limits** – You can configure a cgroup to limit how much of a particular resource (memory or CPU, for example) a process can use.
2. **Prioritization** – You can control how much of a resource (CPU, disk, or network) a process can use compared to processes in another cgroup when there is resource contention.
3. **Accounting** – Resource limits are monitored and reported at the cgroup level.
4. **Control** – You can change the status (frozen, stopped, or restarted) of all processes in a cgroup with a single command.

Step 1-3 will demostrate how to create a cgroup **mycgroup**, set the memory limit for this cgroup to **10000000 bytes (10MB)** and then assign a process to this cgroup. This exercise only demonstrates how to control memory limit but the concept is equally applicable to other system resources as well.