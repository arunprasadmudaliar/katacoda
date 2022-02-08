### Create a cgroup

We will create a directory **mycgroup** under __/sys/fs/cgroup/memory/__
```
mkdir -p /sys/fs/cgroup/memory/foo
```{{execute interrupt}}

Under the directory created in above step, we will create a file **memory.limit_in_bytes** and update it with value **10000000**

```
echo 10000000 > /sys/fs/cgroup/memory/foo/memory.limit_in_bytes
```{{execute}}