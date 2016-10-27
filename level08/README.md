```
level08@nebula:/tmp$ tcpflow -r /home/flag08/capture.pcap
level08@nebula:/tmp$ ls -la
total 8
drwxrwxrwt 6 root    root    160 2016-06-03 14:17 .
drwxr-xr-x 1 root    root    240 2016-06-03 15:42 ..
-rw-rw-r-- 1 level08 level08 206 2016-06-03 14:17 059.233.235.218.39247-059.233.235.223.12121
-rw-rw-r-- 1 level08 level08 266 2016-06-03 14:17 059.233.235.223.12121-059.233.235.218.39247
drwxrwxrwt 2 root    root     40 2016-06-03 15:42 .ICE-unix
drwxrwxrwt 2 root    root     40 2016-06-03 15:42 VMwareDnD
drwx------ 2 root    root    100 2016-06-03 15:42 vmware-root
drwxrwxrwt 2 root    root     40 2016-06-03 15:42 .X11-unix
level08@nebula:/tmp$ hexdump -C 059.233.235.223.12121-059.233.235.218.39247
00000000  ff fd 25 ff fb 26 ff fd  18 ff fd 20 ff fd 23 ff  |..%..&..... ..#.|
00000010  fd 27 ff fd 24 ff fa 20  01 ff f0 ff fa 23 01 ff  |.'..$.. .....#..|
00000020  f0 ff fa 27 01 ff f0 ff  fa 18 01 ff f0 ff fb 03  |...'............|
00000030  ff fd 01 ff fd 22 ff fd  1f ff fb 05 ff fd 21 ff  |....."........!.|
00000040  fa 22 01 03 ff f0 ff fa  21 03 ff f0 ff fb 01 ff  |."......!.......|
00000050  fd 00 ff fe 22 ff fa 22  03 03 e2 03 04 82 0f 07  |....".."........|
00000060  e2 1c 08 82 04 09 c2 1a  0a 82 7f 0b 82 15 0f 82  |................|
00000070  11 10 82 13 11 82 ff ff  12 82 ff ff ff f0 0d 0a  |................|
00000080  4c 69 6e 75 78 20 32 2e  36 2e 33 38 2d 38 2d 67  |Linux 2.6.38-8-g|
00000090  65 6e 65 72 69 63 2d 70  61 65 20 28 3a 3a 66 66  |eneric-pae (::ff|
000000a0  66 66 3a 31 30 2e 31 2e  31 2e 32 29 20 28 70 74  |ff:10.1.1.2) (pt|
000000b0  73 2f 31 30 29 0d 0a 0a  01 00 77 77 77 62 75 67  |s/10).....wwwbug|
000000c0  73 20 6c 6f 67 69 6e 3a  20 00 6c 00 65 00 76 00  |s login: .l.e.v.|
000000d0  65 00 6c 00 38 01 00 0d  0a 50 61 73 73 77 6f 72  |e.l.8....Passwor|
000000e0  64 3a 20 00 0d 0a 01 00  0d 0a 4c 6f 67 69 6e 20  |d: .......Login |
000000f0  69 6e 63 6f 72 72 65 63  74 0d 0a 77 77 77 62 75  |incorrect..wwwbu|
00000100  67 73 20 6c 6f 67 69 6e  3a 20                    |gs login: |
0000010a
level08@nebula:/tmp$ hexdump -C 059.233.235.218.39247-059.233.235.223.12121
00000000  ff fc 25 ff fe 26 ff fb  18 ff fb 20 ff fb 23 ff  |..%..&..... ..#.|
00000010  fb 27 ff fc 24 ff fa 20  00 33 38 34 30 30 2c 33  |.'..$.. .38400,3|
00000020  38 34 30 30 ff f0 ff fa  23 00 53 6f 64 61 43 61  |8400....#.SodaCa|
00000030  6e 3a 30 ff f0 ff fa 27  00 00 44 49 53 50 4c 41  |n:0....'..DISPLA|
00000040  59 01 53 6f 64 61 43 61  6e 3a 30 ff f0 ff fa 18  |Y.SodaCan:0.....|
00000050  00 78 74 65 72 6d ff f0  ff fd 03 ff fc 01 ff fb  |.xterm..........|
00000060  22 ff fa 22 03 01 00 00  03 62 03 04 02 0f 05 00  |"..".....b......|
00000070  00 07 62 1c 08 02 04 09  42 1a 0a 02 7f 0b 02 15  |..b.....B.......|
00000080  0f 02 11 10 02 13 11 02  ff ff 12 02 ff ff ff f0  |................|
00000090  ff fb 1f ff fa 1f 00 b1  00 31 ff f0 ff fd 05 ff  |.........1......|
000000a0  fb 21 ff fa 22 01 07 ff  f0 ff fd 01 ff fb 00 ff  |.!.."...........|
000000b0  fc 22 6c 65 76 65 6c 38  0d 62 61 63 6b 64 6f 6f  |."level8.backdoo|
000000c0  72 7f 7f 7f 30 30 52 6d  38 7f 61 74 65 0d        |r...00Rm8.ate.|
000000ce

[ password is: "backd00Rmate" ]

level08@nebula:/tmp$ su flag08
Password:
sh-4.2$ getflag
You have successfully executed getflag on a target account
sh-4.2$

```
