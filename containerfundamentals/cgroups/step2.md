### Create a file file test.sh that we can use to mimic a running process. The file will basically print **Testing Cgroups** on the screen and will go to sleep for 5 minutes.


Below command will create a **test.sh** file that will echo **Testing Cgroups** and then sleep for 5 minutes.
```
touch test.sh
echo "echo 'Testing Cgroups';sleep 300" > test.sh
chmod +x test.sh
```{{execute interrupt}}

You can also check the contents of the file.
```
cat test.sh
```{{execute}}
