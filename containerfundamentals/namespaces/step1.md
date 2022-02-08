### Create a namespace using **unshare** command

We will run the following **unshare** command to create a new namespace with its own user and PID namespaces. We will then map the root user to the new namespace. In other words we will have root access within the new namespace. then mount a new proc filesystem and finally fork a bash process in the newly created namespace.

```
unshare --user --pid --map-root-user --mount-proc --fork bash
```{{execute}}

This is same as executing the below docker command in a running container:
```
docker exec -it <image> /bin/bash
```

