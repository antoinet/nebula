```
level13@nebula:/home/flag13$ gdb ./flag13
GNU gdb (Ubuntu/Linaro 7.3-0ubuntu2) 7.3-2011.08
Copyright (C) 2011 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "i686-linux-gnu".
For bug reporting instructions, please see:
<http://bugs.launchpad.net/gdb-linaro/>...
Reading symbols from /home/flag13/flag13...(no debugging symbols found)...done.
(gdb) b main
Breakpoint 1 at 0x80484c9
(gdb) run
Starting program: /home/flag13/flag13

Breakpoint 1, 0x080484c9 in main ()
(gdb) disass
Dump of assembler code for function main:
   0x080484c4 <+0>:     push   %ebp
   0x080484c5 <+1>:     mov    %esp,%ebp
   0x080484c7 <+3>:     push   %edi
   0x080484c8 <+4>:     push   %ebx
=> 0x080484c9 <+5>:     and    $0xfffffff0,%esp
   0x080484cc <+8>:     sub    $0x130,%esp
   0x080484d2 <+14>:    mov    0xc(%ebp),%eax
   0x080484d5 <+17>:    mov    %eax,0x1c(%esp)
   0x080484d9 <+21>:    mov    0x10(%ebp),%eax
   0x080484dc <+24>:    mov    %eax,0x18(%esp)
   0x080484e0 <+28>:    mov    %gs:0x14,%eax
   0x080484e6 <+34>:    mov    %eax,0x12c(%esp)
   0x080484ed <+41>:    xor    %eax,%eax
   0x080484ef <+43>:    call   0x80483c0 <getuid@plt>
   0x080484f4 <+48>:    cmp    $0x3e8,%eax
   0x080484f9 <+53>:    je     0x8048531 <main+109>
   0x080484fb <+55>:    call   0x80483c0 <getuid@plt>
   0x08048500 <+60>:    mov    $0x80486d0,%edx
   0x08048505 <+65>:    movl   $0x3e8,0x8(%esp)
   0x0804850d <+73>:    mov    %eax,0x4(%esp)
   0x08048511 <+77>:    mov    %edx,(%esp)
   0x08048514 <+80>:    call   0x80483a0 <printf@plt>
   0x08048519 <+85>:    movl   $0x804870c,(%esp)
   0x08048520 <+92>:    call   0x80483d0 <puts@plt>
   0x08048525 <+97>:    movl   $0x1,(%esp)
   0x0804852c <+104>:   call   0x80483f0 <exit@plt>
   0x08048531 <+109>:   lea    0x2c(%esp),%eax
   0x08048535 <+113>:   mov    %eax,%ebx
   0x08048537 <+115>:   mov    $0x0,%eax
   0x0804853c <+120>:   mov    $0x40,%edx
   0x08048541 <+125>:   mov    %ebx,%edi
   0x08048543 <+127>:   mov    %edx,%ecx
   0x08048545 <+129>:   rep stos %eax,%es:(%edi)
   0x08048547 <+131>:   mov    $0x804874c,%edx
   0x0804854c <+136>:   lea    0x2c(%esp),%eax
   0x08048550 <+140>:   mov    (%edx),%ecx
   0x08048552 <+142>:   mov    %ecx,(%eax)
   0x08048554 <+144>:   mov    0x4(%edx),%ecx
   0x08048557 <+147>:   mov    %ecx,0x4(%eax)
   0x0804855a <+150>:   mov    0x8(%edx),%ecx
   0x0804855d <+153>:   mov    %ecx,0x8(%eax)
   0x08048560 <+156>:   mov    0xc(%edx),%ecx
   0x08048563 <+159>:   mov    %ecx,0xc(%eax)
   0x08048566 <+162>:   mov    0x10(%edx),%ecx
   0x08048569 <+165>:   mov    %ecx,0x10(%eax)
   0x0804856c <+168>:   mov    0x14(%edx),%ecx
   0x0804856f <+171>:   mov    %ecx,0x14(%eax)
   0x08048572 <+174>:   mov    0x18(%edx),%ecx
---Type <return> to continue, or q <return> to quit---q
Quit
(gdb) b *main+48
Breakpoint 2 at 0x80484f4
(gdb) c
Continuing.

Breakpoint 2, 0x080484f4 in main ()
(gdb) p $eax
$1 = 1014
(gdb) set $eax=1000
(gdb) c
Continuing.
your token is b705702b-76a8-42b0-8844-3adabbe5ac58
[Inferior 1 (process 2225) exited with code 063]
(gdb) quit
level13@nebula:/home/flag13$ su flag13
Password:
sh-4.2$ getflag
You have successfully executed getflag on a target account
sh-4.2$

```
