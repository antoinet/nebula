```
level14@nebula:/home/flag14$ cat /tmp/decrypt.py
#!/usr/bin/python
import sys

for line in sys.stdin:
        text = ""
        for idx,c in enumerate(str.strip(line)):
                text += chr(ord(c)-idx)
        print text

level14@nebula:/home/flag14$ cat token | python /tmp/decrypt.py
8457c118-887c-4e40-a5a6-33a25353165

level14@nebula:/home/flag14$ su flag14
Password:
sh-4.2$ getflag
You have successfully executed getflag on a target account
sh-4.2$

```
