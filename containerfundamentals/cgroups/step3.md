### Create a test.sh script and assign its pid to **mycgroup**

Below command will create a test.sh file that will echo **Testing Cgroups** and then sleep for 5 minutes.
```
touch test.sh
echo "Testing Cgroups" > test.sh
chmod +x test.sh
```{{execute interrupt}}

You can also check the contents of the file.
```
cat test.sh
```{{execute}}

Let's execute this script in background and proceed to final step. It should echo **Testing Cgroups** once and return back to the prompt. If prompt is not visible, try pressing **Enter** key.
```
./test.sh &
```

Note the pid from above output and execute the command ***ps -o cgroup <pid>* replace pid with correct value.
```
10:devices:/user.slice,9:pids:/user.slice/user-0.slice/session-5.scope,8:cpu,cpuacct:/user.slice,4:blkio:/user.slice,2:memory:/mycgroup,1:na
```

From the above output we can see that a process **(./test.sh in this case)** is bound to a cgroup **mycgroup** which has the memory limit set to 10MB. If test.sh requests for more than 10MB memory, the process will be killed by OS.