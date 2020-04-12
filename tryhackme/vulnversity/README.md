# Vulnversity Room on TryHackMe

## Answers:

<details>
  <summary>2. Scan the box, how many ports are open?</summary>
  6
</details>

<details>
  <summary>3. What version of the squid proxy is running on the machine?</summary>
  3.5.12
</details>

<details>
  <summary>4. How many ports will nmap scan if the flag -p-400 was used?</summary>
  400
</details>

<details>
  <summary>5. Using the nmap flag -n what will it not resolve?</summary>
  DNS
</details>

<details>
  <summary>6. What is the most likely operating system this machine is running?</summary>
  Ubuntu
</details>

<details>
  <summary>7. What port is the web server running on?
</summary>
  3333
</details>



## Commands being used on this CTF:

```console
$ nmap -p- -A -sC -sV -oN nmap/full 10.10.30.172
```