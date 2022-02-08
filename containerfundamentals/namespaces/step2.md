### Verify if the namespace was created successfully

Most probably, you wont notice any change after the previous command was executed untill you execute below command and try to list the process:
```
ps -ef
```{{execute}}

The output should be similar to below:
```
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 11:54 pts/0    00:00:00 sh
root           2       1  0 11:54 pts/0    00:00:00 ps -ef
```

If you observe the above output carefully, there are 2 process running inside the namespace that we just created and **sh** being the first process with pid 1. Where as on a traditional uniux OS, only an **init** process can have a pid 1. 

There are other ways to confirm that the were able to succesfully isolate the PID namespace. Execute `exit`{{execute}} command and you will be back to the prompt and again execute `ps -ef`{{execute}} command and now you will notice that the process tree has changed and should list all the process running on the system.