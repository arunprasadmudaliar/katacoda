### Update the required memory limit for **mycgroup**

Under the directory created in step 1, we will create a file **memory.limit_in_bytes** and update it with value **10000000**

```
echo 10000000 > /sys/fs/cgroup/memory/foo/memory.limit_in_bytes
```